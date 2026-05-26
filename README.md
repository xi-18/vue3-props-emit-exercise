# 🛒 Vue 3 組件通訊實戰：輕量級電商控制台

歡迎來到 Vue 3 核心修練場！本練習旨在幫助你徹底掌握 Vue 3 `<script setup>` 語法中，組件與組件之間最核心的通信機制：**Props（資料由上往下傳）** 與 **Emit（事件由下往上傳）**。

透過本練習，你將會把一個靜態的網頁，組裝成一個具備資料傳遞與事件響應的「電商主控台」。

---

## 🛠️ 開發環境準備

請在你的電腦上使用終端機（Terminal）依序執行以下指令來初始化專案：

```bash
# 1. 進入專案資料夾
cd vue3-props-emit-exercise

# 2. 安裝專案依賴套件
npm install

# 3. 啟動在地開發伺服器
npm run dev
```

啟動後，請打開瀏覽器造訪終端機顯示的網址（通常是 http://localhost:5173/）。

## 📋 實作任務與驗收標準

本專案總共有兩個核心任務，請根據程式碼檔案中標註 【任務一】 與 【任務二】 的註解提示進行填空：
**🔍 任務一：商品卡片元件（練習 Props）**
**目標檔案：src/components/ProductCard.vue 與 src/App.vue**
實作規格：
在 ProductCard.vue 中，使用 defineProps 宣告接收以下三個屬性：
title: 字串（String），必填
price: 數字（Number），必填
isFeatures: 布林值（Boolean），非必填，預設值為 false
在 App.vue 中，利用 v-for 迴圈將 products 陣列裡的資料，透過 Props 完整傳遞給 ProductCard 組件。
驗收標準：畫面上必須正確顯示三張商品卡片。其中「專業螢幕」與「垂直滑鼠」的卡片上方，必須因為 isFeatures="true" 而自動亮起綠色邊框與「⭐ 推薦商品」的標籤。

**📣 任務二：購物車數量調整（練習 Emit）**
**目標檔案：src/components/CounterButton.vue 與 src/App.vue**
實作規格：
在 CounterButton.vue 中，使用 defineEmits 定義一個自訂事件（例如：change-volume）。
替子組件內的兩個按鈕綁定點擊事件，當點擊「+ 1 件」時，emit 傳送數值 1；點擊「- 1 件」時，emit 傳送數值 -1。
在 App.vue 中引進並渲染 CounterButton，同時監聽該自訂事件，觸發 updateCartCount 函式，讓父組件的 totalCartCount 變數隨點擊即時加減。
驗收標準：點擊下方的按鈕時，網頁頂部綠色區塊的「購物車商品總數」數字必須即時隨之改變。

## 💡 進階挑戰（加分題）

現在的計數器點擊多次後，購物車總數可能會變成「負數」（例如：-3 件）。
請嘗試修改 App.vue 中的 updateCartCount 函式，加入邏輯判斷，讓購物車的最低總數只能卡在 0，不能變成負數。

**🚀 學員作業三大步驟**
完成環境準備並看懂規格後，請按照以下流程進行開發與繳交：

## 建立自己的作業庫：點擊教官提供的連結，在網頁右上角點擊 Use this template ➔ Create a new repository。這會在你的 GitHub 帳號下複製一份專案。

## 下載並實作：將你複製出來的專案 git clone 到電腦上，根據上述的驗收標準與程式碼註解完成填空。

## 推回並繳交：確認瀏覽器 Console 沒有任何紅字報錯後，使用 Git 把進度推回你自己的 GitHub，並把你的 GitHub 網址交給教官批改。

```Bash
git add .
git commit -m "feat: 完成 props 與 emit 實作作業"
git push origin main
```
