# 第一部分 · 岗位基础

AI 全栈不是「一个人把五个岗位的活全干了」，而是**知道每个岗位在决定什么，以及那个决定会变成谁的约束**。

一个需求从想法走到上线，会依次经过五个岗位的手：

```mermaid
flowchart LR
    P["📋 产品<br/>做什么、边界在哪"] --> U["🎨 UI<br/>长什么样、怎么交互"]
    U --> F["🖥️ 前端<br/>用户看到什么"]
    F --> B["⚙️ 后端<br/>系统怎么扛住"]
    B --> O["🛠️ 运维<br/>能不能稳定跑"]
```

## 本部分包含

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h3>📋</h3></td><td><strong>产品</strong></td><td>需求优先级、用户故事与验收、状态机、B/C 端差异、商业化与合规。六个子页可以单独读。</td><td><a href="chan-pin/">chan-pin</a></td></tr><tr><td><h3>🎨</h3></td><td><strong>UI</strong></td><td>信息架构、栅格与 token、组件与设计系统、五态、断点、交付验收。七个模块，外带选型表和映射表。</td><td><a href="ui/">ui</a></td></tr><tr><td><h3>🖥️</h3></td><td><strong>前端</strong></td><td>选型七层、服务端 vs 客户端状态、数据请求层、表单、构建、类型、性能与部署。八个模块加选型表和映射表。</td><td><a href="qian-duan/">qian-duan</a></td></tr><tr><td><h3>⚙️</h3></td><td><strong>后端</strong></td><td>多租户隔离、并发正确性、幂等、状态机、缓存一致性、队列异步、可观测性、部署架构。八个模块加九张选型表和映射表。</td><td><a href="hou-duan/">hou-duan</a></td></tr><tr><td><h3>🛠️</h3></td><td><strong>运维</strong></td><td>部署、观测、成本、灰度；模型服务的运维和传统服务哪里不一样。</td><td><a href="yun-wei.md">yun-wei.md</a></td></tr></tbody></table>

## 已经能单独读的四条线 📖

**产品线**

* [产品岗不是「画原型、写文档」](chan-pin/chan-pin-gang-bu-shi-hua-yuan-xing-xie-wen-dang.md)
* [产品岗的六个知识模块](chan-pin/chan-pin-gang-de-liu-ge-zhi-shi-mo-kuai.md)
* [选型维度表：每个方案背后的技术账](chan-pin/xuan-xing-wei-du-biao-mei-ge-fang-an-bei-hou-de-ji-shu-zhang.md)
* [产品决策 → 技术后果：一张 checklist](chan-pin/chan-pin-jue-ce-ji-shu-hou-guo-yi-zhang-checklist.md)
* [产品岗的七个通用坑](chan-pin/chan-pin-gang-de-qi-ge-tong-yong-keng.md)
* [提问模板：把问题问透](chan-pin/ti-wen-mu-ban-ba-wen-ti-wen-tou.md)

**UI 线**

* [UI 不是美化，UX 不是画流程](ui/ui-wu-qu.md)
* [UI/UX 岗的七个模块](ui/ui-qi-ge-mo-kuai.md)
* [选型表：设计系统、主题、交互](ui/ui-xuan-xing-biao.md)
* [UI 决策 → 技术后果：映射表](ui/ui-ying-she-biao.md)
* [UI 岗的十个通用坑](ui/ui-shi-ge-keng.md)
* [提问模板：评审、生成、验收](ui/ui-ti-wen-mu-ban.md)

**前端线**

* [前端选型不是「选个框架」](qian-duan/qian-duan-xuan-xing-bu-shi-xuan-ge-kuang-jia.md)
* [前端岗的八个模块](qian-duan/qian-duan-gang-de-ba-ge-mo-kuai.md)
* [选型表：框架、数据请求、状态、样式](qian-duan/qian-duan-xuan-xing-biao.md)
* [前端决策 → 技术后果：映射表](qian-duan/qian-duan-jue-ce-ji-shu-hou-guo.md)
* [前端岗的十二个通用坑](qian-duan/qian-duan-gang-de-shi-er-ge-keng.md)
* [提问模板：选型、评审、验收](qian-duan/qian-duan-ti-wen-mu-ban.md)

**后端线**

* [后端选型不是「选个语言框架」](hou-duan/hou-duan-xuan-xing-bu-shi-xuan-ge-yu-yan-kuang-jia.md)
* [后端岗的八个模块](hou-duan/hou-duan-gang-de-ba-ge-mo-kuai.md)
* [选型表：九张表 + 三语言对照](hou-duan/hou-duan-xuan-xing-biao.md)
* [后端决策 → 技术后果：映射表](hou-duan/hou-duan-jue-ce-ji-shu-hou-guo.md)
* [后端岗的十二个通用坑](hou-duan/hou-duan-gang-de-shi-er-ge-keng.md)
* [提问模板：架构、契约、验收](hou-duan/hou-duan-ti-wen-mu-ban.md)

## 看每个岗位时，问三个问题 ❓

{% hint style="info" %}
1. 它在决定什么？
2. 这个决定的代价是什么？
3. 这个决定会变成谁的约束、埋什么坑？
{% endhint %}

## 读完你会得到什么 ✅

* 能听懂每个岗位的语言，知道他们真正在纠结什么
* 能在评审时问出「这个决策技术上接不接得住」
* 知道哪些问题该在自己岗位上解决，哪些必须提前拦下来
