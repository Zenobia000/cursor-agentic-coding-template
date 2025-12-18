---
description: OPTIMIZE - Data-driven performance analysis and optimization in the `current` workspace.
---

# ⚡ OPTIMIZE MODE (v3)

> 像索隆的三刀流一樣，基於數據，精準、快速地斬斷效能瓶頸。

## 1. PLAN 🎯 (規劃)

### Objective
> 遵循「測量-識別-優化-驗證」的循環，系統性地解決效能問題，並**寫入**一份包含前後對比數據的效能報告，以證明優化的有效性。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **架構原則:** `.cursor/rules/backend/overview.mdc` 或 `.cursor/rules/frontend/overview.mdc`
- **測試要求:** `.cursor/rules/testing/overview.mdc` (確保優化不破壞功能)
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始優化之前，請確保：
- ✅ **目標已量化:** 有一個清晰、可量化的效能目標 (e.g., "將 P95 延遲從 800ms 降至 300ms 以下")。
- ✅ **基準已存在:** 已有一份可靠的效能基準測試報告，可能儲存在 `memory-bank/current/` 中。
- ❌ **Failure Action:** 如果目標模糊或沒有基準數據，AI **必須拒絕優化**，並建議：「我們需要先建立效能基準。我應該先編寫一個負載測試腳本來測量當前的 API 延遲嗎？」

## 2. DO 実行 (執行)

### Core Process
> 遵循一個嚴格的、數據驅動的優化循環：

**Step 0: 健康檢查 (Health Check)**
- **檢查目標和基準:** 驗證效能目標是否具體、可衡量，且基準報告是否可信。
- **批判性思考:** 優化是權衡的藝術。AI 應思考目標是否現實，並思考潛在的副作用，例如：「追求極致的低延遲可能會增加伺服器成本或降低數據一致性。我們應該在哪個指標上做權衡？」

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取目標:** 從 `memory-bank/current/tasks.md` 讀取效能優化目標。
- **讀取基準報告:** 從 `memory-bank/current/perf-report-[baseline-date].md` 讀取詳細的基準數據。
- **讀取相關程式碼:** 根據基準報告中指出的瓶頸，讀取相關的產品程式碼。

**Step 2: 假設與實施 (Hypothesize & Implement)**
- **提出假設:** 針對瓶頸，提出一個具體的優化假設。
- **實施優化:** **修改**產品程式碼以實現該優化。

**Step 3: 驗證與測量 (Verify & Measure)**
- **功能驗證:** 運行所有單元測試和整合測試，確保優化沒有破壞任何現有功能。
- **效能驗證:** 在與基準測試**完全相同**的環境下，重新運行效能測試。

**Step 4: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **寫入效能報告:** **創建**一份新的效能報告 `memory-bank/current/perf-report-[optimization-date].md`。此報告**必須**包含優化目標、措施、以及**優化前後的數據對比表**。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **目標是否達成:** 優化後的指標是否達到了預設的目標？
- [ ] **功能無迴歸:** 所有測試是否都已通過？
- [ ] **報告已生成:** 是否已在 `memory-bank/current` 中創建了包含前後對比數據的效能報告？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認權衡:** 在提交一個涉及重要權衡的優化之前，AI **必須**向用戶確認。
- **提交程式碼:** 在用戶確認後，將優化程式碼和新的效能報告提交到版本控制系統。

### Next Steps
> 效能優化是一個持續的過程。
- 👉 **Primary Next Step:** 如果仍有未達標的效能指標，可以執行 `/task-next` 來建議下一個要優化的點。
- 💡 **Alternative:** 將新的效能測試腳本整合到 CI/CD 流程中，建立效能迴歸監控。

---
> **OPTIMIZE MODE (v3) 已啟動。正在檢查 `current` 工作區的效能目標和基準數據...**
