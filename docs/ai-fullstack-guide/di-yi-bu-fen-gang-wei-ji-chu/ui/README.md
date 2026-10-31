---
description: UI
---

# UI

这一节不教你做设计，只教你一件事：**看到一个界面决策，能算出它在技术侧的账。**

后端最常把 UI/UX 归成两类：UI 是「把东西弄好看」，UX 是「画页面跳转图」—— 于是要么全交给设计师，要么选个现成组件库了事。但很多「用起来别扭」的后台，根源既不是审美，也不是流程，而是几个结构决策没做：**信息没有主次、间距没有刻度、状态没有设计**。这三件事，后端来思考反而更有优势。

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h3>🧠</h3></td><td><strong>UI/UX 岗的七个模块</strong></td><td>信息架构、栅格与间距、设计 token、组件与设计系统、交互五态、响应式断点、交付与验收。每个模块都写了「后端为什么必须懂」。</td><td><a href="ui-qi-ge-mo-kuai.md">ui-qi-ge-mo-kuai.md</a></td></tr><tr><td><h3>⚖️</h3></td><td><strong>选型表：设计系统、主题、交互</strong></td><td>组件库怎么选、主题怎么设计、图标字体怎么定、交互模式、断点、动效——六张表，每个选项都带上代价。</td><td><a href="ui-xuan-xing-biao.md">ui-xuan-xing-biao.md</a></td></tr><tr><td><h3>🕳️</h3></td><td><strong>UI 决策 → 技术后果：映射表</strong></td><td>一个设计决定，最后会变成前端的什么工作量、后端的什么接口约束。可以当评审 checklist 用。</td><td><a href="ui-ying-she-biao.md">ui-ying-she-biao.md</a></td></tr><tr><td><h3>🪤</h3></td><td><strong>UI 岗的十个通用坑</strong></td><td>设计稿漂亮但接不住的那些地方。每条都说清表现、后果、怎么防。</td><td><a href="ui-shi-ge-keng.md">ui-shi-ge-keng.md</a></td></tr><tr><td><h3>💬</h3></td><td><strong>提问模板：评审、生成、验收</strong></td><td>拿去就能用的提示词：让 AI 评审设计稿、按 token 生成界面、验收 AI 生成的前端。</td><td><a href="ui-ti-wen-mu-ban.md">ui-ti-wen-mu-ban.md</a></td></tr></tbody></table>

## 建议读法 🛣️

* **只想先避坑**：先读 [UI 不是美化，UX 不是画流程](ui-wu-qu.md)，再看[十个坑](ui-shi-ge-keng.md)。
* **要参与评审**：七个模块挑你不懂的读，然后拿[映射表](ui-ying-she-biao.md)当 checklist。
* **要用 AI 生成界面**：先看[选型表](ui-xuan-xing-biao.md)定好 token 和组件库，再拿[提问模板](ui-ti-wen-mu-ban.md)去生成——没有 token 约束的 AI 生成，每次出来都不一样。

{% hint style="warning" %}
别一上来就让 AI 直接生成整页。「好看」是 AI 最擅长的事，「和整套设计一致」是它最容易翻车的事。先定 token，再生成。
{% endhint %}
