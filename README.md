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
1. Download [`templates/ai_context.md`](templates/ai_context.md)
2. Fill in SECTION 0 (stack), SECTION 1 (files), SECTION 2 (structure), SECTION 3 (kanban)
3. Leave SECTION 4 as `STATUS: EMPTY`
4. Paste the entire file into your next AI chat — the AI handles the rest

**ZH:**
1. 下載 [`templates/ai_context.md`](templates/ai_context.md)
2. 填入 SECTION 0（技術棧）、SECTION 1（檔案）、SECTION 2（物件結構）、SECTION 3（看板）
3. SECTION 4 保持 `STATUS: EMPTY` 不動
4. 將整份檔案貼入 AI 對話 — AI 會接管後續流程

---

## Template Sections / 範本區段說明

| Section | Purpose (EN) | 用途 (ZH) |
|---------|-------------|-----------|
| SECTION 0 | Immutable tech stack | 不變的技術棧 |
| SECTION 1 | Script / module map | 腳本 / 模組地圖 |
| SECTION 2 | Scene / object / component tree | 場景 / 物件 / 元件樹 |
| SECTION 3 | Development kanban | 開發進度看板 |
| SECTION 4 | Active task brief (AI-managed) | 當前任務（AI 自動管理）|
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
├── examples/
│   └── unity_2d_game.md       # Filled example (Unity 2D) / 填寫範例
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

Issues and PRs welcome. See [docs/faq.md](docs/faq.md) for contribution guidelines.
歡迎提交 Issue 與 PR，貢獻說明請見 [docs/faq.md](docs/faq.md)。

---

## License / 授權

MIT — free to use in any project, commercial or personal.
MIT — 可自由用於任何商業或個人專案。