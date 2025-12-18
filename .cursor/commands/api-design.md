---
description: API DESIGN - A guide for designing robust, RESTful APIs into the `current` memory workspace.
---

# 🌐 API DESIGN GUIDE (v3)

> 像娜美畫航海圖一樣，遵循此指南，精確地設計出世界級的 API。

## 1. PLAN 🎯 (規劃)

### Objective
> 作為一個 AI Agent，遵循本指南中定義的最佳實踐，為給定的需求設計出一個符合 RESTful 原則、穩健、可擴展且易於使用的 API 規範。

### Guiding Rules
> 在執行 API 設計時，AI Agent 必須遵循以下規則：
- **主要規則:** `.cursor/rules/principles/global.mdc`
- **架構原則:** `.cursor/rules/backend/overview.mdc`
- **設計模式:** (可選) `.cursor/rules/patterns/`

### Prerequisites Check
> 在開始設計之前，請確保：
- ✅ **需求已定義:** 一個清晰的需求文檔、使用者故事或 `memory-bank/current/projectbrief.md` 已經存在。
- ✅ **資源已識別:** 核心的業務資源、屬性和它們之間的關係已經被初步識別。
- ❌ **Failure Action:** 如果需求不清晰，AI **必須先提出問題**以澄清需求，而不是猜測。

## 2. DO 実行 (執行)

### Core Process
> 遵循一個系統化的 API 設計流程：

**Step 0: 健康檢查 (Health Check)**
- **檢查輸入:** 驗證需求文檔是否清晰、無歧義。
- **批判性思考:** API 設計的目標是解決實際問題。如果需求本身似乎會導致一個複雜或不合理的 API，AI 應提出質疑。

**Step 1: 記憶體互動 - 讀取 (Memory Interaction - Read)**
- **讀取需求:** 從 `memory-bank/current/projectbrief.md`, `memory-bank/current/tasks.md`, 或其他需求來源文件中，完全理解業務目標和功能需求。

**Step 2: 設計核心元素 (Design Core Elements)**
- **端點設計 (Endpoint Design):** 根據資源和 CRUD 操作定義直觀的 URL 結構。
- **數據格式 (Data Formatting):** 設計一致的 JSON 請求/回應格式。
- **認證授權 (Auth & Authz):** 選擇合適的認證機制和權限控制策略。

**Step 3: 設計進階特性 (Design Advanced Features)**
- **資料驗證 (Data Validation):** 建立嚴格的輸入驗證 schema。
- **版本管理 (Versioning):** 制定清晰的 API 版本策略。
- **速率限制 (Rate Limiting):** 設計速率限制策略以防止濫用。

**Step 4: 記憶體互動 - 寫入 (Memory Interaction - Write)**
- **產出設計文檔:** 將最終的 API 設計規範，以 OpenAPI (Swagger) 格式，**輸出到一個新的 `memory-bank/current/creative-api-design-[feature].md` 文件中**。
- **更新上下文:** 在 `memory-bank/current/activeContext.md` 中註明 API 設計已完成。

## 3. CHECK ✓ (檢查)

### Verification Checklist
> 在產出設計文檔後，AI 應自我檢查：
- [ ] **一致性:** 所有端點的命名、數據格式和錯誤處理是否一致？
- [ ] **記憶體同步:** `memory-bank/current/creative-api-design-[feature].md` 是否已成功創建？

## 4. ACT 改善 (行動)

### Finalization
- **向用戶確認:** 報告 API 設計已完成並已存檔。例如：「API 設計已完成，詳細的 OpenAPI 規範已儲存至 `memory-bank/current/creative-api-design-[feature].md`。請您審閱。」

### Next Steps
> API 設計是實施的藍圖。
- 👉 **Primary Next Step:** 執行 `/implement` 指令，根據此 API 設計規範開始編寫後端程式碼。
- 💡 **Alternative:** 執行 `/review-code` 指令，邀請另一位 AI Agent 或人類專家對此 API 設計文檔進行審查。

---
> **API DESIGN GUIDE (v3) 已載入。AI Agent 將遵循此指南進行設計...**