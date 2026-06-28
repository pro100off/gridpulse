# ⚡ GridPulse v14.8.2 💾 Pair Presets

> **Free, open-source, multi-exchange crypto reversal screener** purpose-built as a **companion tool for Pionex Grid Bots** — with directional **STRONG / GRID BUY/SELL** modes, **TF-adaptive Strictness**, MACD + VWAP + ATR + ADX + Funding-aware setups across **Pionex, Bybit, Binance, KuCoin, and OKX** — and one-click **Launch Cards** with copy-paste-ready parameters that take you straight into a Pionex trading session.
>
> **v14.8.2** introduces **💾 Pair Presets** — save and reload named watchlists of pairs directly in your browser, with 5 built-in starter presets and shareable JSON / URL.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Version](https://img.shields.io/badge/version-14.8.2-blue.svg)](https://github.com/pro100off/gridpulse/releases/latest)
[![Pair Presets](https://img.shields.io/badge/💾-Pair%20Presets-42a5f5)](#-pair-presets-new-in-v1482)
[![Pionex Affiliate](https://img.shields.io/badge/🤝-Pionex%20Affiliate-26d97a)](https://bit.ly/43bkdc7)
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
| 📝 **Release notes v14.8.2** | [docs/RELEASE_NOTES_v14.8.2.md](docs/RELEASE_NOTES_v14.8.2.md) |
| 🐛 **Issues** | [GitHub Issues](https://github.com/pro100off/gridpulse/issues) |
| 🚀 **Latest release** | [Releases](https://github.com/pro100off/gridpulse/releases/latest) |

[![GridPulse Screenshot](docs/screenshot.png)](docs/screenshot.png)

---

## 🤝 Pionex Affiliate

GridPulse v14.8.x is positioned as a **dedicated companion tool for Pionex Grid Bots**. The project is enrolled in Pionex's **affiliate referral program** — Pionex is the **default exchange** for new users, and every Launch Card features a prominent **"Open in Pionex"** CTA with UTM-tagged deep links that carry the setup context (symbol, TF, mode) into your Pionex session.

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
- [💾 Pair Presets (new in v14.8.2)](#-pair-presets-new-in-v1482)
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
- [🧾 What's new in v14.8.2](#-whats-new-in-v1482)
- [📜 Version history (carried-over highlights)](#-version-history-carried-over-highlights)
- [⚠ Disclaimer](#-disclaimer)
- [💚 Transparency](#-transparency)
- [📊 Analytics](#-analytics)
- [🤝 Contributing](#-contributing)
- [❓ FAQ](#-faq)
- [📄 License](#-license)

---

## ✨ Features

- **💾 Pair Presets** — save/load named watchlists in browser, with 5 built-in starters (💎 Majors / 🐸 Memes / 🤖 AI / 🏛 Layer 1s / 💧 DeFi), JSON import/export, and shareable URLs
- **🤝 Built around Pionex** — Pionex is the default exchange; Launch Cards map directly to Pionex Grid Bot parameters
- **5 exchanges:** Pionex, Bybit, Binance, KuCoin, OKX (**Spot + USDT Futures**)
- **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, Volume ratio, R:R
- **TF-adaptive Strictness** — thresholds scale automatically by timeframe (**1m softer → 1W stricter**) with a global selector: **soft / normal / strict**
- **Two paths to STRONG setups:**
  - **Exhaustion** — blow-off trend + reversal candle
  - **Quality** — moderate trend + ⭐ VWAP confluence + strong R:R
- **Classified SKIP reasons** with exact per-row tooltip thresholds:
  - ⚡ **WATCH** — strong reversal candle present, but reward (R:R) too low
  - 🌊 **TREND** — market still trending too strongly, no valid reversal yet
  - ⚖ **LOW R:R** — poor reward relative to risk
- **Setup geometry validation** (v14.8.1+) — rejects stale setups where price already crossed entry/stop
- **Funding-aware setups** for perpetual contracts (current rate, 7-day average, daily / annual cost, hold-period projection, LONG/SHORT bias)
- **5 languages:** English · Українська · Español · Русский · 中文
- **Launch Cards** with copy-paste-ready Grid Bot parameters and a **prominent "Open in Pionex" CTA** with UTM tracking — five directional modes: STRONG BUY, GRID BUY, STRONG SELL, GRID SELL, SKIP
- **Pionex Only mode** — single header toggle that locks the screener to Pionex for a focused workflow
- **Breakout entry logic** — `limL` placed at the opposite extreme of the reversal candle (bearish → candle low, bullish → candle high)
- **TradingView integration** — open chart for any setup in one click, with symbol-fallback chain (Bybit ↔ Binance ↔ KuCoin)
- **CSV export** of all scan results (with funding columns)
- **Content-creator tools** — horizontal full screenshot, vertical 1080×1350 PNG Cards (top 5), vertical 1080×1350 PNG Table (top 15), 5-slide Carousel, daily watermark with scan serial counter
- **Privacy-first:** no signup, no cookies, no individual user tracking, no fingerprinting, GDPR-compliant
- **Light / Dark theme** with full localization and high-contrast rows
- **Auto-fallback proxies** — scan still completes even when one exchange API is blocked in your region
- **Custom domain support** — canonical URL: [https://tradescout.trade/](https://tradescout.trade/)
- **Zero-build single-file architecture** — entire app is one `index.html`
- **No npm, no webpack, no dependencies** — works on `file://`, GitHub Pages, Cloudflare Pages, Netlify, Vercel, Apache, nginx, Caddy, or any static host

---

## 🚀 Quick start

### Option A — Use the hosted version (no install)

1. Open [https://tradescout.trade/](https://tradescout.trade/)
2. The screener opens on **Pionex / Spot** by default (you can switch to Bybit / Binance / KuCoin / OKX anytime)
3. *(Optional)* Pick a **preset** from the dropdown (💎 Majors / 🐸 Memes / 🤖 AI Tokens / 🏛 Layer 1s / 💧 DeFi Blue Chips) — pairs fill in automatically
4. Select **timeframes** (defaults: 1h, 4h, 1D)
5. Optionally adjust **Strictness** (`soft` / `normal` / `strict`)
6. Click **▶ Scan** — results usually appear in ~30 seconds
7. Click 📋 next to any symbol to open the **Launch Card**
8. Click the big **🚀 Open in Pionex** button → the setup carries over via UTM-tagged deep link
9. Paste the parameters into a Pionex Grid Bot and manage the trade manually

### Option B — Self-host (1 command)

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
```

Or simply double-click `index.html` — it also works on `file://`.

---

## 💾 Pair Presets (new in v14.8.2)

Tired of pasting `BTCUSDT, ETHUSDT, SOLUSDT, ...` into Custom Pairs before every scan? v14.8.2 introduces **named watchlists** stored directly in your browser — no backend, no account, no cost.

### 5 built-in starter presets

Available immediately on first launch, no setup required:

| Icon | Name | Pairs |
|------|------|-------|
| 💎 | **Majors** | BTC · ETH · SOL · BNB · XRP · ADA · AVAX · DOT · LINK · MATIC |
| 🐸 | **Memes** | DOGE · SHIB · PEPE · WIF · BONK · FLOKI · MEME · POPCAT · BRETT · TURBO |
| 🤖 | **AI Tokens** | FET · AGIX · OCEAN · RNDR · TAO · WLD · GRT · AKT · ARKM · NMR |
| 🏛 | **Layer 1s** | ETH · SOL · AVAX · NEAR · APT · SUI · SEI · INJ · TIA · TON |
| 💧 | **DeFi Blue Chips** | UNI · AAVE · MKR · LDO · SNX · CRV · COMP · SUSHI · GMX · PENDLE |

Built-in presets cannot be edited or deleted — they always reload to defaults. If you want a tweaked version, save it as a new user preset.

### Save your own preset

1. Type pairs into the **Custom Pairs** textarea (comma or space separated)
2. Click **💾 Save as…** next to the preset dropdown
3. Enter a **name** (up to 40 chars), pick an **icon** (20 emoji options)
4. Click **💾 Save**

The preset appears under "My Presets" and is applied immediately.

### Manage presets

Click **⚙ Manage** to open the management modal:

- **✓ Apply** — load the preset and close the modal
- **🗑 Delete** — remove the preset (with confirmation)

### Import / Export

In the ⚙ Manage modal:

- **📤 Export JSON** — downloads `gridpulse_presets_YYYY-MM-DD.json` with all user presets
- **📥 Import JSON** — upload a previously exported file; imported presets are added (not replaced)

JSON format is human-readable:

```json
{
  "version": 1,
  "exportedAt": "2026-06-27T18:34:12.000Z",
  "presets": [
    {
      "id": "p_lwf2k_a3b8c",
      "name": "My AI Watchlist",
      "icon": "🤖",
      "pairs": ["BTCUSDT", "ETHUSDT", "RNDR", "FET", "TAO"],
      "createdAt": 1719511234567
    }
  ]
}
```

### Shareable preset URL

Share a single preset via URL:

```text
https://tradescout.trade/?preset=<base64-encoded-json>
```

When someone opens that link, they see a **consent prompt** asking whether to import the preset (with name + pair count shown). On accept, the preset is added to their local storage and applied. The `?preset=` parameter is then stripped from the URL.

### Storage isolation

Presets live under their own key `gp_presets_v1` — **independent** from `gp_settings_v14_8_2`. This means:

- Resetting screener settings **never** deletes your presets
- Version bumps **don't** invalidate your watchlists
- The two systems evolve separately

| Storage key | Purpose |
|-------------|---------|
| `gp_presets_v1` | All your user presets (JSON array) |
| `gp_preset_last` | ID of the last-applied preset (auto-restored on reload) |
| `gp_settings_v14_8_2` | Screener settings (TFs, filters, theme, sound) — independent |

> 💡 **Pro tip:** Combine presets with the **🤝 Pionex Only** toggle in the header for a fully locked-in workflow — one click selects the watchlist, exchange, and market type.

For a step-by-step walkthrough with screenshots, see [GitHub.USER_GUIDE.md § 3](GitHub.USER_GUIDE.md#3-pair-presets-new-in-v1482).

---

## 🤝 Pionex companion workflow

GridPulse v14.8.x is designed around a **focused, two-tool workflow**:

```text
┌─────────────────────────┐                ┌─────────────────────────┐
│  GridPulse              │                │  Pionex                 │
│  (scan + plan)          │  ────────►     │  (execute)              │
│                         │  Open in       │                         │
│  • Pick preset 💾       │  Pionex CTA    │  • Grid Bot             │
│  • Multi-TF scan        │  + UTM tags    │  • Reverse Grid         │
│  • Launch Card          │                │  • Smart Trade          │
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
| Esc | Close any open modal (chart / Launch Card / preset modals) |
| Double-click row | Highlight selected row, dim others |

> **Tip:** Hotkeys are ignored while typing inside `<input>`, `<textarea>`, or `<select>` so you can keep typing custom pair lists without conflicts.

---

## 🧠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for restricted regions) and calculates all indicators client-side in your browser.

```text
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
2. **Cloudflare Worker proxy** (rate-limited shared instance) — see [Optional Cloudflare Worker proxy](#-optional-cloudflare-worker-proxy)
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
| **STRONG BUY** | bullish | Two routes (see [Two paths to STRONG](#-two-paths-to-strong)). Thresholds are TF-adaptive and globally tuned by Strictness. | Limit buy + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID BUY** | bullish | Moderate trend + controlled VWAP distance + acceptable reward/risk. Thresholds scale by TF / Strictness. | Grid lower / upper / width / lines + ATR-based SL + ATR-based TP |
| **STRONG SELL** | bearish | Mirror of STRONG BUY | Limit sell + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID SELL** | bearish | Mirror of GRID BUY | Grid lower / upper / width / lines + ATR-based SL + ATR-based TP |
| **SKIP** | any | Setup does not qualify; classified into WATCH / TREND / LOW R:R with tooltip explanation | Reference price + warning |

### Mode sort priority

Results table is sorted (when sorting by Mode column) as:

```text
STRONG_BUY  ≡  STRONG_SELL  >  GRID_BUY  ≡  GRID_SELL  >  SKIP
```

Within the same priority, ties are broken by R:R then by depth.

### Setup geometry validation (v14.8.1+)

Stale setups where price has **already crossed** the entry or stop before the scan are now rejected automatically:

- **Bullish:** rejected if `price ≤ stopL` or `price ≥ limL`
- **Bearish:** rejected if `price ≥ stopL` or `price ≤ limL`

This prevents the Launch Card from showing "ghost" setups that would be impossible to enter.

---

## 🎯 TF-adaptive Strictness

Unlike previous versions with static cutoffs, v14.7.6+ scales every threshold by:

```text
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

**Example:** On 4h / normal, STRONG ADX threshold = 25 × 1.00 × 1.00 = **25**. On 1W / strict, it becomes 25 × 1.20 × 1.30 = **39**. On 5m / soft, it drops to 25 × 0.78 × 0.75 ≈ **14.6**.

This is also reflected in the right-side filter panel:

- **ADX ≥ 18** checkbox → effective threshold scales with TF / Strictness
- **R:R ≥ 1.5** checkbox → effective threshold scales with TF / Strictness

---

## 🛡 Classified SKIP reasons

When a setup doesn't qualify for STRONG or GRID, it's no longer a generic "skip". It's classified, with the exact failing thresholds shown in a per-row tooltip.

| Tag | Meaning |
|-----|---------|
| ⚡ **WATCH** | A strong reversal candle is already present, but R:R is too low for entry. Worth keeping on a watchlist for a possible re-entry on a pullback. |
| 🌊 **TREND** | Market is still trending too strongly for grid, and there is no reversal candle yet. Wait for exhaustion. |
| ⚖ **LOW R:R** | The reward is too small relative to the risk. Filter caught it before entry. |
| 🛡 **SKIP** | Edge case that doesn't match any of the above categories. |

### Tooltip example

```text
[4h/normal] ADX 31.2≥28.0 (too trendy for grid) · |VWAP| 6.1%>5.0%
   · strong reversal candle but R:R too low — watch for re-entry
```

This means the row is WATCH, on the 4h timeframe with normal Strictness, and it tells you exactly which numeric thresholds were exceeded.

---

## ⭐ Two paths to STRONG

A STRONG setup can be unlocked in two different ways, so trades aren't gated solely on extreme blow-off conditions.

### 1️⃣ Exhaustion route

The classic blow-off / trend-exhaustion entry:

- ADX ≥ TF-scaled 25
- |VWAP%| > TF-scaled 5
- Volume ≥ 1.5×
- R:R ≥ 2.0
- depth ≥ 5
- Reversal candle present

### 2️⃣ Quality route

Sometimes a clean reversal happens at moderate trend strength. The Quality route catches those by requiring:

- ADX ≥ ~18 (≈ 72 % of the Exhaustion threshold)
- |VWAP%| > ~3 % (≈ 60 % of the Exhaustion threshold)
- Volume ≥ 1.5×
- R:R ≥ 2.0
- depth ≥ ~7 (≈ 140 % of the Exhaustion threshold)
- Reversal candle present
- ⭐ **VWAP confluence required**

Both routes still scale with TF and Strictness.

A subtitle in the Mode tooltip tells you which route fired:

- **Exhaustion (trend blow-off)**
- **Quality (⭐ VWAP confluence)**

---

## 📊 Indicators reference

| Indicator | Period | Notes |
|-----------|--------|-------|
| MACD | 12 / 26 / 9 | Used for divergence + histogram window |
| VWAP | 50 | Rolling, volume-weighted |
| VWAP bands | 50, ±1σ / ±2σ | Used for ⭐ confluence detection |
| ATR | 14 | Drives candle-size filter and Grid SL/TP |
| ADX | 14 | Trend strength; reused for grid range width |
| Volume ratio | last vs. avg of 20 | Used for Vol ≥ 1.1× / 1.5× filters |
| R:R | derived from limit / stop / next swing | Reward-to-risk |

### Reversal candle detection

A **bearish reversal candle** (for a BEAR / STRONG_SELL setup) is the first down-close candle whose high is the highest within the last `Extremum` window (default 5 candles). The next candle must also close down, with high ≤ reversal-candle high.

Bullish reversal mirrors this.

### Entry geometry (limL / stopL / stopC)

For a **bearish** setup:

- `limL` = reversal candle low (breakout-against-trend entry)
- `stopL` = max high of the last 7 candles up to and including the reversal candle
- `stopC` (conservative) = reversalHigh + 2 × (reversalHigh − reversalLow)

For a **bullish** setup, all extremes are mirrored.

### ⭐ VWAP confluence

A setup gets the ⭐ tag when `limL` lands within a tight band around any of:

- VWAP
- VWAP ± 1σ
- VWAP ± 2σ

The tolerance is small (< 0.5 % of price), so this is a real confluence — not just "near VWAP".

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

If ATR is missing, the screener falls back to a fixed 15 % / 20 % rule.

---

## 💰 Funding-aware logic

Only active on **USDT Futures** market.

When enabled, the screener fetches funding data and uses it to:

- show current rate, avg 7d (over 21 payments), daily (×3 sessions), annualized, hold-period cost, and next-payment countdown
- compute a directional bias label:
  - 🟢 LONG-friendly / 🔴 LONG-costly
  - 🟢 SHORT-friendly / 🔴 SHORT-costly
  - ➖ Neutral
- optionally **SKIP** setups that exceed your configured daily funding threshold

### Funding settings

| Setting | Effect |
|---------|--------|
| **CONSIDER FUNDING** | Master switch (Futures only) |
| **USE 7-DAY HISTORY** | Use the 21-sample average instead of the current rate |
| **SKIP IF EXCEEDS THRESHOLD** | Drop adverse rows beyond Max daily funding |
| **Max daily funding** | 0.05% / 0.10% / 0.20% / 0.30% / 0.50% / 1.00% |
| **Hold (days)** | Time horizon for the cost projection in the Launch Card |

### Funding fallback chain

For **Binance Futures** funding under GeoIP block, GridPulse falls back to Bybit's tickers endpoint so the field is still populated. For **Pionex**, it tries:

1. pionex `/market/indexes`
2. pionex `/market/fundingRates`
3. Bybit fallback by base symbol

This is logged transparently with a "Funding source" line in the Launch Card.

---

## 🎛 Settings & filters

All settings are persisted in `localStorage` under the key `gp_settings_v14_8_2` and **auto-migrated** from earlier versions (`v14_8_1`, `v14_8_0`, `v14_7_6`, `v14_7_5`, `v14_7_4`, `v14_7_3`, `v14_7_2`, `v14_7`, `v14_6`, `v14_5`).

Presets use a separate storage key `gp_presets_v1` that's **independent** from settings — clearing settings does not delete presets.

### Left panel — Timeframes & depth

| Control | Description |
|---------|-------------|
| **Timeframe row** | Pick any combination of 1m / 5m / 15m / 30m / 1h / 4h / 1D / 1W / 1M. Click ALL to toggle all. Disabled (struck-through) TFs are unsupported by the current exchange. |
| **Search depth** | How many bars back to look for a reversal pattern. |
| **Min TF** | Minimum number of timeframes that must produce a hit for the symbol to be shown. |
| **Extremum** | Lookback window used when validating the reversal candle's extreme. |
| **Strictness** | soft / normal / strict — global multiplier on every threshold. |

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
| **VWAP filters** | VWAP DIRECTION (price must be on the right side of VWAP) · VWAP CONFLUENCE (require ⭐) |
| **Candle filters** | ATR SIZE ×0.8 · VOLUME ×1.1 |
| **Trend / R:R** | ADX ≥ 18 · R:R ≥ 1.5 (both TF-scaled) |
| **Funding (Futures only)** | CONSIDER FUNDING · USE 7-DAY HISTORY · SKIP IF EXCEEDS THRESHOLD |

### Preset bar (new in v14.8.2)

A dedicated control row between the action buttons and Custom Pairs textarea:

| Control | Description |
|---------|-------------|
| **Preset dropdown** | Pick from 5 built-in starters + your saved user presets. Auto-restores last-used preset on reload. |
| **💾 Save as…** | Save current Custom Pairs as a new preset with name and icon. |
| **⚙ Manage** | Open management modal: apply, delete, import/export JSON. |

### Header toggles

| Toggle | Effect |
|--------|--------|
| ⭐ **Star on GitHub** | Direct link to the repo |
| 🌐 **Language** | EN / UA / ES / RU / ZH switcher |
| 🌙 / ☀️ **Theme** | Dark / Light |
| 🔊 / 🔇 **Sound** | Scan-tick audio synth (WebAudio) |
| 🤝 **Pionex Only** | Lock exchange to Pionex (persists in `localStorage`) |

---

## 📋 Launch Cards

Each row in the results table has a 📋 button. Clicking it opens a **Launch Card** — a focused, copy-paste-ready trading plan with a prominent **"Open in Pionex"** CTA.

### Launch Card layouts per mode

**STRONG BUY / STRONG SELL**

- Entry (Buy/Sell Price) — limL
- Stop Loss — stopL
- Conservative SL — stopC
- Fixed Take Profit — calculated from R:R
- Trailing trigger — ±10 % from entry
- Max trailing drawdown — 5–7 %
- Position size — 10–20 % of capital

**GRID BUY / GRID SELL** (Pionex Grid Bot ready)

- Lower Limit — bot range low
- Upper Limit — bot range high
- Range width — % of price
- Grid lines count — 30 / 40 / 50 depending on width
- Grid mode — Geometric
- Investment — tokens (base asset)
- Stop Loss — ATR-based (see table above)
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
- Buttons:
  - 📋 Copy all (full plain-text plan)
  - 📊 Open chart (TradingView)
  - ✈️ Share to Telegram
  - **🚀 Open in Pionex** (large full-width gradient CTA with UTM tags)

All numeric values are click-to-copy with a confirmation toast.

### UTM tracking on Pionex deep links

When you click **"Open in Pionex"** from a Launch Card, the destination URL is enriched with UTM parameters that carry the setup context:

```text
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
| Full screenshot | 📸 Screenshot button | Horizontal PNG of the whole results section, with watermark and daily scan serial |
| Vertical PNG Cards | Shift + P (TikTok mode) | 1080×1350 PNG of the top 5 setups as readable cards |
| Vertical PNG Table | Shift + Alt + P (TikTok mode) | 1080×1350 PNG of the top 15 setups in compact table form |
| 5-slide Carousel | Shift + C | Five 1080×1350 PNGs: Cover · Top 1 · Top 2 · Top 3 · CTA |
| Daily scan serial | Auto | Per-day counter stored in `localStorage`, included in every export filename + watermark |
| TikTok pager | Shift + T then ◀ ▶ | Paginates results 10 rows per page, ready for vertical video recording |

On iOS, screenshots open in a new tab with instructions to long-press → Save to Photos.

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

### Language priority

1. URL query: `?lang=en`, `?lang=ua`, `?lang=es`, `?lang=ru`, `?lang=zh`
2. `localStorage` preference (`gp_lang`)
3. `navigator.language` autodetect
4. Fallback: English

### What's localized

- All controls, labels, placeholders (including the **Pionex Only** toggle and Strictness selector)
- All log entries
- All Launch Card sections (including the "Open in Pionex" CTA)
- All mode labels and SKIP categories (WATCH / TREND / LOW R:R)
- Funding bias labels
- Welcome hint
- Footer disclosure and license text
- All screenshot / carousel slide content
- All sharing templates (Telegram share text)
- **NEW in v14.8.2:** Full preset UI translation (50+ keys) — dropdown labels, save/manage modals, confirmation prompts, URL import dialog

### Hreflang & SEO

The single-file build ships with hreflang alternates and an `inLanguage` array in JSON-LD so that search engines can correctly serve the right localized URL.

---

## 🛠 Self-hosting

GridPulse is a **single `index.html` file**. There are no build tools, no npm dependencies, and no server-side code.

### 1-minute setup

```bash
# Clone
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse

# Serve locally (any of these work)
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

The single file pulls a few libraries from CDN at runtime:

| Library | Purpose | CDN |
|---------|---------|-----|
| qrcodejs | QR code for Pionex referral | cdnjs |
| html2canvas | PNG / carousel rendering | cdnjs |
| tv.js | TradingView embedded widget | s3.tradingview.com (lazy-loaded only when a chart is opened) |
| Cloudflare Web Analytics | Anonymous traffic counter | static.cloudflareinsights.com |

You can self-host these by replacing the `<script src=...>` tags in `index.html`.

---

## 🔄 Optional Cloudflare Worker proxy

For improved Pionex / Binance reliability in restricted regions, you can deploy your own Cloudflare Worker proxy.

The default deployment uses:

```text
https://gridpulse-proxy.pro100off.workers.dev/?url=
```

This is a rate-limited shared instance. If you fork GridPulse, please deploy your own and update the `CUSTOM_PROXY` constant near the top of the `<script>` block in `index.html`:

```javascript
const CUSTOM_PROXY = 'https://YOUR-WORKER.workers.dev/?url=';
```

A minimal worker is enough — it just needs to forward `?url=<target>` and pass the JSON response back with appropriate CORS headers.

---

## 📁 Repository structure

```text
gridpulse/
├── index.html                       current release (v14.8.2)
├── LICENSE                          CC BY-NC-SA 4.0
├── README.md                        this file
├── CHANGELOG.md                     full version history
├── GitHub.USER_GUIDE.md             detailed user guide
├── docs/
│   ├── screenshot.png               preview image (OG / social cards)
│   └── RELEASE_NOTES_v14.8.2.md     short release notes
└── legacy/                          archived previous versions
    ├── index-v14.2.html
    ├── index-v14.3.html
    ├── index-v14.5.html
    ├── index-v14.7.5.html
    ├── index-v14.7.6.html
    ├── index-v14.8.0.html
    └── index-v14.8.1.html
```

---

## 🧾 What's new in v14.8.2

This is a **UX productivity release** that introduces a long-requested feature: **persistent named watchlists**. No scanning logic was changed.

### 💾 Pair Presets — save your watchlists in one click

The flagship feature: save any list of pairs as a named preset stored directly in your browser, with no backend, no account, and no cost.

**5 built-in starter presets** are shown immediately on first launch:

| Icon | Name | Pairs |
|------|------|-------|
| 💎 | **Majors** | 10 large-cap coins |
| 🐸 | **Memes** | 10 high-volatility meme tokens |
| 🤖 | **AI Tokens** | 10 AI-narrative tokens |
| 🏛 | **Layer 1s** | 10 smart-contract platforms |
| 💧 | **DeFi Blue Chips** | 10 established DeFi protocols |

**Save your own** via the new **💾 Save as…** button — name it, pick from 20 emoji icons, save. Done.

**Manage** via **⚙ Manage** modal — apply, delete, import/export JSON.

**Share** a preset via URL: `tradescout.trade/?preset=<base64-json>` — recipient sees a consent prompt before importing.

**Auto-restore** — your last-used preset is automatically selected on the next visit.

See the dedicated [💾 Pair Presets section](#-pair-presets-new-in-v1482) for the full breakdown.

### 🔐 Storage isolation

Presets live under their own key `gp_presets_v1` — **independent** from `gp_settings_v14_8_2`. Clearing screener settings does not delete presets, and version bumps don't invalidate them.

### 🌐 Full i18n for preset UI

50+ new translation keys across EN / UA / ES / RU / ZH for the entire preset workflow — dropdown, modals, confirmation prompts, URL import dialog.

### 💾 Settings migration

- New storage key: `gp_settings_v14_8_2`
- Automatic migration from `v14_8_1` → `v14_8_0` → … → `v14_5`
- Preset key `gp_presets_v1` is brand new (no migration needed)
- Welcome hint key: `gp_visited_v1480` → `gp_visited_v1482`

### 🐛 No breaking changes

All v14.8.1 scanning logic, geometry validation, classification, TF-adaptive thresholds, Strictness selector, classified SKIP reasons, Pionex companion positioning, Launch Card layouts, and ATR-based GRID SL/TP behaviour are **preserved unchanged**.

---

## 📜 Version history (carried-over highlights)

Full history lives in [CHANGELOG.md](CHANGELOG.md).

### v14.8.1 — "Setup geometry validation"

- 🐛 **Bugfix:** stale setups where price already crossed entry/stop before scan no longer pass the filter
- Strict geometry check added at end of `findSetup()`:
  - Bullish: rejects rows where `price ≤ stopL` or `price ≥ limL`
  - Bearish: rejects rows where `price ≥ stopL` or `price ≤ limL`
- `SET_KEY` → `gp_settings_v14_8_1`

### v14.8.0 — "Pionex Companion"

- 🤝 **Official Partner badge** — visible "Official Partner" marker next to Pionex branding in header, referral banner, and Launch Card footer
- Pionex set as **DEFAULT exchange** (was Bybit)
- Prominent **"Open in Pionex" CTA** in Launch Card — large gradient button with UTM tags
- Larger, more visible referral QR code (64 → 96 px in banner; 46 → 84 px in Launch Card)
- New filter: **"Pionex Only" mode** — locks the exchange dropdown to Pionex
- Launch Card readability boost — base font sizes increased across the board
- Modal max-width 560 → 640 px
- `SET_KEY` → `gp_settings_v14_8_0`

### v14.7.6 — "TF-adaptive thresholds"

- TF-adaptive Strictness — every threshold scales by TF × Strictness
- Two paths to STRONG (Exhaustion + Quality routes)
- Classified SKIP reasons — ⚡ WATCH / 🌊 TREND / ⚖ LOW R:R with per-row tooltip
- Dual TikTok PNG export — Cards (top 5) and Table (top 15)
- ATR-based GRID SL/TP with TF multipliers
- Custom domain — [https://tradescout.trade/](https://tradescout.trade/)
- Hreflang & SEO for all 5 languages
- `SET_KEY` → `gp_settings_v14_7_6`

### v14.7.5

- Directional Grid Modes — replaced unified BOT mode with STRONG_BUY / GRID_BUY / STRONG_SELL / GRID_SELL / SKIP
- Breakout entry logic — limL now points at the opposite extreme of the reversal candle
- Light theme contrast boost — zebra rows, accent-coloured badges with visible borders, no text-shadow blur, contrast-compliant numeric cells
- Light TikTok mode — vertical layout no longer forces black background when light theme is active
- Hotkeys panel — floating ⌨ button (bottom-left) listing all shortcuts
- TikTok-branded UI hidden — TikTok PNG button, Carousel button, vertical-mode toggle, and Launch Card "Export for TikTok" no longer visible. All functions retained, accessible via hotkeys.
- Fixed STRONG SELL Launch Card silently failing (stray Cyrillic char)
- Fixed carousel indicators array (duplicate VWAP% fragment)
- `SET_KEY` → `gp_settings_v14_7_5`

### v14.7.4

- Dark theme contrast boost — brighter text (#f0f4fa), brighter table headers with accent underline + text-shadow, stronger BUY/SELL colours (#26d97a / #ff4566), brighter VWAP / funding cells (.dg / .dr / .dy / .dc / .dp)
- Restored full referral banner UA i18n keys (ref.sub, ref.f2)
- Restored full footer disclosure UA text (foot.disclosure)
- Version markers updated everywhere (title, meta, JSON-LD, ready log, CSV filename, screenshot filename, watermark, lic-mark)
- `SET_KEY` → `gp_settings_v14_7_3`

### v14.7.2

- tt-watermark hidden by default (`display:none`); only shows in TikTok mode
- `updateTTWatermark()` only runs when TikTok mode is on
- Removed redundant `playTick('tick')` — no more audio noise on every miss
- Highlight Row uses double-click (`ondblclick`)
- tt-watermark positioning hardened (right offset + z-index)
- Redesigned carousel slides: zero dead zones

### v14.7.1

- Redesigned 5-slide carousel layout (now used in v14.7.6+)

### v14.7

- 📱 TikTok Mode (Shift+T) — vertical layout, paginated table
- ✨ Highlight Row — spotlight selected row, dim others
- 🏷 Auto-watermark with daily scan serial counter (`localStorage`)
- 📱 Export for TikTok button on Launch Card → 1080×1350 PNG
- 🎬 Auto-Carousel — 5-slide pack (cover + top 3 + CTA)
- 🔊 Scan tick sound (WebAudio synth, no asset deps)
- 🛡 Bold SKIP visual — shield icon, prominent border

### v14.6

- Screenshot button (with watermark + TikTok variants)
- Binance Futures 451 → Bybit mirror fallback
- Pionex PERP discovery, 1M=null, KuCoin direct fetch
- `safeFetch` early-return on API-error payload

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

The 🤝 **Pionex Affiliate** badge reflects participation in the affiliate referral program — Pionex does not direct the screener's classification logic, does not pay for ranking, and does not have any editorial control over the project. There is **no legal/contractual partnership** beyond standard affiliate-program terms.

### Why Pionex specifically?

Pionex's Grid Bot is one of the few exchange-native automation products whose parameters map cleanly to a screener's output (Lower Limit / Upper Limit / Grid Lines / SL / TP). That made it the natural execution target for GridPulse Launch Cards. Other exchanges are still fully supported — Pionex is just the **default** and the **deepest Launch Card integration**.

### Forking

Forks with your own referral are welcome — please keep:

- a visible link back to the original repository,
- the CC BY-NC-SA 4.0 license,
- and the transparency disclosure in the footer.

If you fork the project, please use your **own affiliate code** for the Pionex referral link, and update or remove the 🤝 Pionex Affiliate badge wording to reflect *your* relationship with Pionex (or remove it entirely if you are not an affiliate yourself).

---

## 📊 Analytics

GridPulse uses **Cloudflare Web Analytics** for anonymous, aggregate traffic statistics (page views, country breakdown, referrers).

| Property | Status |
|----------|--------|
| Cookies | ❌ none |
| Personal data | ❌ none |
| Individual tracking | ❌ none |
| Fingerprinting | ❌ none |
| GDPR-compliant | ✅ yes |
| Open about what's tracked | ✅ yes |

All user-specific settings (theme, language, last-used filters, scan serial, custom pairs draft, **saved presets**) stay in your browser's `localStorage` and **never leave your device**.

---

## 🤝 Contributing

Issues and PRs are welcome.

For major changes, please open an issue first so we can discuss direction.

### Especially appreciated

- **Translations** — adding new languages or improving existing ones (EN / UA / ES / RU / ZH).
- **Built-in presets** — proposing curated starter presets for new themes (RWA tokens, gaming, restaking, etc.).
- **Exchange adapters** — pair-list and kline fetchers for additional exchanges.
- **Funding fallbacks** — additional reliable mirrors for restricted regions.
- **UI accessibility** — keyboard navigation, screen-reader labels, colour-contrast audits.

### Contribution rules

1. Keep the build **single-file**. The whole app must remain shippable as one `index.html`.
2. Keep dependencies **CDN-loaded and optional** (no npm).
3. Preserve the CC BY-NC-SA 4.0 license and the transparency footer.
4. Match the existing localization pattern when introducing new strings — **all 5 languages** must be updated together.
5. If you remove the Pionex affiliate branding in your fork, also remove the 🤝 Pionex Affiliate badge — it specifically refers to the upstream project's affiliate-program participation.

---

## ❓ FAQ

**What's new in v14.8.2?**
**Pair Presets** — save and reload named watchlists of pairs directly in your browser. 5 starter presets are built in (Majors, Memes, AI Tokens, Layer 1s, DeFi Blue Chips), and you can save your own with custom names and icons. Full JSON import/export and shareable URLs. See the [💾 Pair Presets section](#-pair-presets-new-in-v1482) for details.

**Will my saved presets survive a settings reset?**
Yes. Presets are stored under their own key `gp_presets_v1`, completely **independent** from `gp_settings_v14_8_2`. Resetting screener settings does not delete presets. Version bumps do not invalidate them.

**Will my presets transfer to a new device automatically?**
No — `localStorage` is per-browser, per-device. To transfer:
1. ⚙ Manage → 📤 Export JSON on the source device
2. Email / cloud-sync the JSON file
3. ⚙ Manage → 📥 Import JSON on the target device

Or, for a single preset, use the shareable URL: `tradescout.trade/?preset=<base64-json>` — recipient sees a consent prompt before importing.

**My presets disappeared after clearing browser data!**
Presets live in `localStorage`. Clearing "Site data" or "All browsing data" removes them — that's how browsers work, not a bug. **Always export to JSON before clearing.**

**Why is Pionex the default exchange now?**
GridPulse v14.8.x is positioned as a companion tool for Pionex Grid Bots. The Launch Card output maps directly to Pionex Grid Bot parameters (Lower Limit, Upper Limit, Grid Lines, ATR-based SL/TP). Other exchanges (Bybit, Binance, KuCoin, OKX) are still fully supported via the dropdown — switching is one click away.

**What does "Pionex Affiliate" mean?**
It means the project is enrolled in Pionex's **affiliate referral program** — the author earns a referral commission when users sign up via the link and trade. It does **not** mean Pionex controls the screener's logic, pays for ranking, or has any editorial input, and it is not a legal/contractual partnership. The classification logic is fully open-source — read it in `index.html`.

**Can I use GridPulse without signing up on Pionex?**
Absolutely. GridPulse is 100 % free and requires no signup on anything. The Pionex referral is optional and supports the project, but every feature works without it.

**Why does Binance Futures sometimes show "Bybit mirror" in the log?**
Some regions return HTTP 451 for `fapi.binance.com`. GridPulse mirrors the pair list and klines from Bybit so your scan still completes — and clearly logs that the fallback happened.

**Why is 1M greyed out on Pionex?**
Pionex's klines API does not currently expose a monthly interval, so the 1M button is disabled (and visually struck-through) when Pionex is selected.

**My scan returns zero rows — what's wrong?**
Check the Activity Log (bottom of the page). The most common causes:

- All proxies are rate-limited at once — wait ~30 seconds and retry.
- You picked a market the chosen exchange doesn't support (e.g. inverse pairs).
- Top MCap filter is too aggressive — try 200 or All.
- Strictness is set to `strict` on a low TF — try `normal` or `soft`.
- Setup geometry validation (v14.8.1+) rejected a stale setup where price already crossed entry or stop.

**Can I scan custom pairs only?**
Yes. Either pick a **preset** from the dropdown, or click **Custom pairs** and paste a comma/space/newline-separated list (e.g. `BTCUSDT, ETHUSDT, SOLUSDT`). GridPulse normalizes the format per exchange (`BTC-USDT` for KuCoin spot, `BTC_USDT_PERP` for Pionex perps, `BTC-USDT-SWAP` for OKX, etc.).

**Is my data sent anywhere?**
No. Indicators run client-side. The only outbound calls are:

- exchange APIs (direct or via proxy),
- TradingView widget (only when you open a chart),
- Cloudflare Web Analytics beacon (anonymous, aggregate),
- and — if you click "Open in Pionex" — the Pionex referral URL with UTM tags carrying only the setup classification (no personal data).

**Why CC BY-NC-SA?**
Because GridPulse is free, but commercial resale is prohibited. Forks and personal use are encouraged. See [LICENSE](LICENSE).

**Where do I report bugs?**
[GitHub Issues](https://github.com/pro100off/gridpulse/issues). Include:

- exchange + market,
- TF list,
- Strictness setting,
- preset name (if related),
- a copy of the relevant Activity Log lines.

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
- 📝 Release notes v14.8.2: [docs/RELEASE_NOTES_v14.8.2.md](docs/RELEASE_NOTES_v14.8.2.md)
- 🚀 Latest release: [Releases](https://github.com/pro100off/gridpulse/releases/latest)
- 📜 License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

⚡ **GridPulse v14.8.2** · 💾 **Pair Presets** · 🤝 **Pionex Affiliate** · Built with care · single-file · no build tools · runs everywhere · © 2026 GridPulse Project
