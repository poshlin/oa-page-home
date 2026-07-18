---
version: alpha
name: 橘子蘋果程式學苑 Design System
description: >
  OA 官網與 landing page 的視覺 SSOT。品牌暖橘為核心、Noto Sans TC、圓潤友善，
  傳達「給國小到高中親子家庭的溫暖 × 專業程式教育」。任何 AI agent 產生或修改任何
  UI 元件前，一律先讀本檔，並依此對齊色彩、字體、間距、圓角、陰影、動效與品牌紅線。
colors:
  # ── 品牌主色（識別核心）──
  primary: "#FFA300"          # 品牌亮橘。絕不變暗、絕不土色、絕不配白字
  primary-dark: "#E08900"     # 橘 hover（仍亮不土）
  primary-light: "#FFF3DC"    # 極淺橘底（區塊/標籤底）
  primary-ink: "#9A5A00"      # 橘語意當文字時的深橘（僅限白底小面積強調）
  # ── 品牌輔色 ──
  teal: "#00C4B3"             # 青綠：線上課程分眾色
  teal-dark: "#009E90"
  teal-light: "#E4F9F7"
  teal-ink: "#00776B"         # 青當文字/連結（過 AA）
  coral: "#FF6F61"            # 珊瑚：實體教室暖色 / 溫度感強調
  coral-dark: "#D64A3D"
  coral-light: "#FFEDEA"
  red: "#FF5859"              # 品牌紅：能量/急迫感強調（首頁、文章）
  red-light: "#FFF0F0"
  navy: "#1B2A4A"             # 深藍：沉穩區塊底
  navy-light: "#E9EEF8"
  # ── 中性色 ──
  text: "#2D2E32"             # 內文主色（深墨，白底 ~11:1）
  dark: "#12151E"             # 最深墨（大標、深底）
  gray: "#5B616D"             # 次要文字
  line: "#E6E8EC"             # 分隔線 / 淺邊框
  surface: "#FFFFFF"          # 卡片 / 面板底
  light: "#FAF9F6"            # 淺米頁面背景
  link: "#00776B"             # 連結色（青墨；務必明寫，避免瀏覽器已訪紫 #551A8B）
typography:
  # fontSize 此處放代表級（桌機）；完整響應式 clamp 見下方「Typography」散文
  display:
    fontFamily: "Noto Sans TC"
    fontSize: 76px
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: -0.02em
  h1:
    fontFamily: "Noto Sans TC"
    fontSize: 56px
    fontWeight: 800
    lineHeight: 1.15
    letterSpacing: -0.02em
  h2:
    fontFamily: "Noto Sans TC"
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: -0.01em
  h3:
    fontFamily: "Noto Sans TC"
    fontSize: 28px
    fontWeight: 700
    lineHeight: 1.3
  h4:
    fontFamily: "Noto Sans TC"
    fontSize: 20px
    fontWeight: 700
    lineHeight: 1.4
  body-lg:
    fontFamily: "Noto Sans TC"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.7
  body:
    fontFamily: "Noto Sans TC"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "Noto Sans TC"
    fontSize: 14px
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: 0.02em
  mono:
    fontFamily: "JetBrains Mono"
    fontSize: 15px
    fontWeight: 500
    lineHeight: 1.6
rounded:
  sm: 8px      # 小元件（標籤、輸入框、小圖示底）
  md: 16px     # 卡片標準圓角
  lg: 24px     # 大面板 / 特色卡
  pill: 999px  # 按鈕、膠囊、chip
spacing:
  base: 8px    # 8pt 網格基準
  s2: 8px
  s3: 12px
  s4: 16px
  s5: 24px
  s6: 32px
  s7: 48px
  s8: 64px
  s9: 96px
  s10: 128px
components:
  button-primary:            # 免費試聽（全站唯一橘實心）
    backgroundColor: "{colors.primary}"
    textColor: "{colors.text}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "16px 36px"
  button-secondary:          # LINE@ 諮詢 / 次要行動（白底外框）
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "16px 32px"
  button-online:             # 線上試聽（青實心，與橘實心成對）
    backgroundColor: "{colors.teal}"
    textColor: "{colors.text}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "16px 36px"
  chip-nav:                  # 營隊/分類導覽膠囊
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "8px 18px"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    rounded: "{rounded.md}"
    padding: "24px"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    rounded: "{rounded.sm}"
    padding: "12px 16px"
  badge:
    backgroundColor: "{colors.primary-light}"
    textColor: "{colors.text}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "4px 12px"
---

> **v0.2｜2026-07-18｜核心決策已定案**
> 方向＝A＋C（以保旭新系統為 SSOT、`oa-page-home` 當骨架；沿用全站不變量：Noto Sans TC 字型、橘/青/紅三色相、Bootstrap 斷點與 container 數值）。
> 已定案：品牌橘 `#FFA300`、內文 `#2D2E32`、按鈕膠囊 999px、標題字重 800、動效「友善彈性（過衝彈跳）」。
> 本檔為 SSOT，之後複製到各 `oa-page-*` repo 根目錄，並在 `CLAUDE.md` 掛「改 UI 前先讀 design.md」。

# 橘子蘋果程式學苑 — Design System (DESIGN.md)

## Overview（視覺主題與氛圍）

橘子蘋果是一間服務**國小到高中親子家庭**的程式教育品牌。視覺要同時說出兩件事：**溫暖親近**（讓家長與孩子放心、有陪伴感）與**專業可信**（14 年、10 萬+ 學員的教育權威）。

第一眼氛圍：**明亮、乾淨、圓潤的暖白空間**，以一抹**高飽和亮橘**作為視覺主角，青綠與珊瑚點綴出活潑，深墨文字壓住重量避免幼稚。留白充足、卡片圓角、按鈕做成友善的膠囊形。整體參照氣質接近 **Notion 的暖色極簡** 與 **Airbnb 的圓角親和**，而非科技冷冽或兒童卡通。

**品牌可辨識的關鍵特徵（Key Characteristics）**
- 亮橘 `#FFA300` 是唯一的品牌主角色，只用在最關鍵的行動與強調，不稀釋。
- 字體全站統一 **Noto Sans TC**，標題重、內文鬆（行高 1.7）。
- 圓潤語言：卡片 16px、按鈕膠囊 999px；不用硬直角（深色選手班主題除外）。
- 暖白背景 `#FAF9F6` + 純白卡片，不用冷灰。
- 程式教育的「技術感」用 **JetBrains Mono** 局部點綴（程式碼、標籤），不喧賓奪主。

> **設計哲學（寫法準則）**：規範活在**散文**裡，token 只是把可量化的值鎖死。描述風格時用**具體參照**（「像 Notion 的暖白」）勝過形容詞堆疊；用**負向約束**（「絕不把橘壓成土色」）定義品牌性格。

---

## Colors（色彩系統）

### 角色與使用時機

| 語意名 | 值 | 角色 / 使用時機 | 禁區 |
|---|---|---|---|
| **primary 亮橘** | `#FFA300` | 品牌識別核心；免費試聽主 CTA、關鍵強調、星星 | 絕不配白字、絕不 darken 成土色、不當大面積背景 |
| primary-dark | `#E08900` | 橘按鈕 hover | — |
| primary-light | `#FFF3DC` | 淺橘區塊底、badge 底 | — |
| **teal 青** | `#00C4B3` | 線上課程分眾、成功/正向狀態 | 配白字僅 2.2:1，白字要壓到 `#00706A` |
| teal-ink | `#00776B` | 青系文字、連結 | — |
| **coral 珊瑚** | `#FF6F61` | 實體教室暖色、溫度感強調 | 白字需大而粗才勉強過 |
| **red 紅** | `#FF5859` | 能量/急迫感強調（首頁、文章 header） | 白字僅 3.08:1，只准大而粗（≥18.66px bold） |
| **text 深墨** | `#2D2E32` | 內文主色、彩色底上的文字 | — |
| dark | `#12151E` | 大標、深色區塊底 | — |
| gray | `#5B616D` | 次要說明文字 | 不當正文主色 |
| line | `#E6E8EC` | 分隔線、淺邊框 | — |
| surface / light | `#FFFFFF` / `#FAF9F6` | 卡片底 / 頁面暖白底 | 不用冷灰當底 |
| link | `#00776B` | 連結；**務必明寫 color** | 不留預設 → 會漏出瀏覽器已訪紫 `#551A8B` |

### 分眾用色（zone accents）— OA 專屬規則
色彩用來標示**課程分眾**，但**不覆蓋** CTA 意圖系統（見 Components）：
- **實體教室** → 傾向 **亮橘 / 珊瑚** 暖色調
- **線上課程** → 傾向 **青綠**
- **能量/招生活動（首頁、文章）** → 可用 **紅** 提升急迫感
- 分區色塊（如縣市卡）用**柔和彩色底 + 深墨字**：北 `#FBE6C2`／中 `#CFEEE2`／南 `#FADBD1`（對應地圖橘/青/珊瑚），皆配 `#2D2E32`（~11:1），有質感又穩過 AA。純灰素色會顯廉價、禁用。

### WCAG 對比實測基準（已線上校準）
- 亮橘 `#FFA300` + 深墨 `#2D2E32` = **6.77:1 ✅**（過 AA）→ 橘鈕標準配法
- 紅 `#FF5859` + 白 = 3.08:1（只過大粗字 3:1 門檻，一般字不過）
- 青 `#00C4B3` + 白 = 2.2:1 ❌（青鈕改配深墨字，或壓深底到 `#00706A`）
- 深墨 `#2D2E32` + 白底 = ~11:1 ✅

> ⚠️ **原版官網 legacy 提醒**：live Rails 官網目前是 `#ffa400`（肉眼同色）+ 內文 `#4d4d4d` + 橘底白字（~1.9 不過），屬**待遷移舊版**，非本系統標準。

---

## Typography（字體排印）

- **字型**：`'Noto Sans TC', -apple-system, BlinkMacSystemFont, 'PingFang TC', 'Microsoft JhengHei', sans-serif`。載入字重 **400 / 500 / 700 / 800**。
- **等寬點綴**：`'JetBrains Mono', 'SF Mono', Consolas, monospace`，僅用於程式碼、技術標籤、數據標號。
- **root font-size = 18px**（沿用官網，全站 rem 以 18px 計；內文 body ≈ 18px）。
- **行高**：內文一律 **1.7**（呼吸感是品牌溫度來源）；標題 1.1–1.4。
- 標題用 `clamp()` 響應式；字重最重 **800**（不用 900）。

### 完整字級階梯（響應式）

| 角色 | font-size | weight | line-height | letter-spacing | 用途 |
|---|---|---|---|---|---|
| **display** | `clamp(46px, 5vw, 76px)` | 800 | 1.1 | -0.02em | 首頁 hero 主標 |
| **h1** | `clamp(34px, 4.5vw, 56px)` | 800 | 1.15 | -0.02em | 頁面主標 |
| **h2** | `clamp(28px, 3.5vw, 40px)` | 700 | 1.2 | -0.01em | 區塊標題 |
| **h3** | `clamp(22px, 2.5vw, 28px)` | 700 | 1.3 | — | 子標題 |
| **h4** | `20px` | 700 | 1.4 | — | 卡片標題 |
| **body-lg** | `18px` | 400 | 1.7 | — | 正文（預設） |
| **body** | `16px` | 400 | 1.7 | — | 次要正文 |
| **label** | `14px` | 500 | 1.5 | 0.02em | 按鈕、標籤 |
| **caption** | `13px` | 500 | 1.4 | 0.02em | 註解、小字 |

> **已定案（字重 800）**：原版官網標題字重是 500、新系統定 800（較重、較有力）。新 nav+footer 上架後統一到 800；在那之前，你的頁面與仍是原版的 nav/footer 之間標題重量會有暫時落差（過渡期可接受）。

---

## Layout（間距與版面）

- **8pt 網格**：所有間距用 8 的倍數 token（`--s2`=8 … `--s10`=128）。small gaps 用 s2/s3，元件內距 s4/s5，區塊間距 s7/s8，大段落 s9/s10。
- **Section 垂直間距**：桌機 `clamp(64px, 10vh, 128px)` 上下；手機收到 48–64px。
- **Container**（沿用 Bootstrap 尺標，讓 nav/footer 包版一致）：`sm 540 / md 720 / lg 960 / xl 1140 / xxl 1320`；**內容主容器 max-width 1140px**，左右 padding 24px（手機 16–20px）。
- 留白哲學：**寧鬆勿擠**，卡片之間至少 s5(24px)，區塊呼吸靠 s8+。

---

## Elevation & Depth（層級與陰影）

用 3 階中性陰影 + 1 個 CTA 專用光暈，全部走 token（色調帶極淡藍墨 `rgba(18,21,30,…)`，比純黑柔和）：

| token | 值 | 用途 |
|---|---|---|
| `--e1` | `0 2px 8px rgba(18,21,30,0.06)` | 靜置卡片、輸入框 |
| `--e2` | `0 8px 24px rgba(18,21,30,0.08)` | hover 抬升、彈窗 |
| `--e3` | `0 16px 44px rgba(18,21,30,0.11)` | 浮動面板、重點卡 |
| `--e-cta` | `0 8px 24px rgba(255,163,0,0.32)` | 橘色主 CTA 專用暖光暈 |

規則：**同一層級用同一階陰影**，不要每個卡片自訂一次性 box-shadow（about / ai-thinking 舊做法要收斂）。

---

## Shapes（形狀 / 圓角）

| token | 值 | 用途 |
|---|---|---|
| `--r-sm` | 8px | 輸入框、小標籤、圖示底 |
| `--r-md` | 16px | **卡片標準** |
| `--r-lg` | 24px | 大面板、特色卡 |
| `--r-pill` | 999px | 按鈕、膠囊、chip、頭像 |

規則：**同一畫面不混圓角與直角**。卡片一律 16px，按鈕一律膠囊。不要出現 12/14/18/20/22/28px 各做各的（ai-thinking 舊做法要收斂到這 4 階）。

---

## Components（元件樣式）

### CTA 意圖系統（全站紅線 — 最重要的一致性規則）
同頁「同意圖」的按鈕**必須**用同一種樣式；橘實心是最稀有的資源，只給免費試聽。

| 意圖 | 樣式 | 說明 |
|---|---|---|
| **免費試聽（主 CTA）** | **亮橘實心 + 深墨字 + 膠囊** | 全站唯一橘實心；`button-primary` |
| **免費試聽（坐在橘色滿版區塊上）** | **白底 + 深墨字 + 膠囊（反轉款）** | 正式例外（2026-07-18 保旭拍板）：橘實心放橘底會隱形；ai-thinking 的 `.btn-trust-cta`/`.btn-footer` 為範本 |
| 線上 vs 實體試聽並列 | 實體＝橘實心、線上＝青實心（對稱、皆深墨字） | 見 `button-online`；兩顆等高對稱、不一實心一外框 |
| LINE@ 諮詢 | 白底 + 深墨字 + 深墨外框（膠囊） | `button-secondary` |
| 區塊主行動（如看營隊） | 白底膠囊鈕 | — |
| 導覽 / 次要跳轉 | 文字連結（帶 →） | 不做成實心鈕 |
| 展開 / 篩選 | 白底膠囊 chip | `chip-nav` |

### 按鈕狀態與鐵則
- **實心鈕務必 `border: 2px solid transparent`**（否則 `<button>` 會漏出瀏覽器預設灰黑框；順便與外框鈕等高對齊）。填色鈕的邊框只能透明或同底色，**絕不掛對比色外框**。
- **連結型 `<a>` 按鈕務必明寫 `color`**（避免已訪紫）。
- hover：橘鈕底色轉 `--orange-dark #E08900`、微幅上浮（`translateY(-2px)` + 陰影升一階）。
- 主 CTA 帶 `--e-cta` 暖光暈；hover 光暈加強。

### data-oa-cta 埋碼規則
- **只加在「免費試聽 modal 的 `<button>`」**，值為位置短代號：`hero` / `middle` / `bottom` / `sticky` 等。
- 錨點、縣市卡、撥號連結、營隊 chip、一般 `<a>` 導覽 **一律不加**。

### 其他元件
- **card**：白底、`--r-md` 16px、`--e1` 陰影、內距 24–32px；hover 升 `--e2`。
- **input-field**：白底、`--r-sm` 8px、`--line` 邊框、focus 換橘/青焦點環。
- **badge / chip**：膠囊、`primary-light` 底 + 深墨字。

---

## Interaction & Motion（互動與動效）

品牌動效個性＝**友善、有彈性**（呼應親子教育的活潑），但不誇張。以 kinetics 彈簧物理值定 token：

| token | 值 | 用途 |
|---|---|---|
| `--ease-spring` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | 主互動：按鈕、卡片、chip 的按下/彈回（輕微過衝） |
| `--ease-out` | `cubic-bezier(0.16, 1, 0.3, 1)` | 內容進場、區塊揭示（滑順沉降） |
| `--dur-fast` | `120ms` | hover / 小互動 |
| `--dur-base` | `180ms` | 標準轉場（按鈕、卡片） |
| `--dur-slow` | `400ms` | 進場、展開、大轉場 |

規則：全站只用這 2 條曲線 + 3 個時長，不要各頁各自 cubic-bezier。務必尊重 `prefers-reduced-motion`（關閉過衝與位移）。

> **已定案（友善彈性）**：主互動用 `--ease-spring` 輕微過衝彈跳（貼親子調性）；內容進場用 `--ease-out` 滑順。選手班深色主題維持自己的滑順風格。

---

## Do's and Don'ts（可做 / 不可做）

**✅ Do**
- 亮橘只給最關鍵動作；一個畫面主 CTA 只有一種橘實心。
- 彩色底一律配深墨字 `#2D2E32`。
- 卡片 16px、按鈕膠囊；同畫面圓角一致。
- 陰影、圓角、間距、動效一律用 token，不寫一次性值。
- 品牌數字（學員數、教室數、師生比）一律引自知識庫 SSOT。

**🚫 Don't**
- ❌ 亮橘配白字；❌ 把橘 darken 成土色（`#C47A00`/`#B85C00` 等一律禁用）。
- ❌ 用 AI 生成 logo；image prompt 不描述 logo 結構。
- ❌ 「免費再上一次」出現在任何文案（非真實政策）。
- ❌ 一個畫面混多種按鈕圓角 / 多種橘色深淺當主色。
- ❌ 實心 `<button>` 不寫 border（會漏灰黑框）。
- ❌ 主 CTA 用紅色搶橘色的位子（ai-thinking 舊做法要修）。
- ❌ 彰化、花蓮寫成有實體教室；❌ 自稱純「兒童程式」（已服務到高中）。

---

## Responsive Behavior（響應式）

- **斷點**（沿用 Bootstrap 5，讓 nav/footer 包版一致）：`576 / 768 / 992 / 1200 / 1400`（min-width）。手機主斷點 **768**。
- **觸控目標** ≥ **44×44px**（WCAG）。
- 收合策略：多欄 → 單欄堆疊；hero 字級靠 clamp 自動縮；sticky 試聽鈕在手機固定底部。
- 圖片 `max-width:100%`、lazy load。

---

## Agent Prompt Guide（給 AI 的使用指南）

**啟用**：在專案 `CLAUDE.md` 加一句：
> 本專案的設計系統定義在根目錄的 `design.md`，產生或修改任何 UI 元件前一律先讀它，並嚴格對齊其色彩、字體、間距、圓角、陰影、動效與 Do's/Don'ts。

**快速色票**：主橘 `#FFA300`（配 `#2D2E32`）｜青 `#00C4B3`｜珊瑚 `#FF6F61`｜紅 `#FF5859`｜內文 `#2D2E32`｜底 `#FAF9F6`。
**快速規則**：Noto Sans TC｜行高 1.7｜卡片 16px｜按鈕膠囊 999px + 深墨字 + `border:2px solid transparent`｜8pt 間距｜免費試聽才用橘實心。

**產生元件時的自檢**：① 顏色有沒有過 AA（彩色底→深墨字）② 圓角/陰影/間距有沒有用 token ③ 是不是誤用橘實心/白字配橘 ④ data-oa-cta 有沒有亂加 ⑤ 動效是不是只用那 2 曲線。

---

## Known Gaps & Themed Variants（已知缺口與主題分支）

- **選手班（contestant）＝刻意的深色奇幻主題分支**：白字、JetBrains Mono 大寫、硬直角、glow 陰影——**允許保留為特例**，但主色仍用品牌橘、CTA 語意仍遵守本系統。
- **✅ ai-thinking 已拉齊（2026-07-18 試點頁）**：文字色 #2D2E32、CTA 紅→橘膠囊、圓角 4 階、陰影/動效 token 化、字重 800、橘底白字 49→0（兩輪獨立驗證）。
- **仍待收斂的舊頁**：about（無陰影 token、藥丸 50px→999px、orange-dark #E69200→#E08900、刪 --orange-deep #C47A00 土色變數）、classroom＋faq（按鈕 12px→膠囊、orange-dark #e8920a→#E08900）、home（--text #2A2D35→#2D2E32、孤兒 font-weight:900）。
- **ai-thinking 文案層待辦（非視覺）**：全頁 15+ 處「ChatGPT、Midjourney」具名工具（含 Course schema、FAQ、內文），與課程文案紅線「AI 思維課不列具體工具名」相抵觸，待保旭拍板改寫方向。
- **✅ faq 紅線已修（2026-07-18，commit `45db87b`）**：btn-primary(+hover)、分類 chip 選中態、tldr-eyebrow、搜尋清除鈕 hover 共 4 處橘底白字改深墨字，已推 OrangeApple-Lab/oa-page-faq。
- 核心決策（按鈕膠囊 999px、字重 800、動效彈性）已於 2026-07-18 定案。
- **原版 Rails 官網**（nav/footer/課程頁等）仍是 `#ffa400`/`#4d4d4d`/Bootstrap，屬 legacy，之後由數位長逐步遷移對齊本系統。
