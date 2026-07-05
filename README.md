# ⚡ GridPulse v14.9.0 🧙 Old School Wisdom

> **Free, open-source, multi-exchange crypto reversal screener** purpose-built as a **companion tool for Pionex Grid Bots** — with directional **STRONG / GRID BUY/SELL** modes, **TF-adaptive Strictness**, MACD + VWAP + ATR + ADX + **MTF Trend Filter** + **Session Filter** + **Liquidity Guard** + Funding-aware setups across **Pionex, Bybit, Binance, KuCoin, and OKX** — and one-click **Launch Cards** with **Trade Plan v2** (TP1/TP2 + Chandelier trailing stop) that take you straight into a Pionex trading session.
>
> **v14.9.0** introduces **Old School Wisdom** — battle-tested filters from decades of trading practice: 🎯 **MTF Trend Filter**, 🤖 **Donchian / Bollinger / ATR** bot range modes, 🌏 **Session Filter**, 💧 **Liquidity Guard**, 🏷 **Unified Bybit-style symbols**, 🔍 **Cell Magnifier**, and ⚡ **STRONG-signal row highlighting**.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Version](https://img.shields.io/badge/version-14.9.0-blue.svg)](https://github.com/pro100off/gridpulse/releases/latest)
[![Old School Wisdom](https://img.shields.io/badge/🧙-Old%20School%20Wisdom-c39bff)](#-whats-new-in-v1490--old-school-wisdom)
[![MTF Filter](https://img.shields.io/badge/🎯-MTF%20Trend%20Filter-26d97a)](#-mtf-trend-filter-new-in-v1490)
[![Pionex Partner](https://img.shields.io/badge/🤝-Pionex%20Partner-26d97a)](https://bit.ly/43bkdc7)
[![Stars](https://img.shields.io/github/stars/pro100off/gridpulse?style=social)](https://github.com/pro100off/gridpulse/stargazers)
[![Single File](https://img.shields.io/badge/build-single--file-success)](index.html)
[![No Build Tools](https://img.shields.io/badge/dependencies-zero-success)]()
[![Languages](https://img.shields.io/badge/i18n-EN%20·%20UA%20·%20ES%20·%20RU%20·%20ZH-purple)]()

---

## 🔗 Quick links

| Resource | URL |
|----------|-----|
| 🌐 **Live demo (canonical)** | [https://tradescout.trade/](https://tradescout.trade/) |
| 🪞 **GitHub Pages mirror** | [https://pro100off.github.io/gridpulse/](https://pro100off.github.io/gridpulse/) |
| 💻 **GitHub repository** | [https://github.com/pro100off/gridpulse](https://github.com/pro100off/gridpulse) |
| 🤝 **Sign up on Pionex** (referral) | [https://bit.ly/43bkdc7](https://bit.ly/43bkdc7) |
| 📢 **Telegram channel** | [https://t.me/tradescoutfree](https://t.me/tradescoutfree) |
| 🐦 **Twitter / X** | [https://x.com/tradeaiscout](https://x.com/tradeaiscout) |
| 📜 **License** | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| 📋 **Changelog** | [CHANGELOG.md](CHANGELOG.md) |
| 📖 **User Guide** | [GitHub.USER_GUIDE.md](GitHub.USER_GUIDE.md) |
| 📝 **Release notes v14.9.0** | [docs/RELEASE_NOTES_v14.9.0.md](docs/RELEASE_NOTES_v14.9.0.md) |
| 🐛 **Issues** | [GitHub Issues](https://github.com/pro100off/gridpulse/issues) |
| 🚀 **Latest release** | [Releases](https://github.com/pro100off/gridpulse/releases/latest) |

[![GridPulse Screenshot](docs/screenshot.png)](docs/screenshot.png)

---

## 🤝 Pionex Affiliate

GridPulse v14.9.x is positioned as a **dedicated companion tool for Pionex Grid Bots**. The project is enrolled in Pionex's **affiliate referral program** — Pionex is the **default exchange** for new users, and every Launch Card features a prominent **"Open in Pionex"** CTA with UTM-tagged deep links that carry the setup context (symbol, TF, mode) into your Pionex session.

> **Disclaimer on partnership wording:** GridPulse is an *affiliate program participant*, not a contractually engaged Pionex partner. The 🤝 badge reflects participation in the referral commission program — Pionex does not direct the screener's classification logic, does not pay for ranking, and has no editorial control over the project.

> Bybit, Binance, KuCoin, and OKX remain **fully supported** via the exchange dropdown. The Pionex-first positioning is about defaults and UX polish — not lock-in.

### Why Pionex?

- **16 free built-in trading bots** (Grid, Reverse Grid, Smart Trade, DCA, etc.)
- **0.05% trading fee** — among the lowest in the industry
- **10M+ users**, licensed exchange, cold storage, 24/7 support
- **Native Grid Bot parameters** map 1:1 to GridPulse Launch Cards (Lower Limit, Upper Limit, Grid Lines, ATR-based SL/TP)

---

## 📑 Table of contents

- [✨ Features](#-features)
- [🚀 Quick start](#-quick-start)
- [🧙 What's new in v14.9.0 — Old School Wisdom](#-whats-new-in-v1490--old-school-wisdom)
- [🎯 MTF Trend Filter (new in v14.9.0)](#-mtf-trend-filter-new-in-v1490)
- [🤖 Bot Range modes (new in v14.9.0)](#-bot-range-modes-new-in-v1490)
- [🌏 Session Filter (new in v14.9.0)](#-session-filter-new-in-v1490)
- [💧 Liquidity Guard (new in v14.9.0)](#-liquidity-guard-new-in-v1490)
- [🏷 Symbol Unification (new in v14.9.0)](#-symbol-unification-new-in-v1490)
- [🔍 Cell Magnifier (new in v14.9.0)](#-cell-magnifier-new-in-v1490)
- [⚡ STRONG-signal row highlighting](#-strong-signal-row-highlighting)
- [🎯 Trade Plan v2](#-trade-plan-v2)
- [💾 Pair Presets](#-pair-presets)
- [🤝 Pionex companion workflow](#-pionex-companion-workflow)
- [⌨ Hotkeys](#-hotkeys)
- [🧠 How it works](#-how-it-works)
- [📈 Directional modes](#-directional-modes)
- [🎯 TF-adaptive Strictness](#-tf-adaptive-strictness)
- [🛡 Classified SKIP reasons](#-classified-skip-reasons)
- [⭐ Two paths to STRONG](#-two-paths-to-strong)
- [📊 Indicators reference](#-indicators-reference)
- [💰 Funding-aware logic](#-funding-aware-logic)
- [🎛 Settings & filters](#-settings--filters)
- [📋 Launch Cards](#-launch-cards)
- [📸 Export & content tools](#-export--content-tools)
- [🌐 Internationalization](#-internationalization)
- [🛠 Self-hosting](#-self-hosting)
- [🔄 Optional Cloudflare Worker proxy](#-optional-cloudflare-worker-proxy)
- [📁 Repository structure](#-repository-structure)
- [📜 Version history (carried-over highlights)](#-version-history-carried-over-highlights)
- [⚠ Disclaimer](#-disclaimer)
- [💚 Transparency](#-transparency)
- [📊 Analytics](#-analytics)
- [🤝 Contributing](#-contributing)
- [❓ FAQ](#-faq)
- [📄 License](#-license)

---

## ✨ Features

- **🎯 MTF Trend Filter (v14.9.0, ON by default)** — rejects setups fighting higher-TF EMA50 direction. Cuts ~60% of counter-trend false positives.
- **🤖 Bot Range modes (v14.9.0)** — Donchian 26 (default), Bollinger 20/2σ, or legacy ATR for tuning grid ranges to market character.
- **🌏 Session Filter (v14.9.0)** — downgrades STRONG→GRID during Asian night (00-06 UTC) where liquidity drops ~40%.
- **💧 Liquidity Guard (v14.9.0)** — hard-blocks STRONG signals for pairs with < $50k avg turnover per bar (20-bar window). Kills memecoin dust from STRONG.
- **🏷 Unified Bybit-style symbol display (v14.9.0)** — all exchanges show `BTCUSDT` / `BTCUSDT.P` regardless of native format.
- **🔍 Cell Magnifier (v14.9.0)** — hover any table cell to enlarge 1.45× with glow. Toggle in header (saved to localStorage).
- **⚡ STRONG-signal row highlighting (v14.9.0)** — gradient background, ⚡ icon in # column, subtle 3s pulse animation.
- **🎯 Trade Plan v2 (v14.9.0)** — STRONG now shows TP1 (close 50% at 1R), TP2 (trail rest at 2R+), Chandelier trailing stop (ATR×3).
- **📈 Freshness bonus in ranking (v14.9.0)** — freshest MACD signals rank first within same mode.
- **💾 Pair Presets** — save/load named watchlists in browser, with 5 built-in starters (💎 Majors / 🐸 Memes / 🤖 AI / 🏛 Layer 1s / 💧 DeFi), JSON import/export, and shareable URLs.
- **🤝 Built around Pionex** — Pionex is the default exchange; Launch Cards map directly to Pionex Grid Bot parameters.
- **5 exchanges:** Pionex, Bybit, Binance, KuCoin, OKX (**Spot + USDT Futures**).
- **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, EMA50 (MTF), Volume ratio, R:R.
- **TF-adaptive Strictness** — thresholds scale automatically by timeframe (**1m softer → 1W stricter**) with a global selector: **soft / normal / strict**.
- **Two paths to STRONG setups:**
  - **Exhaustion** — blow-off trend + reversal candle
  - **Quality** — moderate trend + ⭐ VWAP confluence + strong R:R
- **Classified SKIP reasons** with exact per-row tooltip thresholds:
  - ⚡ **WATCH** — strong reversal candle present, but reward (R:R) too low
  - 🌊 **TREND** — market still trending too strongly, no valid reversal yet
  - ⚖ **LOW R:R** — poor reward relative to risk
  - Plus **v14.9.0 downgrade reasons**: session (Asian night), liquidity (< $50k/bar), MTF (counter-trend).
- **Setup geometry validation** (v14.8.1+) — rejects stale setups where price already crossed entry/stop.
- **Funding-aware setups** for perpetual contracts (current rate, 7-day average, daily / annual cost, hold-period projection, LONG/SHORT bias).
- **5 languages:** English · Українська · Español · Русский · 中文
- **Launch Cards** with copy-paste-ready Grid Bot parameters and a **prominent "Open in Pionex" CTA** with UTM tracking.
- **Pionex Only mode** — single header toggle that locks the screener to Pionex for a focused workflow.
- **Breakout entry logic** — `limL` placed at the opposite extreme of the reversal candle.
- **TradingView integration** — open chart for any setup in one click.
- **CSV export** of all scan results (with funding columns).
- **Content-creator tools** — horizontal full screenshot, vertical 1080×1350 PNG Cards (top 5), vertical 1080×1350 PNG Table (top 15), 5-slide Carousel, daily watermark with scan serial counter.
- **Privacy-first:** no signup, no cookies, no individual user tracking, no fingerprinting, GDPR-compliant.
- **Light / Dark theme** with full localization and high-contrast rows.
- **Auto-fallback proxies** — scan still completes even when one exchange API is blocked in your region.
- **Custom domain support** — canonical URL: [https://tradescout.trade/](https://tradescout.trade/)
- **Zero-build single-file architecture** — entire app is one `index.html`.
- **No npm, no webpack, no dependencies** — works on `file://`, GitHub Pages, Cloudflare Pages, Netlify, Vercel, Apache, nginx, Caddy, or any static host.

---

## 🚀 Quick start

### Option A — Use the hosted version (no install)

1. Open [https://tradescout.trade/](https://tradescout.trade/)
2. The screener opens on **Pionex / Spot** by default (you can switch to Bybit / Binance / KuCoin / OKX anytime)
3. *(Optional)* Pick a **preset** from the dropdown (💎 Majors / 🐸 Memes / 🤖 AI Tokens / 🏛 Layer 1s / 💧 DeFi Blue Chips)
4. Select **timeframes** (defaults: 1h, 4h, 1D)
5. Optionally adjust **Strictness** (soft / normal / strict) and **🤖 Bot Range** mode (Donchian / Bollinger / ATR)
6. Click **▶ Scan** — results usually appear in ~30 seconds
7. Look for ⚡ **STRONG-highlighted rows** at the top of the table
8. Click 📋 next to any symbol to open the **Launch Card** with **Trade Plan v2**
9. Click the big **🚀 Open in Pionex** button → the setup carries over via UTM-tagged deep link
10. Paste the parameters into a Pionex Grid Bot and manage the trade manually

### Option B — Self-host (1 command)

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
```

Or simply double-click `index.html` — it also works on `file://`.

---

## 🧙 What's new in v14.9.0 — Old School Wisdom

v14.9.0 is a **quality release** that codifies decades of practical trading wisdom into hard filters. No cosmetic changes — every addition either reduces false positives or makes real signals more visible.

### Headline features

1. **🎯 MTF Trend Filter** — the single biggest quality improvement. Rejects setups fighting the higher-TF EMA50 direction. **~60% fewer counter-trend false positives**.
2. **🤖 Bot Range modes** — Donchian 26 by default (matches sideways markets better than ATR), Bollinger 20/2σ, or legacy ATR.
3. **🌏 Session Filter** — downgrades STRONG→GRID during 00-06 UTC (Asian night, low liquidity).
4. **💧 Liquidity Guard** — hard-blocks STRONG for pairs with < $50k avg turnover per bar. No more memecoin dust in STRONG.
5. **🏷 Symbol Unification** — every exchange now displays symbols in Bybit style (BTCUSDT, BTCUSDT.P). Cross-exchange comparison is finally readable.
6. **🔍 Cell Magnifier** — hover any cell to enlarge 1.45× with glow. Toggle 🔍 in header.
7. **⚡ STRONG-signal row highlighting** — gradient background, ⚡ icon in # column, subtle 3s pulse. GRID rows get a thin 2px left border.
8. **🎯 Trade Plan v2** — STRONG Launch Cards now show TP1 (close 50% @ 1R), TP2 (trail rest at 2R+), and Chandelier trailing stop (ATR×3).
9. **📈 Freshness bonus** — freshest MACD signals rank first within same mode.

**Zero breaking changes.** All v14.8.2 scanning logic, geometry validation, classification, TF-adaptive thresholds, Strictness selector, classified SKIP reasons, Pionex companion positioning, and Pair Presets behaviour are **preserved unchanged**.

See the dedicated sections below for the full breakdown of each feature.

---

## 🎯 MTF Trend Filter (new in v14.9.0)

The **Multi-TimeFrame Trend Filter** is v14.9.0's headline improvement. It rejects setups whose direction fights the higher-TF EMA50 trend — a classic "don't fight the tape" filter that cuts an estimated **~60% of counter-trend false positives**.

### How it works

For every setup on a given TF, GridPulse fetches candles on a **higher TF** and checks the **EMA50 slope** over the last 3 candles.

- **Bullish setup** rejected if higher-TF EMA50 is falling (uptrend on lower TF against downtrend on higher TF).
- **Bearish setup** rejected if higher-TF EMA50 is rising (downtrend on lower TF against uptrend on higher TF).

### TF → higher-TF mapping

| Scan TF | Higher TF checked |
|---------|-------------------|
| 1m | 15m |
| 5m | 1h |
| 15m | 4h |
| 30m | 4h |
| 1h | 4h |
| 4h | 1D |
| 1D | 1W |
| 1W | 1M |

### Slope tolerance

The EMA50 must slope by at least **±0.1%** over the last 3 candles to count as an active trend. Flat higher-TF EMA50 = filter is neutral (both directions allowed).

### Impact

On a typical multi-TF scan on 4h/1D:

- **v14.8.2:** ~40 setups, of which ~15 were LONGs during clear 1D downtrends (destined to fail).
- **v14.9.0 with MTF ON:** ~25 setups, with counter-trend positions filtered out.

The filter is **ON by default** but can be turned off via the **MTF TREND FILTER** checkbox in the right filter panel.

Every MTF-rejected row is logged transparently in the Activity Log:

```
MTF-SKIP: BTCUSDT/1h fights 4h EMA50 trend
```

---

## 🤖 Bot Range modes (new in v14.9.0)

Grid bot ranges are now computed via one of three algorithms, selectable in the left panel:

| Mode | Formula | Best for |
|------|---------|----------|
| **Donchian 26** (default) | `[min(low, 26 bars) − ATR×0.4, max(high, 26 bars) + ATR×0.4]` | Sideways / range-bound markets. Matches natural swing highs/lows. |
| **Bollinger 20/2σ** | `[SMA(20) − 2σ − ATR×0.5, SMA(20) + 2σ + ATR×0.5]` | Volatile assets with mean-reversion character. |
| **ATR (legacy)** | `[price − ATR×N/2, price + ATR×N/2]` where N=18 if ADX≥18 else 10 | Backwards compatibility with v14.8.2 and earlier. |

The chosen range appears in every Launch Card GRID mode as a new field **"Range source"** (e.g., `Donchian 26 +ATR`) so you always know which algorithm produced the range you're looking at.

### Why Donchian is the new default

Grid bots make money on **oscillations within a range**. Donchian captures the last 26 bars' actual swing highs/lows — the levels the market has *demonstrated* as resistance and support. ATR-based ranges are symmetric around current price, which is often skewed in trending markets. Donchian's asymmetry mirrors the market's actual behaviour better.

---

## 🌏 Session Filter (new in v14.9.0)

Not all trading hours are created equal. The **Session Filter** downgrades STRONG→GRID setups occurring during the **Asian night session (00-06 UTC)** where:

- Liquidity drops ~40% vs. peak
- False breakouts spike due to thin order books
- Stop-hunt behaviour is more common

### How it works

- **07-21 UTC** (main EU/US sessions) — no changes; STRONG signals pass through normally.
- **00-06 UTC** — any setup that would qualify as STRONG_BUY / STRONG_SELL is **downgraded to GRID_BUY / GRID_SELL** instead.
- The downgrade is logged in the Activity Log:

```
Session-DOWNGRADE: BTCUSDT/4h STRONG→GRID (Asian night)
```

### Not aggressive

The Session Filter does **not reject** setups — it only reduces their aggressiveness. You still see the trade opportunity; you just get a Grid Bot recommendation instead of a leveraged directional entry.

**OFF by default.** Enable via **SESSION FILTER (07-21 UTC)** checkbox in the Trend/R:R filter group.

---

## 💧 Liquidity Guard (new in v14.9.0)

A **hard filter** that blocks STRONG classification for illiquid pairs.

### Definition

Average USD turnover per bar (calculated over the last 20 bars) must exceed **$50,000**:

```
avgTurnoverUSD = mean over last 20 bars of ((high + low + close) / 3 × volume)
```

If `avgTurnoverUSD < $50,000`, the pair is marked as **illiquid** — a 💧 icon appears in Activity Log entries — and any STRONG setup is automatically **downgraded to GRID**.

### Why

Memecoins and small-cap tokens frequently produce "picture-perfect" reversal signals on paper. In reality:

- Slippage on $10k trade is 2–5%.
- Stops get hunted the moment your bot enters.
- Grid mode is safer because it doesn't require a single well-timed entry.

The Liquidity Guard says: *"Yes, the technical pattern is valid — but this pair is not liquid enough to trust a STRONG-mode leveraged entry."*

### Log example

```
Liquidity-DOWNGRADE: MEMEUSDT/1h STRONG→GRID (< $50k/bar)
```

The Liquidity Guard is **always ON** — there is no toggle. This is by design; it's a safety floor, not a preference.

---

## 🏷 Symbol Unification (new in v14.9.0)

Different exchanges use different symbol formats:

| Native format | Example |
|---------------|---------|
| Bybit / Binance | `BTCUSDT` |
| KuCoin spot | `BTC-USDT` |
| KuCoin futures | `XBTUSDTM` |
| Pionex spot | `BTC_USDT` |
| Pionex perp | `BTC_USDT_PERP` |
| OKX spot | `BTC-USDT` |
| OKX swap | `BTC-USDT-SWAP` |

### v14.9.0 unified display

All symbols now display in **Bybit style** regardless of exchange:

- Spot: `BTCUSDT`
- Perp: `BTCUSDT.P`
- Preserves multipliers: `1000PEPEUSDT` → `PEPE¹ᵏUSDT`, `10000CHEEMSUSDT` → `CHEEMS¹⁰ᵏUSDT`

The original exchange-native symbol is **preserved internally** for API calls — only the display is normalized. So `BTC-USDT` on KuCoin still fetches via `BTC-USDT`, but you see `BTCUSDT` in the table.

### Why

Cross-exchange comparison is finally readable. Sorting by symbol works. Copy-paste into TradingView or Pionex is consistent. No more mental gymnastics translating `XBTUSDTM` to `BTCUSDT.P`.

---

## 🔍 Cell Magnifier (new in v14.9.0)

Hover any cell in the results table to enlarge it **1.45×** with a glow effect. Great for reading small numeric cells (VWAP%, ATR, Fund% etc.) without zooming the whole page.

### Toggle

The 🔍 button in the header toggles the magnifier globally. State persists in `localStorage` under `gp_mag`.

- **ON** (default): 🔍 icon, `.on` class on button.
- **OFF**: 🔎 icon, no magnification, `body.mag-off` class active.

### Hotkey

Press `Shift + M` to toggle.

### Behaviour

- **Standard cells** — enlarge 1.45× with gradient background + 2px blue outline.
- **Wick / candle cells (columns 8–10)** — enlarge only 1.15× to keep SVG proportions readable.
- **Highlighted rows** — magnifier is disabled to avoid conflict with row highlighting.

---

## ⚡ STRONG-signal row highlighting

STRONG-mode rows now stand out at a glance:

- **STRONG_BUY** — green gradient background (left→right fade), `inset 4px 0 0 var(--grn)` left border, subtle 3s pulse animation.
- **STRONG_SELL** — red gradient background, red left border, red pulse.
- **⚡ icon** appears in the `#` column of every STRONG row, with a drop-shadow glow.
- **GRID_BUY / GRID_SELL** rows get a thin 2px left border in green/red respectively (no gradient, no pulse).

Light theme uses the same pattern with softer green/red palettes for contrast compliance.

### Rationale

In a table of 50+ rows, STRONG signals need to be findable in <1 second. The gradient + pulse + ⚡ combo is intentionally attention-grabbing without being obnoxious. The pulse is only ~15% opacity swing at 3s cadence — visible but not distracting.

---

## 🎯 Trade Plan v2

Launch Cards for STRONG_BUY / STRONG_SELL modes now display a **richer, safer trade plan** based on classic swing-trading playbooks.

### Old plan (v14.8.2 and earlier)

- Entry (limL)
- Stop Loss (stopL)
- Conservative SL (stopC)
- Fixed Take Profit (calculated from R:R)
- Trailing trigger ±10%
- Position size 10–20% of capital

### New plan (v14.9.0)

- Entry (limL)
- Stop Loss (stopL)
- Conservative SL (stopC)
- **🎯 TP1 — close 50% at 1R** (locks in break-even on the remainder)
- **🎯 TP2 — trail the rest at 2R+** (rides the winner)
- **📉 Chandelier trailing stop (ATR×3)** (technical trailing based on realized volatility)
- Position size 10–20% of capital

### Why this matters

The old fixed-TP plan works only if your R:R prediction is accurate. If price stalls at 1.8R, you exit at your stop — a losing trade after being up 180% of risk. The new plan:

1. **Locks in profit at 1R** on half the position (guarantees at least break-even overall if TP2 stops out).
2. **Trails the remainder** using a Chandelier stop (ATR×3 from the highest high since entry), which follows the trend as long as volatility remains normal.

This is the same structure used by professional swing traders and CTAs for decades. It's not novel; it's just now **built into GridPulse**.

### GRID mode plans unchanged

GRID_BUY / GRID_SELL Launch Cards continue to show Pionex Grid Bot parameters (Lower / Upper / Grid Lines / Investment / ATR-based SL/TP). The new **"Range source"** field shows which range algorithm produced the numbers (Donchian / Bollinger / ATR).

---

## 💾 Pair Presets

Named watchlists stored directly in your browser — no backend, no account, no cost. (Unchanged from v14.8.2.)

### 5 built-in starter presets

| Icon | Name | Pairs |
|------|------|-------|
| 💎 | **Majors** | BTC · ETH · SOL · BNB · XRP · ADA · AVAX · DOT · LINK · MATIC |
| 🐸 | **Memes** | DOGE · SHIB · PEPE · WIF · BONK · FLOKI · MEME · POPCAT · BRETT · TURBO |
| 🤖 | **AI Tokens** | FET · AGIX · OCEAN · RNDR · TAO · WLD · GRT · AKT · ARKM · NMR |
| 🏛 | **Layer 1s** | ETH · SOL · AVAX · NEAR · APT · SUI · SEI · INJ · TIA · TON |
| 💧 | **DeFi Blue Chips** | UNI · AAVE · MKR · LDO · SNX · CRV · COMP · SUSHI · GMX · PENDLE |

### Save / Manage / Share

- **💾 Save as…** — save current Custom Pairs as a named preset with custom icon.
- **⚙ Manage** — apply, delete, import/export JSON.
- **Shareable URL** — `tradescout.trade/?preset=<base64-encoded-json>` — recipient sees a consent prompt before importing.

### Storage isolation

Presets live under `gp_presets_v1` — **independent** from `gp_settings_v14_9_0`. Clearing screener settings never deletes your presets.

| Storage key | Purpose |
|-------------|---------|
| `gp_presets_v1` | All your user presets (JSON array) |
| `gp_preset_last` | ID of the last-applied preset (auto-restored on reload) |
| `gp_settings_v14_9_0` | Screener settings (independent) |
| `gp_mag` | Cell Magnifier state (independent) |

---

## 🤝 Pionex companion workflow

GridPulse v14.9.x is designed around a **focused, two-tool workflow**:

```
┌─────────────────────────┐                ┌─────────────────────────┐
│  GridPulse              │                │  Pionex                 │
│  (scan + plan)          │  ────────►     │  (execute)              │
│                         │  Open in       │                         │
│  • Pick preset 💾       │  Pionex CTA    │  • Grid Bot             │
│  • MTF-filtered scan 🎯 │  + UTM tags    │  • Reverse Grid         │
│  • Trade Plan v2 📋     │                │  • Smart Trade          │
│  • Copy parameters      │                │                         │
└─────────────────────────┘                └─────────────────────────┘
```

---

## ⌨ Hotkeys

A floating ⌨ button in the bottom-left corner shows the full hotkey reference at any time.

| Key | Action |
|-----|--------|
| Shift + T | Vertical / TikTok-friendly layout |
| Shift + P | Export PNG Cards (top 5, 1080×1350) |
| Shift + Alt + P | Export PNG Table (top 15, 1080×1350) |
| Shift + C | Generate 5-slide carousel |
| Shift + M | **Toggle cell magnifier (v14.9.0)** |
| Esc | Close any open modal (chart / Launch Card / preset modals) |
| Double-click row | Highlight selected row, dim others |

> **Tip:** Hotkeys are ignored while typing inside `<input>`, `<textarea>`, or `<select>` so you can keep typing custom pair lists without conflicts.

---

## 🧠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for restricted regions) and calculates all indicators client-side in your browser.

```
Exchange API ──► (optional proxy) ──► your browser ──► indicators ──► classifier
                                                                          │
                                                                          ▼
                                                                  Launch Card UI
```

- No personal data is sent to any server.
- Your preferences are stored locally in `localStorage`.
- Scan results are kept only in memory (and `sessionStorage` cache).

### Proxy chain & fallback strategy

For each request, GridPulse tries:

1. **Direct fetch** (for Bybit, Pionex, Binance, KuCoin, OKX endpoints that are CORS-friendly)
2. **Cloudflare Worker proxy** (rate-limited shared instance)
3. **CodeTabs proxy**
4. **AllOrigins proxy**
5. **CORS.lol proxy**
6. **ThingProxy proxy**

Each proxy has a health tracker:

- **Auto-ban** for 30 seconds after a single failure
- **Hard-ban** for 120 seconds after 3 consecutive failures
- Rate-limit warning surfaces in the header when 3+ failures land within 10 seconds

### Binance Futures GeoIP fallback

Some regions return HTTP 451 for `fapi.binance.com`. In that case, GridPulse:

1. Tries `fapi/v1/exchangeInfo` → fails
2. Falls back to `fapi/v1/ticker/price` → if also blocked,
3. Mirrors the pair list and klines via Bybit so the scan still completes
4. Logs the fallback transparently in the Activity Log

### Cache

- **Pair lists:** cached for 60 seconds (`sessionStorage`)
- **Kline data:** cached for 60 seconds per (exchange, market, symbol, TF) key
- **MCap rankings:** cached for 60 seconds per top-N bucket
- **Funding rates:** cached for 60 seconds per (exchange, symbol, history) key

---

## 📈 Directional modes

Each setup is classified into one of five modes:

| Mode | Direction | Logic summary | Launch Card layout |
|------|-----------|---------------|---------------------|
| **STRONG BUY** | bullish | Two routes (Exhaustion / Quality). Thresholds are TF-adaptive and globally tuned by Strictness. MTF-verified. | Entry + SL + Cons.SL + **TP1 + TP2 + Chandelier trail (v14.9.0)** |
| **GRID BUY** | bullish | Moderate trend + controlled VWAP distance + acceptable R:R. Scales by TF / Strictness. | Grid lower / upper / width / lines + ATR-based SL + ATR-based TP + Range source |
| **STRONG SELL** | bearish | Mirror of STRONG BUY | Entry + SL + Cons.SL + TP1 + TP2 + Chandelier trail |
| **GRID SELL** | bearish | Mirror of GRID BUY | Grid lower / upper / width / lines + ATR-based SL + TP + Range source |
| **SKIP** | any | Setup does not qualify; classified into WATCH / TREND / LOW R:R (+ v14.9.0 downgrade reasons) with tooltip explanation | Reference price + warning |

### Mode sort priority

Results table is sorted (when sorting by Mode column) as:

```
STRONG_BUY  ≡  STRONG_SELL  >  GRID_BUY  ≡  GRID_SELL  >  SKIP
```

Within the same priority, ties are broken by **freshness bonus (v14.9.0)** then by R:R then by depth.

### Setup geometry validation (v14.8.1+)

Stale setups where price has **already crossed** the entry or stop before the scan are rejected automatically:

- **Bullish:** rejected if `price ≤ stopL` or `price ≥ limL`
- **Bearish:** rejected if `price ≥ stopL` or `price ≤ limL`

This prevents the Launch Card from showing "ghost" setups that would be impossible to enter.

---

## 🎯 TF-adaptive Strictness

Every threshold scales by:

```
effective_threshold  =  base_value  ×  TF_multiplier  ×  Strictness_multiplier
```

### TF multipliers

| TF | ADX | VWAP | Volume | R:R | Depth |
|----|----:|-----:|-------:|----:|------:|
| 1m | 0.70 | 0.20 | 0.95 | 0.90 | 0.60 |
| 5m | 0.78 | 0.30 | 1.00 | 0.95 | 0.70 |
| 15m | 0.85 | 0.45 | 1.00 | 1.00 | 0.80 |
| 30m | 0.90 | 0.60 | 1.00 | 1.00 | 0.85 |
| 1h | 0.95 | 0.80 | 1.05 | 1.00 | 0.95 |
| 4h | 1.00 | 1.00 | 1.10 | 1.00 | 1.00 |
| 1D | 1.10 | 1.50 | 1.20 | 1.10 | 1.20 |
| 1W | 1.20 | 2.50 | 1.40 | 1.20 | 1.50 |
| 1M | 1.30 | 4.00 | 1.60 | 1.30 | 2.00 |

### Strictness multipliers

| Setting | Multiplier | Use case |
|---------|-----------:|----------|
| **Soft** | 0.75 | Faster signals, more false positives. Great for active scanning. |
| **Normal** | 1.00 | Default balance. |
| **Strict** | 1.30 | Only the cleanest setups. Best for higher TFs (1D, 1W). |

### Base thresholds (before scaling)

| Metric | STRONG | GRID (max/min) |
|--------|-------:|---------------:|
| ADX | ≥ 25 | < 28 |
| VWAP distance % | > 5 % | ≤ 5 % |
| Volume ratio | ≥ 1.5× | — |
| R:R | ≥ 2.0 | ≥ 1.5 |
| Depth | ≥ 5 | — |

---

## 🛡 Classified SKIP reasons

When a setup doesn't qualify for STRONG or GRID, it's classified with the exact failing thresholds shown in a per-row tooltip.

| Tag | Meaning |
|-----|---------|
| ⚡ **WATCH** | A strong reversal candle is already present, but R:R is too low for entry. |
| 🌊 **TREND** | Market is still trending too strongly, and there is no reversal candle yet. |
| ⚖ **LOW R:R** | The reward is too small relative to the risk. |
| 🛡 **SKIP** | Edge case that doesn't match any of the above categories. |

### v14.9.0 additional downgrade reasons

STRONG signals can also be **downgraded to GRID** (visible in tooltip as a suffix) for these reasons:

- **`downgraded — Asian night session (00-06 UTC, low liquidity)`** — Session Filter
- **`downgraded — low liquidity (< $50k avg turnover/bar)`** — Liquidity Guard
- **`rejected — fights higher-TF EMA50 trend`** — MTF Trend Filter (rejects entirely, not downgrade)

### Tooltip example (v14.9.0)

```
[4h/normal] Exhaustion (trend blow-off) · ADX=31.2 VWAP=6.1% Vol=1.72x R:R=2.34 d=6
   · downgraded — low liquidity (< $50k avg turnover/bar)
```

---

## ⭐ Two paths to STRONG

A STRONG setup can be unlocked in two different ways.

### 1️⃣ Exhaustion route

The classic blow-off / trend-exhaustion entry:

- ADX ≥ TF-scaled 25
- |VWAP%| > TF-scaled 5
- Volume ≥ 1.5×
- R:R ≥ 2.0
- depth ≥ 5
- Reversal candle present
- **MTF trend agrees (v14.9.0)** if MTF filter is ON

### 2️⃣ Quality route

Sometimes a clean reversal happens at moderate trend strength:

- ADX ≥ ~18 (≈ 72 % of the Exhaustion threshold)
- |VWAP%| > ~3 % (≈ 60 % of the Exhaustion threshold)
- Volume ≥ 1.5×
- R:R ≥ 2.0
- depth ≥ ~7 (≈ 140 % of the Exhaustion threshold)
- Reversal candle present
- ⭐ **VWAP confluence required**
- **MTF trend agrees (v14.9.0)** if MTF filter is ON

Both routes still scale with TF and Strictness. Both routes are further subject to **Session Filter** and **Liquidity Guard** in v14.9.0.

---

## 📊 Indicators reference

| Indicator | Period | Notes |
|-----------|--------|-------|
| MACD | 12 / 26 / 9 | Used for divergence + histogram window |
| VWAP | 50 | Rolling, volume-weighted |
| VWAP bands | 50, ±1σ / ±2σ | Used for ⭐ confluence detection |
| ATR | 14 | Drives candle-size filter, Grid SL/TP, Chandelier trail |
| ADX | 14 | Trend strength; reused for grid range width |
| **EMA50 (higher TF)** | **50** | **MTF Trend Filter (v14.9.0)** |
| **Donchian channels** | **26** | **Bot Range mode (v14.9.0)** |
| **Bollinger Bands** | **20 / 2σ** | **Bot Range mode (v14.9.0)** |
| Volume ratio | last vs. avg of 20 | Used for Vol ≥ 1.1× / 1.5× filters |
| USD turnover | avg of 20 | **Liquidity Guard (v14.9.0)** |
| R:R | derived from limit / stop / next swing | Reward-to-risk |

### ATR-based Grid SL / TP

For GRID setups, SL and TP are scaled by ATR per timeframe:

| TF | SL = ATR × | TP = ATR × |
|----|----:|----:|
| 1m | 1.5 | 1.2 |
| 5m | 1.8 | 1.4 |
| 15m | 2.0 | 1.5 |
| 30m | 2.2 | 1.6 |
| 1h | 2.5 | 1.8 |
| 4h | 2.8 | 2.0 |
| 1D | 3.0 | 2.2 |
| 1W | 3.5 | 2.5 |
| 1M | 4.0 | 3.0 |

### Chandelier trailing stop (v14.9.0)

For STRONG setups, the Launch Card recommends a **Chandelier trailing stop** at **ATR × 3** from the highest high (for longs) or lowest low (for shorts) since entry. This is the industry-standard technical trailing stop for swing trades.

---

## 💰 Funding-aware logic

Only active on **USDT Futures** market. Unchanged from v14.8.2.

When enabled, the screener fetches funding data and uses it to:

- show current rate, avg 7d (over 21 payments), daily (×3 sessions), annualized, hold-period cost, and next-payment countdown
- compute a directional bias label: 🟢 LONG-friendly / 🔴 LONG-costly / 🟢 SHORT-friendly / 🔴 SHORT-costly / ➖ Neutral
- optionally **SKIP** setups that exceed your configured daily funding threshold

### Funding settings

| Setting | Effect |
|---------|--------|
| **CONSIDER FUNDING** | Master switch (Futures only) |
| **USE 7-DAY HISTORY** | Use the 21-sample average instead of the current rate |
| **SKIP IF EXCEEDS THRESHOLD** | Drop adverse rows beyond Max daily funding |
| **Max daily funding** | 0.05% / 0.10% / 0.20% / 0.30% / 0.50% / 1.00% |
| **Hold (days)** | Time horizon for the cost projection in the Launch Card |

---

## 🎛 Settings & filters

All settings are persisted in `localStorage` under the key `gp_settings_v14_9_0` and **auto-migrated** from earlier versions (`v14_8_2`, `v14_8_1`, `v14_8_0`, `v14_7_6`, `v14_7_5`, `v14_7_4`, `v14_7_3`, `v14_7_2`, `v14_7`, `v14_6`, `v14_5`).

### Left panel — Timeframes & depth

| Control | Description |
|---------|-------------|
| **Timeframe row** | 1m / 5m / 15m / 30m / 1h / 4h / 1D / 1W / 1M |
| **Search depth** | How many bars back to look for a reversal pattern |
| **Min TF** | Minimum number of TFs that must produce a hit |
| **Extremum** | Lookback for validating reversal candle extreme |
| **Strictness** | soft / normal / strict |
| **🤖 Bot Range (v14.9.0)** | **Donchian 26** (default) / Bollinger 20/2σ / ATR (legacy) |

### Right panel — Exchange & filters

| Control | Description |
|---------|-------------|
| **Exchange** | **Pionex** 🤝 (default) · Bybit · Binance · KuCoin · OKX |
| **Market** | Spot · USDT Futures |
| **Type** | Both · Bullish only · Bearish only |
| **Top MCap** | Restrict to CoinGecko top N (50/100/200/500/All) |
| **Max** | Cap the number of returned rows |
| **REVERSAL FILTER** | Require a real reversal candle |
| **CONSERVATIVE STOP** | Adds the wide stopC calculation |
| **VWAP filters** | VWAP DIRECTION · VWAP CONFLUENCE |
| **Candle filters** | ATR SIZE ×0.8 · VOLUME ×1.1 |
| **Trend / R:R** | ADX ≥ 18 · R:R ≥ 1.5 · **MTF TREND FILTER (v14.9.0, ON)** · **SESSION FILTER (v14.9.0, OFF)** |
| **Funding (Futures only)** | CONSIDER FUNDING · USE 7-DAY HISTORY · SKIP IF EXCEEDS THRESHOLD |

### Header toggles

| Toggle | Effect |
|--------|--------|
| ⭐ **Star on GitHub** | Direct link to the repo |
| 🌐 **Language** | EN / UA / ES / RU / ZH switcher |
| 🌙 / ☀️ **Theme** | Dark / Light |
| 🔊 / 🔇 **Sound** | Scan-tick audio synth (WebAudio) |
| 🔍 / 🔎 **Magnifier (v14.9.0)** | Toggle cell hover magnification |
| 🤝 **Pionex Only** | Lock exchange to Pionex |

---

## 📋 Launch Cards

Each row in the results table has a 📋 button. Clicking it opens a **Launch Card** — a focused, copy-paste-ready trading plan.

### Launch Card layouts per mode (v14.9.0)

**STRONG BUY / STRONG SELL — Trade Plan v2**

- Entry (Buy/Sell Price) — limL
- Stop Loss — stopL
- Conservative SL — stopC
- **🎯 TP1 — close 50% at 1R (v14.9.0)**
- **🎯 TP2 — trail rest at 2R+ (v14.9.0)**
- **📉 Chandelier trailing stop (ATR×3) (v14.9.0)**
- Position size — 10–20 % of capital

**GRID BUY / GRID SELL** (Pionex Grid Bot ready)

- Lower Limit — bot range low
- Upper Limit — bot range high
- Range width — % of price
- **Range source (v14.9.0)** — Donchian / Bollinger / ATR
- Grid lines count — 30 / 40 / 50
- Grid mode — Geometric
- Investment — tokens (base asset)
- Stop Loss — ATR-based
- Take Profit — ATR-based

**SKIP**

- Current price
- Entry reference (limL)
- Stop reference (stopL)
- Warning that conditions are not optimal

### Extras in every Launch Card

- Indicator confirmation panel with colour-coded ADX / R:R / Vol / VWAP% / Depth / TF
- R:R bar with green / yellow / red zones
- Funding section (Futures only) — full breakdown + cost over N days + bias
- QR code (84 px) for Pionex referral signup, in a dedicated bordered panel
- **🤝 Pionex Affiliate** badge in the "Trade on Pionex" section
- Buttons: Copy all · Open chart (TradingView) · Share to Telegram · **🚀 Open in Pionex** (large gradient CTA with UTM tags)

### UTM tracking on Pionex deep links

```
?utm_source=gridpulse
&utm_medium=launchcard
&utm_campaign={mode}        # strong_buy, grid_sell, etc.
&utm_content={symbol}_{tf}  # BTCUSDT_4h
```

---

## 📸 Export & content tools

| Tool | Trigger | Output |
|------|---------|--------|
| CSV export | CSV button | Full results + funding columns |
| Full screenshot | 📸 Screenshot button | Horizontal PNG of the whole results section |
| Vertical PNG Cards | Shift + P (TikTok mode) | 1080×1350 PNG of the top 5 setups |
| Vertical PNG Table | Shift + Alt + P (TikTok mode) | 1080×1350 PNG of the top 15 setups |
| 5-slide Carousel | Shift + C | Five 1080×1350 PNGs: Cover · Top 1 · Top 2 · Top 3 · CTA |
| Daily scan serial | Auto | Per-day counter stored in `localStorage` |
| TikTok pager | Shift + T then ◀ ▶ | Paginates results 10 rows per page |

---

## 🌐 Internationalization

All UI text is fully translated into 5 languages:

| Code | Language | Flag |
|------|----------|------|
| en | English | 🇬🇧 |
| ua | Українська | 🇺🇦 |
| es | Español | 🇪🇸 |
| ru | Русский | 🇷🇺 |
| zh | 中文 | 🇨🇳 |

**NEW in v14.9.0:** ~30 additional translation keys per language for MTF Trend Filter labels, Bot Range mode names, Session Filter labels, Liquidity/Session/MTF downgrade tooltips, Trade Plan v2 labels (TP1, TP2, Chandelier), Cell Magnifier log messages, and STRONG-row indicators.

### Language priority

1. URL query: `?lang=en`, `?lang=ua`, `?lang=es`, `?lang=ru`, `?lang=zh`
2. `localStorage` preference (`gp_lang`)
3. `navigator.language` autodetect
4. Fallback: English

---

## 🛠 Self-hosting

GridPulse is a **single `index.html` file**. There are no build tools, no npm dependencies, and no server-side code.

### 1-minute setup

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse

# Serve locally
python3 -m http.server 8000           # Python 3
php -S localhost:8000                 # PHP
npx serve .                           # Node
caddy file-server --listen :8000      # Caddy

# Or just open index.html directly — file:// works too.
```

### Compatible hosts

- ✅ GitHub Pages
- ✅ Cloudflare Pages
- ✅ Netlify
- ✅ Vercel (static)
- ✅ Apache / nginx / Caddy
- ✅ Local `file://`

### External CDN dependencies

| Library | Purpose | CDN |
|---------|---------|-----|
| qrcodejs | QR code for Pionex referral | cdnjs |
| html2canvas | PNG / carousel rendering | cdnjs |
| tv.js | TradingView embedded widget | s3.tradingview.com (lazy-loaded) |
| Cloudflare Web Analytics | Anonymous traffic counter | static.cloudflareinsights.com |

---

## 🔄 Optional Cloudflare Worker proxy

For improved Pionex / Binance reliability in restricted regions, you can deploy your own Cloudflare Worker proxy.

The default deployment uses:

```
https://gridpulse-proxy.pro100off.workers.dev/?url=
```

This is a rate-limited shared instance. If you fork GridPulse, please deploy your own and update the `CUSTOM_PROXY` constant in `index.html`:

```javascript
const CUSTOM_PROXY = 'https://YOUR-WORKER.workers.dev/?url=';
```

---

## 📁 Repository structure

```
gridpulse/
├── index.html                       current release (v14.9.0)
├── LICENSE                          CC BY-NC-SA 4.0
├── README.md                        this file
├── CHANGELOG.md                     full version history
├── GitHub.USER_GUIDE.md             detailed user guide
├── docs/
│   ├── screenshot.png               preview image (OG / social cards)
│   └── RELEASE_NOTES_v14.9.0.md     short release notes
└── legacy/                          archived previous versions
    ├── index-v14.2.html
    ├── index-v14.3.html
    ├── index-v14.5.html
    ├── index-v14.7.5.html
    ├── index-v14.7.6.html
    ├── index-v14.8.0.html
    ├── index-v14.8.1.html
    └── index-v14.8.2.html
```

---

## 📜 Version history (carried-over highlights)

Full history lives in [CHANGELOG.md](CHANGELOG.md).

### v14.8.2 — "Pair Presets"

- 💾 Pair Presets — save/load named watchlists in localStorage
- 5 built-in starter presets (Majors, Memes, AI, Layer 1s, DeFi)
- JSON import/export, shareable URLs
- Full i18n for preset UI
- `SET_KEY` → `gp_settings_v14_8_2`

### v14.8.1 — "Setup geometry validation"

- 🐛 Bugfix: stale setups where price already crossed entry/stop before scan no longer pass the filter
- `SET_KEY` → `gp_settings_v14_8_1`

### v14.8.0 — "Pionex Companion"

- 🤝 Official Partner badge next to Pionex branding
- Pionex set as **DEFAULT exchange** (was Bybit)
- Prominent "Open in Pionex" CTA with UTM tags
- Larger, more visible referral QR code
- "Pionex Only" mode toggle
- Launch Card readability boost
- `SET_KEY` → `gp_settings_v14_8_0`

### v14.7.6 — "TF-adaptive thresholds"

- TF-adaptive Strictness — every threshold scales by TF × Strictness
- Two paths to STRONG (Exhaustion + Quality routes)
- Classified SKIP reasons — ⚡ WATCH / 🌊 TREND / ⚖ LOW R:R
- Dual TikTok PNG export
- ATR-based GRID SL/TP with TF multipliers
- Custom domain — [https://tradescout.trade/](https://tradescout.trade/)
- `SET_KEY` → `gp_settings_v14_7_6`

### v14.7.5 — "Directional Grid Modes"

- Directional Grid Modes — replaced unified BOT mode
- Breakout entry logic
- Light theme contrast boost
- Hotkeys panel
- `SET_KEY` → `gp_settings_v14_7_5`

### v14.7

- 📱 TikTok Mode (Shift+T)
- ✨ Highlight Row
- 🏷 Auto-watermark with daily scan serial counter
- 🎬 Auto-Carousel — 5-slide pack
- 🔊 Scan tick sound

### v14.6

- Screenshot button
- Binance Futures 451 → Bybit mirror fallback
- Pionex PERP discovery

---

## ⚠ Disclaimer

GridPulse is an **analytical tool, NOT financial advice**.

Cryptocurrency trading involves substantial risk of loss. Always do your own research (DYOR).

The screener identifies *potential* setups based on technical indicators. It does not predict price movement and does not guarantee profitability. Past patterns do not guarantee future results.

You are solely responsible for your trading decisions. Authors and contributors of GridPulse accept no liability for losses, missed gains, taxes, or any other damages resulting from the use of this tool.

---

## 💚 Transparency

GridPulse is **free and open-source**.

The author is enrolled in the **Pionex Affiliate Program** and earns a **referral commission from Pionex** when users sign up via the referral link and trade.

- This is the project's **only monetization**.
- There are no ads.
- There are no paid tiers.
- There are no premium features locked behind paywalls.

The 🤝 **Pionex Affiliate** badge reflects participation in the affiliate referral program — Pionex does not direct the screener's classification logic, does not pay for ranking, and does not have any editorial control over the project.

### Why Pionex specifically?

Pionex's Grid Bot is one of the few exchange-native automation products whose parameters map cleanly to a screener's output (Lower Limit / Upper Limit / Grid Lines / SL / TP). That made it the natural execution target for GridPulse Launch Cards.

### Forking

Forks with your own referral are welcome — please keep:

- a visible link back to the original repository,
- the CC BY-NC-SA 4.0 license,
- and the transparency disclosure in the footer.

---

## 📊 Analytics

GridPulse uses **Cloudflare Web Analytics** for anonymous, aggregate traffic statistics.

| Property | Status |
|----------|--------|
| Cookies | ❌ none |
| Personal data | ❌ none |
| Individual tracking | ❌ none |
| Fingerprinting | ❌ none |
| GDPR-compliant | ✅ yes |
| Open about what's tracked | ✅ yes |

All user-specific settings stay in your browser's `localStorage` and **never leave your device**.

---

## 🤝 Contributing

Issues and PRs are welcome. For major changes, please open an issue first.

### Especially appreciated

- **Translations** — adding new languages or improving existing ones.
- **Built-in presets** — proposing curated starter presets for new themes (RWA, gaming, restaking, etc.).
- **Exchange adapters** — pair-list and kline fetchers for additional exchanges.
- **Funding fallbacks** — additional reliable mirrors for restricted regions.
- **UI accessibility** — keyboard navigation, screen-reader labels, colour-contrast audits.

### Contribution rules

1. Keep the build **single-file**. The whole app must remain shippable as one `index.html`.
2. Keep dependencies **CDN-loaded and optional** (no npm).
3. Preserve the CC BY-NC-SA 4.0 license and the transparency footer.
4. Match the existing localization pattern — **all 5 languages** must be updated together.

---

## ❓ FAQ

**What's new in v14.9.0?**
**Old School Wisdom** — 9 quality features that codify decades of practical trading experience: MTF Trend Filter, Donchian/Bollinger/ATR bot ranges, Session Filter, Liquidity Guard, Symbol Unification, Cell Magnifier, STRONG row highlighting, Trade Plan v2 (TP1/TP2 + Chandelier), and freshness bonus in ranking. See the [What's new section](#-whats-new-in-v1490--old-school-wisdom) for details.

**Will v14.9.0 break my saved presets or settings?**
No. Presets live under their own key `gp_presets_v1` and are unaffected. Settings auto-migrate from `gp_settings_v14_8_2` (and all older versions back to `v14_5`) to the new `gp_settings_v14_9_0` key on first load.

**Why is MTF ON by default? Won't it reduce my signal count?**
Yes — it will reduce signals by ~40%. But the removed signals are overwhelmingly counter-trend false positives that would have lost money. If you want the old behaviour, uncheck **MTF TREND FILTER** in the right filter panel.

**What's the difference between Donchian, Bollinger, and ATR bot ranges?**
- **Donchian 26** (default) — uses the highest/lowest of the last 26 candles. Best for sideways markets.
- **Bollinger 20/2σ** — uses SMA(20) ± 2 standard deviations. Best for mean-reversion character.
- **ATR (legacy)** — the pre-v14.9.0 formula. Kept for backwards compatibility.

**Can I disable Liquidity Guard?**
No — it's always ON by design. If you want to trade a low-liquidity pair, use GRID mode (which doesn't require STRONG classification). The Guard exists to prevent STRONG-mode leveraged entries into pairs where slippage will kill your R:R.

**How does the Cell Magnifier work?**
Hover any table cell to see it enlarge 1.45× with a blue glow. Toggle the whole feature via the 🔍 button in the header or press **Shift+M**. Persistent across sessions via `localStorage['gp_mag']`.

**What is Chandelier trailing stop in Trade Plan v2?**
A technical trailing stop that tracks the highest high (for longs) or lowest low (for shorts) since entry, minus ATR × 3. It moves up with your winner but doesn't move against you. Classic swing-trading tool used by professional traders and CTAs since the 1990s.

**Why is Pionex the default exchange now?**
GridPulse v14.9.x is positioned as a companion tool for Pionex Grid Bots. The Launch Card output maps directly to Pionex Grid Bot parameters. Other exchanges (Bybit, Binance, KuCoin, OKX) are still fully supported — switching is one click away.

**Is my data sent anywhere?**
No. Indicators run client-side. The only outbound calls are exchange APIs (direct or via proxy), TradingView widget (only when you open a chart), Cloudflare Web Analytics beacon (anonymous), and — if you click "Open in Pionex" — the Pionex referral URL with UTM tags carrying only the setup classification.

**Where do I report bugs?**
[GitHub Issues](https://github.com/pro100off/gridpulse/issues). Include exchange + market, TF list, Strictness setting, MTF filter state (on/off), Bot Range mode, and a copy of the relevant Activity Log lines.

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License** (CC BY-NC-SA 4.0).

- ✅ Personal use
- ✅ Forking
- ✅ Modification
- ✅ Self-hosting with your own referral
- ❌ Commercial resale
- ⚠ Derivatives must keep the same license and link back to the original

See [LICENSE](LICENSE) for full terms.

---

## 🔗 All links one more time

- 🌐 Live demo: [https://tradescout.trade/](https://tradescout.trade/)
- 🪞 GitHub Pages mirror: [https://pro100off.github.io/gridpulse/](https://pro100off.github.io/gridpulse/)
- 💻 GitHub: [https://github.com/pro100off/gridpulse](https://github.com/pro100off/gridpulse)
- 🤝 Pionex (referral): [https://bit.ly/43bkdc7](https://bit.ly/43bkdc7)
- 📢 Telegram: [https://t.me/tradescoutfree](https://t.me/tradescoutfree)
- 🐦 Twitter / X: [https://x.com/tradeaiscout](https://x.com/tradeaiscout)
- 🐛 Issues: [https://github.com/pro100off/gridpulse/issues](https://github.com/pro100off/gridpulse/issues)
- 📋 Changelog: [CHANGELOG.md](CHANGELOG.md)
- 📖 User Guide: [GitHub.USER_GUIDE.md](GitHub.USER_GUIDE.md)
- 📝 Release notes v14.9.0: [docs/RELEASE_NOTES_v14.9.0.md](docs/RELEASE_NOTES_v14.9.0.md)
- 🚀 Latest release: [Releases](https://github.com/pro100off/gridpulse/releases/latest)
- 📜 License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

⚡ **GridPulse v14.9.0** · 🧙 **Old School Wisdom** · 🎯 **MTF Trend Filter** · 🤝 **Pionex Partner** · Built with care · single-file · no build tools · runs everywhere · © 2026 GridPulse Project
