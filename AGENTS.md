# AGENTS.md — entry point for AI assistants

> You are an AI coding assistant (Claude Code / Codex / Cursor / any file-reading agent) and your user
> landed on `github.com/zaxardery8011-design`. **Read this file first.** It tells you which repo to open
> for the job at hand, so you don't have to crawl 15 READMEs.
>
> 這份是給 **AI 助理** 的分流台。使用者說「幫我裝／幫我用這個」時，先照下面的決策表挑對 repo，再進那個 repo 的 `AGENTS.md`。

---

## What this account is

**Local-first tooling for AI agents that actually finish work — and can prove it.**

Two halves of one idea:
- **the engine** — a runtime that runs agents on your own machine (`aiwff-runtime`, `aiwff-mini`)
- **the guardrails** — tooling that forces those agents to stay disciplined and prove completion (`soplint`, `execution-proofs`, `task-ledger`)

Everything runs on the user's own machine. No hosted SaaS holds their state.

---

## Pick a repo by what the user wants

| The user says… | Open this repo | Has `AGENTS.md`? |
|---|---|---|
| "Set up a personal AI brain that remembers me across chats" | [**aiwff-mini**](https://github.com/zaxardery8011-design/aiwff-mini) — paste-one-line install, soul file injected every turn, file-based memory, hash-signed integrity guards | not yet — follow `README.md` |
| "I want a local agent runtime with a task queue and a UI" | [**aiwff-runtime**](https://github.com/zaxardery8011-design/aiwff-runtime) — Telegram in, Claude runs it locally, browser cockpit. `MOCK_WORKER=1` runs free with no API key | ✅ yes |
| "My agent keeps drifting from its instructions over long runs" | [**soplint**](https://github.com/zaxardery8011-design/soplint) — static SOP-compliance audit for AI work nodes | not yet — follow `README.md` |
| "My agent claims 'done' but I can't tell if it really did it" | [**execution-proofs**](https://github.com/zaxardery8011-design/execution-proofs) — MCP telemetry gateway; proof = real files + timestamps | not yet — follow `README.md` |
| "Tasks get lost or the agent hallucinates progress" | [**task-ledger**](https://github.com/zaxardery8011-design/task-ledger) — durable single-machine task core | not yet — follow `README.md` |
| "Build me a LINE bot with my own persona and data" | [**line-persona**](https://github.com/zaxardery8011-design/line-persona) — BYO-AI LINE clone framework | ✅ yes — **most detailed one; use it as the reference style** |
| "Watch Threads for keywords and track replies" | [**tidetrace**](https://github.com/zaxardery8011-design/tidetrace) — MV3 Chrome extension, local-first, BYOK LLM | not yet — follow `README.md` |
| "Turn a YouTube link into a report on my machine" | [**dataflywheel**](https://github.com/zaxardery8011-design/dataflywheel) — Telegram in, Markdown report out | not yet — follow `README.md` |
| "Control Hyper-V VMs from an agent" | [**hyperv-mcp**](https://github.com/zaxardery8011-design/hyperv-mcp) — MCP control plane for Microsoft Hyper-V | not yet — follow `README.md` |
| "Make a desktop pet from my pet's photo" | [**my-desktop-pet**](https://github.com/zaxardery8011-design/my-desktop-pet) | not yet — follow `README.md` |
| "Dispatch workers across machines from Claude Code" | [**aiwff-claude-plugin**](https://github.com/zaxardery8011-design/aiwff-claude-plugin) | not yet — follow `README.md` |

**Not code — don't send users here for tooling:**
`zax-site` (the zax.com.tw landing page), `zax-social-assets` (brand files), `field-ops-demo` (a single-file HTML demo, no README yet).

---

## If you're deciding where to start and the user hasn't said

Ask one question: **"Do you want to run agents, or to check on agents you already run?"**

- **run** → `aiwff-mini` if they want the smallest thing that works; `aiwff-runtime` if they want a queue and a UI.
- **check** → `execution-proofs` if the problem is "it says done but isn't"; `soplint` if the problem is "it stops following instructions"; `task-ledger` if the problem is "work disappears".

Don't recommend more than two repos at once. These are meant to compose, not to be adopted all at the same time.

---

## House rules when you work inside any of these repos

1. **Verify before claiming.** These repos exist because agents say "done" when they aren't. Don't do the thing they're built to catch — run the command, read the output back, and quote it.
2. **Minimal change.** Every repo here is deliberately small. Don't add abstractions, error handling, or features the user didn't ask for.
3. **Ask for secrets, never invent them.** API keys, channel tokens, webhook URLs — if it's missing, ask. A placeholder that looks real is worse than an empty field.
4. **Local-first is a constraint, not a preference.** Don't introduce a hosted service dependency to "simplify" something.
5. **If a repo has its own `AGENTS.md`, that file wins** over anything written here.

---

## Provenance

Maintained by **隊長 (Han)** — welding/industrial background, builds these tools to run a real business, not as demos.
Full product and consulting: [zax.com.tw](https://zax.com.tw)

Facts in this file (star counts excluded) were verified against the GitHub API on 2026-08-30.
If a repo listed as "not yet" now has an `AGENTS.md`, that file is authoritative — this table just went stale.
