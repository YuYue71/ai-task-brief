# Section Guide / 區段填寫指南

> Detailed instructions for filling in each section of `ai_context.md`.
> `ai_context.md` 各區段的詳細填寫說明。

---

## SECTION 0 — Immutable Stack

**EN:** Fill this once and never change it unless your core technology changes. The AI uses this to infer available APIs, naming conventions, and platform constraints without asking.

**ZH:** 填寫一次，除非核心技術變更否則不動。AI 會以此推斷可用 API、命名慣例與平台限制，無需每次說明。

**Tips:**
- Be specific with versions: `Unity 6.4` not just `Unity`
- List only packages that affect how you write code, not every dependency
- "Tone & Style" helps the AI match output register (e.g. avoid casual comments in enterprise code)

---

## SECTION 1 — Module Map

**EN:** A file tree of your project's scripts or modules, annotated with one-line responsibility descriptions. Keep it to files the AI might need to touch or reference — omit assets, configs, and auto-generated files.

**ZH:** 專案腳本 / 模組的檔案樹，每個檔案附一行職責說明。只列 AI 可能需要觸碰或參照的檔案，省略資源、設定檔與自動生成檔。

**Update trigger:** Add a node when a new script is created; remove when a file is deleted. The AI will do this automatically via the Update Protocol.

---

## SECTION 2 — Object / Component Structure

**EN:** The scene hierarchy or component dependency graph of your project. This is the most valuable section — it lets the AI understand *how your objects are wired together* without seeing the project file.

**ZH:** 專案的場景層級或元件依賴圖。這是最有價值的區段，讓 AI 無需開啟專案即能理解物件的連線關係。

**What to include:**
- Root objects and their key components in parentheses
- Parent-child relationships that affect logic (e.g. a SpriteRenderer that must be a child to flip correctly)
- Inspector field bindings that are non-obvious (e.g. `_GameManager` holds a reference array to animation objects)
- Disabled-by-default objects and why (e.g. skill visuals, death screens)

**What to omit:** Lights, cameras with no custom logic, empty organisational GameObjects with no components.

---

## SECTION 3 — Development Kanban

**EN:** A linear phase breakdown of your project. Phases should be coarse (5–8 items each). The AI uses this to understand what has been built, what is in progress, and what does not exist yet — preventing it from referencing systems that haven't been implemented.

**ZH:** 專案的線性階段分解。每階段粗粒度列 5–8 項。AI 以此判斷哪些系統已建立、進行中或尚未存在，避免引用未實作的系統。

**Symbols:** `✓` = complete, `□` = pending, `~` = in progress (optional)

---

## SECTION 4 — Active Task Brief

**EN:** This section is AI-managed. You should almost never edit it manually. Leave it as `STATUS: EMPTY` when starting a new conversation; the AI will fill it based on your instructions.

**ZH:** 此區段由 AI 管理，幾乎不需要手動編輯。開啟新對話時保持 `STATUS: EMPTY`，AI 會根據指示自動填入。

**Manual override:** If you want to pre-fill a task before opening the chat, replace the STATUS block with the comment template format shown in `ai_context.md`.

---

## SECTION 5 — Coding Contract

**EN:** Rules the AI must follow when writing code. The defaults cover literate programming, bilingual annotation, and risk marking. Add project-specific rules at the bottom — for example, preferred patterns, banned libraries, or line-length limits.

**ZH:** AI 撰寫代碼時必須遵守的規則。預設涵蓋文字化編程、雙語標記與風險標示。可在底部補充專案特定規則，例如偏好的設計模式、禁用的套件或行長限制。

---

## SECTION 6 — AI Output Rules

**EN:** Meta-rules about *how* the AI responds, independent of code style. These are pre-set and rarely need changing. If you want to allow conversational preamble, remove the first rule.

**ZH:** AI 回應方式的元規則，與代碼風格無關。預設值通常不需更動。若允許前言，刪除第一條規則即可。

---

## Update Protocol

**EN:** After every completed task, the AI asks whether to update the template. You provide the next task direction and a list of changed files. The AI then outputs a complete new `.md` — replace your local file with it.

**ZH:** 每次任務完成後，AI 詢問是否更新範本。提供下一個任務方向與變更的檔案清單，AI 即輸出完整新版 `.md`，以此覆蓋本地檔案即可。

**Recommended workflow / 建議工作流程:**
```
完成任務
  → AI 詢問更新
  → 回覆：下一任務 + 檔案清單
  → AI 輸出新 .md
  → 複製貼上覆蓋本地 ai_context.md
  → commit to version control
```