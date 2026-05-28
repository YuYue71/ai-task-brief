# FAQ

---

**Q: Does this work with ChatGPT, Gemini, or other AI assistants?**
**Q: 這份範本適用於 ChatGPT、Gemini 或其他 AI 助手嗎？**

EN: Yes. The template is plain Markdown and contains no tool-specific syntax. Any instruction-following AI that accepts a long system context will parse it correctly.

ZH: 適用。範本為純 Markdown，不含任何特定工具的語法。任何能接受長系統上下文的指令型 AI 皆可正確解析。

---

**Q: The template is long. Will it use too many tokens?**
**Q: 範本很長，會消耗太多 Token (語言模型計算單位) 嗎？**

EN: A fully filled template is approximately 600–900 tokens — less than a single code file. The context it provides saves far more tokens than it costs, by eliminating clarification rounds.

ZH: 完整填寫的範本約 600–900 Token，少於一個完整的代碼檔案。它所提供的上下文遠比消耗的 Token 節省更多來回釐清的成本。

---

**Q: Do I need to paste the entire file every time?**
**Q: 每次都需要貼入整份檔案嗎？**

EN: Yes, for every new conversation. AI assistants have no memory between sessions by default. The template *is* the memory. Some platforms (e.g. Claude) support persistent memory or system prompts — in those cases you can load the template there instead.

ZH: 是，每次新對話都需要貼入。AI 助手預設在對話間無記憶，範本本身即是記憶的替代。部分平台（如 Claude）支援持久記憶或系統提示，屆時可將範本載入其中。

---

**Q: What if my project doesn't have a scene hierarchy (e.g. a web app)?**
**Q: 我的專案沒有場景層級（例如 Web 應用程式），怎麼辦？**

EN: SECTION 2 is flexible. Use it for component dependency graphs, API route maps, database schema sketches, or React component trees — anything that shows how your code pieces connect.

ZH: SECTION 2 的用途彈性很大。可用於元件依賴圖、API 路由地圖、資料庫 Schema 草圖或 React 元件樹，任何能表達代碼連線關係的結構皆適用。

---

**Q: How do I handle multiple scenes or entry points?**
**Q: 如何處理多個場景或入口點？**

EN: Add sub-sections inside SECTION 2, one per scene or entry point. Keep only the *active* scene fully detailed; summarise others in one line.

ZH: 在 SECTION 2 內新增子區段，每個場景或入口點各一段。只對當前活躍的場景詳細展開，其餘以一行摘要帶過。

---

**Q: Can I contribute a filled example for my engine / framework?**
**Q: 我可以貢獻針對我的引擎 / 框架的填寫範例嗎？**

EN: Yes — open a PR adding a new file to `examples/`. File name should follow `[engine_type].md` (e.g. `react_webapp.md`, `godot_2d.md`). Include a comment at the top citing the source project type.

ZH: 可以，開一個 PR 在 `examples/` 中新增檔案即可。檔名格式為 `[引擎_類型].md`（例：`react_webapp.md`、`godot_2d.md`），頂部加註來源專案類型的說明。

---

**Q: The AI isn't following the Update Protocol. What should I do?**
**Q: AI 沒有執行範本更新協議，怎麼辦？**

EN: Explicitly remind the AI: *"Follow the Update Protocol at the bottom of the template."* If it still ignores it, paste only the Update Protocol section and ask it to process the session.

ZH: 明確提醒 AI：「請執行範本底部的更新協議。」若仍未執行，單獨貼出更新協議區段並要求其處理本次對話的更新。