# Vic 技術美術支援服務 - 官方網站

這是一個為「Vic 技術美術支援服務」設計的簡單、單頁式靜態網站。

## 如何預覽

直接在網頁瀏覽器中開啟 `index.html` 檔案即可查看網站內容。

## 專案結構

-   `index.html`: 網站的主要 HTML 檔案，包含了所有的結構、樣式 (CSS) 和腳本 (JavaScript)。
-   `portfolio.json`: 一個 JSON 檔案，用來定義「精選案例」區塊的內容。
-   `images/`: 存放作品集圖片的資料夾。
-   `README.md`: 本檔案。

## 如何客製化網站內容

### 修改基本文字

直接編輯 `index.html` 檔案中的文字內容，例如服務說明、關於我、聯絡資訊等。

### 修改「精選案例」

若要新增、修改或刪除作品集項目，請編輯 `portfolio.json` 檔案。

每個作品集項目都是一個 JSON 物件，包含以下欄位：

-   `type`: 媒體類型。可以是 `"image"` (圖片) 或 `"video"` (影片)。
-   `provider`: (僅適用於影片) 如果是 YouTube 影片，請設為 `"youtube"`。
-   `src`: 媒體來源。
    -   對於圖片：請填寫相對於 `images/` 資料夾的圖片路徑，例如 `"images/project-c.png"`。
    -   對於 YouTube 影片：請填寫 YouTube 提供的內嵌 (embed) URL。
-   `title`: 專案標題。
-   `description`: 專案的詳細說明。

**範例：**

```json
[
  {
    "type": "image",
    "src": "images/project-a.png",
    "title": "自動化綁定工具 (Maya)",
    "description": "為某遊戲工作室開發了一套模組化的自動綁定工具..."
  },
  {
    "type": "video",
    "provider": "youtube",
    "src": "https://www.youtube.com/embed/your_video_id",
    "title": "Houdini 數位資產庫",
    "description": "協助動畫團隊建立了一套 Houdini Engine 數位資產庫..."
  }
]
```

### 修改「費用方案」

若要調整費用，請直接修改 `index.html` 中 `id="fees"` 的 `section` 區塊。
