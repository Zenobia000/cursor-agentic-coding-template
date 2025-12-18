---
description: PLAN MODE - Task planning and decomposition into the `current` memory workspace.
---

# 📋 PLAN MODE (v3)

> 將宏大的目標分解為清晰、可執行的任務藍圖，確保每一步都有據可依。

## 1. PLAN 🎯 (規劃)

### Objective
> 將高層次的專案目標 (來自 `memory-bank/current/projectbrief.md`)，分解成一個結構化、有優先級、且包含依賴關係的詳細任務列表 (WBS)，並寫入 `memory-bank/current/tasks.md` 作為當前週期的「唯一真相來源」。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **核心實踐:** `.cursor/rules/process/planning-process.md` (假設此文件存在或將被創建)
- **任務追蹤:** `.cursor/rules/process/task-tracking.md` (假設此文件存在或將被創建)
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始規劃之前，請確保：
- ✅ **專案已初始化:** `/van` 指令已成功執行，`memory-bank/current/` 結構完整。
- ✅ **目標已定義:** `memory-bank/current/projectbrief.md` 文件已存在且內容清晰。
- ❌ **Failure Action:** 如果 `projectbrief.md` 不存在或為空，應先執行 `/task-init` 來定義目標。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個從宏觀到微觀、且具備批判性思維的分解流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查 `projectbrief.md`:** 驗證 `memory-bank/current/projectbrief.md` 是否存在且內容充實。
- **批判性思考:** 如果簡報內容模糊不清或有矛盾，**必須先向用戶提出澄清問題**，而不是基於不清晰的需求進行規劃。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取目標:** 從 `memory-bank/current/projectbrief.md` 中讀取核心目標、範圍和約束。
- **讀取現有任務:** 讀取 `memory-bank/current/tasks.md`，了解是否已有存在的任務，以避免重複規劃。

**Step 2: 任務分解 (Decomposition)**
- 將大的目標 (Epics) 分解為更小的使用者故事 (Stories)，再進一步細化為具體的技術任務 (Tasks)。

**Step 3: 依賴映射 (Dependency Mapping)**
- 識別任務之間的依賴關係，並在 WBS 中明確標出。

**Step 4: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **更新 `tasks.md`:** 將完整的任務分解結構**覆蓋寫入** `memory-bank/current/tasks.md`。
- **更新上下文:** 更新 `memory-bank/current/activeContext.md`，註明 `PLAN MODE` 已完成。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **無遺漏:** 所有在 `projectbrief.md` 中提到的功能點是否都已被分解為至少一個任務？
- [ ] **記憶體同步:** `memory-bank/current/tasks.md` 的內容是否已成功更新並反映了最新的規劃？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認:** 在覆寫 `tasks.md` 之後，報告操作已完成。例如：「我已根據您的專案簡報，將詳細的任務計畫更新至 `memory-bank/current/tasks.md`。」

### Next Steps
> 規劃完成後，下一步是針對具體任務進行技術設計。
- 👉 **Primary Next Step:** 執行 `/creative` 指令，為最高優先級的任務進行架構和技術設計。
- 💡 **Alternative:** 如果某些任務的需求仍不清晰，可以執行 `/task-init` 針對該模糊點進行一次小範圍的澄清和規劃。

---
> **PLAN MODE (v3) 已啟動。正在檢查 `current` 工作區的健康狀態，準備進行任務分解...**
