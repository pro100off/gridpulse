# ⚡ GridPulse v14.2 — User Guide

**Multi-Exchange Crypto Reversal Screener**

> Free, open-source tool that scans Bybit, Binance, KuCoin, OKX and Pionex for MACD-based reversal setups, enriches them with VWAP / ATR / ADX / R:R / Funding analysis, and generates one-click "Launch Cards" for Pionex Grid Bots and Smart Trade orders.

- **Live demo:** https://pro100off.github.io/gridpulse/
- **Source:** https://github.com/pro100off/gridpulse
- **License:** CC BY-NC-SA 4.0
- **Disclaimer:** This is an analytical tool, **not financial advice**. Crypto trading is risky. Always do your own research (DYOR).

---

## Table of Contents

1. [What GridPulse Does](#1-what-gridpulse-does)
2. [How a Scan Works (Pipeline)](#2-how-a-scan-works-pipeline)
3. [Quick Start](#3-quick-start)
4. [Interface Overview](#4-interface-overview)
5. [Left Panel — Timeframes & Depth](#5-left-panel--timeframes--depth)
6. [Right Panel — Exchange, Filters & Boosters](#6-right-panel--exchange-filters--boosters)
7. [The Funding Block (Futures Only)](#7-the-funding-block-futures-only)
8. [Action Buttons](#8-action-buttons)
9. [Counters Bar](#9-counters-bar)
10. [Results Table — Every Column Explained](#10-results-table--every-column-explained)
11. [Trading Modes (BUY / SELL / BOT / SKIP)](#11-trading-modes-buy--sell--bot--skip)
12. [Launch Cards](#12-launch-cards)
13. [TradingView Charts](#13-tradingview-charts)
14. [Custom Pairs & CSV Export](#14-custom-pairs--csv-export)
15. [Language, Theme & Saved Settings](#15-language-theme--saved-settings)
16. [Proxies, Caching & Rate Limits](#16-proxies-caching--rate-limits)
17. [Troubleshooting](#17-troubleshooting)
18. [Glossary](#18-glossary)

---

## 1. What GridPulse Does

GridPulse looks for **momentum-reversal setups** across crypto trading pairs. Its core engine is the **MACD histogram**: it locates points where momentum was peaking (bearish setup) or bottoming (bullish setup), then confirms the turn with a candle pattern and a battery of optional technical filters.

For every confirmed setup it calculates:

- **Entry (Limit)** and **Stop Loss** levels (standard and conservative).
- **Risk : Reward (R:R)** ratio.
- **VWAP** distance and band confluence.
- **ATR** (volatility) and **ADX** (trend strength).
- For futures: **Funding Rate** (now, 7-day average, daily cost, annualized, hold-period cost).
- A recommended **trading Mode** (Grid Buy / Grid Sell / Grid Bot / Skip) plus suggested **bot ranges**.

It then produces a **Launch Card** — a ready-to-use parameter sheet for executing the trade on Pionex.

GridPulse runs **entirely in your browser**. No account, no server, no data is stored remotely. All API calls go directly to exchanges or through public CORS proxies.

---

## 2. How a Scan Works (Pipeline)

When you press **▶ Scan**, GridPulse runs these steps in order:

1. **Read settings** — exchange, market, timeframes, depth, filters, funding options.
2. **Fetch Market Cap ranking** from CoinGecko (used to rank/limit pairs by Top MCap).
3. **Fetch the pair list** for the chosen exchange/market (or use your Custom Pairs).
4. **Filter by Top MCap** if a limit is set.
5. **For each pair**, for each selected timeframe:
   - Download candles (klines).
   - Compute the MACD histogram.
   - Run `findSetup()` to detect a reversal and validate it against every enabled filter.
6. **If a pair has enough timeframe hits** (≥ Min TF), optionally fetch its **Funding Rate**.
7. **Apply Funding-Skip** if enabled and the rate is adverse beyond your threshold.
8. **Rank results** by Market Cap, trim to **Max**, and render the table.
9. Log a warning if **0 klines loaded** (proxy/exchange blocked → set a custom proxy).

---

## 3. Quick Start

1. Open the live demo or your own GitHub Pages deployment.
2. Leave the defaults (Exchange = **Pionex**, Market = **Spot**, Timeframes = **1h / 4h / 1D**).
3. Press **▶ Scan**.
4. Within ~30 seconds, top setups appear in the results table.
5. Click the **📋 icon** next to any symbol to open its **Launch Card**.
6. Click the **symbol name** to open the live **TradingView chart**.

> **Tip:** Start with Pionex or OKX. These work without a proxy. Binance and Bybit may need a custom proxy in geo-restricted regions (see §16).

---

## 4. Interface Overview

From top to bottom:

- **License bar** — license, author, Telegram, GitHub links.
- **Referral banner** — Pionex sign-up (the project's only monetization).
- **Header** — logo, GitHub star, language switch, theme toggle, clock, mode summary.
- **Two control panels** — Left (timeframes & depth), Right (exchange, filters, funding).
- **Action buttons** — Scan, Stop, Custom pairs, CSV, Open Pionex, Share.
- **Counters bar** — live scan statistics.
- **Progress bar** — scan progress.
- **Results table** — all detected setups.
- **Activity log** — collapsible diagnostic log.
- **Footer & social bar** — disclosure, links.

---

## 5. Left Panel — Timeframes & Depth

### Timeframes (TF)

Buttons: **ALL, 1m, 5m, 15m, 30m, 1h, 4h, 1D, 1W, 1M**.

- Click to toggle a timeframe on/off (blue = active).
- **ALL** toggles every supported timeframe at once.
- Unsupported timeframes for the selected exchange appear **greyed out / struck through** and cannot be selected (e.g. some exchanges have no 1M futures candles).
- Your selection is saved automatically.

The scanner analyses **each selected timeframe independently** for every pair. More timeframes = more thorough but slower scans.

### Search depth

How many recent MACD histogram bars to look back through when hunting for the reversal pivot. Options: **3, 5, 7, 10, 15, 20** (default **5**).

- **Lower (3–5):** only the freshest setups; fewer but more current results.
- **Higher (10–20):** catches setups that began developing several bars ago; more results, but some may be "older."

### Min TF

The **minimum number of timeframes** a pair must produce a setup on before it qualifies. Options: **1, 2, 3** (default **1**).

- **1:** any single timeframe match is enough.
- **2–3:** require multi-timeframe confluence — far fewer, higher-conviction results.

### Extremum

The look-back window used to confirm that the reversal candle is a genuine local **extreme** (a real swing high for bearish, swing low for bullish). Options: **3, 5, 7, 10** (default **5**).

- **Higher values** demand a more significant pivot (stronger but rarer signals).
- **Lower values** are more permissive.

---

## 6. Right Panel — Exchange, Filters & Boosters

### Exchange

Choose the data source: **Bybit, Binance, KuCoin, Pionex (default), OKX**.

- **Pionex / OKX:** generally work with direct access — most reliable in restricted regions.
- **Bybit / Binance:** may be geo-blocked (HTTP 403/451). GridPulse routes them through public proxies; if those fail, set a custom proxy (§16).
- Switching exchanges automatically refreshes which timeframes are available.

### Market

- **USDT Futures (linear):** perpetual contracts. **Enables the Funding block.**
- **Spot (default):** spot pairs. Funding options are ignored on spot.

> Pionex futures are not publicly available via API — use Spot on Pionex, or switch to another exchange for futures.

### Type

Filter setup direction:

- **Both (default):** bullish and bearish setups.
- **Bullish:** only long setups (MACD bottoming).
- **Bearish:** only short setups (MACD peaking).

### Top MCap

Restrict the scan to the top N coins by market capitalization (CoinGecko ranking). Options: **50, 100 (default), 200, 500, All**.

- Lower = faster, focuses on liquid majors.
- **All (0):** scans every pair regardless of rank (slowest, includes micro-caps).

### Max

Maximum number of results kept in the final table. Options: **50, 100 (default), 200**. Results are ranked by market cap first, then trimmed.

### Core Filters

| Filter | What it does |
|--------|--------------|
| **REVERSAL FILTER** (on by default) | Requires a confirmed reversal candle + a confirmation candle, not just a MACD turn. When **off**, the scanner returns "soft" MACD-only signals (no entry/stop levels). |
| **CONSERVATIVE STOP** | Displays the wider conservative stop-loss column emphasis (a stop placed at 2× the reversal-candle range beyond entry). |

### Booster Filters (all optional, off by default)

These tighten quality. Each one a setup must pass to qualify:

**VWAP filters (cyan)**
- **VWAP DIRECTION:** price must sit on the "correct" side of VWAP for the setup direction (below VWAP for longs, above for shorts).
- **VWAP CONFLUENCE:** the entry level must align closely with VWAP or a VWAP standard-deviation band (a high-probability confluence zone, flagged with ⭐).

**Candle (orange)**
- **ATR SIZE ×0.8:** the reversal candle's range must be at least 0.8 × ATR — filters out tiny, insignificant candles.
- **VOLUME ×1.1:** the reversal candle's volume must be ≥ 1.1 × the 20-bar average — confirms participation.

**Trend / R:R (yellow)**
- **ADX ≥ 18:** require a minimum trend strength (avoids dead, directionless markets).
- **R:R ≥ 1.5:** require the risk:reward ratio to be at least 1.5.

> **How to use them:** Start with all boosters **off** to see raw setups, then enable a few (e.g. VOLUME + R:R) to narrow down to the highest-quality candidates.

---

## 7. The Funding Block (Futures Only)

Visible/active only when **Market = USDT Futures**. Funding rate is the periodic payment between long and short perpetual holders.

### Checkboxes

- **CONSIDER FUNDING:** fetch and display funding data for qualifying pairs (adds the Fund% / Fund/d / Fund/H / F.Bias columns and the funding section in Launch Cards).
- **USE 7-DAY HISTORY:** base the daily/annualized estimates on the **7-day average (21 payments)** instead of the single current rate — smoother, more representative.
- **SKIP IF EXCEEDS THRESHOLD:** automatically discard setups whose **adverse** daily funding exceeds your Max Daily Funding threshold (e.g. drop longs that pay too much).

### Dropdowns

- **Max daily funding:** the threshold for the Skip filter. Options: 0.05% → 1.00% (default **0.10%**).
- **Hold (days):** the expected holding period used to compute the total **Fund/H** (funding cost over N days). Options: 1, 3 (default), 7, 14, 30.

### Funding data sources & fallbacks

- Each exchange's native funding endpoint is queried first.
- For **Pionex** (no public funding API), GridPulse falls back to **Binance**, then to **Bybit**, labeling the source accordingly (`binance-fallback`, `bybit-fallback`).
- If no source returns data, the table shows **⚠ Funding N/A** instead of a misleading dash.

---

## 8. Action Buttons

| Button | Function |
|--------|----------|
| **▶ Scan** | Start scanning with current settings. |
| **● Stop** | Abort an in-progress scan (partial results are kept). |
| **Custom pairs** | Toggle a text box where you type your own pairs (overrides the auto pair list). |
| **CSV** | Export the current results to a CSV file (36 columns, UTF-8 with BOM for Excel). |
| **🤖 Open Pionex** | Open Pionex via the referral link in a new tab. |
| **📤 Share Screener** | Share the app link (native share sheet, or copies to clipboard). |

---

## 9. Counters Bar

Updates live during a scan:

| Counter | Meaning |
|---------|---------|
| **Scanned** | Pairs processed so far. |
| **Setups** | Total qualifying setups found. |
| **Bullish** | Long setups. |
| **Bearish** | Short setups. |
| **Reversal** | Setups with a confirmed reversal candle. |
| **VWAP ⭐** | Setups at a VWAP confluence zone. |
| **R:R ≥ 2** | Setups with a risk:reward of 2.0 or better. |

---

## 10. Results Table — Every Column Explained

Click any underlined header to **sort** by that column (click again to reverse).

| Column | Description |
|--------|-------------|
| **#** | Row number. |
| **Rank** | CoinGecko market-cap rank (`—` if unranked). |
| **Symbol** | Trading pair. Click the name → TradingView chart. Click **📋** → Launch Card. |
| **Price** | Latest close price. |
| **Setup** | **BULL** (green) or **BEAR** (red). |
| **TF** | Timeframe of this setup. |
| **Depth** | How many MACD bars the momentum move spanned. |
| **Rev** | Mini-candle drawing of the reversal candle (B/S marker). |
| **Conf** | Mini-candle of the confirmation candle (✓ = confirmed). |
| **MACD** | Mini-histogram of the last 20 MACD bars. |
| **Limit** | Suggested limit entry price. |
| **Lim%** | Distance from current price to the limit (green <2%, yellow <5%, red ≥5%). |
| **Stop** | Standard stop-loss price. |
| **Stp%** | Distance to the standard stop. |
| **Cons.SL** | Conservative stop-loss (2× reversal range beyond entry). |
| **Cons%** | Distance to the conservative stop. |
| **VWAP%** | Price distance from VWAP (color reflects favorability for the direction). |
| **VWAP★** | ⭐ if the entry sits at a VWAP confluence zone. |
| **Vol%** | Reversal-candle volume vs the 20-bar average. |
| **ATR** | Average True Range (absolute volatility). |
| **ADX** | Trend strength (green ≥25, yellow ≥18, red <18). |
| **R:R** | Risk:reward ratio (green ≥2, yellow ≥1.5, red <1.5). |
| **Fund%** | Current funding rate (futures only). |
| **Fund/d** | Estimated daily funding (×3 payments). |
| **Fund/H** | Total funding cost over your Hold period. |
| **F.Bias** | Funding bias label (see below) or **⚠ Funding N/A**. |
| **Mode** | Recommended trading mode (hover for the reasoning). |
| **Bot Range** | Suggested grid-bot price range (ATR-based; hover for detail). |
| **B/S Range** | Tighter buy/sell range (ATR ×5; hover for detail). |

### F.Bias values

- 🟢 **LONG-friendly / SHORT-friendly** — funding pays you in this direction.
- 🔴 **LONG-costly / SHORT-costly** — funding costs you in this direction.
- ➖ **Neutral** — negligible funding.
- ⚠ **Funding N/A** — data unavailable (proxy/source blocked).

---

## 11. Trading Modes (BUY / SELL / BOT / SKIP)

GridPulse recommends one of four modes per setup. Hover the Mode cell to see exactly why it was chosen.

- **📥 GRID BUY** — strong bullish reversal: reversal candle present, ADX ≥ 25, price well below VWAP (< −5%), volume ≥ 1.5×, depth ≥ 5, R:R ≥ 2. A directional long.
- **📤 GRID SELL** — the bearish mirror of GRID BUY (price > +5% above VWAP, etc.). A directional short.
- **🤖 GRID BOT** — range-bound conditions (no strong trend, ADX < 28, price within ±5% of VWAP). Best suited to a range/grid bot. The **Bot Range** column gives the suggested range.
- **⚠ SKIP** — conditions are not favorable (e.g. trend too strong for a grid, or criteria unmet). Wait for a better setup or inspect the chart.

The **Bot Range** widens automatically when ADX ≥ 18 (ATR ×18) vs ranging markets (ATR ×10). The **B/S Range** is a tighter ATR ×5 band for scalping/limit entries.

---

## 12. Launch Cards

Click the **📋 icon** beside any symbol to open its Launch Card — a ready-to-execute parameter sheet. It contains:

1. **📊 Parameters for Pionex** — mode-specific values (entry, stop, take-profit, trailing, grid range, grid line count, investment, position size). **Click any value to copy it.**
2. **📈 Indicator confirmation** — ADX, Volume, VWAP%, VWAP⭐, Depth, TF, plus an R:R progress bar.
3. **💰 Funding** (futures) — current/avg/daily/annualized rates, hold cost, next payment countdown, source, bias, and a directional warning.
4. **📝 Step-by-step guide** — exact Pionex actions for the chosen mode (fully localized).
5. **🚀 Trade on Pionex** — referral QR code and sign-up link.

**Footer buttons:** Copy All (full text summary), Share to Telegram, Open Chart (TradingView), Open Pionex.

> Press **Esc** or click outside the card to close it.

---

## 13. TradingView Charts

Click a **symbol name** to open an embedded TradingView chart with **MACD** and **VWAP** studies pre-loaded. A timeframe bar lets you switch intervals on the fly. The header shows the setup summary (type, levels, ADX, R:R, funding, mode).

GridPulse tries multiple exchange symbol formats automatically (a "fallback chain") to maximize the chance the chart loads. If TradingView has no matching symbol, you'll see "Chart unavailable for this symbol."

---

## 14. Custom Pairs & CSV Export

### Custom Pairs

Click **Custom pairs**, then enter symbols separated by commas, spaces, or new lines:

GridPulse normalizes each symbol to the correct format for the selected exchange/market automatically. When the box is filled, it **overrides** the auto pair list (Top MCap filtering is skipped).

### CSV Export

Click **CSV** to download all current results as `gridpulse_v14_1_YYYY-MM-DD.csv`. It includes 36 columns covering every metric (prices, percentages, VWAP, ATR, ADX, R:R, full funding breakdown, mode, reasoning, and both suggested ranges). The file is UTF-8 with a BOM so it opens cleanly in Excel.

---

## 15. Language, Theme & Saved Settings

- **Language switch** (header): 🇬🇧 EN, 🇺🇦 UA, 🇪🇸 ES, 🇷🇺 RU, 🇨🇳 ZH. The entire UI — including Launch Cards, step guides, and the footer — re-renders instantly. Your choice is remembered.
- **Theme toggle** (🌙 / ☀️): switch between dark and light themes. Remembered.
- **Saved settings:** all selects, checkboxes, timeframe choices, and theme persist in your browser's local storage and reload automatically next visit.

---

## 16. Proxies, Caching & Rate Limits

### Why proxies?

Browsers block cross-origin requests (CORS), and some exchanges geo-block certain regions. GridPulse uses a layered approach:

- Direct access for Pionex and Bybit where possible.
- A rotation of public CORS proxies (codetabs, allorigins, cors.lol, thingproxy) with automatic health-tracking and failover.
- An optional custom proxy — the most reliable option.

### Setting a custom proxy (recommended for Binance/Bybit)

In index.html, find this line:

    const CUSTOM_PROXY = '';

Set it to your own Cloudflare Worker (or similar), e.g.:

    const CUSTOM_PROXY = 'https://your-worker.your-name.workers.dev/?url=';

A ready-made worker is provided in docs/cloudflare-worker.js. Deploy it (free tier is enough), paste its URL, and Binance/Bybit will scan reliably.

### Caching

Pair lists, candles, funding and market-cap data are cached in your browser's session storage for 60 seconds, so repeated scans are faster and gentler on the APIs.

### Rate-limit warning

If proxies start failing rapidly, a "⚠ Proxy overloaded" badge appears in the header. Wait a moment and retry, or configure a custom proxy.

---

## 17. Troubleshooting

| Symptom | Likely cause | Fix |
|---------|--------------|-----|
| Binance futures: 0 setups, log says "0 klines loaded… Set CUSTOM_PROXY" | Public proxies are rate-limited/blocked for Binance futures (-1003 IP banned). | Deploy and set a CUSTOM_PROXY (see §16). Not a code bug. |
| Bybit returns nothing | Geo-block (HTTP 403). | Use the custom proxy, or switch to Pionex/OKX. |
| "Pair list is empty — nothing to scan" | Pair fetch failed (proxy/geo). | Switch exchange, set a custom proxy, or check the Activity log. |
| F.Bias shows ⚠ Funding N/A | Funding source blocked for that pair. | Set a custom proxy, or accept that funding is unavailable for it. |
| Chart won't load | TradingView has no matching symbol. | Try a different exchange's version of the pair. |
| Whole page looks unstyled / nothing works | A copy/paste error broke the HTML or CSS (e.g. a duplicated/truncated line). | Open the browser console (F12) and check for a red error; fix the indicated line. |
| Scan is very slow | Many timeframes × many pairs, or proxy retries. | Reduce timeframes, lower Top MCap, or set a custom proxy. |

> Note on Binance/Bybit: in geo-restricted regions these exchanges block public access and proxies. This is an external limitation, not a defect in GridPulse — a clean custom proxy resolves it.

---

## 18. Glossary

- MACD — Moving Average Convergence Divergence; the histogram measures momentum acceleration. Core of GridPulse's reversal detection.
- Reversal candle — the candle marking the momentum turn; a confirmation candle must follow.
- VWAP — Volume-Weighted Average Price; a fair-value reference. Bands are ±1σ / ±2σ.
- ATR — Average True Range; absolute volatility, used to size stops and grid ranges.
- ADX — Average Directional Index; trend strength (not direction). ≥25 = strong, <18 = weak/ranging.
- R:R — Risk:Reward ratio; potential reward divided by risk. Higher is better.
- Funding Rate — periodic perpetual-futures payment between longs and shorts. Positive = longs pay shorts.
- Depth — number of MACD histogram bars the momentum move spanned.
- Grid Bot — a bot that places staggered buy/sell orders across a price range; ideal in sideways markets.
- Launch Card — GridPulse's ready-to-execute parameter sheet for a setup.

---

GridPulse v14.2 · © 2026 GridPulse Project · CC BY-NC-SA 4.0
This tool is for educational and analytical purposes only and does not constitute financial advice.
