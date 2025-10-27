# Plan（前端技術計畫 — 僅描述前端如何執行）

## 檔案結構（建議）
/index.html
/result.html
/assets/css/style.css
/assets/js/index.js
/assets/js/result.js
/assets/vendor/* (CDN fallback 或本地 vendor 若需要)

## head 最佳化（遵從你提供之項目）
- `<html lang="zh-Hant">`
- `<meta name="viewport" content="width=device-width, initial-scale=1">`
- `<title>頁面標題 | 品牌名</title>` （品牌名放在後方，用 `|`）
- meta description（由你填寫）
- canonical link（留空或由後端填入）
- Open Graph 與 Twitter Card meta（範本留在 head）
- `<meta name="robots" content="noindex, nofollow">` 僅用於 `result.html`
- `<meta name="max-image-preview" content="large">`
- fonts 與外部資源使用 `preconnect`，避免不必要的 block
- 所有外部 script 加 `defer`

## 圖表與互動
- Chart.js 在 DOM 與資料取得完成後初始。
- result.html 若無 id → 使用 SweetAlert2 顯示錯誤且提供「測試模式」按鈕；測試 ID 以常數保留在 `result.js` 中。

## 圖片與可及性
- 所有圖片都要 `alt`、`loading="lazy"`、`decoding="async"`，並盡可能提供 `width`、`height`。
