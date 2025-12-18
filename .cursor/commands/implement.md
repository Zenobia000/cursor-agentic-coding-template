---
description: IMPLEMENT MODE - Guided, test-driven code implementation in the `current` workspace.
---

# 💻 IMPLEMENT MODE (v3)

> 將設計藍圖轉化為功能齊全、經過測試、且高品質的程式碼。

## 1. PLAN 🎯 (規劃)

### Objective
> 根據 `tasks.md` 中指定的任務和其關聯的 `creative-*.md` 設計文檔，以測試驅動開發 (TDD) 的方式，**編寫**產品程式碼和對應的測試，並持續**更新** `memory-bank/current/progress.md` 來記錄進度。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **測試優先:** `.cursor/rules/testing/overview.mdc`
- **程式碼品質:** `.cursor/rules/backend/overview.mdc` 或 `.cursor/rules/frontend/overview.mdc`
- **指令執行:** `.cursor/rules/isolation_rules/Core/command-execution.mdc`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始編碼之前，請確保：
- ✅ **任務已設計:** `memory-bank/current/tasks.md` 中的當前任務已關聯一個或多個 `creative-*.md` 設計文檔。
- ✅ **設計已批准:** 相關的設計文檔已被用戶確認。
- ❌ **Failure Action:** 如果找不到對應的設計文檔，AI **必須拒絕編碼**，並建議用戶先執行 `/creative` 來完成技術設計。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個嚴格的、包含健康檢查的測試驅動開發循環：

**Step 0: 健康檢查 (Health Check)**
- **檢查設計完整性:** 讀取 `tasks.md` 所連結的 `creative-*.md` 文件。驗證設計文檔是否清晰、完整。
- **批判性思考:** 如果設計文檔含糊不清 (e.g., "然後處理數據")，AI **必須要求更具體的設計細節**。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取任務與設計:** 從 `memory-bank/current/tasks.md` 讀取任務要求，從關聯的 `creative-*.md` 讀取詳細的技術設計。

**Step 2: 迭代開發 (Iterative Development)**
- **遵循 TDD:**
    1. **寫一個失敗的測試 (Red):** 根據設計，為即將實現的最小功能單元編寫一個測試，並確認它因功能未實現而失敗。
    2. **寫最少的程式碼讓測試通過 (Green):** 編寫最簡潔的產品程式碼，恰好能讓該測試通過。
    3. **重構 (Refactor):** 在測試保護下，優化剛才編寫的程式碼。
- **重複此循環**，直到任務的所有功能點都已實現。

**Step 3: 記憶體互動 - 寫入與更新 (Memory Interaction - Write & Update)**
- **寫入產品程式碼:** 在專案的源碼目錄中**創建**或**修改**對應的檔案。
- **寫入測試程式碼:** 在專案的測試目錄中**創建**或**修改**對應的測試檔案。
- **持續更新進度:** 在每個重要的開發節點，**更新** `memory-bank/current/progress.md` 文件，簡要說明進度。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **功能符合設計:** 實作的功能是否完全符合 `creative-*.md` 中的設計？
- [ ] **測試全部通過:** 所有相關的測試是否都已通過？
- [ ] **記憶體同步:** `memory-bank/current/progress.md` 是否已更新？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶報告:** 在一個主要功能的實作完成後，向用戶報告。例如：「任務『用戶登入』已完成，包含完整的程式碼和 95% 的測試覆蓋率。」

### Next Steps
> 完成一個實作任務後，繼續推進專案。
- 👉 **Primary Next Step:** 執行 `/task-next`，讓 PM 小助理建議下一個最高優先級的任務。
- 💡 **Alternative:** 如果所有任務都已完成，請執行 `/reflect` 指令，對整個實作階段進行一次全面的回顧。

---
> **IMPLEMENT MODE (v3) 已啟動。正在檢查 `current` 工作區的設計文檔，準備開始 TDD 循環...**