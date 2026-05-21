# 系統/平台開發流程說明（PDP）

一份單頁式的標準作業程序（SOP）文件，協助非數位單位的同仁熟悉系統／平台從概念到上線的完整開發流程。

## 內容

整份文件為單一檔案 `index.html`，分為四個頁籤：

- **前導頁** — 如何使用這份文件、常見誤區、流程總覽快速表，以及「自行開發 vs 委外廠商」的判斷指引
- **名詞對照表** — MRD、PRD、RFP、UAT 等英文縮寫與專有名詞的白話解釋
- **自行開發流程** — 團隊自行開發的五大階段（Concept → Plan/Design → Build/Test → Release Candidate → Review）
- **委外廠商流程** — 委外情境下額外的選商、合約、Kick-off、UAT、技術移交等步驟

## 瀏覽方式

- 本機：直接用瀏覽器開啟 `index.html`
- 線上：透過 GitHub Pages（見下方部署說明）

## 部署（GitHub Pages）

1. 將本儲存庫推送到 GitHub（儲存庫需設為 Public）
2. 進入儲存庫 **Settings → Pages**
3. Source 選「Deploy from a branch」，Branch 選 `main`、資料夾 `/ (root)`，按 Save
4. 約 1–2 分鐘後，頁面會發布於 `https://<帳號>.github.io/<儲存庫名稱>/`

## 更新內容

1. 編輯 `index.html`
2. 提交並推送：

   ```
   git add index.html
   git commit -m "更新說明"
   git push
   ```

3. GitHub Pages 約 1 分鐘後自動重新發布

## 設計說明

- 單一 HTML 檔，內含所有 CSS 與 JavaScript，無需建置流程、無外部相依套件
- 已針對手機瀏覽優化（RWD）：頁籤可橫向滑動、對照表與名詞表在窄螢幕自動改為單欄
- header 標題與頁籤置中顯示
- 內文標點一律使用全型
- 配色以藍色系為主，輔以綠色標示「委外新增」步驟
