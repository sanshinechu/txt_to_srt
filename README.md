# YouTube 字幕轉換器（TXT ➜ SRT）部署指南

這個專案是一個單一檔案的前端工具（`index.html`）。你可以用以下任一方式發佈：

---

## A. GitHub Pages（推薦）
1. 到 GitHub 建立一個新的公開 Repository（例如：`subtitle-tool`）。
2. 將 `index.html` 上傳到這個 repo 的根目錄（不要放子資料夾）。
3. 在 repo 的 **Settings → Pages**：
   - Source 選擇 **Deploy from a branch**
   - Branch 選擇 **main**（或你的預設分支），/（root）
   - 按 Save。幾十秒後會出現一個公開網址，例如：
     `https://你的帳號.github.io/subtitle-tool/`
4. 用這個網址就能在任何地方開啟工具；在 **Google Sites** 內可用「插入 → 嵌入 → 網址」放入。

---

## B. Netlify（拖曳上傳）
1. 前往 https://app.netlify.com/ ，登入。
2. 使用 **Add new site → Deploy manually**。
3. **把 `index.html` 直接拖曳**到上傳區域。
4. 發佈後會得到一個網址（可自訂子網域）。

---

## C. Vercel（連接 GitHub）
1. 前往 https://vercel.com/ ，登入。
2. **New Project** → 匯入你的 GitHub repo。
3. Framework 選擇 **Other**（或直接 Default），部署後會得到網址。

---

## D. CodePen（快速測試）
1. 到 https://codepen.io/ ，新增 **Pen**。
2. 將 `index.html`：
   - `<body>` 內內容貼到 **HTML** 面板。
   - `<style>` 內內容貼到 **CSS** 面板（可留在 HTML 也行）。
   - `<script>` 內內容貼到 **JS** 面板（記得把 `tailwind` CDN 加在 HTML）。
3. 儲存後會得到一個可嵌入的連結。

---

## 備註
- 本工具不需要後端伺服器，純前端可離線使用（首次載入需網路以取得 Tailwind CDN）。
- 如果要完全離線，建議改為本地建置 Tailwind 或移除 Tailwind 樣式。
