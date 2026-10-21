# The Stage（線上鏡像）

**網址：https://stage.entrepreneurship-lab.com**

The Stage 是 Alex（成大管理學院）的課堂舞台工具：點名、分組、抽籤、抽卡、計時。
它本來就是一個完全離線、雙擊即開的單一 HTML 檔；這個 repo 只是把同一個檔案放上網，
讓老師在任何教室打網址就能用。

## 這個 repo 裡沒有原始碼

- 原始碼（`src/`、`build.py`）住在 Alex 的 OneDrive「授課工具包」資料夾，不在 GitHub。
- `index.html` 由那邊的 `python3 build.py` 自動產生並推上來。**不要直接在這裡改 `index.html`**，下次 build 會整個覆蓋。
- 線上版與離線成品唯一的差別：線上版多一行 `<meta name="robots" content="noindex">`，不讓搜尋引擎收錄。

## 助教：怎麼拿到離線版

1. 開 https://stage.entrepreneurship-lab.com
2. 按 Ctrl+S（Mac 是 ⌘S），存檔類型選「**網頁，僅 HTML**」（不要選「完整網頁」，Chrome 會改寫內容）。
3. 存下來的檔案雙擊就能開，不需要網路。

## 資料不會在線上版與離線版之間自動同步

名單、點名紀錄、分組結果都存在瀏覽器的 localStorage，而瀏覽器把「網址開的」和「檔案開的」當成兩個不同的來源。
要把資料從一邊搬到另一邊，用工具右側面板的「匯出 JSON ／ 匯入 JSON」。

## 授權

- 程式：Alex Chang。
- 字型：源泉圓體 Heavy 子集（ButTaiwan，SIL Open Font License 1.1）。
- 音效：全部 CC0，來源清單在原始碼資料夾的 `音效來源.md`。
- 第三方庫（內嵌）：spin-wheel、canvas-confetti、SheetJS、anime.js。
