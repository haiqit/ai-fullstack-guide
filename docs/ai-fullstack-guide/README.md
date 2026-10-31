# AI 全栈开发指南

一本写给工程师的 AI 全栈实战书。不追热点，只回答一个问题：**怎么把 AI 能力做成能上线、能运维、成本算得清的系统。**

> 📌 状态：草稿，持续更新 🐙 源码与勘误：[haiqit/ai-fullstack-guide](https://github.com/haiqit/ai-fullstack-guide)

## 这本书想解决什么 🤔

大多数 AI 教程的终点，是「Demo 跑通了」。但一旦上线，等着你的是另一组问题：

* ⏱️ 一次请求要 8 秒，用户还愿意等吗？
* 💸 这个月账单翻了三倍，钱花在哪儿？
* 🌊 模型抽风、接口超时，服务会不会跟着雪崩？
* 📉 改了一版提示词，到底是变好了还是变坏了？

这本书用后端工程的视角，把这些问题的答案整理成可以复用的方法和取舍。

## 全书结构 🗂️

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h3>🗺️</h3></td><td><strong>第一部分 · 全景介绍</strong></td><td>先把地图画清楚：一次请求到底经过哪几层。</td><td><a href="/broken/pages/9MG5hjNgBNWv5WLlB5j9">Broken link</a></td></tr><tr><td><h3>👥</h3></td><td><strong>第二部分 · 岗位基础</strong></td><td>产品、UI、前端、后端、运维，各自需要懂什么。</td><td><a href="di-yi-bu-fen-gang-wei-ji-chu/">di-yi-bu-fen-gang-wei-ji-chu</a></td></tr><tr><td><h3>🧪</h3></td><td><strong>第三部分 · 岗位实操</strong></td><td>按岗位动手：产品设计、UI、前端、后端、运维部署。</td><td><a href="di-er-bu-fen-gang-wei-shi-cao/">di-er-bu-fen-gang-wei-shi-cao</a></td></tr><tr><td><h3>🧰</h3></td><td><strong>第四部分 · 开发工具</strong></td><td>模型、IDE、MCP、Skills，怎么选、怎么用。</td><td><a href="di-san-bu-fen-kai-fa-gong-ju/">di-san-bu-fen-kai-fa-gong-ju</a></td></tr><tr><td><h3>🔁</h3></td><td><strong>第五部分 · 工作流</strong></td><td>Vibe Coding、SDD、Harness：人和 AI 怎么配合。</td><td><a href="di-si-bu-fen-gong-zuo-liu/">di-si-bu-fen-gong-zuo-liu</a></td></tr><tr><td><h3>🚀</h3></td><td><strong>第六部分 · 项目开发</strong></td><td>新项目从零起，老项目怎么接，一条流程走完。</td><td><a href="di-wu-bu-fen-xiang-mu-kai-fa/">di-wu-bu-fen-xiang-mu-kai-fa</a></td></tr></tbody></table>

一句话记住这六块：**先看地图（一），再补岗位（二、三），配上工具（四），跑通流程（五），最后落到项目（六）。**

## 三条阅读路线 🛣️

{% columns %}
{% column width="50%" %}
**🔄 后端转 AI**

从第一部分看起 → 第二部分只读「后端」和「运维」→ 第五部分工作流 → 第六部分跟一个项目跑完。

你已有的工程直觉（超时、降级、观测、灰度）在这条链路上大部分能直接复用。
{% endcolumn %}

{% column width="50%" %}
**🎓 从零入门**

第一部分 → 第二部分五个岗位都过一遍 → 第三部分按岗位练手 → 第六部分做完整项目。

不用先把模型原理啃完。先知道每一层在干什么，遇到再回头补。
{% endcolumn %}
{% endcolumns %}

{% hint style="info" icon="compass" %}
**只想先动手？** 直接去第六部分的「新项目」，照着流程做一个最小可上线的版本，卡住了再回来查对应章节。
{% endhint %}

## 这本书不写什么 🚧

{% hint style="warning" %}
**四条自我约束**

* 不写「三天速成」这种承诺
* 不写无法验证的性能数字；没实测过的地方明确标「待压测」
* 不把「理解原理」写成「亲手实践过」
* 不把某个框架说成唯一正确答案
{% endhint %}

## 许可 📄

* 书稿与文档：[CC BY-SA 4.0](https://github.com/haiqit/ai-fullstack-guide/blob/main/LICENSE-DOCS)
* 示例代码：[MIT](https://github.com/haiqit/ai-fullstack-guide/blob/main/LICENSE-CODE)
