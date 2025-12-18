---
description: DEBUG - Systematic, test-driven debugging of code in the `current` workspace.
---

# 🐛 DEBUG MODE (v3)

> 像羅賓解讀歷史正文一樣，系統化地解析 Bug，找到根本原因，並徹底修復它。

## 1. PLAN 🎯 (規劃)

### Objective
> 準確地重現、分析、定位並修復一個已知的 Bug，並**寫入**一個新的回歸測試 (Regression Test) 來鎖定此 Bug，確保其不再復現。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **測試優先:** `.cursor/rules/testing/overview.mdc`
- **程式碼品質:** `.cursor/rules/backend/overview.mdc` 或 `.cursor/rules/frontend/overview.mdc`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始除錯之前，請確保：
- ✅ **清晰的 Bug 報告:** 已提供預期行為、實際行為、**可重現步驟**和完整的錯誤訊息。
- ✅ **可運行的環境:** 開發環境已就緒，可穩定重現 Bug。
- ❌ **Failure Action:** 如果重現步驟不清晰，AI **必須**首先要求提供更詳細的資訊。

## 2. DO 実行 (執行)

### Core Process
> 採用測試驅動除錯 (Test-Driven Debugging) 的方法論：

**Step 0: 健康檢查 (Health Check)**
- **檢查可重現性:** 驗證提供的重現步驟是否真的能觸發 Bug。
- **批判性思考:** 這個 Bug 是穩定出現 (Bohrbug) 還是偶爾出現 (Heisenbug)？如果是後者，AI 應告知用戶這會增加除錯難度，並尋求更多線索。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取錯誤:** 仔細分析錯誤訊息、堆疊追蹤和相關日誌。
- **讀取程式碼:** 閱讀堆疊追蹤中涉及的相關程式碼。

**Step 2: 編寫失敗的測試 (Write a Failing Test)**
- **首要目標:** **寫入**一個新的單元測試或整合測試，該測試能夠精確地重現 Bug。
- **驗證失敗:** 運行此測試，並確認它如預期般**失敗**。

**Step 3: 分析與修復 (Analyze & Fix)**
- **形成假設:** 基於失敗的測試和程式碼，提出關於 Bug 根本原因的假設。
- **實驗與定位:** 使用日誌、斷點等方式驗證假設，直到定位根本原因。
- **寫入修復:** **修改**產品程式碼以修復 Bug。

**Step 4: 驗證修復 (Verify the Fix)**
- **運行測試:** 再次運行在 Step 2 中編寫的測試，**確認它現在能夠通過**。
- **運行全量測試:** 運行整個專案的測試套件，確保修復沒有引入任何迴歸問題。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **回歸測試已添加:** 是否已創建了一個新的、能夠捕獲此 Bug 的測試？
- [ ] **所有測試通過:** 整個測試套件是否都已成功運行？
- [ ] **根本原因已找到:** 是否明確了 Bug 的根本原因？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認:** 在修改產品程式碼**之前**，可以先向用戶展示失敗的測試和計劃中的修復方案。
- **提交修復:** 將修復程式碼**和新的測試**作為一個原子提交到版本控制系統。

### Next Steps
> Bug 修復是提升系統健壯性的絕佳機會。
- 👉 **Primary Next Step:** 繼續執行 `/implement` 或 `/task-next` 來處理下一個任務。
- 💡 **Alternative:** 如果此 Bug 暴露了某個模組的設計缺陷，可以執行 `/creative` 來為該模組的重構進行技術設計。

---
> **DEBUG MODE (v3) 已啟動。正在檢查可重現性，準備編寫失敗的測試...**
