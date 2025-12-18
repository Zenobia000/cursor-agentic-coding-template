---
description: ARCHIVE MODE - Archives the `current` workspace to preserve a completed work cycle.
---

# 📚 ARCHIVE MODE (v3)

> 封存當前週期的知識與成果，為未來鋪路，確保沒有任何智慧被遺忘。

## 1. PLAN 🎯 (規劃)

### Objective
> 將一個已完成開發週期的所有工作成果 (即 `memory-bank/current/` 中的所有內容) 進行結構化歸檔，並清理工作區，為下一個週期的乾淨啟動做準備。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **Git 工作流:** `.cursor/rules/process/git-workflow.mdc`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始封存之前，請確保：
- ✅ **實作已完成:** `memory-bank/current/tasks.md` 中絕大多數任務都已標記為 `completed`。
- ✅ **反思已完成:** 一個對應的 `reflection-*.md` 文件已存在於 `memory-bank/current/` 中。
- ❌ **Failure Action:** 如果任務未完成或反思不存在，AI **必須拒絕封存**，並建議用戶先執行 `/implement` 或 `/reflect`。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個嚴謹的、不可逆的封存流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查拓撲完整性:** 驗證 `memory-bank/current/` 中的 `tasks.md`, `progress.md`, 和 `reflection-*.md` 文件是否存在且狀態一致。
- **批判性思考:** 封存是一個週期的終點。AI 應檢查是否存在任何「半成品」。如果發現，應向用戶提問並請求確認。

**Step 1: 文件定稿 (Finalize Documentation)**
- 基於 `memory-bank/current/reflection-*.md` 的內容，更新 `README.md` 和 `CHANGELOG.md`。

**Step 2: 記憶體互動 - 讀取與寫入 (Memory Interaction - Read & Write)**
- **創建封存目錄:** 創建一個新的、以日期命名的封存目錄，例如 `archive/sprint-2025-12-18/`。
- **複製記憶體:** 將**整個** `memory-bank/current/` 目錄的內容**複製**到新的封存目錄中。
- **清理工作區:** 在**用戶確認**後，清理 `memory-bank/current/` 中的內容。

**Step 3: 版本控制 (Version Control)**
- **Git Add:** 將新的 `archive/` 目錄和更新的 `README.md` / `CHANGELOG.md` 添加到 Git 暫存區。
- **Git Commit:** 創建一個標準化的提交訊息，例如 `chore(project): archive sprint-2025-12-18 work cycle`。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **封存目錄已創建:** `archive/sprint-..../` 目錄和其內容是否已成功創建？
- [ ] **記憶體已複製:** 封存目錄中的文件是否與封存前的 `memory-bank/current/` 內容完全一致？
- [ ] **Git 狀態正確:** `git status` 是否顯示了預期的變更？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認:** 在執行清理和提交等不可逆操作**之前**，AI **必須**向用戶請求最終批准。例如：「我已準備好將本次週期的所有成果封存到 `archive/sprint-..../` 並創建一個 Git 提交。**清理工作區並提交後，此操作不可逆。** 是否繼續？」

### Next Steps
> 封存完成後，一個完整的週期便告結束。
- 👉 **Primary Next Step:** 執行 `/van` 指令，重新初始化一個乾淨的 `memory-bank/current` 工作區。
- 💡 **Alternative:** 將專案移交給維護團隊，並告知他們 `archive/` 目錄是最終的知識庫。

---
> **ARCHIVE MODE (v3) 已啟動。正在檢查 `current` 工作區健康狀態，準備進行週期封存...**