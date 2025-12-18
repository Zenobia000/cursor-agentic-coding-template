---
description: VAN MODE - Initializes or verifies the project's shared memory structure (`current` workspace).
---

# 🚀 VAN MODE (v3)

> 冒險啟航！初始化專案，建立共享記憶庫 (`memory-bank`)，為所有 AI 協作奠定堅實的基礎。

## 1. PLAN 🎯 (規劃)

### Objective
> 檢查 `memory-bank` 的拓撲完整性，如果 `memory-bank/current` 工作區不存在或不完整，則**創建**或**修復**核心的共享記憶體文件 (`tasks.md`, `activeContext.md`, `projectbrief.md`)。這是確保所有 AI Agent 能在同一狀態下協作的關鍵第一步。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`
- **檔案操作:** 嚴格遵循檔案操作的最佳實踐，避免意外覆蓋。

### Prerequisites Check
> `VAN MODE` 是所有流程的起點。
- ✅ **無前置條件:** 隨時可以執行此指令來初始化或驗證專案環境。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個具備安全檢查的冪等 (idempotent) 初始化流程：

**Step 0: 健康檢查 (State Check)**
- **檢查 `memory-bank/current` 目錄:** 檢測 `memory-bank/current/` 目錄是否存在。
- **檢查核心文件:** 檢測 `current/` 目錄下的 `tasks.md`, `activeContext.md`, `projectbrief.md` 是否存在。
- **批判性思考:** 這是**狀態診斷**。AI 的任務是找出缺失的部分，並準備修復它們。

**Step 1: 記憶體互動 - 讀取與分析 (Memory Interaction - Read & Analyze)**
- **讀取文件系統:** 獲取 `memory-bank/current/` 目錄的當前狀態。
- **生成執行計畫:** 根據診斷結果，生成一個創建或修復檔案的計畫。

**Step 2: 記憶體互動 - 確認與寫入 (Memory Interaction - Confirm & Write)**
- **向用戶確認 (Confirm):** 在執行任何**寫入**操作之前，AI **必須**向用戶清晰地報告它將要執行的操作，並請求批准。
    - **如果 `current` 目錄不存在:** 「`memory-bank/current` 工作區不存在。我將為您創建該工作區以及所有核心文件。是否繼續？」
    - **如果文件已存在:** 「警告：`memory-bank/current` 中的 `tasks.md` 文件已存在且包含內容。重新初始化將會**覆蓋**它，可能導致數據丟失。您確定要繼續嗎？」
- **執行寫入 (Write):** 在得到用戶**肯定**的答覆後，執行文件和目錄的創建/覆蓋操作。

## 3. CHECK ✓ (檢查)

### Verification Checklist
> 在完成初始化後，進行最終的完整性檢查：
- [ ] **工作區目錄存在:** `memory-bank/current/` 目錄是否已成功創建或確認存在？
- [ ] **核心文件存在:** `current/` 下的核心文件是否都已存在？
- [ ] **權限正常:** AI Agent 是否有權限讀寫 `memory-bank/current/` 目錄？

## 4. ACT 改善 (行動)

### Finalization
- **報告完成:** 在所有文件操作完成後，向用戶報告：「專案初始化完成。共享記憶體 `memory-bank/current` 工作區已準備就緒。」

### Next Steps
> 專案的基礎設施已準備就緒，下一步是定義目標並進行規劃。
- 👉 **Primary Next Step:** 執行 `/task-init`，讓用戶提出第一個高層次目標。
- 💡 **Alternative:** 如果是恢復一個現有項目，可以執行 `/task-next`，讓 PM 小助理分析 `tasks.md` 並建議下一步的工作。

---
> **VAN MODE (v3) 已啟動。正在診斷 `memory-bank/current` 工作區狀態，準備進行初始化...**