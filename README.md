# 🛡️ SQL Injection 互動式教學與測驗平台 (SQL Injection Learning & Quiz Platform)

一個輕量、現代化、響應式（Responsive）且完全無後端依賴的 **SQL Injection（SQL 注入攻擊）互動式教學與線上測驗網站**。

專為資安初學者、資訊課程學生及教師設計，支援純靜態網頁部署，可直接免費託管於 **GitHub Pages**。

---

## 🌟 平台特色

### 1. 💡 觀念說明與防禦範例
- **原理剖析**：清楚呈現動態字串拼接與參數化查詢（Prepared Statements）在資料庫層面的運作差異。
- **多語言範例**：提供 Python (sqlite3/psycopg2)、Node.js (mysql2)、PHP (PDO) 及 Java (JDBC) 的防護範例程式碼。

### 2. 🎮 互動式模擬沙盒 (Interactive Playground)
- **多重情境**：提供「驗證繞過（Login Bypass）」與「資料搜尋（Data Search）」實作情境。
- **模式切換**：支援切換「漏洞模式（Dynamic）」與「安全模式（Prepared Statements）」。
- **即時 SQL 預覽**：輸入 Payload 時即時組裝 SQL 指令，直觀了解漏洞觸發機制。

### 3. 📝 隨機線上測驗系統 (Quiz System)
- **學生身分驗證**：強制填寫「班級、座號、姓名」方可開啟測驗。
- **隨機抽取題庫**：從豐富題庫中**隨機抽取 10 題**，且**題目與選項順序皆打亂**，有效防範抄襲。
- **即時計分與等級評定**：交卷後立即顯示分數與答對題數。

### 4. 📊 成績管理與答案公佈欄 (Leaderboard & Review)
- **學生歷史紀錄**：自動紀錄學生歷次測驗分數與完成時間。
- **教師資料匯入/匯出**：學生可下載成績 JSON 檔，教師匯入後即可統整全班成績榜。
- **詳細答案解析**：交卷後開放公佈欄，提供完整題目解析與破局思路。

---

## 🚀 部署至 GitHub Pages 步驟

本專案無需任何 Node.js Build 流程或後端伺服器，只需單一 `index.html` 即可運作。

1. **建立 GitHub 儲存庫 (Repository)**：
   - 在 GitHub 上建立一個全新的 **Public** 儲存庫（例如 `sqli-tutorial`）。

2. **上傳網頁檔案**：
   - 將本專案的 `index.html` 檔案上傳至該儲存庫的主幹分支（`main` 或 `master`）。

3. **開啟 GitHub Pages**：
   - 前往儲存庫的 **Settings** -> **Pages**。
   - 在 **Build and deployment** 下方的 **Branch** 選擇 `main` (或 `master`)，目錄選擇 `/ (root)`。
   - 點擊 **Save**。

4. **完成發布**：
   - 等待 1~2 分鐘，頁面上方將出現您的專屬網站網址：
     `https://<YOUR-USERNAME>.github.io/<REPOSITORY-NAME>/`

---

## 👨‍🏫 教師教學與成績收集指南

由於本平台採用純前端架構（Local Data），成績紀錄保存在個別學生的瀏覽器中。教師可透過以下方式收集成績：

1. **學生端交卷**：學生完成測驗後，前往「成績榜與公佈欄」。
2. **匯出成績**：學生點擊 **「匯出所有成績 (JSON)」** 按鈕下載 `.json` 成績檔並繳交給教師。
3. **教師端彙整**：教師開啟本網站，點擊 **「匯入資料」** 將全班學生的 JSON 檔案匯入，即可在榜單中瀏覽完整班級排名與成績。

---

## 📖 包含的 SQLi 主題題庫

- SQL Injection 核心原理與定義
- 經典語法與邏輯（`' OR '1'='1`、`--` 註解符號）
- 萬用密碼與身份驗證繞過
- 聯合查詢注入（UNION-based SQLi）
- 盲注（Blind SQLi：Boolean-based / Time-based）
- 參數化查詢（Prepared Statements / Parameterized Queries）
- ORM 框架與防禦縱深（WAF、最小權限原則）

---

## 📄 授權條款 (License)

本專案採用 [MIT License](LICENSE) 授權，歡迎自由修改、延伸教學內容或用於學術與商業教學。
