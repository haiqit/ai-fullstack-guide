# OpenSpec

不是每个项目都从零开始。大多数时候，你面对的是一坨已经跑了两年的代码，需求散在聊天记录、Jira 和几个人的脑子里。OpenSpec 想干的就一件事：**在动手之前，把这次要改什么写成一份人和 AI 都能读的东西。**

它不追求把开发变成流水线。作者自己的定位是四句话：fluid not rigid、iterative not waterfall、easy not complex、built for brownfield。翻成人话就是——规矩要有，但别把路堵死，尤其是别假设你在一张白纸上盖房子。

## 一次改动长什么样 🗂️

你不直接让 AI 写代码，而是先在 `openspec/` 下开一个 change 目录。AI 和你一起把四份东西填出来：

```
openspec/
├── specs/                        # 已经生效的能力规格
└── changes/
    ├── add-dark-mode/            # 一次进行中的改动
    │   ├── proposal.md           # 为什么要做，改什么
    │   ├── design.md             # 技术方案
    │   ├── tasks.md              # 实现清单
    │   └── specs/                # 本次改动涉及的规格
    └── archive/
        └── 2026-01-23-add-dark-mode/
```

注意最后那个 `archive/`。改动做完不是删掉，而是归档，同时把 `specs/` 里的能力规格更新掉。**specs 是现在系统长什么样，changes 是这次要把它变成什么样。** 这两个东西分开，是 OpenSpec 跟「随手写个 PRD」最大的区别。

## 装它 🧰

macOS / Linux 一条命令：

```bash
curl -fsSL https://openspec.dev/cli/install.sh | sh
```

Windows 用 PowerShell：

```powershell
irm https://openspec.dev/cli/install.ps1 | iex
```

有包管理器的话更稳：

{% tabs %}
{% tab title="npm" %}
```bash
npm install -g @fission-ai/openspec@latest   # 需要 Node 22.12+
```
{% endtab %}

{% tab title="Homebrew" %}
```bash
brew install openspec
```
{% endtab %}
{% endtabs %}

进到项目目录，初始化：

```bash
cd your-project
openspec init
```

`init` 会问你用哪些 AI 工具，然后按工具生成对应的斜杠命令。支持三十多种，主流的都在。

## 四个命令跑完一轮 🏃

默认配置下就四个命令，够用了：

| 命令                    | 什么时候用     | 结果                                        |
| --------------------- | --------- | ----------------------------------------- |
| `/opsx:explore`       | 还没想清楚要做什么 | 读代码、比较方案，产出一份思路                           |
| `/opsx:propose <改动名>` | 知道要做什么了   | 建 change 目录，写 proposal、specs、design、tasks |
| `/opsx:apply`         | 方案审过了     | 按 tasks 逐条实现                              |
| `/opsx:archive`       | 做完了       | 归档到 `changes/archive/`，同步更新 `specs/`      |

想细一点，可以切到扩展档：

```bash
openspec config profile
openspec update
```

之后会多出 `/opsx:new`、`/opsx:continue`、`/opsx:ff`、`/opsx:verify`、`/opsx:bulk-archive`、`/opsx:onboard`。我的建议是先别切，默认的四个已经能覆盖大部分日常。

命令的写法会因工具而异：Claude Code 里是 `/opsx:propose`，Cursor 和 Copilot 可能是 `/opsx-propose`，Codex 是 `$openspec-propose`。别背，`init` 结束时会告诉你。

## 规格到底写成什么样 ✍️

没有自定义语法，就是普通 Markdown，一条需求配几个场景：

```markdown
## ADDED Requirements

### Requirement: 主题切换
应用应当允许用户在浅色和深色主题之间切换，
默认跟随系统偏好。

#### Scenario: 用户切换深色模式
- **WHEN** 用户点击主题切换按钮
- **THEN** 应用切到深色模式，并记住这个选择
```

这种写法有个好处：它同时约束了 AI 和验收。`WHEN / THEN` 是能被测试直接对应的，写完规格基本就知道测试该怎么写。比「支持深色模式」这种一句话需求硬得多。

## 和 Spec Kit 比，差在哪 ⚖️

|    | OpenSpec               | Spec Kit                        |
| -- | ---------------------- | ------------------------------- |
| 体量 | 轻，一个 CLI + 一堆 Markdown | 重，模板、脚本、扩展、预设全都有                |
| 阶段 | 没有硬性门禁，哪个文件都能改         | 有明确的阶段推进                        |
| 上手 | `openspec init` 完事     | 要 Python 3.11+、uv、选 integration |
| 适合 | 已有项目、需求变化快             | 新项目、团队要对齐一套固定流程                 |

这不是谁好谁坏。**你要的是「随手能改的规格」，选 OpenSpec；你要的是「谁都不能跳步」，选 Spec Kit。**

## 几个我踩过的坑 🕳️

* **proposal 写成 PRD。** 越写越厚，最后连自己都不看。proposal 只需要回答「为什么做、做什么、不做什么」，方案交给 design。
* **同时开三个 change。** `changes/` 下三个目录互相引用同一份 specs，改到最后不知道哪个是准的。一次一个，做完归档再开下一个。
* **忘了 archive。** 这是最常见的。change 做完了不归档，`specs/` 就没更新，下次 AI 读到的还是旧规格，然后你开始怀疑它为什么老做错。
* **跳过 explore 直接 propose。** 老项目里尤其要命。你以为改的是一个工具函数，实际它被七个地方依赖。让 AI 先读一遍代码，比事后返工便宜。
* **升级完 CLI 不跑 `openspec update`。** 新命令没注册上，你在那儿敲半天没反应。

{% hint style="warning" icon="triangle-exclamation" %}
官方建议配高推理模型，并且**在开始实现前清一次上下文**。规格已经在文件里了，不需要把整段讨论也带进实现阶段——带进去只会让模型分心。
{% endhint %}

## 什么时候别用 🚫

* 改个文案、调个样式，开 change 目录的成本比改动本身高。
* 纯探索、写个一次性脚本。
* 团队里没人愿意看 Markdown。规格没人读，它就只是 AI 的上下文，价值少一半。

## 一句话

**OpenSpec 把「先说清楚再动手」做成了一个目录结构——轻到你能天天用，又硬到 AI 没法糊弄。**
