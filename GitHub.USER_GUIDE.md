# 📖 GridPulse User Guide

**Version:** 14.8.2 "Pair Presets"
**Last updated:** 2026-06-27
**Audience:** Anyone using [tradescout.trade](https://tradescout.trade/) or a self-hosted GridPulse instance.

---

## 📑 Table of contents

1. [Getting started in 60 seconds](#1-getting-started-in-60-seconds)
2. [The screener layout](#2-the-screener-layout)
3. [Pair Presets (new in v14.8.2)](#3-pair-presets-new-in-v1482)
4. [Configuring a scan](#4-configuring-a-scan)
5. [Reading the results table](#5-reading-the-results-table)
6. [Understanding the modes](#6-understanding-the-modes)
7. [Launch Card — from scan to Pionex bot](#7-launch-card--from-scan-to-pionex-bot)
8. [Funding rate awareness](#8-funding-rate-awareness)
9. [Screenshots, carousels & sharing](#9-screenshots-carousels--sharing)
10. [Keyboard shortcuts & hotkey panel](#10-keyboard-shortcuts--hotkey-panel)
11. [FAQ — real-world troubleshooting](#11-faq--real-world-troubleshooting)
12. [Glossary](#12-glossary)

---

## 1. Getting started in 60 seconds

1. Open **[tradescout.trade](https://tradescout.trade/)** in any modern browser.
2. The default settings already work: **Pionex / Spot / 1h+4h+1D / Top 100 MCap**.
3. Click the green **▶ Scan** button.
4. Wait ~20–60 seconds. You'll see setups appear in real time.
5. Click the 📋 icon next to a symbol → **Launch Card** opens with copy-paste-ready Pionex parameters.
6. Click **🚀 Open in Pionex** → the trading page opens in a new tab.

That's the whole workflow. The rest of this guide explains each piece in detail.

![Quick start overview](docs/img/quickstart-overview.png)

---

## 2. The screener layout

The page is divided into 5 horizontal zones, top to bottom:

| Zone | What it contains |
|------|------------------|
| **Referral banner** | Pionex sign-up link, QR code, Official Partner badge |
| **Header** | App title, language switcher, theme, sound, Pionex Only toggle |
| **Two control panels** | Left: timeframes & depth · Right: exchange, filters, funding |
| **Action bar** | ▶ Scan / ● Stop / Custom Pairs / CSV / Screenshot / Share buttons |
| **Preset bar** (new) | Preset dropdown · 💾 Save as… · ⚙ Manage |
| **Counter cards** | Live stats: Scanned / Setups / Bullish / Bearish / Reversal / VWAP⭐ / R:R≥2 |
| **Results table** | 29 columns, sortable by any column |
| **Activity log** | Collapsible log of every fetch, filter rejection, error |

![Layout zones](docs/img/layout-zones.png)

---

## 3. Pair Presets (new in v14.8.2)

**Purpose:** instead of typing `BTCUSDT, ETHUSDT, SOLUSDT, …` into Custom Pairs every time, save it once as a named **preset** and apply it with a single click.

### 3.1. Built-in starter presets

On first launch you'll see 5 starter presets in the dropdown. They cover the most common trading themes:

| Preset | Use case |
|--------|----------|
| 💎 **Majors** | Conservative scans on the 10 largest coins |
| 🐸 **Memes** | High-volatility plays — works best on 15m–1h |
| 🤖 **AI Tokens** | Narrative trades on AI sector |
| 🏛 **Layer 1s** | Smart-contract platforms |
| 💧 **DeFi Blue Chips** | Established DeFi protocols |

Built-in presets **cannot be edited or deleted** — they always reload to defaults. If you want a tweaked version, save it as a new user preset.

![Preset dropdown with built-ins](docs/img/preset-dropdown.png)

### 3.2. Saving your own preset

1. Type your pairs into the **Custom Pairs** textarea (comma or space separated). Example:
   ```
   BTCUSDT, ETHUSDT, RNDR, FET, TAO, WLD, AKT
   ```
2. Click **💾 Save as…** next to the preset dropdown.
3. A modal opens. Enter:
   - **Name** — up to 40 chars. Example: *My AI Watchlist*.
   - **Icon** — pick from 20 emoji (💎 🐸 🤖 🏛 💧 🚀 ⚡ 🔥 📊 🎯 …).
   - **Pairs** — pre-filled from the textarea, edit if needed.
4. Click **💾 Save**.

The preset appears in the dropdown under **My Presets**, and is auto-applied immediately.

![Save preset modal](docs/img/preset-save-modal.png)

### 3.3. Managing presets

Click **⚙ Manage** to open the management modal. For each user preset you can:

- **✓ Apply** — load the preset and close the modal.
- **🗑 Delete** — remove the preset (with confirmation prompt).

Built-in presets are not shown here (they cannot be modified).

### 3.4. Import / Export (backup & cross-device sync)

In the **⚙ Manage** modal:

- **📤 Export JSON** — downloads `gridpulse_presets_YYYY-MM-DD.json` with all your user presets. Built-ins are not exported (they're always available).
- **📥 Import JSON** — upload a previously exported file. Imported presets are added to your existing ones (not replaced); duplicate IDs get a new ID.

The JSON format is human-readable:

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

### 3.5. Shareable preset URL

You can share a preset as a single URL:

1. Export your presets to JSON.
2. Take any one preset object from the file.
3. Base64-encode it.
4. Append to URL: `https://tradescout.trade/?preset=<base64>`

When someone opens that link, they see a **consent prompt** asking whether to import the preset (with name + pair count shown). On accept, the preset is added to their local storage and applied immediately. The `?preset=` parameter is then stripped from the URL.

### 3.6. Storage details

| Key | Stores |
|-----|--------|
| `gp_presets_v1` | All your user presets (JSON array) |
| `gp_preset_last` | ID of the last-applied preset (auto-restored on reload) |

These keys are **independent** from `gp_settings_v14_8_2` — clearing screener settings does NOT delete presets, and version bumps (e.g. future v14.9.x) do NOT migrate them. Your watchlists are safe across upgrades.

> 💡 **Pro tip:** Combine presets with **Pionex Only** toggle in the header for a fully locked-in workflow — one click selects the watchlist, exchange, and market type.

---

## 4. Configuring a scan

### 4.1. Left panel — Timeframes & depth

| Control | Purpose | Recommended |
|---------|---------|-------------|
| **TF buttons** | Which candle intervals to scan | 1h + 4h + 1D for swing; 15m + 30m + 1h for day |
| **Search depth** | How many recent candles to look back for a reversal | 5 (default) or 7 |
| **Min TF** | Symbol must hit ≥ this many TFs to be reported | 1 (default) or 2 for confluence |
| **Extremum** | Lookback for confirming the candle is a local extreme | 5 (default) |
| **Strictness** | Soft / Normal / Strict — scales all thresholds | Normal (default) |

> 💡 **Why TF-adaptive?** A 1m chart has very different noise vs a 1W chart. v14.7.6+ scales ADX, VWAP distance, volume ratio, R:R, and depth requirements **per TF × strictness**. So `Normal` on 1m is softer than `Normal` on 1W — by design.

### 4.2. Right panel — Exchange, filters & boosters

#### Exchange & market

- **Exchange** — Pionex (default), Bybit, Binance, KuCoin, OKX
- **Market** — Spot (default) or USDT Futures
- **Type** — Both / Bullish / Bearish

#### MCap & limits

- **Top MCap** — limit scan to top 50 / 100 / 200 / 500 by market cap (uses CoinGecko ranking). Set to **All** for full exchange listing.
- **Max** — max rows in results table.

#### Reversal & stops

- ☑ **REVERSAL FILTER** — require a confirmed 2-candle reversal pattern (default ON).
- ☐ **CONSERVATIVE STOP** — show a wider, safer SL based on 2× candle range.

#### VWAP filters

- ☐ **VWAP DIRECTION** — bullish setups only if price is below VWAP (and vice versa).
- ☐ **VWAP CONFLUENCE** — entry must align with VWAP or ±1σ / ±2σ band.

#### Candle filters

- ☐ **ATR SIZE ×0.8** — reversal candle must be at least 80% of 14-ATR.
- ☐ **VOLUME ×1.1** — reversal candle volume must be ≥110% of 20-period average.

#### Trend / R:R

- ☐ **ADX ≥ 18** — trend strength gate (TF-adaptive, scales with Strictness).
- ☐ **R:R ≥ 1.5** — reward-to-risk ratio gate (TF-adaptive).

#### Funding (Futures only)

- ☐ **CONSIDER FUNDING** — fetch funding rate per symbol. Reveals 2 sub-controls.
- ☐ **7-DAY HISTORY** — use 7-day funding average (21 payments) instead of current rate. More accurate but slower.
- ☐ **SKIP IF EXCEEDS** — auto-skip setups where adverse daily funding exceeds the threshold.
- **Max daily funding** — 0.05% / 0.10% (default) / 0.20% / 0.30% / 0.50% / 1.00%.
- **Hold (days)** — 1 / 3 (default) / 7 / 14 / 30 — used to compute total funding cost for the position.

### 4.3. Custom pairs (manual override)

Click **Custom pairs** to expand the textarea. Paste a comma/space/newline-separated list:

```
BTCUSDT ETHUSDT SOLUSDT
DOGEUSDT, AVAXUSDT
LINKUSDT
```

Pairs are auto-normalized to the selected exchange's format:
- Bybit / Binance / Pionex spot → `BTCUSDT`
- Pionex futures → `BTC_USDT_PERP`
- KuCoin spot → `BTC-USDT`
- KuCoin futures → `XBTUSDTM` (BTC ↔ XBT swap)
- OKX → `BTC-USDT` (spot) or `BTC-USDT-SWAP` (futures)

When custom pairs are present, **Top MCap** filter is bypassed.

### 4.4. Pionex Only mode

Top-right header toggle: **🤝 Pionex Only**.

When enabled:
- Exchange dropdown locks to Pionex.
- Dropdown becomes grayed-out (cannot accidentally switch).
- State persists in `localStorage` (`gp_pionex_only`).

Useful for users who exclusively use Pionex and want to remove cognitive overhead.

---

## 5. Reading the results table

The table has **29 columns**. The most important ones:

| Column | What it means |
|--------|---------------|
| **#** | Row number |
| **Rank** | CoinGecko market cap rank |
| **Symbol** | Click the symbol → opens TradingView chart. Click 📋 → opens Launch Card |
| **Price** | Current last price |
| **Setup** | 🟢 BULL or 🔴 BEAR |
| **TF** | Timeframe of this setup |
| **Depth** | Number of consecutive same-sign MACD bars before reversal |
| **Rev** | Mini-candle visualization of the reversal candle |
| **Conf** | Confirmation candle (the one after Rev) |
| **MACD** | 20-bar mini histogram |
| **Limit / Lim%** | Entry price + distance from current price |
| **Stop / Stp%** | Stop-loss price + distance |
| **Cons.SL / Cons%** | Conservative stop (2× candle range) |
| **VWAP% / VWAP★** | Distance to VWAP + confluence star |
| **Vol%** | Reversal candle volume vs 20-period average |
| **ATR** | 14-period ATR value |
| **ADX** | 14-period ADX |
| **R:R** | Reward-to-risk ratio |
| **Fund% / Fund/d / Fund/H / F.Bias** | Funding now / daily / hold-period / direction bias |
| **Mode** | STRONG BUY / GRID BUY / STRONG SELL / GRID SELL / SKIP |
| **Bot Range** | Suggested grid bot range (ATR-based, wider) |
| **B/S Range** | Buy/sell range (ATR-based, tighter, for STRONG modes) |

Click any column header to sort. Double-click a row to **highlight** it (others dim).

![Results table with highlighted row](docs/img/results-table.png)

---

## 6. Understanding the modes

GridPulse classifies every setup into one of 5 **modes** that map directly onto trading actions.

### 6.1. STRONG BUY / STRONG SELL — directional entry

Use when you want to trade the reversal as a directional position (limit order + stop-loss).

**Triggers** (at least one path must be true):

- **Exhaustion path** — very strong trend (high ADX), extreme VWAP distance, large reversal candle, R:R ≥ 2.0. This is a classic "blow-off top/bottom" pattern.
- **Quality path** — moderate trend, ⭐ VWAP confluence, R:R ≥ 2.0, deeper history. Less dramatic but more reliable.

**Launch Card provides:** Entry price, Stop Loss, Conservative SL, Take Profit, Trailing trigger, Position size guidance.

### 6.2. GRID BUY / GRID SELL — bot deployment

Use when conditions favor a grid bot rather than a directional trade — moderate volatility, not too trendy.

**Triggers:** ADX below "too trendy" threshold, VWAP distance within range, R:R ≥ 1.5.

**Launch Card provides:** Grid Lower / Upper / Width, Grid lines count, Mode (Geometric), Investment, ATR-based Stop Loss and Take Profit for the entire grid.

### 6.3. 🛡 SKIP — with classified sub-reasons

Hover the SKIP badge to see why the setup was rejected. Sub-categories:

| Label | Meaning | What to do |
|-------|---------|------------|
| ⚡ **WATCH** | Good reversal candle but R:R too low | Add to watchlist; re-scan in a few candles |
| 🌊 **TREND** | Market is trending; no reversal yet | Wait for a reversal candle |
| ⚖ **LOW R:R** | Reward not worth the risk | Skip or wait for better entry |

The tooltip shows exact threshold values for the current TF and Strictness — e.g. `[4h/normal] ADX 32.5≥28 (too trendy for grid) · no reversal candle`.

![SKIP tooltip](docs/img/skip-tooltip.png)

---

## 7. Launch Card — from scan to Pionex bot

Click the 📋 icon next to any symbol in the results table.

The Launch Card adapts its layout to the mode:

### STRONG BUY example

```
═════════════════════════════════════
   BTCUSDT / 4h   📥 STRONG BUY
═════════════════════════════════════

📊 Parameters for PIONEX
─────────────────────────────────────
  Entry (Buy Price)      67450.0  🟢
  Stop Loss              65200.0  🔴
  Conservative SL        64100.0  🔴
  Fixed Take Profit      72500.0  🩵
  Trailing trigger +10%  74195.0  🟡
  Max trailing drawdown  5–7%     🟡
  Position size          10–20% of capital
─────────────────────────────────────
  👆 Click a value to copy

📈 Indicator confirmation
  ADX      24.3      Volume   142%
  VWAP%   -3.21%    VWAP⭐    ⭐ YES
  Depth    7         TF       4h

  R:R ratio: 2.45x  ████████░░░░  (green)

💰 Funding (Perpetual) — if futures
  Current rate     +0.0085%   🟢
  Per day (×3)     +0.0255%   🟡
  Cost over 3d     +0.0765%   🟢
  Bias             🟢 LONG-friendly

🚀 Trade on Pionex            🤝 OFFICIAL PARTNER
  [ QR ]   Sign up and get 16 free bots
           · 0.05% fee
           🤝 GridPulse × Pionex

  ┌─────────────────────────────────────┐
  │  🚀 Open in Pionex — Trade this setup │
  └─────────────────────────────────────┘
─────────────────────────────────────
[📋 Copy all] [✈️ Share to TG] [📊 Open chart]
```

### Workflow

1. Click 📋 → Launch Card opens.
2. Click any value (e.g. *Entry*) → it's copied to clipboard. Toast appears: **✓ Copied!**
3. Click **🚀 Open in Pionex** → Pionex trading page opens in a new tab (with UTM tracking).
4. Paste values into Pionex bot configuration.

![Launch Card example](docs/img/launchcard-example.png)

### GRID BUY / GRID SELL layout

For grid modes, the Launch Card shows:

- **Lower / Upper Limit** — the grid range
- **Range width** — as percentage
- **Grid lines count** — 30 / 40 / 50 depending on width
- **Grid mode** — Geometric (recommended for crypto)
- **Investment** — base asset (tokens, not USDT)
- **Stop Loss (ATR-based)** — TF-adaptive multiplier
- **Take Profit (ATR-based)** — exit the grid in profit

---

## 8. Funding rate awareness

USDT-Perpetual contracts charge a **funding rate** every 8 hours (3× per day). It can quietly eat your profits if you trade against the crowd.

GridPulse fetches funding data when you enable **CONSIDER FUNDING** in the right panel (futures only):

- **Fund%** — current funding rate.
- **Fund/d** — daily rate (= current × 3, or 7-day average × 3 if "7-DAY HISTORY" is on).
- **Fund/H** — total cost over your configured hold period (1–30 days).
- **F.Bias** — color-coded direction bias:
  - 🟢 **LONG-friendly** — negative funding → shorts pay longs.
  - 🔴 **LONG-costly** — positive funding → longs pay shorts.
  - 🟢 **SHORT-friendly** — positive funding → longs pay shorts.
  - 🔴 **SHORT-costly** — negative funding → shorts pay longs.
  - ➖ **Neutral** — funding very close to zero.

### Auto-skip

Enable **SKIP IF EXCEEDS** to auto-reject setups where adverse funding crosses your threshold. Useful when you don't want to manually filter every row.

### Source fallbacks

- Pionex funding endpoint → falls back to Bybit if unavailable.
- Binance funding endpoint → falls back to Bybit when geo-blocked (451 errors).

The fallback source is shown in the Launch Card.

---

## 9. Screenshots, carousels & sharing

### 9.1. Horizontal screenshot (default)

Click **📸 Screenshot** in the action bar. Generates a wide PNG with:
- Header with version, exchange, timeframes, generation timestamp.
- 5 stat cards (Total Setups, BUY, SELL, BOT, SKIP).
- The full results table.
- Watermark with scan serial number.
- Footer with disclaimer.

Best for: GitHub issues, Telegram desktop, blog posts.

### 9.2. TikTok PNG (vertical 1080×1350)

Two variants, both accessible via hotkeys:

- `Shift + P` → **Cards** mode (top 5 setups as readable cards). Best for mobile-first social.
- `Shift + Alt + P` → **Table** mode (top 15 setups, compact table). Best when you want more data visible.

Or open TikTok mode first (`Shift + T`), then use the pager buttons.

### 9.3. 5-slide carousel

`Shift + C` generates 5 separate PNG files in 1080×1350:

1. **Cover** — title + total stats + top symbols teaser.
2. **Top 1 setup** — full detail card.
3. **Top 2 setup** — full detail card.
4. **Top 3 setup** — full detail card.
5. **CTA** — "follow for daily scans" call to action.

Ranking uses STRONG > GRID > SKIP, then by R:R descending, then depth.

Best for: Instagram carousels, TikTok image posts, Twitter threads.

### 9.4. Share buttons

- **📤 Share Screener** — Web Share API or copy-to-clipboard fallback. Shares the app URL with a short pitch.
- **✈️ Share to TG** (Launch Card) — opens Telegram share dialog with formatted setup details + referral link.

---

## 10. Keyboard shortcuts & hotkey panel

Click the **⌨** floating button (bottom-left) to see all shortcuts.

| Shortcut | Action |
|----------|--------|
| `Shift + T` | Toggle TikTok / vertical mode |
| `Shift + P` | Export PNG Cards (top 5) |
| `Shift + Alt + P` | Export PNG Table (top 15) |
| `Shift + C` | Generate 5-slide carousel |
| `Esc` | Close any modal (chart / Launch Card / preset modals) |
| Double-click row | Highlight row, dim others (double-click again to clear) |

Hotkeys are disabled when focus is inside an `<input>`, `<textarea>`, or `<select>`.

---

## 11. FAQ — real-world troubleshooting

### Q: I get "Proxy overloaded — retrying…" in the header.

**A:** GridPulse uses public CORS proxies to fetch exchange data. When they hit rate limits or temporary outages, this warning appears. The screener automatically rotates through 5 proxies (custom Cloudflare Worker, codetabs, allorigins, cors.lol, thingproxy). Just wait 10–30 seconds — it usually self-resolves. If it persists for minutes, try:

1. Hard-refresh the page (`Ctrl+Shift+R` / `Cmd+Shift+R`).
2. Switch to a different exchange (e.g. Bybit instead of Binance).
3. Clear `sessionStorage` (DevTools → Application → Clear).

### Q: Binance returns "451 Restricted location" / Binance Futures gives no data.

**A:** Binance blocks data-center IPs that public CORS proxies run on. v14.6+ automatically falls back to **Bybit market-data mirror** so the scan completes. You'll see:
```
⚠ Binance Futures API blocked — using Bybit market-data mirror for scan continuity
```
This is expected and normal. For Binance spot, the fallback is less aggressive — if all proxies fail, the scan returns empty.

> 💡 **Workaround:** Set "Pionex Only" or pick another exchange. Pionex is the recommended default in v14.8.0+.

### Q: A symbol I expect to see isn't in the results.

**A:** Possible reasons (check Activity log at bottom):

- **Filter rejection** — e.g. `ATR SIZE ×0.8` or `VOLUME ×1.1` filtered it out. Try disabling some filters.
- **Min TF not reached** — symbol only triggered on 1 TF but you require ≥ 2.
- **Outside MCap top N** — increase to Top 500 or "All".
- **Funding auto-skip** — adverse funding above your threshold (you'll see `Funding-SKIP:` in log).
- **Geometry rejection** — price already crossed entry or stop (v14.8.1 strictness). Look at the chart to confirm.
- **API rate limit** — for that specific symbol on this scan. Re-run after 30s.

Hover the row's mode badge for a detailed reason string with exact thresholds.

### Q: How do I scan only DeFi tokens?

**A:** Two options:

1. Apply the built-in 💧 **DeFi Blue Chips** preset (10 pairs).
2. Click **💾 Save as…**, paste your full DeFi list, save as e.g. *My DeFi Watchlist* with 💧 icon.

The preset bypasses the MCap filter, so all listed pairs are scanned regardless of rank.

### Q: I exported presets on my desktop — how do I get them on my phone?

**A:** Three ways:

1. **Email** the JSON file to yourself → open in mobile browser → Import via ⚙ Manage.
2. **Cloud sync** the JSON file (Google Drive, iCloud, Dropbox) → import on phone.
3. **Share URL** — for a single preset, generate a `?preset=<base64>` link (see [section 3.5](#35-shareable-preset-url)) and message it to yourself.

### Q: My presets disappeared after clearing browser data!

**A:** Presets live in `localStorage`. If you clear "Site data" or "All browsing data", they're gone — that's a browser feature, not a bug. **Always export to JSON before clearing.** Settings → 💾 Save as… → ⚙ Manage → 📤 Export JSON.

### Q: Can I run this offline?

**A:** Partially. The HTML/CSS/JS works offline once loaded, but exchange APIs need internet. You can:
1. Clone the repo locally.
2. Open `index.html` directly (or via `python3 -m http.server`).
3. Use it as long as your internet is up — no GridPulse server required.

### Q: Why is Pionex 1M (monthly) timeframe disabled?

**A:** Pionex API doesn't expose 1M klines for spot or perpetuals. The button auto-disables for Pionex. Switch to Bybit / Binance / KuCoin / OKX to scan 1M.

### Q: What's the difference between "Bot Range" and "B/S Range"?

**A:**

- **Bot Range** (ATR × 18 if ADX ≥ 18, else ATR × 10) — wider, for **grid bot deployment**. Used when mode is GRID_BUY / GRID_SELL.
- **B/S Range** (ATR × 5) — tighter, for **buy/sell directional trade**. Used when mode is STRONG_BUY / STRONG_SELL as a fallback bot range if you want to convert a STRONG signal into a tight grid.

The Launch Card automatically uses the right one based on mode.

### Q: How accurate is the CoinGecko rank?

**A:** Top 250 is fetched per page, up to 4 pages = Top 1000. The data is cached for 60 seconds per scan to avoid hitting CoinGecko's rate limit. If you see `Rank: —` in the table, that symbol isn't in CoinGecko's top 1000 (or the API call failed — check Activity log).

### Q: Does GridPulse store any data on a server?

**A:** **No.** Everything runs in your browser. The only server contact is:
- Exchange APIs (Bybit, Binance, KuCoin, OKX, Pionex) for price/funding data.
- CoinGecko for market cap rankings.
- Public CORS proxies (used as fallbacks).
- Cloudflare Insights beacon (anonymous analytics, can be blocked by uBlock Origin).

No login, no tracking cookies, no user accounts. Your presets and settings live in your browser's `localStorage`.

---

## 12. Glossary

| Term | Definition |
|------|------------|
| **ADX** | Average Directional Index. Measures trend strength (0–100). >25 = strong trend; <18 = weak / ranging. |
| **ATR** | Average True Range. Measures recent volatility in price units. |
| **B/S Range** | Buy/Sell range. Tight ATR-based range, used as fallback grid for STRONG signals. |
| **Bot Range** | Wider ATR-based range, used as primary grid for GRID signals. |
| **Conservative SL** | Stop-loss placed 2× candle range beyond the reversal candle extreme. Wider than standard SL. |
| **Depth** | Number of consecutive same-direction MACD histogram bars before the reversal candle. |
| **Funding rate** | Periodic payment (every 8h on most exchanges) between longs and shorts in perpetual futures. |
| **GRID BUY / SELL** | Recommended mode for grid bot deployment in current market conditions. |
| **Launch Card** | Modal with copy-paste-ready Pionex bot parameters. Opens via 📋 icon. |
| **MACD** | Moving Average Convergence Divergence. Primary momentum indicator (12 / 26 / 9). |
| **Mode** | Final classification of a setup: STRONG_BUY / GRID_BUY / STRONG_SELL / GRID_SELL / SKIP. |
| **Preset** | Named watchlist of pairs, saved in browser storage (new in v14.8.2). |
| **Quality path** | STRONG mode trigger via moderate trend + ⭐ VWAP confluence + R:R ≥ 2. |
| **Reversal candle** | The candle where MACD histogram changes direction. Must satisfy strict shape rules. |
| **R:R** | Reward-to-Risk ratio. Computed as `potential_reward / risk_to_stop`. |
| **STRONG BUY / SELL** | High-conviction directional setup. Trade as limit + stop-loss. |
| **Strictness** | Global multiplier for all thresholds: soft (0.75×) / normal (1.0×) / strict (1.3×). |
| **TF-adaptive** | Thresholds scale per timeframe — 1m is softer, 1W is stricter. |
| **VWAP** | Volume-Weighted Average Price (50-period). Used as a directional filter. |
| **VWAP confluence ⭐** | Entry price aligns with VWAP or its ±1σ / ±2σ bands. Quality marker. |

---

**End of guide** · GridPulse v14.8.2 · 2026-06-27

Found a typo or unclear section? Open an issue on [GitHub](https://github.com/pro100off/gridpulse/issues) or message [@tradescoutfree](https://t.me/tradescoutfree) on Telegram.
