# 🌏 國中地理出題系統 (Geography Exam Maker)

這是一個專為國中地理老師設計的線上出題系統。您可以選擇年級、章節、考試類型，系統會自動產生考卷與詳解，並支援列印或存為 PDF。

## 🌟 功能特色
*   **Wizard 出題流程**：簡單三步驟 (設定範圍 -> 挑選題目 -> 預覽列印)。
*   **題庫管理中心**：提供圖形化介面，可手動新增或刪除題目。
*   **歷屆題庫擴充**：內建國中一至三年級 (台灣/中國/世界地理) 基礎題庫。
*   **自動排版**：專為 A4 列印設計的考卷格式，包含學生作答區與教師解答區。

## 🚀 線上使用
本專案已部署於 GitHub Pages，請直接訪問：
**[線上出題系統連結](https://timcause-bbnet.github.io/geography-exam-maker/)**
*(請將 `timcause-bbnet` 替換為您的 GitHub 帳號)*

---

## 📖 題庫管理說明 (重要)

本系統提供兩種新增題目的方式，請依需求選擇：

### 方法一：直接在網頁上新增 (個人暫存)
*   **適用情境**：臨時出題、個人單機使用。
*   **操作**：點選網頁上方的「📂 題庫管理」或選題流程中的「+ 新增題目」。
*   **資料儲存位置**：**瀏覽器快取 (Local Storage)**。
*   **注意**：
    *   資料**只存在您的這台電腦/瀏覽器**中。
    *   若清除瀏覽器快取或換電腦，**資料會消失**。
    *   這些題目**不會**同步到 GitHub。

### 方法二：修改原始碼 (永久保存)
*   **適用情境**：建立永久題庫、跨裝置使用、分享給其他老師。
*   **操作**：
    1.  在電腦上開啟專案資料夾。
    2.  編輯檔案：`src/data/initialQuestions.js`。
    3.  依照格式複製貼上並修改題目內容。
    4.  將更新後的程式碼上傳 (Push) 至 GitHub。
*   **優點**：資料會永久保存在雲端，重新整理網頁也不會不見。

---

## 🛠️ 本地安裝與開發

如果您希望在自己的電腦上執行程式碼：

### 1. 安裝環境
請確保電腦已安裝 [Node.js](https://nodejs.org/)。

### 2. 下載與安裝
```bash
# 複製專案
git clone https://github.com/timcause-bbnet/geography-exam-maker.git

# 進入資料夾
cd geography-exam-maker

# 安裝套件
npm install
```

### 3. 啟動開發伺服器
```bash
npm run dev
```
啟動後，瀏覽器打開 `http://localhost:5173` (或 5174) 即可看見畫面。

## 📦 部署上線

若您修改了程式碼 (例如更新了 `initialQuestions.js`)，請執行以下指令更新線上網站：

```bash
# 1. 確保程式碼已 Commit
git add .
git commit -m "更新題庫或功能"
git push origin master

# 2. 部署到 GitHub Pages (產生網頁)
npm run deploy
```

## 📂 專案結構
*   `src/data/syllabus.js`: 課綱定義 (年級/學期/章節對照表)
*   `src/data/initialQuestions.js`: 永久題庫檔案
*   `src/App.jsx`: 主要程式邏輯
