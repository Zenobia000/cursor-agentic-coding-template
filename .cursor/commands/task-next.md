---
description: TASK NEXT - Get a PM briefing on the next most strategic tasks from the `current` workspace.
---

# 👨‍💼 TASK NEXT (PM Assistant v3)

> 您的專案經理小助手已上線。為您過濾上下文噪音，分析戰況，並從多個策略角度建議下一步的最佳行動。

## 1. PLAN 🎯 (規劃)

### Objective
> 在您需要重新聚焦時，為您提供一份關於當前 `memory-bank/current/tasks.md` 的摘要簡報，並從多個策略角度建議接下來應該執行的任務。此指令是一個**只讀**分析器，旨在幫助決策，**不會修改** `tasks.md`。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **規劃與追蹤:** `.cursor/rules/process/planning-process.md` 和 `.cursor/rules/process/task-tracking.md`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在獲取簡報之前，請確保：
- ✅ **`tasks.md` 存在:** `memory-bank/current/tasks.md` 是您專案的「唯一真相來源」。
- ❌ **Failure Action:** 如果 `tasks.md` 不存在，AI **必須**建議用戶先運行 `/van` 來初始化專案。

## 2. DO 実行 (執行)

### Core Process
> PM 小助手將為您執行以下分析流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查 `tasks.md` 狀態:** 驗證 `memory-bank/current/tasks.md` 是否存在、有效，且包含待辦任務。
- **批判性思考:** 如果所有任務都已完成，AI 應報告：「恭喜！所有任務都已完成。建議執行 `/reflect` 進行復盤。」 如果沒有可執行的任務（所有 `pending` 任務都被阻塞），AI 應報告：「目前沒有可立即開始的新任務，我們需要先完成正在進行中的『XXX』任務。」

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取任務列表:** 完整**讀取**並解析 `memory-bank/current/tasks.md` 的內容。

**Step 2: 多維度評估 (Multi-dimensional Evaluation)**
- **識別候選者:** 找出所有狀態為 `pending` 且其依賴項均已 `completed` 的可執行任務。
- **評估視角:** 從以下 PM 視角對每個候選任務進行評估：
    *   **👑 關鍵路徑 (Critical Path):** 哪個任務是後續最多待辦任務的阻塞點？
    *   **💎 最高價值 (Highest Value):** 哪個任務最貼近 `projectbrief.md` 中定義的核心目標？
    *   **⚡️ 快速取勝 (Quick Win):** 哪個任務預估工作量最小，可以快速完成以建立動能？
    *   **🛡️ 風險緩解 (Risk Mitigation):** 哪個任務能解決最大的技術或業務不確定性？

**Step 3: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **輸出 PM 簡報:** 將分析結果彙總成一份清晰、結構化的「PM 簡報」，作為**輸出**直接呈現給用戶。**此指令不修改 `tasks.md`。**
- **(可選) 更新上下文:** 可以在 `memory-bank/current/activeContext.md` 中輕量地記錄一次「PM 簡報已提供」。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **簡報是否清晰:** 輸出的 PM 簡報是否易於理解，並清楚解釋了每個建議背後的原因？
- [ ] **只讀原則:** AI 是否確保了沒有修改 `tasks.md`？

## 4. ACT 改善 (行動)

### Finalization
- **等待用戶決策:** AI 的任務在提供簡報後即完成，等待用戶做出最終決策。

### Next Steps
> AI 將根據用戶的決策，進入相應的模式。
- 👉 **Primary Next Step:** 用戶選擇一個建議後，AI 應準備執行 `/creative` 或 `/implement` 指令，來處理被選中的任務。
- 💡 **Alternative:** 如果用戶認為所有建議都不合適，AI 應建議：「看起來我們的計畫可能需要調整。建議執行 `/plan` 來重新審視和分解任務。」

---
> **TASK NEXT (PM Assistant v3) 已啟動。正在檢查 `current` 工作區的健康狀態，準備提供任務簡報...**