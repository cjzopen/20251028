# Constitution（專案前端原則）

## 重述（只包含使用者已提供之條件）
- 前端不使用框架；以原生 HTML + JavaScript + Bootstrap 5.3.8 為核心。
- 圖表使用 Chart.js。
- 所有提醒、確認、錯誤、成功提示使用 SweetAlert2@11.26.3。
- 字型使用 "Noto Sans TC"，僅載入 weight 400 與 700。
- 所有載入之 JS 檔都必須加入 `defer`。
- 頁面：
  - 問卷填寫頁：`/index.html`
  - 結果頁：`/result.html`（支援 `?id=` 與無參數情況，提供測試用 id）
- 圖片處理：所有可見外圖片應加 `loading="lazy"`、`decoding="async"`、`alt`（裝飾性圖片以 `*`）並明列 `width` 與 `height`。
- CSS 命名需符合 Bootstrap 風格（語意化命名），並避免使用以 `ad`、`ads`、`advert`、`sponsor` 等為開頭或檔名/類別/ID（以避開 adblock）。
- 問卷共有 27 題（題目由 MIS API 提供），複選分數規則尚未定義（會在 Tasks 中標註需 MIS 確認）。
- 結果呈現：每題以長條圖（x: L1~L5, y: 數量），下方以 `<ul>` 列出 L1~L5 的完整文字選項，再顯示建議文字。

## 不在前端責任範圍
- Email 寄送、資料庫儲存、統計演算法的原始資料產生、建議文案的產出邏輯（皆由 MIS 提供）。
