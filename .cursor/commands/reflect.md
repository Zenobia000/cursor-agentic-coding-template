---
description: REFLECT MODE - Retrospective analysis in the `current` workspace for lesson learning.
---

# 🔍 REFLECT MODE (v3)

> 從已完成的工作中汲取經驗，提煉智慧，為未來的成功鋪路。

## 1. PLAN 🎯 (規劃)

### Objective
> 對一個已完成的開發週期進行全面的、數據驅動的回顧，總結成果，反思過程，並將所有學習到的經驗**寫入**一份新的 `memory-bank/current/reflection-[date].md` 文件中，作為未來改進的基礎。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **流程改進:** `.cursor/rules/process/planning-process.md`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始反思之前，請確保：
- ✅ **週期已結束:** `memory-bank/current/tasks.md` 中絕大多數任務都已標記為 `completed`。
- ✅ **歷史記錄存在:** `memory-bank/current/progress.md` 文件存在，並包含了本週期的開發日誌。
- ❌ **Failure Action:** 如果工作尚未完成，AI **必須拒絕**反思，並建議：「看起來本週期還有未完成的任務。建議先完成它們再進行反思。」

## 2. DO 実行 (執行)

### Core Process
> 遵循一個客觀、公正、面向未來的復盤框架：

**Step 0: 健康檢查 (Health Check)**
- **檢查拓撲完整性:** 驗證 `memory-bank/current/` 中的 `tasks.md` 和 `progress.md` 的數據是否完整且可以互相印證。
- **批判性思考:** 反思的目的是為了改進，而非指責。AI 在分析時應採取中立的語氣。如果發現某個任務延遲嚴重，應客觀描述事實，並探討原因。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取所有相關記憶:**
    - `memory-bank/current/tasks.md` (規劃了什麼)
    - `memory-bank/current/progress.md` (實際執行過程)
    - `memory-bank/current/creative-*.md` (設計決策)
    - `git log` (提交歷史)
- **綜合分析:** 將上述所有資訊結合起來，建立一個關於本週期的完整畫像。

**Step 2: 復盤分析 (Retrospective Analysis)**
- **客觀總結 (What happened?):** 總結完成了哪些主要功能，指標數據如何。
- **分析亮點 (What went well?):** 識別流程中的成功實踐、高效決策。
- **分析痛點 (What could be improved?):** 識別流程中的瓶頸、錯誤的估算、技術債。
- **提煉學習 (What did we learn?):** 總結出可供未來直接使用的、可操作的經驗教訓。

**Step 3: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **創建反思報告:** 將上述所有分析結果，**寫入**到一個**新的** `memory-bank/current/reflection-[date].md` 文件中。
- **(可選) 更新任務列表:** 如果在反思中識別出新的技術債務，可以**更新** `memory-bank/current/tasks.md`，將這些技債作為下個週期的 PENDING 任務。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **報告已生成:** `memory-bank/current/reflection-[date].md` 是否已成功創建？
- [ ] **分析是否深入:** 報告是否不僅僅是羅列事實，而是提供了對原因的深入分析？
- [ ] **學習是否可操作:** 總結的經驗教訓是否具體、可衡量、可應用？

## 4. ACT 改善 (行動)

### Finalization
- **與用戶互動:** 在生成報告後，AI 可以主動向用戶提問，以獲取更深層次的見解。例如：「報告已生成。從您個人的角度來看，本次週期最大的挑戰是什麼？」
- **提交報告:** 將最終的 `reflection-[date].md` 文件提交到版本控制系統。

### Next Steps
> 反思是為了更好地前進。
- 👉 **Primary Next Step:** 執行 `/archive` 指令，將本週期的所有工作成果整理歸檔。
- 💡 **Alternative:** 如果反思中發現了需要立即修復的嚴重技術債，可以執行 `/task-init` 和 `/implement`，在開始新週期之前先償還債務。

---
> **REFLECT MODE (v3) 已啟動。正在檢查 `current` 工作區的週期完整性，準備進行復盤分析...**