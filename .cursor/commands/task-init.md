---
description: TASK INIT - Initialize a new high-level task or epic into the `current` workspace.
---

# 🚀 TASK INIT (v3)

> 為一次新的冒險啟航！將用戶的模糊想法，轉化為一個清晰、可追蹤的任務 Epic。

## 1. PLAN 🎯 (規劃)

### Objective
> 將一個新的、高層次的用戶需求，轉化為一個結構化的 Epic 任務，並在**用戶確認後**，將其**添加**到 `memory-bank/current/tasks.md` 的頂部，作為後續 `/plan` 指令的輸入。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **規劃流程:** `.cursor/rules/process/planning-process.md`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在初始化一個新任務之前，請確保：
- ✅ **`tasks.md` 存在:** 核心任務文件 `memory-bank/current/tasks.md` 已由 `/van` 指令創建。
- ✅ **需求已提供:** 用戶已提出一個新的目標或需求。
- ❌ **Failure Action:** 如果 `tasks.md` 不存在，AI 應建議先運行 `/van`。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個從需求到 Epic 的結構化轉化流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查需求清晰度:** 分析用戶的請求。
- **批判性思考:** 如果用戶的需求極度模糊 (e.g., "給我做個 AI")，AI **必須**通過提問來引導用戶聚焦。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取用戶需求:** 這是本指令的主要輸入。
- **(可選) 讀取專案簡報:** 快速掃描 `memory-bank/current/projectbrief.md`，以確保新任務與專案大方向一致。

**Step 2: 結構化分析 (Structured Analysis)**
- **定義目標 (Goal):** 用一句話總結任務的最終目標。
- **定義驗收條件 (DoD):** 列出 3-5 個關鍵的、可衡量的「完成定義」。
- **初步分解 (WBS):** 創建一個非常高層次的階段劃分。
- **風險評估 (Risks):** 識別 1-3 個最顯而易見的風險。

**Step 3: 記憶體互動 - 確認與寫入 (Memory Interaction - Confirm & Write)**
- **向用戶確認 (Confirm):** 將上述分析結果，以一個清晰的「任務提案」形式呈現給用戶，並**請求批准**。
- **追加寫入 `tasks.md` (Append):** 在得到用戶**肯定**的答覆後，將這個結構化的 Epic 任務**追加**到 `memory-bank/current/tasks.md` 文件的頂部。**注意：是追加 (append)，不是覆蓋 (overwrite)。**

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **提案是否清晰:** AI 生成的「任務提案」是否準確且簡潔地反映了用戶的需求？
- [ ] **用戶是否確認:** AI 是否在寫入 `tasks.md` 之前，獲得了用戶的明確批准？
- [ ] **`tasks.md` 是否已更新:** 檢查 `memory-bank/current/tasks.md` 文件，確認新的 Epic 任務是否已成功追加。

## 4. ACT 改善 (行動)

### Finalization
- **報告完成:** 在更新 `tasks.md` 後，向用戶報告。例如：「好的，我已經將『XXX』任務作為一個新的 Epic 添加到我們的計畫中。」

### Next Steps
> Epic 的創建是詳細規劃的開始。
- 👉 **Primary Next Step:** 執行 `/plan` 指令。`/plan` 指令會讀取剛剛創建的 Epic，並將其進一步分解為詳細的、可執行的子任務。
- 💡 **Alternative:** 如果識別出的風險非常高，可以先執行一個研究性質的任務 (Spike)，對不確定的技術點進行預研。

---
> **TASK INIT (v3) 已啟動。正在聆聽您的新想法，並準備將其轉化為行動藍圖...**
