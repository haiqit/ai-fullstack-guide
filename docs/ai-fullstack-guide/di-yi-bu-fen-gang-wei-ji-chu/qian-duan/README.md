# 前端

这一节不教你写前端，只教你算一笔账：**一个前端方案定下来，后端、运维、还有以后改代码的人，各要付多少代价。**

后端最常把前端选型简化成「React 还是 Vue」。但框架只是七层里的第一层，而且 AI 时代它已经不是最难的一层——AI 对主流框架的生成质量都还不错，真正容易埋雷的是数据请求层和状态管理。这两层选错，不是重写页面，是改每一个页面。

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h3>🧭</h3></td><td><strong>前端选型不是「选个框架」</strong></td><td>七层选型、AI 时代哪个更关键，以及一个你一定见过的「越改越乱」的例子。</td><td><a href="qian-duan-xuan-xing-bu-shi-xuan-ge-kuang-jia.md">qian-duan-xuan-xing-bu-shi-xuan-ge-kuang-jia.md</a></td></tr><tr><td><h3>🧠</h3></td><td><strong>前端岗的八个模块</strong></td><td>选型三问、服务端 vs 客户端状态、数据请求层、表单、状态管理、构建依赖、类型、性能部署。每个都写了「后端为什么必须懂」。</td><td><a href="qian-duan-gang-de-ba-ge-mo-kuai.md">qian-duan-gang-de-ba-ge-mo-kuai.md</a></td></tr><tr><td><h3>⚖️</h3></td><td><strong>选型表：框架、数据请求、状态、样式</strong></td><td>七张表：框架与渲染、数据请求、状态管理、样式、构建、测试、部署。每个选项都带代价。</td><td><a href="qian-duan-xuan-xing-biao.md">qian-duan-xuan-xing-biao.md</a></td></tr><tr><td><h3>🕳️</h3></td><td><strong>前端决策 → 技术后果：映射表</strong></td><td>16 个前端决策，分别给后端、运维埋什么坑。评审时可以当 checklist。</td><td><a href="qian-duan-jue-ce-ji-shu-hou-guo.md">qian-duan-jue-ce-ji-shu-hou-guo.md</a></td></tr><tr><td><h3>🪤</h3></td><td><strong>前端岗的十二个通用坑</strong></td><td>状态混放、密钥泄露、offset 分页、SSR 没人运维……每条都说清表现、后果、怎么防。</td><td><a href="qian-duan-gang-de-shi-er-ge-keng.md">qian-duan-gang-de-shi-er-ge-keng.md</a></td></tr><tr><td><h3>💬</h3></td><td><strong>提问模板：选型、评审、验收</strong></td><td>框架选型、数据请求层设计、状态选型、接口契约评审、性能优化、AI 代码验收。</td><td><a href="qian-duan-ti-wen-mu-ban.md">qian-duan-ti-wen-mu-ban.md</a></td></tr></tbody></table>

## 建议读法 🛣️

* **刚接手前端项目**：先读[前端选型不是「选个框架」](qian-duan-xuan-xing-bu-shi-xuan-ge-kuang-jia.md)，再看[十二个坑](qian-duan-gang-de-shi-er-ge-keng.md)。
* **要跟前端一起定架构**：八个模块里优先看模块二和模块三（状态分层、数据请求层），这两块是后端接口设计直接决定的。
* **要验收 AI 写的前端**：拿[模板六](qian-duan-ti-wen-mu-ban.md)自查，再对着[映射表](qian-duan-jue-ce-ji-shu-hou-guo.md)过一遍接口。

{% hint style="warning" %}
前端这条线上，后端能主导的其实只有一件事：**把接口设计成前端好用的样子。** 错误码分类、游标分页、统一返回结构、幂等键——这四件事定下来，前端的复杂度直接降一半。剩下的前端技术选型，参与评审就好，不必自己去拍。
{% endhint %}
