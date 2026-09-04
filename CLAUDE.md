# oa-page-home 專案指引

## 🔴 上線當天必做（漏了就是全站最嚴重的失誤）

**把 `index.html` 的 `<meta name="robots">` 改回：**

```html
<meta name="robots" content="index, follow, max-image-preview:large, max-snippet:-1">
```

2026-09-04 起暫時設為 `noindex, follow`，原因是本 repo 的 GitHub Pages 預覽
（`https://poshlin.github.io/oa-page-home/`）是公開的，原本 `index, follow`
等於讓 Google 收錄一份尚未發布、內容與線上首頁不同的副本。

**這是首頁。忘了改回來＝整個首頁從 Google 消失。** 檔案第 16 行附近有同樣的紅字註解。

另外：交接完成、公司端建好 `OrangeApple-Lab/oa-page-home` 之後，
請一併關閉本 repo 的 GitHub Pages 並封存（about／classroom／faq／online／
contestant-prototype／course-math 已於 2026-09-04 完成此步驟）。

本專案的設計系統定義在根目錄的 `DESIGN.md`。產生或修改任何 UI 元件前，一律先讀它，並嚴格對齊其色彩、字體、間距、圓角、陰影、動效與 Do's and Don'ts（含：亮橘 #FFA300 絕不配白字、免費試聽才用橘實心、實心鈕必寫 border: 2px solid transparent）。
