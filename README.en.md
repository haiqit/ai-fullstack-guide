<div align="center">

# 🚀 AI Full-Stack Field Guide · From Zero to Production

<sub>ai-fullstack-guide</sub>

**Continuously updated in 2026** · Taking AI capabilities from "the demo runs" to "a system that ships, can be observed, and whose cost you can actually explain" — structured lessons + runnable examples + an interview mindset + a production-grade project, aligned with what "AI application engineer" jobs really ask for.

[简体中文](./README.md) · **English**

[![AI Full-Stack](https://img.shields.io/badge/AI-Full--Stack-2ea44f)](#)
[![language](https://img.shields.io/badge/language-English-2ea44f)](#)
[![GitHub stars](https://img.shields.io/github/stars/haiqit/ai-fullstack-guide?style=social)](https://github.com/haiqit/ai-fullstack-guide)
[![Read online](https://img.shields.io/badge/Read%20Online-Visit-1f6feb)](https://haiqit.gitbook.io/ai-fullstack-guide)

[Quick Start](#how-to-read) · [Outline](#table-of-contents) · [Changelog](https://github.com/haiqit/ai-fullstack-guide/commits/main)

📚 **Read online** → [https://haiqit.gitbook.io/ai-fullstack-guide](https://haiqit.gitbook.io/ai-fullstack-guide)

</div>

---

## What this book is about

Most AI tutorials end at "the demo runs." Once you ship, a different set of questions shows up:

- A request takes 8 seconds — will users wait?
- This month's bill tripled — where did the money go?
- The model hiccups, an API times out — does the whole service fall over with it?
- You changed the prompt — did it get better or worse?

This book turns the engineering answers to those questions into reusable methods and trade-offs.

Six parts, in this order: **roles first, then tooling, then a real project.**

```text
① Roles         Product · UI · Frontend · Backend · Ops
      ↓
② Hands-on      One practice track per role
③ Tooling       Models · IDE · MCP · Skills
      ↓
④ Workflow      Vibe Coding · SDD · Harness
      ↓
⑤ Building      Process · New project · Legacy project
      ↓
⑥ Capstone      One project, end to end
```

Part 1 (Roles) is complete. Each role is its own line and reads like a small booklet. Every one follows the same shape:

> Bust the misconception → knowledge modules → selection tables → decisions → decision-to-consequence map → common pitfalls → prompt templates

## Who it's for

- **Backend engineers** with Go / Java / Python service experience who want to move into AI
- **Full-stack engineers** who want model capabilities inside their product, not just an API call
- **AI application developers** whose demo works but falls apart under real traffic

## Who it's not for

- Readers looking for model training, fine-tuning, or paper reproduction (out of scope)
- Complete beginners with no programming background

## Table of contents

Status: ✅ complete · 🚧 in progress.

- ✅ **Part 1 · Roles**
  - **Product**: prioritization, user stories and acceptance, state machines, B2B vs B2C, monetization and compliance
  - **UI**: information architecture, grids and tokens, components and design systems, the five states, breakpoints, delivery and acceptance
  - **Frontend**: seven selection layers, server vs client state, the data layer, forms, build, types, performance and deployment
  - **Backend**: multi-tenancy, concurrency correctness, idempotency, state machines, cache consistency, queues, observability, deployment architecture
  - **Ops**: deployment and release, reliability engineering, infrastructure and security
- 🚧 **Part 2 · Hands-on**: product design, UI practice, frontend dev, backend dev, ops deployment
- 🚧 **Part 3 · Tooling**: models, IDE, MCP, Skills
- 🚧 **Part 4 · Workflow**: Vibe Coding, SDD, Harness, recommendations
- 🚧 **Part 5 · Building**: process, new project, legacy project
- 🚧 **Part 6 · Capstone**

The manuscript lives in `docs/ai-fullstack-guide/` and is published through GitBook — see the link at the top.

## How to read

- Each chapter follows "problem → options → trade-off → example"
- Performance numbers are only included with a source; anything not benchmarked is explicitly marked as untested
- Code is mostly Python, with Go analogies where it helps; backend chapters include Go / Python / Java comparisons

## What this book won't do

- Promise you a three-day crash course
- Quote performance numbers it can't verify
- Call "understood the principle" the same thing as "shipped it"
- Declare any framework the one correct answer

## Contributing

Open source — corrections and additions welcome:

- **Found a mistake** → open an [Issue](https://github.com/haiqit/ai-fullstack-guide/issues)
- **Want to change content** → send a Pull Request
- **New chapter** → discuss the scope in an Issue first

## License

- Book text and docs: [CC BY-SA 4.0](./LICENSE-DOCS)
- Sample code: [MIT](./LICENSE-CODE)
