# Options Mastery

A comprehensive, mathematical, and intuitive guide to derivatives pricing, hedging mechanics, and the Greeks.  
Built for **S&T and Options Traders** preparing for sell-side interviews or deepening their quantitative finance knowledge.

---

## Overview

**Options Mastery** is a self-contained static website composed of 10 interactive modules covering the full lifecycle of derivatives theory — from forwards & futures basics through to advanced second-order Greeks. Every module features:

- **Rich mathematical exposition** rendered with KaTeX
- **Interactive calculators & simulators** (Black-Scholes pricing, Greeks sensitivities, P&L simulators)
- **Real-time Canvas charts** with hover-tracking, crosshair guides, and dynamic tooltips
- **Tabbed navigation** within each module for progressive learning

---

## Modules

| #  | File | Topic | Highlights |
|----|------|-------|------------|
| 01 | `01_Forwards_Futures.html` | Forwards & Futures | No-arbitrage pricing, spot-forward parity, contango vs backwardation, futures margins |
| 02 | `02_Option_Fundamentals.html` | Option Fundamentals | Payoff structures, Black-Scholes intuition, intrinsic vs time value, put-call parity |
| 03 | `03_All_About_Volatility.html` | All About Volatility | Realized vs implied vol, volatility surface, skew, curvature, vol risk premium |
| 04 | `04_Greeks_Part1_Intro.html` | Greeks Part I: Intro | Greeks taxonomy, Taylor series approximation, static vs dynamic hedging |
| 05 | `04_Greeks_Part2_Delta.html` | Greeks Part II: Delta | Delta exposure, BS Delta sensitivities, Δ vs P(ITM), Delta hedging P&L |
| 06 | `04_Greeks_Part3_Gamma.html` | Greeks Part III: Gamma | Convexity, Gamma scalping, BS Gamma, pin risk, Dollar Gamma |
| 07 | `04_Greeks_Part4_Theta.html` | Greeks Part IV: Theta | Time decay, Theta vs moneyness/vol/maturity, Theta-Gamma trade-off |
| 08 | `04_Greeks_Part5_Vega.html` | Greeks Part V: Vega | IV exposure, Vega risk across strikes & maturities, Vega matrices, Volga/Vanna |
| 09 | `04_Greeks_Part6_Rho.html` | Greeks Part VI: Rho | Interest rate sensitivity, strike discounting, funding cost channels, LEAPS risk |
| 10 | `04_Greeks_Part7_2ndOrders.html` | Greeks Part VII: 2nd Orders | Volga, Vanna, Charm, Delta Drift family, Master Greeks Table |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Structure** | Semantic HTML5 |
| **Styling** | Vanilla CSS (dark theme with CSS custom properties) |
| **Logic** | Vanilla JavaScript (no frameworks) |
| **Math Rendering** | [KaTeX 0.16.9](https://katex.org/) with auto-render |
| **Charts** | HTML5 Canvas API (custom-drawn, no chart libraries) |
| **Fonts** | IBM Plex Sans, Fira Code / JetBrains Mono (monospace) |

No build step. No bundler. No dependencies to install.

---

## Getting Started

### Local

Simply open `index.html` in any modern browser:

```
# Double-click index.html, or:
start index.html          # Windows
open index.html           # macOS
xdg-open index.html       # Linux
```

All modules are linked from the landing page. Each module is a standalone HTML file — you can also open any module directly.

### Hosted

Drop the entire `Refined_Notes/` folder onto any static hosting provider:

- **GitHub Pages** — push to a repo and enable Pages on the branch
- **Netlify / Vercel** — drag-and-drop the folder
- **Any web server** — serve as-is, no server-side processing needed

> **Note:** The site loads KaTeX and Google Fonts from CDN, so an internet connection is required for math rendering and optimal typography.

---

## Project Structure

```
Refined_Notes/
├── index.html                        # Landing page — links to all modules
├── 01_Forwards_Futures.html          # Module 01
├── 02_Option_Fundamentals.html       # Module 02
├── 03_All_About_Volatility.html      # Module 03
├── 04_Greeks_Part1_Intro.html        # Module 04
├── 04_Greeks_Part2_Delta.html        # Module 05
├── 04_Greeks_Part3_Gamma.html        # Module 06
├── 04_Greeks_Part4_Theta.html        # Module 07
├── 04_Greeks_Part5_Vega.html         # Module 08
├── 04_Greeks_Part6_Rho.html          # Module 09
├── 04_Greeks_Part7_2ndOrders.html    # Module 10
├── LAST_REVIEWED.md                  # QA review progress tracker
└── README.md                         # ← You are here
```

---

## Design System

The site uses a consistent dark theme across all modules with accent colors per topic area:

| Token | Value | Usage |
|-------|-------|-------|
| `--bg` | `#05080a` | Page background |
| `--surface` | `#090e12` | Elevated surfaces |
| `--card` | `#0e1519` | Card backgrounds |
| `--text` | `#e2e8f0` | Primary text |
| `--accent` | Module-specific | Primary accent (e.g. `#4ade80` green for index, `#fbbf24` amber for Gamma) |
| `--green` | `#4ade80` | Positive values / profit |
| `--red` | `#f87171` | Negative values / loss |

---

## Interactive Features

Every module includes some or all of the following interactive elements:

- **Parameter controls** — Numeric inputs with HTML validation bounds (`min`, `step`) for spot price, strike, volatility, rate, time, etc.
- **Reinit buttons** — One-click reset to default parameters on every calculator
- **Real-time charts** — Canvas-rendered graphs that update instantly on parameter change
- **Hover tracking** — Crosshair guides, coordinate markers, and floating HUD tooltips on all charts
- **Interactive legends** — Dynamic legend values that update as you move across a chart
- **KPI result panels** — Computed Greek values displayed in styled metric cards

---

## Contributing / Review Workflow

Module review progress is tracked in [`LAST_REVIEWED.md`](LAST_REVIEWED.md). The review process ensures:

1. Input validation bounds are set on all controls (no negative vol, strike, etc.)
2. Falsy JavaScript fallback bugs are resolved (`0` values for rate or contract size are valid, not defaulted)
3. Math label casing is preserved (inline `text-transform: none` overrides where needed)
4. Hover tracking and tooltips are present on all Canvas charts
5. Reinit buttons are available on every interactive section

---

## License

© 2025–2026 Quantitative Finance Notes. Built for S&T and Options Traders.
