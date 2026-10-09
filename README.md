<!--
  Profile README for zaxardery8011-design（放到 repo zaxardery8011-design/zaxardery8011-design 的 README.md）
  語言：繁中先行，最底附 English
-->

# 一台電腦，當一座 AI 廠區
### 別人做的是讓 AI 跑得動。我們做的是讓一個人管得住一群會唬爛的 AI

我們主核心用 Claude，在自己的電腦上養了一群 AI 分工做事
做久了發現，難的不是讓它跑，是知道它說「做完了」的時候到底有沒有做完
這裡放的就是我們一路踩坑做出來的東西，全部開源

> **兩個自己身上量出來的數字，難看的我們也照貼**
> 1. 自己的規矩檔有 63 條硬規則，違規當下真的會擋下來的只有 **5 條**，其他都只是寫在那邊的字（2026-09-09 自查）
> 2. 外部 AI 交回來的引用抽查 3 筆，**2 筆是編的**——頻道是真的，標題是捏的。抓到它的是一條規則，不是更強的模型

---

## 從哪個門進來（30 秒）

| 你想要的是 | 從這裡進 | 先做這一步 |
|---|---|---|
| 🏭 **看一台電腦怎麼當 AI 廠區** | **[aiwff-runtime](https://github.com/zaxardery8011-design/aiwff-runtime)** | 預設 `MOCK_WORKER=1`，不用 API key、不用付錢就能跑完整一圈 |
| 📏 **替你自己的 AI 加規矩** | **[soplint](https://github.com/zaxardery8011-design/soplint)** | 拿你現有的 AI 指令檔跑一次，看它哪裡會飄 |
| 🧰 **拿現成的小工具就好** | **[line-persona](https://github.com/zaxardery8011-design/line-persona)**（LINE 分身）／**[tidetrace](https://github.com/zaxardery8011-design/tidetrace)**（脆關鍵字巡邏）／**[x-fetch](https://github.com/zaxardery8011-design/x-fetch)** | 每支 README 第一段就是安裝 |

> 🤖 你是 AI 助理在讀這頁？→ **[AGENTS.md](./AGENTS.md)** 直接帶你到對的 repo，不用一支一支爬

**不用一次全裝**，挑今天卡住你的那一個就好

---

## 全部列表

**護欄**
- [execution-proofs](https://github.com/zaxardery8011-design/execution-proofs) — 逼 AI 用真檔案和時間戳證明「做完了」，不是用嘴
- [task-ledger](https://github.com/zaxardery8011-design/task-ledger) — 單機任務帳本，防 AI 謊報進度

**主腦**
- [aiwff-mini](https://github.com/zaxardery8011-design/aiwff-mini) — 會自己安裝的個人主腦：靈魂檔每輪注入、被改動會告警
- [minibrain-kit](https://github.com/zaxardery8011-design/minibrain-kit) — 給你的 AI 讀的地圖：我們在用哪些開源、怎麼用
- [minibrain-cli](https://github.com/zaxardery8011-design/minibrain-cli) — 六個動詞包本機工具，寫給另一個 AI 照著做
- [aiwff-claude-plugin](https://github.com/zaxardery8011-design/aiwff-claude-plugin) — Claude Code 派工小幫手

**其他**
- [dataflywheel](https://github.com/zaxardery8011-design/dataflywheel) — 丟 YouTube 網址到 Telegram，本機產 Markdown 筆記
- [hyperv-mcp](https://github.com/zaxardery8011-design/hyperv-mcp) — 用 MCP 操作 Hyper-V
- [field-ops-demo](https://github.com/zaxardery8011-design/field-ops-demo) — 外勤打卡／派工／回報單檔示範
- [my-desktop-pet](https://github.com/zaxardery8011-design/my-desktop-pet) — 把你家寵物照片變成桌面動畫
- [zax-site](https://github.com/zaxardery8011-design/zax-site) — zax.com.tw 官網原始碼

---

## 走到這裡了，來報到

- 🩺 **[AI 健檢（公開測試版）](https://github.com/zaxardery8011-design/aiwff-checkup-public)** — 先對照你的自評和電腦上的掃描，找可能缺的那一段。**測試版，會誤判，自動判定還沒校準完**，結果要人再看；覺得不準歡迎開 issue 告訴我們
- 🏘️ **[未來村](https://future-village.github.io)** — 用過、試過、想一起玩的，來這裡報到
- 💬 **LINE 主腦實驗室** — 不想裝東西？先跟一個跑起來的主腦聊聊 → [`@395jcpsb`](https://line.me/R/ti/p/@395jcpsb)
- 🌐 **[zax.com.tw](https://zax.com.tw)** — 完整版、客製與顧問

---

判斷與拍板：隊長；草稿與查證：主腦

<details>
<summary>English</summary>

Anyone can make AI agents run. We build the part that lets one person keep a crowd of bluffing agents in check — on one ordinary computer.

- See a single PC run as an AI work floor → **aiwff-runtime** (`MOCK_WORKER=1`, no API key needed)
- Put rules on your own AI → **soplint**
- Just want a ready-made tool → **line-persona** / **tidetrace** / **x-fetch**

AI assistants: start at [AGENTS.md](./AGENTS.md).
Public-beta checkup — compares your self-assessment with a scan of your machine to spot the piece that may be missing. Test version: it misjudges, auto-scoring is not calibrated yet, and a human should review the result: [aiwff-checkup-public](https://github.com/zaxardery8011-design/aiwff-checkup-public). Check in at [future-village.github.io](https://future-village.github.io).
</details>
