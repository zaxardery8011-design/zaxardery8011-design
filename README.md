<!--
  Profile README for GitHub user `zaxardery8011-design`.
  To publish: this file goes to repo `zaxardery8011-design/zaxardery8011-design` as README.md.
  Language policy: English body + one zh-TW line on key sections (matches flagship README).
-->

# Anyone can make AI agents run. I build the part that lets one person keep a crowd of bluffing agents in check.
### 別人做的是讓 AI 跑得動。我們做的是讓一個人管得住一群會唬爛的 AI。

Context compaction, tool loading, parallel calls, subagents: since September 2026 the big vendors ship all of that for free. It is the floor now.
What is not on the floor: a way for **one person to audit what a fleet of agents claims**. That is what these repos are.

> **Three numbers from our own audit. We publish the ugly ones.**
> 1. Of 63 hard rules in our own governance file, only **5** actually block at the moment of violation. The other 53 are text warnings.
> 2. Lesson repeat rate **5/5**: five lessons written on one day each had a sibling written 119 days earlier.
> 3. External AI citations spot-checked: **2 of 3 were fabricated**. Real channels, invented titles. Caught by a rule, not by a bigger model.
>
> 三個自己身上量出來的數字：63 條規則只有 5 條真的會擋；教訓重犯 5/5；外部 AI 回件三筆有兩筆引用是編的。抓到它的是一條規則，不是更強的模型。

---

## Start here — 30 seconds

**Not sure which repo?** Answer one question:

| Your situation | Start with | Why |
|---|---|---|
| I want a personal AI brain that **remembers me across chats** | **[aiwff-mini](https://github.com/zaxardery8011-design/aiwff-mini)** | Smallest thing that works. Paste one line into any AI tool and it installs itself. |
| I want to **run agents on my own machine** with a queue and a UI | **[aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)** | Free to try — `MOCK_WORKER=1` runs the full loop with no API key. |
| My agent **says "done" but I can't tell if it did** | **[execution-proofs](https://github.com/zaxardery8011-design/execution-proofs)** | Proof = real files and timestamps, not the model's word. |
| My agent **drifts from its instructions** over long runs | **[soplint](https://github.com/zaxardery8011-design/soplint)** | Static audit that catches instruction drift. |

> 🤖 **You're an AI assistant reading this?** → **[AGENTS.md](./AGENTS.md)** routes you to the right repo without crawling 15 READMEs.
> 🇹🇼 **不確定從哪開始？** 想要「記得住你的個人主腦」→ `aiwff-mini`；想要「跑得動的本機 agent 平台」→ `aiwff-runtime`；覺得「AI 說做完但沒做」→ `execution-proofs`。

**These compose, but don't adopt them all at once.** Pick the one that matches the problem you have today.

---

## ⭐ Flagship — [aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)

**A local minimal brain.** Send a task to Telegram, Claude runs it on *your* machine, the result is pushed back, and you watch progress in the browser. Every task, log, and artifact is a plain file on your computer — no hosted SaaS holding your state.

```bash
git clone https://github.com/zaxardery8011-design/aiwff-runtime
cd aiwff-runtime && cp .env.example .env && npm start   # default MOCK_WORKER=1 → free, no API key
```

**免費跑通**：預設 mock 模式不需 API key、不需付費，就能看完整「建任務 → 執行 → 寫結果」。想接真 Claude worker 才需要付費的 Claude 訂閱。

→ **[See how it runs](https://github.com/zaxardery8011-design/aiwff-runtime#quick-start)**

---

## The discipline toolchain — 核心工具鏈

| Repo | What it is | Stars |
|---|---|---|
| ⭐ **[aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)** | The local agent runtime — the engine that runs disciplined agents | ![](https://img.shields.io/github/stars/zaxardery8011-design/aiwff-runtime?style=flat&label=%E2%98%85&color=orange) |
| **[aiwff-mini](https://github.com/zaxardery8011-design/aiwff-mini)** | A personal brain that installs itself — soul file injected every turn, file-based memory across chats, hash-signed integrity guards | ![](https://img.shields.io/github/stars/zaxardery8011-design/aiwff-mini?style=flat&label=%E2%98%85&color=orange) |
| **[soplint](https://github.com/zaxardery8011-design/soplint)** | Static SOP-compliance audit for AI work nodes — catches instruction drift over long runs | ![](https://img.shields.io/github/stars/zaxardery8011-design/soplint?style=flat&label=%E2%98%85&color=orange) |
| **[execution-proofs](https://github.com/zaxardery8011-design/execution-proofs)** | MCP telemetry gateway — forces agents to prove "done" with real files & timestamps | ![](https://img.shields.io/github/stars/zaxardery8011-design/execution-proofs?style=flat&label=%E2%98%85&color=orange) |
| **[line-persona](https://github.com/zaxardery8011-design/line-persona)** | BYO-AI LINE clone framework — how the runtime reaches real users | ![](https://img.shields.io/github/stars/zaxardery8011-design/line-persona?style=flat&label=%E2%98%85&color=orange) |
| **[tidetrace](https://github.com/zaxardery8011-design/tidetrace)** | Threads keyword patrol Chrome extension — local highlight + reply tracking + BYOK LLM | ![](https://img.shields.io/github/stars/zaxardery8011-design/tidetrace?style=flat&label=%E2%98%85&color=orange) |

---

## Why this stack

An agent you can trust isn't one model call — it's an **engine that runs** wrapped in **guardrails that keep it honest**. `aiwff-runtime` is the engine; `soplint` and `execution-proofs` are the guardrails; `line-persona` is how it reaches real users. Put them together and you get a local AI work node that finishes work *and* proves it.

---

## All repos — 完整開源矩陣

Beyond the core chain above, the rest of the matrix:

- **[zax-site](https://github.com/zaxardery8011-design/zax-site)** — zax.com.tw landing page (Next.js 16 + Tailwind v4).
- **[dataflywheel](https://github.com/zaxardery8011-design/dataflywheel)** — send a YouTube URL via Telegram, get a Markdown report on your own machine.
- **[hyperv-mcp](https://github.com/zaxardery8011-design/hyperv-mcp)** — agentic control plane for Microsoft Hyper-V via MCP.
- **[field-ops-demo](https://github.com/zaxardery8011-design/field-ops-demo)** — single-file HTML demo: mobile clock-in / dispatch / reporting for field teams.
- **[my-desktop-pet](https://github.com/zaxardery8011-design/my-desktop-pet)** — turn your real pet photo into an animated transparent desktop companion.
- **[task-ledger](https://github.com/zaxardery8011-design/task-ledger)** — durable single-machine task core that prevents AI agent progress hallucination.
- **[aiwff-claude-plugin](https://github.com/zaxardery8011-design/aiwff-claude-plugin)** — fleet-aware worker dispatch helpers for Claude Code.

## 📌 About the pins — 釘選順序

Pinned repos follow one line, from core outward: **aiwff-runtime** (the engine) → **soplint** / **execution-proofs** (the guardrails) → **line-persona** (reaching users) → **tidetrace** (a standalone tool that ships).

## Elsewhere

- **[zax.com.tw](https://zax.com.tw)** — full AIWFF version, custom builds, and consulting.
- **LINE 主腦實驗室** — don't want to install anything? Chat with a running brain first, then decide. / 不想自己裝？先在 LINE 跟一個跑起來的主腦聊，體驗過再決定。 *(link coming — ask via [zax.com.tw](https://zax.com.tw) meanwhile)*
