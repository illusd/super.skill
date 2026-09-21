# Super Skill — Animation / Design Engineering / Typography / Libraries

> The most complete motion & design-engineering skill for AI coding agents.  
> Unifies Emil Kowalski philosophy, Apple Fluid Interfaces, 50+ animation libraries, production recipes, typography, and component recommendations.

---

## 中文版 (zh-TW)

### 這是什麼？

`super` 是一個「超級動畫與設計工程技能」。它把以下內容完整整合成單一 skill：

- **Emil Kowalski 完整哲學**：Build / Review / Find / Improve / Vocabulary / Recipes / Pick UI Library / Prototype
- **Apple Designing Fluid Interfaces**（轉譯到 Web）
- **50+ 主流動畫庫**（GSAP、Motion、Three.js、Lottie、Lenis、Locomotive Scroll、Matter.js、p5.js、Swiper…）
- **生產級 Recipes**（Button、Popover、Modal、Toast、Drawer、Stagger、Hold-to-confirm、Drag-to-dismiss…）
- **當代免費字體系統**（Geist、Inter、Satoshi 等）
- **嚴格的 Review 與審計流程**

### 檔案結構

```
super/
├── SKILL.md                          # 主技能（決策邏輯 + 所有模式）
└── references/
    ├── animation-libraries.md        # 50+ 動畫庫完整地圖 + 決策啟發式
    ├── animation-recipes.md          # 生產級動畫配方
    ├── animation-vocabulary.md       # 動畫術語反查表
    ├── pick-ui-library.md            # 元件庫意見導向推薦
    └── typography.md                 # 字體與光學規則
```

### 支援的模式

| 模式 | 觸發範例 |
|------|----------|
| **Build** | 「幫我做一個 drawer 進場動畫」 |
| **Review** | 「review 這段動畫 code」 |
| **Find** | 「這個介面哪些地方該加動畫？」 |
| **Improve** | 「審計整個專案的動畫」 |
| **Vocabulary** | 「彈跳出來的感覺叫什麼？」 |
| **Typography** | 「推薦一組 dashboard 字體」 |
| **Libraries** | 「該用 GSAP 還是 Motion？」 |
| **Pick Library** | 「推薦一個 toast 元件庫」 |
| **Prototype** | 「做出三種不同風格的 pricing card」 |

### 安裝

把整個 `super` 資料夾放到你的 agent skills 目錄即可（例如 `.grok/skills/super` 或 `.claude/skills/super`）。

### 核心理念

1. **克制優先** — 最好的動畫常常是「不要動畫」
2. **頻率閘門** — 高頻操作永不動畫
3. **最便宜工具** — CSS → WAAPI → Motion → GSAP → 專用庫
4. **看不見的細節會累積** — origin、easing、tracking、optical size
5. **Taste is trained** — 品味是訓練出來的

---

## English Version (en-US)

### What is this?

`super` is a comprehensive **animation + design-engineering skill** for AI coding agents. It unifies:

- **Full Emil Kowalski philosophy**: Build / Review / Find / Improve / Vocabulary / Recipes / Pick UI Library / Prototype
- **Apple’s Designing Fluid Interfaces** (translated to the web)
- **50+ production animation libraries** (GSAP, Motion, Three.js, Lottie, Lenis, Locomotive Scroll, Matter.js, p5.js, Swiper, and more)
- **Production-ready recipes** (Button, Popover, Modal, Toast, Drawer, Stagger, Hold-to-confirm, Drag-to-dismiss…)
- **Contemporary free typography system** (Geist, Inter, Satoshi…)
- **Strict review and audit workflows**

### File Structure

```
super/
├── SKILL.md                          # Main skill (decision logic + all modes)
└── references/
    ├── animation-libraries.md        # 50+ libraries map + decision heuristics
    ├── animation-recipes.md          # Production animation recipes
    ├── animation-vocabulary.md       # Motion vocabulary reverse-lookup
    ├── pick-ui-library.md            # Opinionated component library recommendations
    └── typography.md                 # Font system + optical rules
```

### Supported Modes

| Mode | Example triggers |
|------|------------------|
| **Build** | “Make a drawer entrance animation” |
| **Review** | “Review this animation code” |
| **Find** | “Where should this interface animate?” |
| **Improve** | “Audit all motion in the codebase” |
| **Vocabulary** | “What’s the name of that bouncy pop-in?” |
| **Typography** | “Recommend fonts for a dashboard” |
| **Libraries** | “Should I use GSAP or Motion?” |
| **Pick Library** | “Recommend a toast component library” |
| **Prototype** | “Show me three different pricing card directions” |

### Installation

Place the entire `super` folder into your agent’s skills directory (e.g. `.grok/skills/super` or `.claude/skills/super`).

### Core Principles

1. **Restraint first** — the best animation is often no animation
2. **Frequency gate** — never animate high-frequency / keyboard actions
3. **Cheapest tool that works** — CSS → WAAPI → Motion → GSAP → specialists
4. **Invisible details compound** — origin, easing, tracking, optical size
5. **Taste is trained** — not innate

---

## Credits

- Emil Kowalski — animation philosophy, recipes, review standards
- Apple — Designing Fluid Interfaces (WWDC)
- Community — GSAP, Motion, Three.js, Lottie, Lenis, and the broader open-source motion ecosystem
- Typography — Geist (Vercel), Inter, Satoshi, and other contemporary free faces

---

**License**: Use freely. Keep the craft bar high.
