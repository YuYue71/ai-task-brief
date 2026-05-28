# [Project Name / 專案名稱] — AI Task Brief
> Paste this entire file at the start of every AI conversation.
> 每次開啟新任務前，將此檔案完整貼入對話首則。
>
> **i18n:** This template is in English by default. When an AI first processes
> STATUS: EMPTY, it will detect your language and append inline translations
> automatically. No configuration needed.
> **i18n:** 此範本預設為英文。AI 首次處理 STATUS: EMPTY 時，會自動偵測使用者語言
> 並在英文後方行內附加譯文，無需任何設定。

---

## [SECTION 0] Immutable Stack

| Field | Value |
|-------|-------|
| Engine / Framework | [e.g. Unity 6.4 / React 18 / Python 3.12] |
| Language | [e.g. C# / TypeScript / Python] |
| Core Packages | [e.g. Input System / LDtkUnity / Tailwind] |
| Project Type | [e.g. 2D Platformer / Web App / CLI Tool] |
| Tone & Style | [e.g. Dark narrative / Enterprise dashboard / Minimal utility] |

---

## [SECTION 1] Module Map

```
[project-root]/
├── [ModuleA]/
│   ├── FileA.ext   # responsibility
│   └── FileB.ext   # responsibility
├── [ModuleB]/
│   └── FileC.ext   # responsibility
└── [placeholder]/
```

---

## [SECTION 2] Object / Component Structure

> Fill in the core object tree or component dependency graph.
> Annotate key components or responsibilities in parentheses.

```
[Root / Entry Point]
├── [ObjectA]   ([Component1], [Component2])
│   ├── [ChildA1]   ([Component])
│   └── [ChildA2]   ([Component])
├── [ObjectB]   ([Component])
└── [ObjectC]   ([Component])
```

**Architecture notes:** [Any context that helps the AI — animation system, state management pattern, data flow, etc.]

---

## [SECTION 3] Development Kanban

```
[Phase 1] [Phase Name]  □[TaskA]  □[TaskB]  □[TaskC]
[Phase 2] [Phase Name]  □[TaskA]  □[TaskB]
[Phase 3] [Phase Name]  □[TaskA]  □[TaskB]
[Phase 4] [Phase Name]  □[TaskA]
[Final]   Release / Deploy
```
> Mark completed items: □ → ✓

---

## [SECTION 4] Active Task Brief

```
STATUS: EMPTY — no task scheduled

AI reading this state must follow this flow:
1. Inform the user that no task is currently scheduled
2. List incomplete items in the current phase from SECTION 3 as reference
3. Ask: "Please describe the next task goal, files involved, and any key context"
4. After receiving a reply, fill in the fields below and output an updated .md
```

<!-- After receiving task details, AI replaces the STATUS block above with this format:

[GOAL]
(Specific objective of this task)

[FILES BEING MODIFIED]
- path/to/file.ext

[DEPENDENCIES]
- path/to/file.ext  # reason

[KEY VARIABLES / STATE]
- variableName (Type — description)

[CODE SNIPPET / ERROR LOG]
(Paste relevant code or error message here)

[OUTPUT CONSTRAINTS]
1. Output modified code block only — no prose outside code.
2. Bug analysis, timing notes, and collaboration risks go inside code comments.
3. If information is insufficient for 100% correct code, stop and list questions.
-->

---

## [SECTION 5] Coding Contract

- **Literate Programming:**
  - Top of every file: comment block listing all internal dependencies
  - Above every function: comment stating its exact responsibility
  - External function / third-party API calls: inline comment with source file and expected behavior
- **Bilingual annotation:** Every English technical term followed by its translation, e.g. `Thread Pool (執行緒池)`
- **Risk annotation:** Null-reference, race condition, and performance risks must be marked inside code comments
- [Add project-specific rules here]

---

## [SECTION 6] AI Output Rules

- No preamble, no postamble — deliver code or solution directly
- Insufficient information → stop generation, output question list
- Engineering sweet spot reached → refuse further micro-optimization, state reason explicitly
- No apologies — on error, execute a Cognitive Pivot and analyse the root cause directly

---

## [Update Protocol / 範本更新協議]

After each task is complete, the AI must automatically:
1. Ask: "Task complete. Update the template? If yes, provide: ① next task direction ② list of files added / removed / modified this session"
2. On reply, output a new .md covering:
   - SECTION 1 — add/remove module nodes
   - SECTION 2 — add/remove object nodes or component annotations
   - SECTION 3 — tick completed items (□ → ✓)
   - SECTION 4 — replace with next task content, or write STATUS: EMPTY to trigger the inquiry flow