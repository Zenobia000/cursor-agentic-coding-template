---
description: WRITE TESTS - Write comprehensive, high-quality tests for a given piece of code in the `current` workspace.
---

# 🧪 WRITE TESTS MODE (v3)

> 像烏索普的彈弓一樣，編寫精準、可靠的測試，確保程式碼的每一個角落都堅不可摧。

## 1. PLAN 🎯 (規劃)

### Objective
> 為一個特定的功能或程式碼模組，設計並**寫入**一組全面、有效的測試，以鎖定其行為、防止迴歸，並作為可執行的文檔。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **測試聖經:** `.cursor/rules/testing/overview.mdc`
- **特定框架規則:** `.cursor/rules/backend/overview.mdc` 或 `.cursor/rules/frontend/overview.mdc`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始編寫測試之前，請確保：
- ✅ **程式碼已存在:** 需要被測試的產品程式碼已經存在。
- ✅ **行為已定義:** 該程式碼的預期行為是清晰的 (來自 `memory-bank/current/tasks.md` 或用戶說明)。
- ❌ **Failure Action:** 如果不清楚要測試什麼，AI **必須**首先提問：「為了編寫有意義的測試，我需要了解 `my_function` 的預期行為。當輸入為 `null` 時，它應該拋出錯誤還是返回一個默認值？」

## 2. DO 実行 (執行)

### Core Process
> 遵循一個策略性的、由外向內的測試編寫流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查測試環境:** 驗證專案的測試框架是否已安裝且可以正常運行。
- **批判性思考:** 我應該寫哪種類型的測試？如果這是一個複雜的用戶流程，一個高層的整合測試可能比單元測試更有價值。如果這是一個純粹的演算法，單元測試則是最佳選擇。AI 應能判斷並提出策略。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取需求:** 從 `memory-bank/current/tasks.md` 或 `creative-*.md` 讀取功能的驗收條件。
- **讀取產品程式碼:** 仔細閱讀需要被測試的函數或模組的源碼。

**Step 2: 測試策略與案例設計 (Strategy & Case Design)**
- **選擇測試類型:** 決定編寫單元測試、整合測試還是 E2E 測試。
- **設計測試案例:** 系統性地設計測試案例，確保覆蓋：
    - **Happy Path:** 正常、預期的輸入和流程。
    - **Sad Paths:** 已知的錯誤路徑、異常輸入 (如 `null`)。
    - **Edge Cases:** 邊界值 (如 0, -1, 空字串)。

**Step 3: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **確認策略 (Confirm):** 對於一個較大的模組，在開始編碼前，可以向用戶**確認**測試策略。例如：「我計劃為 `UserService` 編寫 5 個單元測試和 1 個整合測試。這個方案可以嗎？」
- **編寫測試程式碼:** 在得到用戶同意後，**創建**或**修改**對應的測試文件 (e.g., `*.test.js`, `test_*.py`)。

**Step 4: 執行與迭代 (Run & Iterate)**
- **運行測試:** 執行新編寫的測試，確保它們能夠正確地運行。
- **迭代:** 根據測試結果，可能需要返回去修改測試程式碼或產品程式碼。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **測試已創建:** 新的測試文件是否已成功寫入到正確的測試目錄中？
- [ ] **測試可運行:** 新增的測試是否能被測試運行器發現並成功執行？
- [ ] **命名清晰:** 測試的描述是否清晰地說明了它在「Given-When-Then」下的行為？

## 4. ACT 改善 (行動)

### Finalization
- **報告結果:** 向用戶報告測試編寫已完成，並提供測試結果的摘要。
- **提交程式碼:** 將新的測試文件提交到版本控制系統。

### Next Steps
> 測試是信心的來源。
- 👉 **Primary Next Step:** 如果測試是開發任務的一部分，現在可以執行 `/task-next` 來獲取下一個任務。
- 💡 **Alternative:** 如果在編寫測試的過程中發現了 Bug，應立即切換到 `/debug` 模式。

---
> **WRITE TESTS MODE (v3) 已啟動。正在檢查 `current` 工作區的測試環境，準備為您的程式碼建立品質防線...**
