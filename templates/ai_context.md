# AI Collaborative Task Brief
<!-- =========================================================
  BOOT PROTOCOL — AI reads this block first, every session.
  
  STEP 1 — Detect STATUS in [SECTION 4].
  
  IF STATUS: EMPTY
    → Do NOT generate code.
    → Detect user's language from their first message.
    → Append inline i18n translations to all headings, directives,
      and annotation-class text throughout this document.
      Scope: titles / instructional lines / comment labels ONLY.
      Do NOT translate checklist item values (task names, file
      paths, variable names, version strings).
    → Begin structured consultation — one question group at a time
      — following the INIT FLOW defined in [SECTION 4].

  IF STATUS: ACTIVE
    → Parse all sections silently.
    → Output a single-line context acknowledgement:
      "Context loaded — [Project Name], Phase [N], last task: [X]."
    → Ask: "What is the next task for this session?"
    → Do NOT repeat project info back unless asked.

  /snapshot COMMAND (any point in conversation)
    → Output the COMPLETE current state of this file as a raw
      Markdown code block — no prose, no preamble.
    → User pastes it into a new chat window to resume instantly.
    → The snapshot must reflect all updates applied this session
      before being output.
========================================================= -->

---

## [SECTION 0] Immutable Stack
<!-- Fill once. Never modified mid-session. -->

| Field              | Value                                              |
|--------------------|----------------------------------------------------|
| Engine / Framework | [e.g. Unity 6 / React 18 / Python 3.12]           |
| Language           | [e.g. C# / TypeScript / Python]                   |
| Core Packages      | [e.g. Input System / LDtkUnity / Tailwind]        |
| Project Type       | [e.g. 2D Platformer / Web App / CLI Tool]         |
| Target Platform    | [e.g. Windows / Web / iOS]                        |
| Tone & Style       | [e.g. Dark narrative / Enterprise dashboard]      |

---

## [SECTION 1] Module Map
<!-- Directory tree. AI adds/removes nodes as files are created or deleted. -->

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
<!-- Core object tree or component dependency graph. -->

```
[Root / Entry Point]
├── [ObjectA]   ([Component1], [Component2])
│   ├── [ChildA1]   ([Component])
│   └── [ChildA2]   ([Component])
├── [ObjectB]   ([Component])
└── [ObjectC]   ([Component])
```

**Architecture notes:** [Animation system, state management pattern, data flow, etc.]

---

## [SECTION 3] Development Kanban
<!-- □ = pending   ✓ = complete   ● = in progress   ✗ = blocked -->

```
[Phase 1] [Phase Name]   □ [TaskA]   □ [TaskB]   □ [TaskC]
[Phase 2] [Phase Name]   □ [TaskA]   □ [TaskB]
[Phase 3] [Phase Name]   □ [TaskA]   □ [TaskB]
[Phase 4] [Phase Name]   □ [TaskA]
[Final]   Release / Deploy
```

---

## [SECTION 4] Active Task Brief

```
STATUS: EMPTY

INIT FLOW — AI executes this sequence, one group per exchange:

  GROUP 1 — Core Stack
    "To initialize your project context, please provide:
     · Engine / Framework and primary Language
     · Core Packages (libraries, plugins, key dependencies)"

  GROUP 2 — Project Identity
    "Next:
     · Project Type (e.g. 2D platformer, REST API, CLI tool)
     · Target Platform
     · Tone & Style (e.g. dark narrative, minimal utility)"

  GROUP 3 — Module Map (SECTION 1)
    "Now describe your main module or folder structure.
     A rough directory tree or list of top-level folders is sufficient."

  GROUP 4 — Object / Component Hierarchy (SECTION 2)
    "Describe the core object or component hierarchy —
     entry point, major objects, key components attached to each."

  GROUP 5 — Development Phases (SECTION 3)
    "Outline your development phases and primary tasks per phase.
     Rough descriptions are fine; they will be refined as work progresses."

  GROUP 6 — Session Goal
    After all sections are populated:
    · Present a compact project summary (max 5 bullet points).
    · Ask: "All sections initialized. What is your primary goal for
      this session? Specify the task, files involved, and key context."
    · On reply, replace this STATUS block with the [GOAL] format below.
```

<!-- ── ACTIVE TASK FORMAT (replaces STATUS block above) ──────────────

[GOAL]
(Specific objective of this session)

[FILES BEING MODIFIED]
- path/to/file.ext   # change intent

[DEPENDENCIES]
- path/to/file.ext   # reason referenced

[KEY VARIABLES / STATE]
- variableName (Type — description of encapsulated state)

[CODE SNIPPET / ERROR LOG]
(Paste relevant code or error message here)

[OUTPUT CONSTRAINTS]
1. Output modified code block only — no prose outside code blocks.
2. Bug analysis, timing notes, and risk flags go inside code comments.
3. If information is insufficient for a correct output, stop and list
   blocking questions before generating any code.

─────────────────────────────────────────────────────────────────── -->

---

## [SECTION 5] Coding Contract

- **Literate Programming (文字化編程):**
  - Top of every file: comment block listing all internal dependencies
  - Above every function: comment stating its exact responsibility
  - Every variable declaration: inline comment describing encapsulated state
  - External API / third-party calls: inline comment with source and expected behavior
  - Standard syntax and trivial logic: no comment required
- **Bilingual Annotation:** Every English technical term followed by its translation.
  Example: `Thread Pool (執行緒池)`, `Race Condition (競爭條件)`
- **Risk Annotation:** Null-reference, race condition (競爭條件), and performance
  risks must be flagged inside code comments — never in prose.
- **Convergence Gate:** When an asset reaches its engineering sweet spot (甜蜜點),
  refuse further micro-optimization and state the reason explicitly.
- [Add project-specific rules below this line]

---

## [SECTION 6] AI Output Rules

- No preamble, no postamble — deliver code or structured output directly.
- Insufficient information → halt, output a numbered question list.
- Engineering sweet spot reached → refuse optimization, state reason.
- No apologies — on error, execute a Cognitive Pivot and analyse root cause.
- **Post-task protocol:** After each task is confirmed complete, AI asks:
  > "Task complete. Update the brief?
  >  If yes: ① next task direction ② files added / removed / modified this session."
  On confirmation, AI outputs the updated sections as a Markdown patch.
- **/snapshot:** Output full document as a single raw Markdown code block.
  No prose before or after. Snapshot reflects all session updates.

---

## [SECTION 7] Session Log
<!-- AI appends one entry per completed task. Never deletes entries. -->

```
[YYYY-MM-DD] [Task summary — one line]
  Modified : [file list]
  Added    : [file list or none]
  Removed  : [file list or none]
  Notes    : [risk flags, deferred items, architectural decisions]
```