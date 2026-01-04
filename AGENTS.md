# AGENTS.md - AI 代理工作指南

## 專案概覽

**專案名稱**: Blackjack 21點介紹網站  
**專案類型**: 純前端靜態網站  
**目標**: 將現有的焊接服務網站樣板改造為21點（Blackjack）遊戲介紹網站

### 專案狀態
- **當前狀態**: 基於 WELDORK 焊接網站樣板
- **目標狀態**: 21點遊戲介紹與規則說明網站
- **技術棧**: HTML, CSS, JavaScript, Bootstrap 5

### 核心技術
- **前端框架**: Bootstrap 5.x
- **樣式**: CSS (已包含在 `css/` 目錄)
- **JavaScript**: Vanilla JS + 第三方庫 (Owl Carousel, WOW.js 等)
- **字體圖標**: Font Awesome 5.10.0, Bootstrap Icons
- **Google Fonts**: Poppins, Roboto

---

## 目錄結構

```
blackjack-intro-web/
├── css/                    # 樣式表目錄
│   ├── bootstrap.min.css   # Bootstrap 5 核心樣式
│   └── style.css           # 自訂樣式
├── js/                     # JavaScript 目錄
│   └── main.js             # 主要 JavaScript 檔案
├── lib/                    # 第三方函式庫
│   ├── animate/            # Animate.css 動畫庫
│   ├── owlcarousel/        # Owl Carousel 輪播庫
│   └── ...                 # 其他函式庫
├── img/                    # 圖片資源目錄
├── scss/                   # SCSS 原始碼 (如需客製化樣式)
├── index.html              # 首頁 - 主要內容頁
├── about.html              # 關於頁面
├── service.html            # 服務頁面 (將改為規則說明)
├── feature.html            # 特色頁面
├── team.html               # 團隊頁面
├── testimonial.html        # 見證頁面
├── contact.html            # 聯絡頁面
├── 404.html                # 404 錯誤頁面
├── AGENTS.md               # 本文件 - AI 代理工作指南
└── README.md               # (待建立) 專案說明文件
```

---

## 設置與運行指令

### 環境需求
- **瀏覽器**: 現代瀏覽器 (Chrome, Firefox, Edge, Safari)
- **本地伺服器** (可選): 用於測試，可使用以下任一方式

### 本地開發伺服器運行方式

#### 方法 1: 使用 Python HTTP Server
```powershell
# Python 3.x
cd d:\Project\Web\blackjack-intro-web
python -m http.server 8000

# 開啟瀏覽器訪問: http://localhost:8000
```

#### 方法 2: 使用 Node.js http-server
```powershell
# 需先安裝 http-server: npm install -g http-server
cd d:\Project\Web\blackjack-intro-web
http-server -p 8000

# 開啟瀏覽器訪問: http://localhost:8000
```

#### 方法 3: 使用 PHP 內建伺服器
```powershell
cd d:\Project\Web\blackjack-intro-web
php -S localhost:8000

# 開啟瀏覽器訪問: http://localhost:8000
```

#### 方法 4: 直接開啟檔案
```powershell
# 直接在瀏覽器中開啟
start index.html
```

### 生產環境部署
由於這是純前端靜態網站，可直接部署到以下平台：
- **GitHub Pages**: 將專案推送到 GitHub 並啟用 Pages
- **Netlify / Vercel**: 拖放部署或 Git 整合
- **任何靜態網站託管服務**

部署指令範例（GitHub Pages）:
```powershell
# 確保專案在 Git 倉庫中
git init
git add .
git commit -m "Initial commit: Blackjack intro website"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main

# 在 GitHub repository settings 中啟用 GitHub Pages
```

---

## 開發工作流程

### 改造步驟規劃

1. **內容規劃階段**
   - 定義21點遊戲介紹網站的核心內容區塊
   - 規劃頁面結構：
     - 首頁：21點遊戲簡介、精美輪播
     - 遊戲規則：基本規則、進階策略
     - 術語解釋：21點專業術語
     - 歷史與文化：21點的起源與發展
     - 策略指南：基本策略表、計牌法簡介（教育目的）

2. **視覺設計階段**
   - 更換主題色彩：從工業風格改為賭場/撲克牌風格
   - 準備21點相關圖片素材
   - 設計響應式佈局

3. **內容替換階段**
   - 替換 HTML 文字內容
   - 更新圖片資源
   - 調整導航結構

4. **樣式客製化階段**
   - 修改 `css/style.css` 以符合21點主題
   - 調整色彩方案（建議：黑、紅、綠賭桌色系）
   - 優化字體與排版

5. **測試與優化階段**
   - 跨瀏覽器測試
   - 響應式設計測試（手機、平板、桌面）
   - 性能優化
   - SEO 優化

### 核心修改檔案
- `index.html` - 主頁面，需完全改寫內容
- `css/style.css` - 主要樣式表，需調整主題色
- `img/` - 替換所有圖片為21點相關圖片
- 各個子頁面 HTML 檔案

---

## 編碼規範與約定

### HTML 規範
- 使用 HTML5 語義化標籤
- 保持 Bootstrap 5 類別命名一致性
- 所有交互元素必須有唯一的 `id` 屬性（便於測試）
- 圖片必須包含 `alt` 屬性（無障礙與 SEO）

### CSS 規範
- 使用 Bootstrap 5 的 utility classes 優先
- 自訂樣式寫在 `css/style.css`
- 遵循 BEM 命名規範（如需新增組件）
- 保持響應式設計（mobile-first）

### JavaScript 規範
- 使用 ES6+ 語法
- 避免使用全域變數
- 註解清晰說明功能邏輯
- 保持程式碼模組化

### 命名約定
- **檔案名稱**: 小寫字母，使用連字符 (kebab-case)
  - ✅ `game-rules.html`
  - ❌ `gameRules.html`, `GameRules.html`
  
- **CSS 類別**: Bootstrap 風格或 BEM
  - Bootstrap: `.btn-primary`, `.card-body`
  - BEM: `.blackjack-card__suit--red`

- **JavaScript 變數**: camelCase
  - ✅ `playerHand`, `dealerScore`
  - ❌ `player_hand`, `PlayerHand`

### 圖片規範
- 格式：JPG (照片), PNG (透明背景), SVG (圖標)
- 命名：描述性，使用連字符
  - ✅ `blackjack-table.jpg`, `card-ace-spades.png`
- 優化：壓縮後再使用，建議使用 TinyPNG 或類似工具
- 尺寸：根據使用位置準備適當尺寸，避免過大

### Bootstrap 5 響應式斷點

Bootstrap 5 採用 **mobile-first** 設計理念，以下是三個最常見的響應式斷點：

#### 1. **手機裝置 (Extra Small & Small)**
- **斷點範圍**: `< 768px`
- **適用裝置**: 手機（直向與橫向）
- **Bootstrap 前綴**: 
  - `xs` (< 576px) - 無需前綴，這是預設值
  - `sm` (≥ 576px) - 使用 `-sm-` 前綴

**使用範例**:
```html
<!-- 在手機上佔滿全寬（12欄），sm 以上佔 6 欄 -->
<div class="col-12 col-sm-6">內容區塊</div>

<!-- 在 xs 時隱藏，sm 以上顯示 -->
<div class="d-none d-sm-block">在手機上隱藏</div>
```

#### 2. **平板裝置 (Medium)**
- **斷點範圍**: `768px - 991px`
- **適用裝置**: 平板電腦（iPad、Android 平板等）
- **Bootstrap 前綴**: `-md-`

**使用範例**:
```html
<!-- 手機全寬、平板佔 6 欄、桌面佔 4 欄 -->
<div class="col-12 col-md-6 col-lg-4">響應式卡片</div>

<!-- 在 md 以上置中對齊 -->
<div class="text-start text-md-center">文字內容</div>

<!-- 平板以上改變排列方向 -->
<div class="flex-column flex-md-row d-flex">
  <div>項目1</div>
  <div>項目2</div>
</div>
```

#### 3. **桌面裝置 (Large & Extra Large)**
- **斷點範圍**: `≥ 992px`
- **適用裝置**: 桌上型電腦、筆記型電腦
- **Bootstrap 前綴**: 
  - `lg` (≥ 992px) - 使用 `-lg-` 前綴
  - `xl` (≥ 1200px) - 使用 `-xl-` 前綴
  - `xxl` (≥ 1400px) - 使用 `-xxl-` 前綴

**使用範例**:
```html
<!-- 桌面顯示 4 欄佈局 -->
<div class="row">
  <div class="col-12 col-md-6 col-lg-3">卡片 1</div>
  <div class="col-12 col-md-6 col-lg-3">卡片 2</div>
  <div class="col-12 col-md-6 col-lg-3">卡片 3</div>
  <div class="col-12 col-md-6 col-lg-3">卡片 4</div>
</div>

<!-- 只在桌面顯示側邊欄 -->
<div class="d-none d-lg-block">側邊導航</div>
```

#### Bootstrap 5 斷點完整對照表

| 斷點名稱 | Class 前綴 | 最小寬度 | 常見裝置 | 容器最大寬度 |
|---------|-----------|---------|---------|------------|
| Extra small | (無) | < 576px | 手機（直向） | 100% |
| Small | `sm` | ≥ 576px | 手機（橫向） | 540px |
| Medium | `md` | ≥ 768px | 平板 | 720px |
| Large | `lg` | ≥ 992px | 桌面 | 960px |
| Extra large | `xl` | ≥ 1200px | 大桌面 | 1140px |
| Extra extra large | `xxl` | ≥ 1400px | 超大桌面 | 1320px |

#### 實用技巧

1. **優先使用三個主要斷點**（xs/sm、md、lg）可滿足大部分需求
2. **採用 mobile-first 思維**：先設計手機版，再逐步優化大螢幕
3. **常用響應式 utility classes**：
   - 顯示/隱藏：`d-{breakpoint}-{value}` (如 `d-none`, `d-md-block`)
   - 文字對齊：`text-{breakpoint}-{alignment}` (如 `text-center`, `text-lg-start`)
   - Flexbox：`flex-{breakpoint}-{direction}` (如 `flex-row`, `flex-md-column`)
   - 間距：`m{side}-{breakpoint}-{size}` (如 `mb-3`, `mt-md-5`)

4. **測試建議**：使用瀏覽器開發者工具的 Responsive Design Mode 測試各斷點顯示效果

---

## SEO 最佳實踐

每個頁面都應包含：

1. **標題標籤** (`<title>`)
   ```html
   <title>21點遊戲規則完整指南 | Blackjack 介紹網站</title>
   ```

2. **Meta 描述** (`<meta name="description">`)
   ```html
   <meta name="description" content="完整的21點遊戲規則介紹，包含基本規則、進階策略、術語解釋，適合新手與進階玩家。">
   ```

3. **Meta 關鍵字** (可選)
   ```html
   <meta name="keywords" content="21點, Blackjack, 遊戲規則, 賭場遊戲, 撲克牌">
   ```

4. **Open Graph 標籤** (社交媒體分享)
   ```html
   <meta property="og:title" content="21點遊戲完整指南">
   <meta property="og:description" content="學習21點遊戲的所有規則與策略">
   <meta property="og:image" content="https://your-domain.com/img/og-image.jpg">
   ```

5. **結構化標題**
   - 每頁僅一個 `<h1>`
   - 使用階層式標題 `<h2>`, `<h3>` 等

---

## 安全性與最佳實踐

### 資料處理
- **無後端**: 本專案為純前端，不處理敏感資料
- **表單**: 如有聯絡表單，使用第三方服務（如 Formspree, Netlify Forms）
- **外部連結**: 使用 `rel="noopener noreferrer"` 屬性

### 依賴管理
- **Bootstrap 5**: 使用 CDN 或本地版本
- **第三方庫**: 
  - 優先使用知名、維護良好的庫
  - 定期檢查安全更新
  - 當前使用的庫：
    - Owl Carousel 2.x
    - WOW.js (動畫)
    - Font Awesome 5.10.0

### 性能優化
- 壓縮 CSS/JS 檔案
- 圖片延遲載入 (lazy loading)
- 使用 CDN 加速資源載入
- 啟用瀏覽器快取

---

## 內容建議與主題規劃

### 建議頁面結構

#### 1. **首頁 (index.html)**
- Hero 輪播：展示21點精美視覺
- 遊戲簡介：什麼是21點
- 核心特色：為什麼受歡迎
- 快速連結：規則、策略、歷史

#### 2. **遊戲規則 (rules.html)** [改造自 service.html]
- 基本規則
- 牌值計算
- 遊戲流程
- 特殊情況（Blackjack, Bust, Insurance 等）

#### 3. **策略指南 (strategy.html)** [改造自 feature.html]
- 基本策略表
- 進階技巧
- 常見錯誤

#### 4. **術語表 (terms.html)** [改造自 about.html]
- Hit, Stand, Double Down 等術語解釋
- 中英對照

#### 5. **歷史文化 (history.html)** [改造自 team.html]
- 21點的起源
- 發展歷程
- 文化影響

#### 6. **聯絡我們 (contact.html)**
- 保留原有結構
- 調整為問題反饋或建議表單

### 色彩方案建議
```css
/* 賭場風格配色 */
:root {
    --primary-green: #0d5e2a;      /* 賭桌綠 */
    --card-red: #d32f2f;           /* 紅心/方塊 */
    --card-black: #1a1a1a;         /* 黑桃/梅花 */
    --gold-accent: #ffd700;        /* 金色點綴 */
    --bg-felt: #1b5e20;            /* 絨布質感背景 */
}
```

---

## 常見問題與解決方案

### Q: 如何快速預覽修改？
A: 使用本地開發伺服器（參見「設置與運行指令」章節），搭配瀏覽器的開發者工具即時除錯。

### Q: 圖片素材從哪裡獲取？
A: 
- 免費圖庫：Unsplash, Pexels, Pixabay
- AI 生成：可使用 AI 工具生成21點相關圖片
- 自行設計：使用 Figma, Canva 等設計工具

### Q: 如何保持響應式設計？
A: Bootstrap 5 已內建響應式網格系統，使用 `.col-*` 類別即可。測試時使用瀏覽器開發者工具的裝置模擬功能。

### Q: 需要編譯 SCSS 嗎？
A: 如果只修改現有的 `css/style.css`，不需要。如果要從 `scss/` 目錄重新編譯：
```powershell
# 需安裝 sass
npm install -g sass

# 編譯指令
sass scss/style.scss css/style.css --watch
```

---

## 版本控制建議

### Git 工作流程
```powershell
# 初始化專案 (如尚未初始化)
git init

# 建立 .gitignore
echo "node_modules/`n.DS_Store`nThumbs.db" > .gitignore

# 提交變更
git add .
git commit -m "feat: 改造首頁為21點主題"

# 推送到遠端
git push origin main
```

### 提交訊息規範
使用語義化提交訊息：
- `feat:` 新功能
- `fix:` 修復問題
- `docs:` 文件更新
- `style:` 樣式調整
- `refactor:` 重構程式碼

範例：
```
feat: 新增21點基本規則頁面
fix: 修正首頁輪播圖響應式問題
style: 調整賭桌綠色主題配色
docs: 更新 AGENTS.md 開發指南
```

---

## 測試檢查清單

在完成開發後，確保通過以下檢查：

### 功能測試
- [ ] 所有頁面連結正常運作
- [ ] 導航選單在各裝置上正常顯示
- [ ] 輪播圖自動播放與手動切換正常
- [ ] 表單（如有）提交功能正常
- [ ] 所有圖片正常載入

### 響應式測試
- [ ] 手機畫面 (< 576px)
- [ ] 平板畫面 (576px - 992px)
- [ ] 桌面畫面 (> 992px)
- [ ] 橫向/直向模式切換

### 瀏覽器相容性
- [ ] Chrome
- [ ] Firefox
- [ ] Safari
- [ ] Edge

### SEO 檢查
- [ ] 每頁都有獨特的 `<title>`
- [ ] 每頁都有 meta description
- [ ] 圖片都有 alt 屬性
- [ ] 標題階層正確 (H1 → H2 → H3)

### 效能檢查
- [ ] 圖片已壓縮優化
- [ ] CSS/JS 檔案已最小化（生產環境）
- [ ] 首頁載入時間 < 3 秒

---

## 擴展建議

未來可考慮的功能擴展：

1. **互動式規則演示**
   - 使用 JavaScript 實作簡單的21點遊戲演示
   - 讓訪客可以體驗基本流程

2. **策略計算器**
   - 根據當前手牌給出建議動作的工具

3. **多語言支援**
   - 英文/繁體中文切換

4. **深色模式**
   - 適合長時間閱讀

5. **文章/部落格功能**
   - 定期更新21點相關文章與技巧

---

## 聯絡資訊與貢獻

### 專案維護者
- 請在此填寫專案負責人資訊

### 貢獻指南
如需為專案貢獻：
1. Fork 專案倉庫
2. 建立功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交變更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

---

## 授權資訊

**原始樣板**: WELDORK - Welding Website Template  
**樣板作者**: HTML Codex  
**樣板授權**: 請參閱 LICENSE.txt  
**樣板來源**: https://htmlcodex.com/welding-website-template

**改造專案**: Blackjack 21點介紹網站  
**改造目的**: 教育與資訊分享  

---

## 更新記錄

### 2026-01-05
- ✅ 移除所有頁面的 Newsletter 訂閱區塊
  - 清理了 index.html, about.html, service.html, feature.html, appoinment.html, team.html, testimonial.html, contact.html, 404.html 共 9 個頁面

### 2026-01-03
- ✅ 建立 AGENTS.md 文件
- ✅ 定義專案目標與技術棧
- ✅ 規劃開發工作流程與規範

### 待辦事項
- [ ] 規劃並設計21點主題視覺風格
- [ ] 準備圖片素材
- [ ] 改造首頁內容
- [ ] 建立遊戲規則頁面
- [ ] 建立策略指南頁面
- [ ] 撰寫使用者友善的 README.md

---

**本文件最後更新**: 2026-01-03  
**文件版本**: 1.0.0
