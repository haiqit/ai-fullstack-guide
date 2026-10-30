# Agent 的基本构件

## 四个构件

* **工具**：模型可以调用的外部能力。
* **记忆**：跨轮次保留的上下文。
* **规划**：把目标拆成可执行的步骤。
* **执行循环**：调用模型 → 解析动作 → 执行 → 回填结果 → 继续。

## 执行循环

```python
while not done:
    action = model.decide(state)
    if action.type == "final":
        return action.answer
    result = tools.run(action)
    state = state.append(action, result)
```

真实的循环还要加上步数上限、超时、预算和人工中断。

## 可控性三件事

1. **可预测**：同样的输入尽量走同样的路径。
2. **可回放**：每一步的模型输入输出都要留痕。
3. **可中止**：任何时候都能停下来，而不是等它自己结束。
