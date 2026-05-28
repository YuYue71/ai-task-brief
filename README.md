以下為更新後的 `README.md` 內容，已整合「協作狀態轉移協議」並維持原有架構。

---

# AI Task Brief — Universal AI Collaboration Template

# AI 任務範本 — 通用 AI 協作上下文框架

> A zero-config context template that gets any AI assistant up to speed on your project in seconds.
> 一份零設定的上下文範本，讓任何 AI 助手在數秒內進入你的專案狀態。

---

## What is this? / 這是什麼？

**EN:** `AI Task Brief` is a structured Markdown template you paste at the start of every AI conversation. It eliminates the "explain my project again" tax by encoding your tech stack, file structure, scene hierarchy, progress board, and current task into a single living document that the AI can parse instantly.

**ZH:** `AI Task Brief` 是一份結構化的 Markdown 範本，在每次 AI 對話開始時貼入。它將技術棧、檔案結構、物件層級、進度看板與當前任務編碼進單一文件，讓 AI 無需重複說明即可立即進入狀況。

---

## How it works / 運作流程

```
┌─────────────────────────────────────────────────┐
│  1. Copy template  →  Fill SECTION 0–3 once     │
│     複製範本           填寫 SECTION 0–3（一次性）  │
├─────────────────────────────────────────────────┤
│  2. Paste into AI chat at conversation start    │
│     每次對話開頭貼入 AI 對話                        │
├─────────────────────────────────────────────────┤
│  3. AI reads STATUS in SECTION 4                │
│     AI 讀取 SECTION 4 的 STATUS 旗標              │
│     EMPTY  →  AI asks for next task             │
│     FILLED →  AI starts working immediately     │
├─────────────────────────────────────────────────┤
│  4. Task done → AI prompts template update      │
│     任務完成 → AI 主動詢問並輸出更新版 .md          │
└─────────────────────────────────────────────────┘

```

---

## Quick Start / 快速開始

**EN:**

1. **Easy Way:** Copy the raw content of `templates/ai_context.md` and paste it into your AI chat.
2. **Automated Setup:** The AI will detect the `STATUS: EMPTY` and automatically guide you through a brief interview to populate the tech stack, structure, and current tasks.
3. **GitHub Direct:** You can also provide the URL [https://github.com/YuYue71/ai-task-brief/blob/main/templates/ai_context.md](https://www.google.com/search?q=https://github.com/YuYue71/ai-task-brief/blob/main/templates/ai_context.md) to your AI to initialize the project context instantly.

**ZH:**

1. **簡易方式：** 複製 `templates/ai_context.md` 的原始內容並貼入 AI 對話。
2. **自動導引：** AI 偵測到 `STATUS: EMPTY` 後，會自動引導你完成技術棧、結構與當前任務的填寫，無需手動修改 Markdown。
3. **GitHub 直連：** 你也可以直接將 GitHub 連結 [https://github.com/YuYue71/ai-task-brief/blob/main/templates/ai_context.md](https://www.google.com/search?q=https://github.com/YuYue71/ai-task-brief/blob/main/templates/ai_context.md) 提供給 AI，讓它直接抓取範本內容並初始化對話。

---

## Workflow Migration Protocol / 協作狀態轉移協議

**EN:** Need to switch AI chats or start a fresh session? No problem. Simply ask your current AI to "generate a full status snapshot .md". The AI will consolidate your entire project context into a single file that you can paste into any new chat window to instantly restore your workspace.

**ZH:** 需要更換聊天窗口或重啟協作環境嗎？只需要求當前 AI：「請生成目前專案進度的完整任務菜單 (Full Status Snapshot) .md」。AI 將彙整當前所有 context 到一份文件中，你只需將其貼入新的聊天窗口，即可無痛轉移並恢復完整工作環境。

---

## Template Sections / 範本區段說明

| Section | Purpose (EN) | 用途 (ZH) |
| --- | --- | --- |
| SECTION 0 | Immutable tech stack | 不變的技術棧 |
| SECTION 1 | Script / module map | 腳本 / 模組地圖 |
| SECTION 2 | Scene / object / component tree | 場景 / 物件 / 元件樹 |
| SECTION 3 | Development kanban | 開發進度看板 |
| SECTION 4 | Active task brief (AI-managed) | 當前任務（AI 自動管理） |
| SECTION 5 | Coding contract | 編碼規範 |
| SECTION 6 | AI output rules | AI 輸出規則 |

---

## i18n / 多語言支援

**EN:** The default template language is English. When an AI first builds your task list from `STATUS: EMPTY`, it will detect the language you write in and automatically append translations inline — no configuration needed.

**ZH:** 預設範本語言為英文。當 AI 首次從 `STATUS: EMPTY` 建置任務清單時，會自動偵測你所使用的語言，並在英文後方行內附加對應語言的譯文，無需任何設定。

---

## Files / 檔案說明

```
ai-task-brief/
├── templates/
│   └── ai_context.md          # The template / 主範本
├── docs/
│   ├── section-guide.md       # Detailed section guide / 區段填寫指南
│   └── faq.md                 # FAQ / 常見問題
├── .github/
│   └── ISSUE_TEMPLATE/
│       └── template-feedback.md
├── README.md
├── CHANGELOG.md
└── LICENSE

```

---

## Contributing / 貢獻

Issues and PRs welcome. See [docs/faq.md]() for contribution guidelines.
歡迎提交 Issue 與 PR，貢獻說明請見 [docs/faq.md]()。

---

## License / 授權

MIT — free to use in any project, commercial or personal.
MIT — 可自由用於任何商業或個人專案。