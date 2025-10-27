# Tasks（任務拆解）

## 優先基礎
- [ ] 建立 index.html（包含 progress bar、表單區、個人資訊欄）
- [ ] 建立 result.html（含缺少 id 的處理與測試 id）
- [ ] 建立 /assets/css/style.css（載入 Noto Sans TC 400/700、Bootstrap override）
- [ ] 建立 /assets/js/index.js（題目載入、動態渲染、進度條、送出）
- [ ] 建立 /assets/js/result.js（讀 id、fetch、Chart.js、顯示建議）
- [ ] 整合 SweetAlert2@11.26.3 與 Chart.js CDN（皆 defer）

## 與 MIS 需確認的事項（必須）
- [ ] 取得問卷題目 API endpoint 與 response 範例（題目 27 題的欄位格式）
- [ ] 送出問卷的 POST endpoint 與接受欄位格式
- [ ] result 查詢 API endpoint 與 response 範例（包含分佈統計與建議文字）
- [ ] 複選題分數計算邏輯（若有複選）
- [ ] 測試 ID 的實際範例值（或允許前端模擬）

## 測試
- [ ] 本地靜態檔案測試（模擬回傳 JSON）
- [ ] 設計師可在 HTML 直接修改樣式並看到變更
