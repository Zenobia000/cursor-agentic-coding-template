---
description: CREATIVE MODE - Make and document key design, architecture, and technical choices in the `current` workspace.
---

# 🎨 CREATIVE MODE (v3)

> 做出明智的設計決策，為專案奠定堅實的架構基礎，確保每一次的創造都有跡可循。

## 1. PLAN 🎯 (規劃)

### Objective
> 針對一個具體的、已規劃好的任務，進行深入的技術設計和架構規劃，並將所有決策、理由和權衡，以「架構決策記錄 (ADR)」的形式，**寫入**一份新的 `memory-bank/current/creative-[topic].md` 文件中。

### Guiding Rules
> 在執行此指令時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **架構原則:** `.cursor/rules/backend/overview.mdc` 或 `.cursor/rules/frontend/overview.mdc`
- **設計模式:** `.cursor/rules/patterns/`
- **核心隔離:** `.cursor/rules/isolation_rules/main.mdc`

### Prerequisites Check
> 在開始設計之前，請確保：
- ✅ **任務已規劃:** `memory-bank/current/tasks.md` 中存在一個清晰、待設計的任務。
- ✅ **上下文已同步:** `memory-bank/current/activeContext.md` 反映了當前的工作焦點。
- ❌ **Failure Action:** 如果沒有已規劃的任務，AI **必須**建議用戶先執行 `/plan` 或 `/task-next`。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個包含批判性思維的結構化決策流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查任務清晰度:** 從 `memory-bank/current/tasks.md` 讀取當前任務。驗證其描述和驗收條件是否足夠清晰以進行設計。
- **批判性思考:** 如果任務描述過於寬泛 (e.g., "建立後端")，AI **必須**拒絕設計，並建議用戶先使用 `/plan` 將任務進一步細化。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取任務:** 從 `memory-bank/current/tasks.md` 中讀取當前要設計的任務的詳細資訊。
- **讀取全局上下文:** 讀取 `memory-bank/current/projectbrief.md` 以確保設計與專案總體目標一致。

**Step 2: 設計與決策 (Design & Decision Making)**
- **分析選項:** 針對任務需求，考慮 2-3 個可行的技術方案。
- **評估權衡:** 分析每個方案的優點 (Pros)、缺點 (Cons) 和風險 (Risks)。
- **做出選擇:** 選擇最適合當前專案約束和目標的方案，並清晰地闡明選擇的**理由**。

**Step 3: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **創建 ADR 文件:** 將上述的設計過程和最終決策，**寫入**到一個**新的** `memory-bank/current/creative-[topic].md` 文件中。
- **更新任務列表:** **更新** `memory-bank/current/tasks.md` 文件，在對應的任務下，添加一個指向剛剛創建的設計文檔的連結。

## 3. CHECK ✓ (檢查)

### Verification Checklist
- [ ] **決策已記錄:** `memory-bank/current/creative-[topic].md` 是否已成功創建？
- [ ] **任務已連結:** `memory-bank/current/tasks.md` 中對應的任務是否已更新，並包含了指向新設計文檔的連結？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認:** 在完成寫入操作後，向用戶報告。例如：「我已為任務『XXX』完成了技術設計，並將決策記錄在 `memory-bank/current/creative-auth-flow.md` 中。`tasks.md` 也已同步更新。」

### Next Steps
> 設計完成後，下一步就是將藍圖變為現實。
- 👉 **Primary Next Step:** 執行 `/implement` 指令，AI 將會讀取 `tasks.md` 和新創建的 `creative-*.md` 文件，開始進行編碼。
- 💡 **Alternative:** 如果設計方案存在較大不確定性，可以先執行 `/implement` 創建一個快速的「原型 (Prototype)」來驗證其可行性。

---
> **CREATIVE MODE (v3) 已啟動。正在檢查 `current` 工作區的任務健康狀態，準備進行技術決策...**