# 🌱 甲五 Sober Picnic — Vibe Coding 指令集與開發歷程

> **專案名稱**：甲五 - Sober Picnic 無酒精永續野餐  
> **團隊成員**：蔡欣妘（組長）、呂品依、林子淇、洪婷鈺、劉欣漶、錢奕靜、高銘鴻、林恩駿  
> **指導老師**：丁美靜、王婉禎、李悅端、李律鋒  
> **技術架構**：HTML5 / CSS3 (CSS Grid & Flexbox) / RWD 響應式設計 / GitHub / InfinityFree Hosting  

---

## 📌 關於 Vibe Coding 開發模式

本專案採用 **Vibe Coding（自然語言與 AI 協作開發）** 模式。透過與 AI Writing Coach & Senior Developer 進行連續對話，將企劃企劃書（PDF）轉換為符合 HW07 標準的正規商業網站。

在開發過程中，團隊精準運用了提示詞工程（Prompt Engineering），包含 **脈絡設定（Context Provisioning）**、**視覺語意化描述（Design Token Translation）**、**跨環境路徑除錯（Path & Environment Debugging）** 等多項指令技巧。

---

## 💡 關鍵 Vibe Coding 指令集（Prompt Logs）

以下為本專案在開發各階段所使用的核心提示詞指令：

### 1. 專案主題變更與企劃書解析指令 (Prompt for Context & Document Parsing)
> **使用情境**：將原始 HW07 的棒球場主題轉換為《甲五 Sober Picnic》無痕野餐正式網站，要求 AI 讀取企劃書 PDF 並解析結構。

```text
「請依照開學至今所有之前所學，建議一個具有導覽列、側邊欄，並具有分頁的完整網頁。
需要具有完整的 SEO 內容、Grid System、RWD 功能（可用手持裝置觀看可以顯示完整資訊）等。
需要將 CSS 檔案進行切割後放置在 css 檔案匣內，圖片放置在 images 檔案匣內。
幫我保留 hw07 所有的程式建構，清除所有先前關於洲際棒球場的資料，放上所有這個檔案（甲五_Sober picnic.pdf）的相關資料重新製作並設計一個新的正式網站。」
```

---

### 2. 視覺風格與色調調整指令 (Prompt for Design System & Aesthetics)
> **使用情境**：擺脫預設樣式，要求 AI 以品牌精神「無痕、低碳、清醒社交」為導向，設計專屬配色與 UI 質感。

```text
「風格幫我設計成無痕野餐這種帶有清醒野餐、清新感的色調風格。」
```
* **AI 轉化出的 CSS 設計系統（Tokens）**：
  * **野餐綠（Sage Green `#4a7c59`）**：品牌主調，代表自然與無痕。
  * **燕麥奶茶（Oatmeal White `#f7f9f6`）**：背景柔和色，提供閱讀舒適感。
  * **氣泡金黃（Soft Yellow `#e3a857`）**：點綴色，象徵陽光與水果氣泡水。

---

### 3. 多分鏡圖片與網格展示指令 (Prompt for Dynamic Layouts)
> **使用情境**：針對專案中有多張廣告分鏡圖與客群 Persona 卡片的需求，指示 AI 設計 CSS Grid 畫廊。

```text
「我的分鏡圖很多張，請幫我在網頁上設計適合多圖呈現的排版方式。」
```

---

### 4. 跨伺服器環境除錯指令 (Prompt for Environment & Subfolder Path Debugging)
> **使用情境**：處理 InfinityFree 子資料夾 `/project1/` 與相對路徑 `../` 對不齊、HTML 漏寫 `href` 屬性導致 CSS 樣式與圖片失效的診斷指令。

```text
「https://d1243359.ct.ws/project1/project1.html 看的出來問題在哪嗎？
我現在 html 網頁跑得出來，css 的獨立網頁也跑得出來，但網頁風格跑不出來。」
```
* **AI 協助排查出的 Bug 關鍵**：
  1. HTML 中的 `<link rel="stylesheet">` 漏寫 `href` 屬性。
  2. 網頁位於 `/project1/` 子資料夾時，相對路徑需修正為 `href="../css/style.css"` 或移動檔案至 `htdocs` 根目錄。

---

## 📂 專案檔案目錄架構

```text
sober-picnic-website/
├── README.md             <-- 本說明文件
├── index.html            <-- 專案主頁面 (HTML5 / SEO 標籤 / 語意化結構)
├── css/
│   └── style.css         <-- 獨立 CSS3 樣式檔 (CSS Grid / RWD 斷點 / CSS 變數)
└── images/               <-- 專案靜態圖片資源
    ├── hero-picnic.jpg   <-- 野餐情境與分鏡圖
    ├── persona-1.jpg     <-- 客群角色 蔡欣儒
    ├── persona-2.jpg     <-- 客群角色 林鈺涵
    └── persona-3.jpg     <-- 客群角色 吳濬丞
```

---

## 🔗 相關連結 (Project Links)

* 🌐 **正式上線網站（InfinityFree 託管）**：[https://d1243359.ct.ws/project1/project1.html](https://d1243359.ct.ws/project1/project1.html)
