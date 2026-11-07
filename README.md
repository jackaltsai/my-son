# 九宮格寫作提問練習

依據山口拓朗《文章寫得又快又好，九宮格寫作術》做的練習工具。流程是：先問 → 再答 → 分類 → 寫成文章。

整個 app 只有一個 `index.html`（HTML + CSS + JS 都在裡面），不需要建置。

## 怎麼開

**方法一：直接打開**

用瀏覽器打開 `index.html`（雙擊，或拖進瀏覽器）。

**方法二：本機伺服器**

```bash
npm run dev
```

然後打開 http://localhost:3000 。第一次執行會自動下載 [`serve`](https://www.npmjs.com/package/serve)，不需要先 `npm install`。

## 功能

1. **九宮格提問**：中心格寫主題，周圍 8 格用 7W3H（Who、What、When、Where、Why、Which、Whom、How、How many、How much）隨機出題。
   - 「基礎問題」的答案是事實，「鏟子問題」的答案因人而異。
   - 🎲 全部重新出題（答案會清空），或用每格的 ↻ 只換那一題（答案保留）。
2. **主題清單**：6 類、36 個主題，可以從下拉選單挑，或隨機抽。
3. **問答整理**：自動整理成純文字，可以複製。
4. **分類・排序・文章骨架**：
   - 把每個回答標成「事實」或「感受／意見」。
   - 勾選要用的素材，用拖曳或 ▲▼ 排順序。
   - 自動產生「開頭／本文／結論」大綱，可以複製。
5. **輸出 PDF**：A4 版面，包含九宮格和「文章構想筆記」區。

進度存在瀏覽器的 `localStorage`（key：`ninegrid-writing`），換瀏覽器或清除網站資料就會不見。

## 外部依賴

- Google Fonts：Noto Sans TC、Noto Serif TC
- [html2canvas](https://html2canvas.hertzen.com/) 1.4.1、[jsPDF](https://github.com/parallax/jsPDF) 2.5.1（從 cdnjs 載入）

所以要連網才能載入字型和 PDF 功能。

## 已知問題

- PDF 是圖片型，裡面的文字不能選取或搜尋。
- PDF 的中文字型和分頁還沒完整實測。
- 題庫和主題清單寫死在 `index.html` 裡。
