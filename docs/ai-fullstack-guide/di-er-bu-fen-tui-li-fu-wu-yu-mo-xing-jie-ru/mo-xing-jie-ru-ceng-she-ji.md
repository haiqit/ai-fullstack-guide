# 模型接入层设计

## 接入层应该负责什么

* **超时与重试**：区分「还没输出」和「已经输出一半」。
* **限流**：按租户、按接口、按模型分别限。
* **降级**：模型不可用时返回缓存、小模型结果或模板回复。
* **多模型路由**：按任务难度、成本预算、可用性切换。
* **计量**：记录输入/输出 token，供成本核算。

## 重试的三个坑

1. **不幂等**：同一次请求重试可能得到不同答案，带工具调用的场景尤其明显。
2. **成本翻倍**：失败的重试同样消耗 token。
3. **流式已输出**：已经推给用户的片段不能撤回，只能在应用层拼接或提示重试。

## 降级策略

```python
async def chat_with_fallback(req):
    try:
        return await primary_model.chat(req, timeout=8)
    except TimeoutError:
        return await small_model.chat(req, timeout=3)
    except ModelUnavailable:
        return cached_or_template(req)
```

关键原则：**降级路径必须是提前设计好的，而不是出事时临时写的。**
