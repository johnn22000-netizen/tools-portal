# 教學與實用工具平台 (Tools Portal)

[English](#english) | [繁體中文](#繁體中文)

---

<a name="繁體中文"></a>
## 繁體中文說明

### 📌 專案簡介
本專案為微型線上工具庫入口網站，採用 **GitHub Pages（前端 UI） + Google Apps Script（中樞 API） + 個人 Google Sheets（獨立資料庫）** 的無伺服器（Serverless）架構。

使用者無需註冊獨立帳號，僅需提供開放編輯權限的 Google Sheet 連結，即可生成具備加密保護（Token 加密防止逆向工程）的個人專屬工具連結。所有資料皆儲存在使用者自己的 Google 雲端硬碟中，安全且完全免費。

---

### 🚀 使用者操作教學

#### 使用前準備
1. **建立 Google 試算表**：開啟 Google Drive，建立一份新的空白 Google Sheet。
2. **開放權限**：點選右上角「共用」-> 將「一般存取權」改為 **「知道連結的人」**，並將權限設為 **「編輯者」**。
3. **複製連結**：複製該試算表的分享網址。

#### 申請與開啟工具
1. 在本入口網頁瀏覽並選擇欲使用的工具，點擊 **「申請/生成專屬連結」**。
2. 輸入您的 Gmail 與剛剛複製的 Google Sheet 連結。
3. 系統將自動產生一組帶有加密 Token 的專屬 URL（例如：`https://.../tool_A/?token=xxxx`）。
4. 點選專屬連結進入工具，系統將會 **自動在您的 Google Sheet 中建立所需的子資料庫（工作表與標頭）**，即可開始使用。

---

### ⚙️ 後端 API 設定
本平台集中使用以下 Google Apps Script (GAS) Web App 作為中樞 API：
```javascript
const GAS_API_URL = "[https://script.google.com/macros/s/AKfycbzq_tuayTvoxvzJw59NCWo5KFDDN2v2oPtIR6jHKf3E8HqizvupYAHOVMaID3192WcWmg/exec](https://script.google.com/macros/s/AKfycbzq_tuayTvoxvzJw59NCWo5KFDDN2v2oPtIR6jHKf3E8HqizvupYAHOVMaID3192WcWmg/exec)";'''
aaa

