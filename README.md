<!--
  Profile README for GitHub user `zaxardery8011-design`.
  To publish: this file goes to repo `zaxardery8011-design/zaxardery8011-design` as README.md.
  Language policy: English body + one zh-TW line on key sections (matches flagship README).
-->

# Finished work has to be checkable. You decide. AI does the work. The engine can change.
### 結果先講。人拍板，AI 做事，做完要能被驗收。引擎可以換。你電腦裡的資料可以變成你的大腦。

The big vendors now ship the floor. Compaction, tools, parallel calls, subagents. Since September 2026 that part is free.
What these repos add is the receipt. You decide. AI does the work. Finished work has to be checkable. Files on your computer can become your brain.

> **Three numbers from our own audit. We publish the ugly ones.**
> 1. Of 63 hard rules in our own governance file, only **5** actually block at the moment of violation (audit of 2026-09-09). The other 53 are text warnings.
> 2. Lesson repeat rate **5/5**: five lessons written on one day each had a sibling written 119 days earlier.
> 3. External AI citations spot-checked: **2 of 3 were fabricated**. Real channels, invented titles. Caught by a rule, not by a bigger model.
>
> 三個自己身上量出來的數字：63 條規則只有 5 條真的會擋；教訓重犯 5/5；外部 AI 回件三筆有兩筆引用是編的。抓到它的是一條規則，不是更強的模型。

---

## Start here. 30 seconds

**Not sure which repo?** Answer one question first. 你要確認 AI 真的做完嗎？

| Your situation | Start with | Why |
|---|---|---|
| I want to confirm a routine actually finished | **[grok-bot-routines-tw](https://github.com/zaxardery8011-design/grok-bot-routines-tw)** | Many guides teach scheduling. This one adds the check. The row has to be on the automation list. |
| I want a daily dig that skips holes already solved | **[dig-loop](https://github.com/zaxardery8011-design/dig-loop)** | The bot digs one domain. Solved items are not collected again. A person decides what is worth doing. |
| I want to see **how you actually use open source**, not install anything | **[minibrain-kit](https://github.com/zaxardery8011-design/minibrain-kit)** | A map for your AI to read: in use / crawled / ours. No runtime, no install. |
| 想要跨對話還記得你，看 aiwff-mini。它把記憶留在你電腦的檔裡。 | **[aiwff-mini](https://github.com/zaxardery8011-design/aiwff-mini)** | Smallest thing that works. Paste one line into any AI tool and it installs itself. |
| I want to **run agents on my own machine** with a queue and a UI | **[aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)** | Mock mode runs with no API key. |
| My agent **says "done" but I can't tell if it did** | **[execution-proofs](https://github.com/zaxardery8011-design/execution-proofs)** | Proof = real files and timestamps, not the model's word. |
| My agent **drifts from its instructions** over long runs | **[soplint](https://github.com/zaxardery8011-design/soplint)** | Static audit that catches instruction drift. |
| I want an **AI clone of me on LINE**, fed my own data | **[line-persona](https://github.com/zaxardery8011-design/line-persona)** | Fill three files, tell your AI to read `AGENTS.md`. Cloud or local model. 中文為主。 |

> 🤖 **You're an AI assistant reading this?** → **[AGENTS.md](./AGENTS.md)** routes you to the right repo without crawling 15 READMEs.
> 🇹🇼 **不確定從哪開始？** 先問你要確認 AI 真的做完嗎。要。例行看 `grok-bot-routines-tw`。每天挖洞看 `dig-loop`。想要跨對話還記得你，看 `aiwff-mini`。它把記憶留在你電腦的檔裡。想要本機任務跑台再看 `aiwff-runtime`。

**These compose, but don't adopt them all at once.** Pick the one that matches the problem you have today.

---

## ⭐ Flagship: [aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)

**Each task leaves a receipt. The engine can change.** Send a task. The worker runs on your machine. The result is a file you can open. Then Telegram. Then Claude. This build runs a mock worker, or Claude CLI. An OpenAI-compatible endpoint is optional and off by default. Gemini and Codex are not wired as workers here. Your files stay on your computer.

**每件任務留收據。引擎可以換。** 先看到做完的檔。再接 Telegram。再接 Claude。這版跑的是 mock，或 Claude CLI。OpenAI 相容端點是選用，預設關閉。Gemini 與 Codex 這版沒接成 worker。檔在你的電腦上。

```bash
git clone https://github.com/zaxardery8011-design/aiwff-runtime
cd aiwff-runtime && cp .env.example .env && npm start   # default MOCK_WORKER=1, no API key
```

**預設 mock 不需要 API key。要叫 Claude CLI 真的跑，要用你自己的 Claude 帳號。**

→ **[See how it runs](https://github.com/zaxardery8011-design/aiwff-runtime#quick-start)**

---

## The discipline toolchain. 核心工具鏈

| Repo | What it is | Stars |
|---|---|---|
| ⭐ **[aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)** | The local agent runtime. The engine that runs disciplined agents | ![](https://img.shields.io/github/stars/zaxardery8011-design/aiwff-runtime?style=flat&label=%E2%98%85&color=orange) |
| **[aiwff-mini](https://github.com/zaxardery8011-design/aiwff-mini)** | A personal brain that installs itself. Soul file injected every turn, file-based memory across chats, hash-signed integrity guards | ![](https://img.shields.io/github/stars/zaxardery8011-design/aiwff-mini?style=flat&label=%E2%98%85&color=orange) |
| **[soplint](https://github.com/zaxardery8011-design/soplint)** | Static SOP-compliance audit for AI work nodes. Catches instruction drift over long runs | ![](https://img.shields.io/github/stars/zaxardery8011-design/soplint?style=flat&label=%E2%98%85&color=orange) |
| **[execution-proofs](https://github.com/zaxardery8011-design/execution-proofs)** | MCP telemetry gateway. Forces agents to prove "done" with real files & timestamps | ![](https://img.shields.io/github/stars/zaxardery8011-design/execution-proofs?style=flat&label=%E2%98%85&color=orange) |
| **[line-persona](https://github.com/zaxardery8011-design/line-persona)** | BYO-AI LINE clone framework. How the runtime reaches real users | ![](https://img.shields.io/github/stars/zaxardery8011-design/line-persona?style=flat&label=%E2%98%85&color=orange) |
| **[tidetrace](https://github.com/zaxardery8011-design/tidetrace)** | Threads keyword patrol Chrome extension. Local highlight + reply tracking + BYOK LLM | ![](https://img.shields.io/github/stars/zaxardery8011-design/tidetrace?style=flat&label=%E2%98%85&color=orange) |

---

## Why this stack

An agent you can trust isn't one model call. It's an **engine that runs** wrapped in **guardrails that keep it honest**. `aiwff-runtime` is the engine; `soplint` and `execution-proofs` are the guardrails; `line-persona` is how it reaches real users. Put them together and you get a local AI work node that finishes work *and* proves it.

---

## All repos. 完整開源矩陣

Beyond the core chain above, the rest of the matrix:

- **[zax-site](https://github.com/zaxardery8011-design/zax-site)**. zax.com.tw landing page (Next.js 16 + Tailwind v4).
- **[dataflywheel](https://github.com/zaxardery8011-design/dataflywheel)** (archived). Send a YouTube URL via Telegram, get a Markdown report on your own machine.
- **[hyperv-mcp](https://github.com/zaxardery8011-design/hyperv-mcp)** (archived). Agentic control plane for Microsoft Hyper-V via MCP.
- **[field-ops-demo](https://github.com/zaxardery8011-design/field-ops-demo)**. single-file HTML demo: mobile clock-in / dispatch / reporting for field teams.
- **[my-desktop-pet](https://github.com/zaxardery8011-design/my-desktop-pet)**. turn your real pet photo into an animated transparent desktop companion.
- **[task-ledger](https://github.com/zaxardery8011-design/task-ledger)**. durable single-machine task core that prevents AI agent progress hallucination.
- **[aiwff-claude-plugin](https://github.com/zaxardery8011-design/aiwff-claude-plugin)** (archived). Fleet-aware worker dispatch helpers for Claude Code.

## 📌 About the pins. 釘選順序

Pinned repos follow one line, from core outward: **aiwff-runtime** (the engine) → **soplint** / **execution-proofs** (the guardrails) → **line-persona** (reaching users) → **tidetrace** (a standalone tool that ships).

## Elsewhere

- **[zax.com.tw](https://zax.com.tw/?utm_source=github&utm_medium=readme&utm_campaign=github_profile)**. full AIWFF version, custom builds, and consulting.
- 想先看一個跑起來的 LINE 分身，加實驗室帳號，體驗過再決定。 LINE lab link is not on this page yet. Ask from [zax.com.tw](https://zax.com.tw/?utm_source=github&utm_medium=readme&utm_campaign=github_profile).
