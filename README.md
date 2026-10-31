<div align="center">
<img src="./images/banner.png" alt="AI 全栈实战指南" width="950px">
# 🚀 AI 全栈实战指南 · 从零到企业级落地

<sub>ai-fullstack-guide</sub>

**2026 持续更新中** · 目标是把 AI 能力从「跑通一个 Demo」推进到「一套能上线、能运维、成本算得清的系统」—— 系统教程 + 可运行的示例 + 面试视角 + 企业级项目，对齐「AI 应用开发工程师」的真实工作要求。

**简体中文** · [English](./README.en.md)

[![AI 全栈](https://img.shields.io/badge/AI-全栈-2ea44f)](#)
[![language](https://img.shields.io/badge/language-Chinese-2ea44f)](#)
[![GitHub stars](https://img.shields.io/github/stars/haiqit/ai-fullstack-guide?style=social)](https://github.com/haiqit/ai-fullstack-guide)
[![在线阅读](https://img.shields.io/badge/在线阅读-点击访问-1f6feb)](https://haiqit.gitbook.io/ai-fullstack-guide)

[快速开始](#怎么读) · [教程大纲](#目录) · [更新日志](https://github.com/haiqit/ai-fullstack-guide/commits/main)

📚 **在线阅读** → [https://haiqit.gitbook.io/ai-fullstack-guide](https://haiqit.gitbook.io/ai-fullstack-guide)

</div>

---

## 这本书在讲什么

大多数 AI 教程的终点，是「Demo 跑通了」。但一旦上线，等着你的是另一组问题：

- 一次请求要 8 秒，用户还愿意等吗？
- 这个月账单翻了三倍，钱花在哪儿？
- 模型抽风、接口超时，服务会不会跟着雪崩？
- 改了一版提示词，到底是变好了还是变坏了？

这本书用工程视角，把这些问题的答案整理成可以复用的方法和取舍。

全书分六部分，顺序是**先补岗位，再配工具，最后落到项目**：

```text
① 岗位基础   产品 · UI · 前端 · 后端 · 运维
      ↓
② 岗位实操   按岗位动手
③ 开发工具   模型 · IDE · MCP · Skills
      ↓
④ 工作流     Vibe Coding · SDD · Harness
      ↓
⑤ 项目开发   流程 · 新项目 · 老项目
      ↓
⑥ 项目实战   完整项目走一遍
```

第一部分「岗位基础」已经写完，五个岗位各成一条线，可以当五本小册子单独读。每个岗位都是同一个路子：

> 先破误解 → 知识模块 → 选型表 → 决策 → 技术后果映射表 → 通用坑 → 提问模板

## 适合谁读

- **后端工程师**：有 Go / Java / Python 服务端经验，想转向 AI 方向
- **全栈工程师**：想把模型能力接进自己的产品，而不是停留在调 API
- **AI 应用开发者**：已经能写出 Demo，但要解决它在真实流量下的稳定性问题

## 不适合谁

- 想深造模型训练、微调、论文复现的读者（本书不覆盖训练向内容）
- 完全零编程基础的读者

## 目录

状态：✅ 已成体系，🚧 写作中。

- ✅ **第一部分 · 岗位基础**
  - **产品**：需求优先级、用户故事与验收、状态机、B/C 端差异、商业化与合规
  - **UI**：信息架构、栅格与 token、组件与设计系统、五态、断点、交付验收
  - **前端**：选型七层、服务端 vs 客户端状态、数据请求层、表单、构建、类型、性能与部署
  - **后端**：多租户隔离、并发正确性、幂等、状态机、缓存一致性、队列异步、可观测性、部署架构
  - **运维**：部署与发布、稳定性保障、基础设施与安全
- 🚧 **第二部分 · 岗位实操**：产品设计、UI 实战、前端开发、后端开发、运维部署
- 🚧 **第三部分 · 开发工具**：模型、IDE、MCP、Skills
- 🚧 **第四部分 · 工作流**：Vibe Coding、SDD、Harness、工具推荐
- 🚧 **第五部分 · 项目开发**：开发流程、新项目、老项目
- 🚧 **第六部分 · 项目实战**

书稿在 `docs/ai-fullstack-guide/`，通过 GitBook 同步发布，在线阅读地址见文首。

## 怎么读

- 每章尽量以「问题 → 方案 → 取舍 → 示例」的顺序组织
- 性能数字只写有来源的；没实测过的地方明确标「待压测」
- 代码以 Python 为主，需要对照后端习惯的地方会给 Go 类比；后端章节做 Go / Python / Java 三语言对照

## 这本书不写什么

- 不写「三天速成」这种承诺
- 不写无法验证的性能数字
- 不把「理解原理」写成「亲手实践过」
- 不把某个框架说成唯一正确答案

## 参与贡献

本书开源，欢迎勘误、补充和讨论：

- **发现错误** → 提 [Issue](https://github.com/haiqit/ai-fullstack-guide/issues)
- **修改内容** → 提交 Pull Request
- **新增章节** → 先在 Issue 里讨论范围，再动手

## 许可

- 书稿与文档内容：[CC BY-SA 4.0](./LICENSE-DOCS)
- 示例代码：[MIT](./LICENSE-CODE)
