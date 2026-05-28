# AI Task Brief — Universal AI Collaboration Template
# AI 任務範本 — 通用 AI 協作上下文框架

> A zero-config Markdown context template that gets any AI assistant up to speed on your project in seconds.
> 一份零設定的 Markdown 上下文範本，讓任何 AI 助手在數秒內進入你的專案狀態。

---

## What is this? / 這是什麼？

`AI Task Brief` is a structured Markdown template you paste at the start of every AI conversation. It encodes your tech stack, file structure, component hierarchy, progress board, and current task into a single living document — no repeated explanations, no lost context.

`AI Task Brief` 是一份結構化的 Markdown 範本，在每次 AI 對話開始時貼入。它將技術棧、檔案結構、元件層級、進度看板與當前任務編碼進單一文件，讓 AI 無需重複說明即可立即進入狀況。

---

## How it works / 運作流程

```
1. Copy template  →  Paste into AI chat
   複製範本           貼入 AI 對話開頭

2. AI reads STATUS in SECTION 4
   AI 讀取 SECTION 4 的 STATUS 旗標

   STATUS: EMPTY   →  AI runs the init interview (one question group at a time)
                      AI 執行初始化問答（每次一組問題）

   STATUS: ACTIVE  →  AI silently parses all sections, confirms context in one line,
                      then asks for the session task
                      AI 靜默解析所有區段，單行確認後直接詢問本次任務

3. Task done  →  AI prompts update  →  You confirm  →  AI outputs Markdown patch
   任務完成    →  AI 主動詢問更新    →  確認後 AI 輸出更新的 .md patch

4. /snapshot  →  AI outputs full current state as a raw Markdown block
   /snapshot  →  AI 輸出當前完整狀態的 raw Markdown 區塊，可直接搬運至新對話
```

---

## Quick Start / 快速開始

**Option 1 — Direct paste / 直接貼入**

Copy the raw content of `templates/ai_context.md` and paste it at the start of any AI chat. The AI detects `STATUS: EMPTY` and guides you through setup automatically.

複製 `templates/ai_context.md` 的原始內容，貼入任意 AI 對話開頭。AI 偵測到 `STATUS: EMPTY` 後會自動引導填寫，無需手動編輯 Markdown。

**Option 2 — GitHub direct link / GitHub 直連**

Provide the raw file URL to your AI:

直接將原始檔連結提供給 AI：

```
https://raw.githubusercontent.com/YuYue71/ai-task-brief/main/templates/ai_context.md
```

The AI fetches and initializes the template in one step.
AI 會直接抓取並初始化範本。

---

## Template Sections / 範本區段說明

| Section | Purpose / 用途 | Mutability / 可變性 |
|---------|---------------|-------------------|
| SECTION 0 | Immutable tech stack / 不可變技術棧 | Set once / 設定後鎖定 |
| SECTION 1 | Module / file map / 模組與檔案地圖 | Updated on file changes / 隨檔案異動更新 |
| SECTION 2 | Object / component hierarchy / 物件與元件層級 | Updated on arch changes / 隨架構演進更新 |
| SECTION 3 | Development kanban / 開發進度看板 | Updated per task / 每次任務後更新 |
| SECTION 4 | Active task brief (AI-managed) / 當前任務（AI 自動管理） | Managed by AI / AI 維護 |
| SECTION 5 | Coding contract / 編碼規範 | Project-specific / 依專案設定 |
| SECTION 6 | AI output rules + snapshot protocol / AI 輸出規則與快照協議 | Fixed / 固定 |
| SECTION 7 | Session log (append-only) / Session 紀錄（只增不刪） | Append only / 僅追加 |

---

## i18n / 多語言支援

The template is English by default. When the AI first processes `STATUS: EMPTY`, it detects your language from your first message and appends inline translations to all structural text — headings, directives, and annotation labels. Task values (task names, file paths, variable names) are never translated.

範本預設為英文。AI 首次處理 `STATUS: EMPTY` 時，會從你的第一則訊息偵測語言，並在所有結構性文字後方附加行內譯文（標題、指示語、註解標籤）。任務名稱、檔案路徑、變數名稱不在翻譯範圍內。

---

## Session Migration / 協作狀態轉移

To move to a new chat window at any point:

需要轉移到新聊天窗口時：

```
/snapshot
```

The AI outputs the complete current state of the brief as a raw Markdown code block. Paste it into a new chat — the AI resumes instantly with full context.

AI 輸出當前完整任務菜單的 raw Markdown 區塊。貼入新聊天窗口後，AI 可立即恢復全部上下文，無需重新說明。

---

## Repository Structure / 檔案結構

```
ai-task-brief/
├── templates/
│   └── ai_context.md          # Main template / 主範本
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

Issues and PRs are welcome. See [docs/faq.md](docs/faq.md) for contribution guidelines.

歡迎提交 Issue 與 PR，貢獻說明請見 [docs/faq.md](docs/faq.md)。

---

## License / 授權

MIT — free to use in any project, commercial or personal.
MIT — 可自由用於任何商業或個人專案。