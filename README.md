石頭哥收到！你想要開源這個繪本模板，讓大家都能複製使用，但**圖片版權要保護**——這是對脆友 `happy556642` 女兒創作的尊重，非常正確。

---

## 需要修改的地方

### 1. README.md（完整教學 + 版權聲明）

我直接給你一份完整的 `README.md`，貼上即可：

```markdown
# 📖 翻頁式繪本模板（Picture Book Flip Template）

一個純 HTML/CSS/JS 製作的**橫向翻頁繪本模板**，支援手機觸控滑動、鍵盤方向鍵、底部導航點與目錄跳轉。無需安裝任何軟體，上傳到 GitHub Pages 即可分享。

---

## ⚠️ 版權聲明（重要）

**本模板程式碼開源，歡迎自由複製、修改、使用。**

**但所有示範圖片（01-cover.png 至 09-ending.png）的著作權，歸屬於 Threads 脆友 [@happy556642](https://www.threads.net/@happy556642) 的 6 歲女兒所有。**

> 🚫 **禁止複製、轉載、修改、商業使用這些圖片。**
> 
> 若您使用本模板製作自己的繪本，請**替換成您自己或您孩子的原創圖畫**。

---

## ✨ 功能特色

| 功能 | 說明 |
|------|------|
| 📱 手勢翻頁 | 左右滑動即可翻頁，iPhone/Android 皆適用 |
| ⌨️ 鍵盤支援 | 方向鍵、空白鍵、PageUp/Down 皆可翻頁 |
| 🔘 導航圓點 | 底部顯示目前頁數，點擊可跳轉 |
| 📑 目錄索引 | 點右上角「☰」開啟目錄，快速跳轉任意頁面 |
| 🎨 繪本風格 | 溫暖米白紙張底色，適合兒童繪本展示 |
| ⚡ 零安裝 | 純 HTML 單檔案，不用安裝任何軟體 |

---

## 🚀 快速開始（3 步驟）

### Step 1：準備圖片
- 將孩子的畫作掃描或拍照
- 統一命名格式：`01-cover.png`、`02-page1.png`、`03-page2.png`...
- 建議尺寸：1920×1080 或等比例，檔案建議 `.png` 或 `.jpg`

### Step 2：建立 GitHub 倉庫
1. 登入 [GitHub](https://github.com)
2. 點右上角 `+` → `New repository`
3. 命名：`my-picture-book`（隨意）
4. 勾選 `Add a README file` → `Create repository`

### Step 3：上傳檔案
```
my-picture-book/
├── index.html          ← 複製本模板的 HTML
└── images/
    ├── 01-cover.png
    ├── 02-page1.png
    └── ...（您的圖片）
```

1. `Add file` → `Create new file` → 檔名 `index.html` → 貼上模板程式碼 → Commit
2. `Add file` → `Create new file` → 檔名 `images/README.md` → 空白內容 → Commit（建立資料夾）
3. 進入 `images/` → `Add file` → `Upload files` → 上傳您的圖片 → Commit

### Step 4：開啟 GitHub Pages
1. 進入倉庫 `Settings` → `Pages`
2. `Source` 選 `Deploy from a branch`
3. `Branch` 選 `main` / `/(root)` → `Save`
4. 等待 1-2 分鐘，網址：`https://您的帳號.github.io/my-picture-book/`

---

## 📝 自訂修改指南

### 修改繪本標題
找到 `<title>` 和封面頁的 `<h1>`、`<p>`：
```html
<title>您的繪本標題</title>
<h1 class="cover-title">您的繪本標題</h1>
<p class="cover-subtitle">獻給 XX 歲 XX 的專屬繪本</p>
```

### 修改頁數與圖片
找到 `<section>` 區塊，複製貼上增加或減少頁數：
```html
<section class="slide slide-fullimage" data-index="X">
    <img src="images/您的圖片.png" alt="描述" class="page-image" loading="lazy">
    <div class="page-num">XX / 總頁數</div>
</section>
```

### 修改目錄標題
找到 `pageTitles` 陣列：
```javascript
const pageTitles = [
  '封面：您的標題',
  '第一頁描述',
  '第二頁描述',
  // ...依此類推
];
```

### 修改顏色風格
找到 `:root` 區塊，調整色碼：
```css
:root {
  --bg: #fdf6e3;        /* 背景色 */
  --text-primary: #5c4a3d;  /* 主文字色 */
  --accent: #e67e22;    /* 強調色（橘色） */
}
```

---

## 📂 檔案結構範例

```
my-picture-book/
├── index.html          ← 翻頁引擎（本模板）
├── README.md           ← 說明文件（可選）
└── images/             ← 圖片資料夾
    ├── 01-cover.png
    ├── 02-page1.png
    ├── 03-page2.png
    └── ...
```

---

## 🛠️ 技術規格

| 項目 | 說明 |
|------|------|
| 技術 | 純 HTML5 + CSS3 + JavaScript（無框架） |
| 瀏覽器 | Chrome、Safari、Firefox、Edge 最新版 |
| 手機 | iPhone、Android 皆可 |
| 特效 | CSS Scroll Snap 橫向吸附翻頁 |
| 背景 | CSS 漸層（無 WebGL，手機省電） |

---

## 📜 授權條款

- **程式碼**：MIT License，歡迎自由使用、修改、分享
- **示範圖片**：版權歸屬 @happy556642 的 6 歲女兒，禁止複製使用
- **您上傳的圖片**：請確保擁有著作權或已取得授權

---

## 💡 常見問題

**Q：可以放到其他平台嗎？**
> 可以！任何支援靜態網頁托管的平台都行（Netlify、Vercel、Cloudflare Pages 等）。

**Q：圖片格式一定要 PNG 嗎？**
> 不一定，`.jpg`、`.jpeg`、`.webp` 都可以，記得修改 `index.html` 裡的副檔名。

**Q：最多可以放幾頁？**
> 沒有限制，但建議 10-20 頁以內，手機載入較快。

**Q：可以加上背景音樂嗎？**
> 可以，在 `<body>` 內加入 `<audio>` 標籤，但需注意自動播放政策。

---

## 🙏 特別感謝

本模板靈感來自 **Threads 脆友 [@happy556642](https://www.threads.net/@happy556642)** 分享的 6 歲女兒畫作。孩子的畫筆，是心靈「擴容」的痕跡。

> 「不需要太多的贅述，讓她在色彩中，看見自己溫柔且堅定的力量。」

---

**Made with ❤️ by 石頭哥（[@iiStone](https://vocus.cc/user/@iiStone)）**
```

---

## 2. index.html 需要加的版權註解

在 HTML 最上方（`<!DOCTYPE html>` 下面）加一段註解：

```html
<!--
  📖 翻頁式繪本模板（Picture Book Flip Template）
  程式碼開源，歡迎自由使用與修改。
  
  ⚠️ 版權聲明：
  本模板內的示範圖片（01-cover.png 至 09-ending.png）
  著作權歸屬於 Threads 脆友 @happy556642 的 6 歲女兒所有。
  禁止複製、轉載、修改、商業使用這些圖片。
  
  請替換成您自己或您孩子的原創圖畫。
-->
```

---
