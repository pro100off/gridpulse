# ⚡ GridPulse v14.9.2 🔔 Alerts + Backtest + Journal

> **Free, open-source, multi-exchange crypto reversal screener** purpose-built as a **companion tool for Pionex Grid Bots** — with directional **STRONG / GRID BUY/SELL** modes, **TF-adaptive Strictness**, MACD + VWAP + ATR + ADX + **MTF Trend Filter** + **Session Filter** + **Liquidity Guard** + Funding-aware setups across **Pionex, Bybit, Binance, KuCoin, and OKX** — and one-click **Launch Cards** with **Trade Plan v3** (ATR-based TP1/TP2/TP3 + Chandelier trailing stop) that take you straight into a Pionex trading session.
>
> **v14.9.2** adds the **Automation & Journaling suite**: 🔄 **Auto-refresh scanning**, 🔔 **Desktop / ✈️ Telegram / 🎮 Discord alerts** for STRONG setups, 💰 **Position Sizing** calculator, 📊 **Backtest** (historical win-rate per setup), and a full 📓 **Signal Journal** with auto TP/SL resolution, **Net R** tracking and overflow-safe archiving — all localized across 5 languages.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Version](https://img.shields.io/badge/version-14.9.2-blue.svg)](https://github.com/pro100off/gridpulse/releases/latest)
[![Alerts + Backtest + Journal](https://img.shields.io/badge/🔔-Alerts%20·%20Backtest%20·%20Journal-c39bff)](#-whats-new-in-v1492--alerts--backtest--journal)
[![MTF Filter](https://img.shields.io/badge/🎯-MTF%20Trend%20Filter-26d97a)](#-mtf-trend-filter)
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
| 📝 **Release notes v14.9.2** | [docs/RELEASE_NOTES_v14.9.2.md](docs/RELEASE_NOTES_v14.9.2.md) |
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
- [🔔 What's new in v14.9.2 — Alerts + Backtest + Journal](#-whats-new-in-v1492--alerts--backtest--journal)
- [🔄 Auto-refresh scanning](#-auto-refresh-scanning)
- [🔔 Alerts — Desktop / Telegram / Discord](#-alerts--desktop--telegram--discord)
- [💰 Position Sizing calculator](#-position-sizing-calculator)
- [📊 Backtest engine](#-backtest-engine)
- [📓 Signal Journal](#-signal-journal)
- [🎯 MTF Trend Filter](#-mtf-trend-filter)
- [🤖 Bot Range modes](#-bot-range-modes)
- [🌏 Session Filter](#-session-filter)
- [💧 Liquidity Guard](#-liquidity-guard)
- [🏷 Symbol Unification](#-symbol-unification)
- [🔍 Cell Magnifier](#-cell-magnifier)
- [⚡ STRONG-signal row highlighting](#-strong-signal-row-highlighting)
- [🎯 Trade Plan v3](#-trade-plan-v3)
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
- [🗄 Storage keys](#-storage-keys)
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

- **🔄 Auto-refresh scanning (v14.9.2)** — re-run scans automatically every N minutes (1–1440), with new setups since the last run highlighted.
- **🔔 Desktop notifications (v14.9.2)** — browser push alerts for STRONG_BUY / STRONG_SELL setups (30s cooldown per symbol).
- **✈️ Telegram alerts (v14.9.2)** — push STRONG setups to a Telegram chat with entry, SL, TP, R:R, position size and risk.
- **🎮 Discord alerts (v14.9.2)** — push STRONG setups to a Discord channel via webhook.
- **💰 Position Sizing calculator (v14.9.2)** — balance + risk% → units, position value, leverage-equivalent, reward/loss in USDT, injected into every Launch Card.
- **📊 Backtest engine (v14.9.2)** — historical win-rate per setup, reproducing the live MACD-reversal pipeline over the last N bars. Win-rate badge in the Mode column + Expected Value in the Launch Card.
- **📓 Signal Journal (v14.9.2)** — auto-log every new STRONG setup, auto-resolve TP/SL/Expired, track Win Rate + **Net R**, overflow-safe archive, CSV export.
- **🎯 MTF Trend Filter (ON by default)** — rejects setups fighting higher-TF EMA50 direction. Cuts ~60% of counter-trend false positives.
- **🤖 Bot Range modes** — Donchian 26 (default), Bollinger 20/2σ, or legacy ATR for tuning grid ranges to market character.
- **🌏 Session Filter** — downgrades STRONG→GRID during Asian night (00-06 UTC) where liquidity drops ~40%.
- **💧 Liquidity Guard** — hard-blocks STRONG signals for pairs with < $50k avg turnover per bar (20-bar window).
- **🏷 Unified Bybit-style symbol display** — all exchanges show `BTCUSDT` / `BTCUSDT.P` regardless of native format.
- **🔍 Cell Magnifier** — hover any table cell to enlarge 1.45× with glow. Toggle in header (saved to localStorage).
- **⚡ STRONG-signal row highlighting** — gradient background, ⚡ icon in # column, subtle 3s pulse animation.
- **🎯 Trade Plan v3** — STRONG shows TP1 (1R), TP2 (ATR×N target), TP3 (3R+ trail) and Chandelier ATR×3 trailing stop.
- **📈 Freshness bonus in ranking** — freshest MACD signals rank first within same mode.
- **💾 Pair Presets** — save/load named watchlists, 5 built-in starters, JSON import/export, shareable URLs.
- **🤝 Built around Pionex** — Pionex is the default exchange; Launch Cards map directly to Pionex Grid Bot parameters.
- **5 exchanges:** Pionex, Bybit, Binance, KuCoin, OKX (**Spot + USDT Futures**).
- **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, EMA50 (MTF), Volume ratio, R:R.
- **TF-adaptive Strictness** — thresholds scale automatically by timeframe (**1m softer → 1W stricter**) with a global selector: **soft / normal / strict**.
- **Two paths to STRONG setups:** Exhaustion (blow-off + reversal candle) and Quality (moderate trend + ⭐ VWAP confluence + strong R:R).
- **Classified SKIP reasons** with per-row tooltip thresholds: ⚡ WATCH, 🌊 TREND, ⚖ LOW R:R, plus session / liquidity / MTF downgrades.
- **Setup geometry validation** — rejects stale setups where price already crossed entry/stop.
- **Funding-aware setups** for perpetual contracts (current rate, 7-day average, daily / annual cost, hold-period projection, LONG/SHORT bias).
- **5 languages:** English · Українська · Español · Русский · 中文 — **including full v14.9.2 automation & journal strings**.
- **Launch Cards** with copy-paste-ready Grid Bot parameters, a Position Sizing block, and a prominent "Open in Pionex" CTA with UTM tracking.
- **Pionex Only mode** — single header toggle that locks the screener to Pionex.
- **Breakout entry logic** — `limL` placed at the opposite extreme of the reversal candle.
- **TradingView integration** — open chart for any setup in one click.
- **CSV export** of all scan results (with funding columns) and of the Signal Journal.
- **Content-creator tools** — horizontal full screenshot, vertical 1080×1350 PNG Cards (top 5), vertical 1080×1350 PNG Table (top 15), 5-slide Carousel, daily watermark with scan serial counter.
- **Privacy-first:** no signup, no cookies, no individual user tracking, no fingerprinting, GDPR-compliant.
- **Light / Dark theme** with full localization and high-contrast rows.
- **Auto-fallback proxies** — scan still completes even when one exchange API is blocked in your region.
- **Zero-build single-file architecture** — entire app is one `index.html`.

---

## 🚀 Quick start

### Option A — Use the hosted version (no install)

1. Open [https://tradescout.trade/](https://tradescout.trade/)
2. The screener opens on **Pionex / Spot** by default (switch to Bybit / Binance / KuCoin / OKX anytime)
3. *(Optional)* Pick a **preset** from the dropdown (💎 Majors / 🐸 Memes / 🤖 AI Tokens / 🏛 Layer 1s / 💧 DeFi Blue Chips)
4. Select **timeframes** (defaults: 1h, 4h, 1D)
5. Optionally adjust **Strictness** (soft / normal / strict) and **🤖 Bot Range** mode (Donchian / Bollinger / ATR)
6. *(Optional, v14.9.2)* Set **💰 Balance / Risk%**, enable **🔄 Auto**, **🔔 Notify**, **✈️ TG**, **🎮 Discord**, or **📊 Backtest** in the automation panel
7. Click **▶ Scan** — results usually appear in ~30 seconds
8. Look for ⚡ **STRONG-highlighted rows** at the top of the table
9. Click 📋 next to any symbol to open the **Launch Card** with **Trade Plan v3** and a **Position Sizing** block
10. Click the big **🚀 Open in Pionex** button → the setup carries over via UTM-tagged deep link
11. New STRONG setups are auto-logged to the 📓 **Journal** — open it anytime to review Win Rate and **Net R**

### Option B — Self-host (1 command)

    git clone https://github.com/pro100off/gridpulse.git
    cd gridpulse
    python3 -m http.server 8000
    # Open http://localhost:8000 in your browser

Or simply double-click `index.html` — it also works on `file://`.

---

## 🔔 What's new in v14.9.2 — Alerts + Backtest + Journal

v14.9.2 turns GridPulse from a one-shot scanner into a **continuous, self-tracking workflow**. All new features live in a dedicated automation panel above the results table.

### Headline features

1. **🔄 Auto-refresh scanning** — set an interval (1–1440 min) and GridPulse re-scans automatically, flashing new setups since the last run.
2. **🔔 Desktop notifications** — browser push alerts for STRONG setups, 30s cooldown per symbol.
3. **✈️ Telegram alerts** — bot token + chat_id → STRONG setups arrive in your Telegram with full trade plan and position size. Test button included.
4. **🎮 Discord alerts** — webhook URL → STRONG setups posted to your Discord channel. Test button + URL validation.
5. **💰 Position Sizing** — balance + risk% → units, value, leverage-equivalent, reward/loss in USDT, added to every Launch Card.
6. **📊 Backtest** — per-setup historical win-rate that reproduces the *live* signal pipeline (MACD reversal + rc/cc), shown as a badge in the Mode column and as Expected Value in the Launch Card.
7. **📓 Signal Journal** — every new STRONG setup is auto-logged; status auto-resolves to TP / SL / Expired by walking candles forward. Stats: Total, TP Hit, SL Hit, Win Rate, **Net R (closed)**.
8. **🗄 Overflow-safe journal** — 200-entry cap prunes *expired → closed → pending last*, so pending trades are never lost; pruned closed-trade stats fold into a persistent archive so Win Rate / Net R never reset.
9. **🌐 Full 5-language i18n** — every automation, journal, position-sizing and alert string is translated across EN / UA / ES / RU / ZH (no English fallback remaining).

**Zero breaking changes.** All v14.9.1 scanning logic, ATR-based R:R, filter-aware classification, geometry validation, TF-adaptive thresholds, Strictness selector, classified SKIP reasons, Pionex companion positioning, and Pair Presets behaviour are **preserved unchanged**.

Alerts and journaling fire **only for STRONG_BUY / STRONG_SELL** setups to avoid noise from GRID / SKIP rows.

---

## 🔄 Auto-refresh scanning

Set an interval in minutes (1–1440) and toggle **Auto** ON. GridPulse re-runs the full scan on that cadence without any manual clicks.

- New setups (not present in the previous run) briefly flash with a highlight so you can spot fresh opportunities.
- The interval can be changed live — the timer restarts with the new value immediately.
- State (on/off + interval) persists in `localStorage`.
- Status line shows the active cadence, e.g. `🔄 Auto-refresh every 15m`.

Auto-refresh cooperates with alerts and the journal: each auto-scan can push notifications and log new STRONG setups automatically — ideal for leaving GridPulse open in a background tab.

---

## 🔔 Alerts — Desktop / Telegram / Discord

All three channels fire **only for STRONG_BUY / STRONG_SELL** setups, with a 30-second cooldown per symbol to prevent spam.

### Desktop notifications

Click **Notify → ON** and grant the browser permission. You'll get a native push for each new STRONG setup with pattern, score, entry, SL and R:R.

### Telegram

1. Create a bot with [@BotFather](https://t.me/BotFather) and copy the **bot token**.
2. Get your **chat_id** from [@userinfobot](https://t.me/userinfobot).
3. Paste both into the ✈️ **TG** fields, click **ON**, then 🧪 to send a test.

Each alert includes direction, symbol, TF, mode, entry / SL / TP, R:R, ADX, volume, and the computed **position size + risk** from your Position Sizing settings.

### Discord

1. Server Settings → Integrations → Webhooks → **New Webhook** → copy URL.
2. Paste into the 🎮 **Discord** field, click **ON**, then 🧪 to test.

The webhook URL is validated against the official Discord webhook pattern before enabling.

> **Note on secrets:** tokens and webhook URLs are stored in your browser's `localStorage` only and are never sent anywhere except directly to Telegram / Discord. Treat this as convenience-grade storage — don't use it on a shared/public machine.

---

## 💰 Position Sizing calculator

Enter your **account balance** and **risk % per trade** in the automation panel. GridPulse then computes, for every setup:

- **Risk in USDT** — `balance × risk%`
- **Position size (units)** — `riskUsd / |entry − stop|`
- **Position value (USDT)** and **% of balance**
- **Leverage-equivalent** (for futures) — how much leverage the position value implies vs. balance
- **Reward if TP hit** and **Loss if SL hit** in USDT
- **Expected Value / trade** — when Backtest is ON, combines historical win-rate with reward/risk

This block is injected directly into every Launch Card, right under the parameters section, and the same numbers are included in Telegram / Discord alerts.

R:R guards are shown inline: a warning appears if R:R < 1.0 (reward smaller than risk) or R:R < 1.5 (below recommended).

---

## 📊 Backtest engine

Toggle **📊 Backtest → ON**. For every result, GridPulse walks back over the last N bars and counts how often an *identical* setup — reproduced through the **live `findSetup` MACD-reversal + rc/cc pipeline** — reached TP before SL within a forward window.

- Win-rate badge appears in the **Mode** column, e.g. `BT 62% (18)` (rate + sample size).
- Colour-coded: ≥60% green (high), 45–60% yellow (mid), <45% red (low), `n=…` grey when the sample is below the minimum.
- The Launch Card shows **Expected Value / trade** derived from the backtest rate and your position sizing.

Because the backtest reproduces the exact signal pipeline (not raw candle patterns), the win-rate reflects **what the screener would actually have traded** — a far more honest number than naive pattern statistics.

Defaults: 500-bar lookback, 20-bar forward window, minimum 10 samples to report a rate.

---

## 📓 Signal Journal

Open the 📓 **Journal** button in the automation panel. Every new STRONG setup from a scan is auto-logged with its entry, SL, TP, R:R, mode, depth and timestamp.

### Auto status resolution

When you open the journal, GridPulse fetches forward candles for each pending entry and resolves its status:

- **✅ TP** — take-profit hit first
- **❌ SL** — stop-loss hit first
- **⌛ Expired** — neither hit within 7 days
- **⏳ Pending** — not enough forward data yet

Ambiguous bars (both TP and SL touched) are resolved conservatively by proximity of the bar's open to each level.

### Statistics

| Stat | Meaning |
|------|---------|
| **Total Signals** | Live entries + archived (pruned) entries |
| **TP Hit ✅** | Closed winners |
| **SL Hit ❌** | Closed losers |
| **Win Rate** | TP / (TP + SL) across live + archive |
| **Net R (closed)** | Cumulative R — each TP adds +R:R of the trade, each SL subtracts −1R |

### Overflow protection & archive

The journal is capped at 200 entries. On overflow it prunes in priority order **expired → closed (TP/SL) → pending last**, so **pending trades are never evicted** by new signals. Any pruned *closed* trade's stats (wins, losses, Net R) are folded into a persistent archive (`gp_v11_journal_v1_arch`) — so Win Rate and Net R **never reset** just because old rows scrolled off. "Clear Journal" wipes both the live journal and the archive.

### Export & dedup

- **📥 Export CSV** — full journal with timestamps, entry/SL/TP, R:R, status, close time and close price.
- **Dedup** — the same sym+tf+pattern logged within the last 4 hours is skipped to avoid duplicate entries across frequent auto-scans.

---

## 🎯 MTF Trend Filter

The **Multi-TimeFrame Trend Filter** rejects setups whose direction fights the higher-TF EMA50 trend — a classic "don't fight the tape" filter that cuts an estimated **~60% of counter-trend false positives**.

### How it works

For every setup on a given TF, GridPulse fetches candles on a **higher TF** and checks the **EMA50 slope** over the last 3 candles.

- **Bullish setup** rejected if higher-TF EMA50 is falling.
- **Bearish setup** rejected if higher-TF EMA50 is rising.

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

The EMA50 must slope by at least **±0.1%** over the last 3 candles to count as an active trend. Flat higher-TF EMA50 = filter is neutral. **ON by default** via the **MTF TREND FILTER** checkbox. Every MTF-rejected row is logged transparently as `MTF-SKIP: BTCUSDT/1h fights 4h EMA50 trend`.

---

## 🤖 Bot Range modes

Grid bot ranges are computed via one of three algorithms, selectable in the left panel:

| Mode | Formula | Best for |
|------|---------|----------|
| **Donchian 26** (default) | `[min(low, 26 bars) − ATR×0.4, max(high, 26 bars) + ATR×0.4]` | Sideways / range-bound markets |
| **Bollinger 20/2σ** | `[SMA(20) − 2σ − ATR×0.5, SMA(20) + 2σ + ATR×0.5]` | Volatile / mean-reversion assets |
| **ATR (legacy)** | `[price − ATR×N/2, price + ATR×N/2]` where N=18 if ADX≥18 else 10 | Backwards compatibility |

The chosen range appears in every GRID Launch Card as **"Range source"** (e.g. `Donchian 26 +ATR`). Donchian is the default because grid bots profit from oscillation within demonstrated swing highs/lows, which Donchian captures better than symmetric ATR ranges.

---

## 🌏 Session Filter

Downgrades STRONG→GRID setups during the **Asian night session (00-06 UTC)** where liquidity drops ~40%, false breakouts spike, and stop-hunts are common.

- **07-21 UTC** — no changes; STRONG signals pass normally.
- **00-06 UTC** — STRONG_BUY / STRONG_SELL are **downgraded to GRID**, logged as `Session-DOWNGRADE: BTCUSDT/4h STRONG→GRID (Asian night)`.

It does not reject setups — only reduces aggressiveness. **OFF by default** via **SESSION FILTER (07-21 UTC)** checkbox.

---

## 💧 Liquidity Guard

A **hard filter** that blocks STRONG classification for illiquid pairs. Average USD turnover per bar (over the last 20 bars) must exceed **$50,000**:

    avgTurnoverUSD = mean over last 20 bars of ((high + low + close) / 3 × volume)

If below the threshold, the pair is marked illiquid (💧 icon in the Activity Log) and any STRONG setup is **downgraded to GRID** — logged as `Liquidity-DOWNGRADE: MEMEUSDT/1h STRONG→GRID (< $50k/bar)`. The Guard is **always ON** by design — a safety floor, not a preference.

---

## 🏷 Symbol Unification

All symbols display in **Bybit style** regardless of exchange:

- Spot: `BTCUSDT`
- Perp: `BTCUSDT.P`
- Preserves multipliers: `1000PEPEUSDT` → `PEPE¹ᵏUSDT`, `10000CHEEMSUSDT` → `CHEEMS¹⁰ᵏUSDT`

The original exchange-native symbol is preserved internally for API calls — only the display is normalized, so cross-exchange comparison, sorting and copy-paste stay consistent.

---

## 🔍 Cell Magnifier

Hover any results-table cell to enlarge it **1.45×** with a glow effect. Toggle globally via the 🔍 button in the header (state persists in `localStorage['gp_mag']`) or press **Shift + M**. Wick/candle SVG cells enlarge only 1.15× to keep proportions; magnifier is disabled on highlighted rows.

---

## ⚡ STRONG-signal row highlighting

STRONG-mode rows stand out at a glance:

- **STRONG_BUY** — green gradient background, green left border, subtle 3s pulse.
- **STRONG_SELL** — red gradient background, red left border, red pulse.
- **⚡ icon** in the `#` column of every STRONG row.
- **GRID_BUY / GRID_SELL** — thin 2px left border in green/red (no gradient, no pulse).

Light theme uses softer palettes for contrast compliance.

---

## 🎯 Trade Plan v3

Launch Cards for STRONG modes display a rich, ATR-based trade plan:

- Entry (limL)
- Stop Loss (stopL)
- Conservative SL (stopC)
- **🎯 TP1 — 1R**
- **🎯 TP2 — ATR×N target** (TF-adaptive multiplier)
- **🎯 TP3 — 3R+ trail**
- **📉 Chandelier trailing stop (ATR×3)**
- Position size (from the v14.9.2 Position Sizing calculator)

GRID Launch Cards continue to show Pionex Grid Bot parameters (Lower / Upper / Grid Lines / Investment / ATR-based SL/TP) with the **Range source** field.

---

## 💾 Pair Presets

Named watchlists stored directly in your browser — no backend, no account, no cost.

### 5 built-in starter presets

| Icon | Name | Pairs |
|------|------|-------|
| 💎 | **Majors** | BTC · ETH · SOL · BNB · XRP · ADA · AVAX · DOT · LINK · MATIC |
| 🐸 | **Memes** | DOGE · SHIB · PEPE · WIF · BONK · FLOKI · MEME · POPCAT · BRETT · TURBO |
| 🤖 | **AI Tokens** | FET · AGIX · OCEAN · RNDR · TAO · WLD · GRT · AKT · ARKM · NMR |
| 🏛 | **Layer 1s** | ETH · SOL · AVAX · NEAR · APT · SUI · SEI · INJ · TIA · TON |
| 💧 | **DeFi Blue Chips** | UNI · AAVE · MKR · LDO · SNX · CRV · COMP · SUSHI · GMX · PENDLE |

- **💾 Save as…** — save current Custom Pairs as a named preset with custom icon.
- **⚙ Manage** — apply, delete, import/export JSON.
- **Shareable URL** — `tradescout.trade/?preset=<base64-encoded-json>` — recipient sees a consent prompt before importing.

Presets live under `gp_presets_v1`, independent from screener settings — clearing settings never deletes your presets.

---

## 🤝 Pionex companion workflow

GridPulse v14.9.x is designed around a focused, two-tool workflow:

    ┌─────────────────────────┐                ┌─────────────────────────┐
    │  GridPulse              │                │  Pionex                 │
    │  (scan + plan + track)  │  ────────►     │  (execute)              │
    │                         │  Open in       │                         │
    │  • Pick preset 💾       │  Pionex CTA    │  • Grid Bot             │
    │  • MTF-filtered scan 🎯 │  + UTM tags    │  • Reverse Grid         │
    │  • Trade Plan v3 📋     │                │  • Smart Trade          │
    │  • Auto-log to Journal 📓│               │                         │
    │  • Alerts 🔔✈️🎮        │                │                         │
    └─────────────────────────┘                └─────────────────────────┘

---

## ⌨ Hotkeys

A floating ⌨ button in the bottom-left corner shows the full hotkey reference at any time.

| Key | Action |
|-----|--------|
| Shift + T | Vertical / TikTok-friendly layout |
| Shift + P | Export PNG Cards (top 5, 1080×1350) |
| Shift + Alt + P | Export PNG Table (top 15, 1080×1350) |
| Shift + C | Generate 5-slide carousel |
| Shift + M | Toggle cell magnifier |
| Esc | Close any open modal (chart / Launch Card / preset / journal modals) |
| Double-click row | Highlight selected row, dim others |

> **Tip:** Hotkeys are ignored while typing inside `<input>`, `<textarea>`, or `<select>`.

---

## 🧠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for restricted regions) and calculates all indicators client-side in your browser.

    Exchange API ──► (optional proxy) ──► your browser ──► indicators ──► classifier
                                                                              │
                                                                              ▼
                                                                      Launch Card UI
                                                                      + Journal + Alerts

- No personal data is sent to any server.
- Your preferences, presets and journal are stored locally in `localStorage`.
- Scan results are kept only in memory (and `sessionStorage` cache).

### Proxy chain & fallback strategy

For each request, GridPulse tries: **direct fetch** → **Cloudflare Worker proxy** → **CodeTabs** → **AllOrigins** → **CORS.lol** → **ThingProxy**. Each proxy has a health tracker (auto-ban 30s after one failure, hard-ban 120s after 3 consecutive), and a rate-limit warning surfaces in the header when 3+ failures land within 10 seconds.

### Binance Futures GeoIP fallback

Some regions return HTTP 451 for `fapi.binance.com`. GridPulse tries `fapi/v1/exchangeInfo`, then `fapi/v1/ticker/price`, then mirrors the pair list and klines via Bybit so the scan still completes — logged transparently in the Activity Log.

### Cache

- **Pair lists / kline data / MCap rankings / funding rates:** cached 60s each (`sessionStorage`).

---

## 📈 Directional modes

Each setup is classified into one of five modes:

| Mode | Direction | Logic summary | Launch Card layout |
|------|-----------|---------------|---------------------|
| **STRONG BUY** | bullish | Two routes (Exhaustion / Quality). Filter-aware, TF-adaptive, MTF-verified. | Entry + SL + Cons.SL + **TP1 + TP2 + TP3 + Chandelier trail** + Position Sizing |
| **GRID BUY** | bullish | Moderate trend + controlled VWAP distance + acceptable R:R. | Grid lower / upper / width / lines + ATR-based SL + TP + Range source |
| **STRONG SELL** | bearish | Mirror of STRONG BUY | Entry + SL + Cons.SL + TP1 + TP2 + TP3 + Chandelier trail + Position Sizing |
| **GRID SELL** | bearish | Mirror of GRID BUY | Grid lower / upper / width / lines + ATR-based SL + TP + Range source |
| **SKIP** | any | Classified into WATCH / TREND / LOW R:R (+ downgrade reasons) with tooltip explanation | Reference price + warning |

### Mode sort priority

    STRONG_BUY  ≡  STRONG_SELL  >  GRID_BUY  ≡  GRID_SELL  >  SKIP

Within the same priority, ties are broken by **freshness bonus**, then R:R, then depth.

### Setup geometry validation

Stale setups where price has already crossed the entry or stop before the scan are rejected automatically (bullish: rejected if `price ≤ stopL` or `price ≥ limL`; bearish: mirror).

---

## 🎯 TF-adaptive Strictness

Every threshold scales by:

    effective_threshold  =  base_value  ×  TF_multiplier  ×  Strictness_multiplier

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
| **Soft** | 0.75 | Faster signals, more false positives |
| **Normal** | 1.00 | Default balance |
| **Strict** | 1.30 | Only the cleanest setups (best for 1D, 1W) |

### Base thresholds (before scaling)

| Metric | STRONG | GRID (max/min) |
|--------|-------:|---------------:|
| ADX | ≥ 25 | < 28 |
| VWAP distance % | side-aware | — |
| Volume ratio | ≥ 1.5× | — |
| R:R | ≥ 2.0 | ≥ 1.5 |
| Depth | ≥ 5 | — |

> **v14.9.1 note:** thresholds are **filter-aware** — if a filter checkbox (ADX / VOL / RR / VWAP) is OFF, that criterion is relaxed or ignored during classification instead of blocking it.

---

## 🛡 Classified SKIP reasons

| Tag | Meaning |
|-----|---------|
| ⚡ **WATCH** | A strong reversal candle is present, but R:R is too low for entry. |
| 🌊 **TREND** | Market is still trending too strongly, no reversal candle yet. |
| ⚖ **LOW R:R** | Reward too small relative to risk. |
| 🛡 **SKIP** | Edge case that doesn't match any of the above. |

STRONG signals can also be **downgraded to GRID** (shown as a tooltip suffix): `downgraded — Asian night session`, `downgraded — low liquidity`, or **rejected** entirely by the MTF filter (`fights higher-TF EMA50 trend`).

---

## ⭐ Two paths to STRONG

### 1️⃣ Exhaustion route

- ADX ≥ TF-scaled 25 · Volume ≥ 1.5× · R:R ≥ 2.0 · depth ≥ 5 · reversal candle · VWAP on correct side · MTF trend agrees (if ON)

### 2️⃣ Quality route

- ADX ≥ ~18 (≈72% of Exhaustion) · Volume ≥ 1.5× · R:R ≥ 2.0 · depth ≥ ~7 (≈140%) · reversal candle · ⭐ VWAP confluence required · MTF trend agrees (if ON)

Both routes scale with TF and Strictness, and are subject to Session Filter and Liquidity Guard.

---

## 📊 Indicators reference

| Indicator | Period | Notes |
|-----------|--------|-------|
| MACD | 12 / 26 / 9 | Divergence + histogram window |
| VWAP | 50 | Rolling, volume-weighted |
| VWAP bands | 50, ±1σ / ±2σ | ⭐ confluence detection |
| ATR | 14 | Candle-size filter, Grid SL/TP, Chandelier trail, TP targets |
| ADX | 14 | Trend strength; reused for grid range width |
| EMA50 (higher TF) | 50 | MTF Trend Filter |
| Donchian channels | 26 | Bot Range mode |
| Bollinger Bands | 20 / 2σ | Bot Range mode |
| Volume ratio | last vs. avg of 20 | Vol ≥ 1.1× / 1.5× filters |
| USD turnover | avg of 20 | Liquidity Guard |
| R:R | ATR-based TP vs. entry/stop | Reward-to-risk |

### ATR-based Grid SL / TP

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

### ATR-based Take Profit (STRONG, v14.9.1)

TP targets scale by TF (1m ×2.0 → 1M ×5.0 ATR), giving fair R:R across all timeframes. STRONG cards also recommend a **Chandelier trailing stop** at ATR × 3 from the extreme since entry.

---

## 💰 Funding-aware logic

Only active on **USDT Futures** market. When enabled, the screener fetches funding data and uses it to:

- show current rate, avg 7d (over 21 payments), daily (×3 sessions), annualized, hold-period cost, and next-payment countdown
- compute a directional bias label: 🟢 LONG-friendly / 🔴 LONG-costly / 🟢 SHORT-friendly / 🔴 SHORT-costly / ➖ Neutral
- optionally **SKIP** setups that exceed your configured daily funding threshold

| Setting | Effect |
|---------|--------|
| **CONSIDER FUNDING** | Master switch (Futures only) |
| **USE 7-DAY HISTORY** | Use the 21-sample average instead of the current rate |
| **SKIP IF EXCEEDS THRESHOLD** | Drop adverse rows beyond Max daily funding |
| **Max daily funding** | 0.05% / 0.10% / 0.20% / 0.30% / 0.50% / 1.00% |
| **Hold (days)** | Time horizon for the cost projection in the Launch Card |

---

## 🎛 Settings & filters

All settings are persisted in `localStorage` under `gp_settings_v14_9_2` and **auto-migrated** from earlier versions (`v14_9_1`, `v14_9_0`, `v14_8_2` … back to `v14_5`).

### Left panel — Timeframes & depth

| Control | Description |
|---------|-------------|
| **Timeframe row** | 1m / 5m / 15m / 30m / 1h / 4h / 1D / 1W / 1M |
| **Search depth** | How many bars back to look for a reversal pattern |
| **Min TF** | Minimum number of TFs that must produce a hit |
| **Extremum** | Lookback for validating reversal candle extreme |
| **Strictness** | soft / normal / strict |
| **🤖 Bot Range** | Donchian 26 (default) / Bollinger 20/2σ / ATR (legacy) |

### Right panel — Exchange & filters

| Control | Description |
|---------|-------------|
| **Exchange** | Pionex 🤝 (default) · Bybit · Binance · KuCoin · OKX |
| **Market** | Spot · USDT Futures |
| **Type** | Both · Bullish only · Bearish only |
| **Top MCap** | Restrict to CoinGecko top N (50/100/200/500/All) |
| **Max** | Cap the number of returned rows |
| **REVERSAL FILTER** | Require a real reversal candle |
| **CONSERVATIVE STOP** | Adds the wide stopC calculation |
| **VWAP filters** | VWAP DIRECTION · VWAP CONFLUENCE |
| **Candle filters** | ATR SIZE ×0.8 · VOLUME ×1.1 |
| **Trend / R:R** | ADX ≥ 18 · R:R ≥ 1.5 · MTF TREND FILTER (ON) · SESSION FILTER (OFF) |
| **Funding (Futures only)** | CONSIDER FUNDING · USE 7-DAY HISTORY · SKIP IF EXCEEDS THRESHOLD |

### Automation panel (v14.9.2)

| Control | Description |
|---------|-------------|
| **🔄 Auto** | Auto-refresh interval (1–1440 min) + ON/OFF |
| **🔔 Notify** | Desktop notifications ON/OFF |
| **✈️ TG** | Telegram bot token + chat_id + ON/OFF + 🧪 test |
| **🎮 Discord** | Webhook URL + ON/OFF + 🧪 test |
| **💰 Balance / Risk%** | Position sizing inputs |
| **📊 Backtest** | Historical win-rate ON/OFF |
| **📓 Journal** | Open Signal Journal |

### Header toggles

| Toggle | Effect |
|--------|--------|
| ⭐ **Star on GitHub** | Direct link to the repo |
| 🌐 **Language** | EN / UA / ES / RU / ZH switcher |
| 🌙 / ☀️ **Theme** | Dark / Light |
| 🔊 / 🔇 **Sound** | Scan-tick audio synth (WebAudio) |
| 🔍 / 🔎 **Magnifier** | Toggle cell hover magnification |
| 🤝 **Pionex Only** | Lock exchange to Pionex |

---

## 📋 Launch Cards

Each row has a 📋 button that opens a **Launch Card** — a focused, copy-paste-ready trading plan.

**STRONG BUY / STRONG SELL — Trade Plan v3**

- Entry (Buy/Sell Price), Stop Loss, Conservative SL
- 🎯 TP1 (1R) · 🎯 TP2 (ATR×N) · 🎯 TP3 (3R+ trail)
- 📉 Chandelier trailing stop (ATR×3)
- **💰 Position Sizing block (v14.9.2)** — units, value, % of balance, reward/loss, Expected Value

**GRID BUY / GRID SELL** (Pionex Grid Bot ready)

- Lower Limit · Upper Limit · Range width · Range source · Grid lines · Grid mode · Investment · ATR-based SL · ATR-based TP

**SKIP** — current price, entry/stop reference, warning that conditions are not optimal.

### Extras in every Launch Card

- Indicator confirmation panel (colour-coded ADX / R:R / Vol / VWAP% / Depth / TF)
- R:R bar with green / yellow / red zones
- Backtest win-rate + Expected Value (when Backtest is ON)
- Funding section (Futures only) — full breakdown + cost over N days + bias
- QR code for Pionex referral signup + 🤝 Pionex Affiliate badge
- Buttons: Copy all · Open chart (TradingView) · Share to Telegram · 🚀 Open in Pionex (UTM-tagged)

### UTM tracking on Pionex deep links

    ?utm_source=gridpulse
    &utm_medium=launchcard
    &utm_campaign={mode}        # strong_buy, grid_sell, etc.
    &utm_content={symbol}_{tf}  # BTCUSDT_4h

---

## 📸 Export & content tools

| Tool | Trigger | Output |
|------|---------|--------|
| CSV export | CSV button | Full results + funding columns |
| Journal CSV | 📥 in Journal | Full signal journal with statuses |
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

**NEW in v14.9.2:** the entire automation & journaling suite — Auto-refresh, Notify, Telegram, Discord, Position Sizing, Backtest, and all Signal Journal columns / statuses / stats (including Net R) — is fully translated across **all 5 languages**, with no English fallback remaining.

### Language priority

1. URL query: `?lang=en`, `?lang=ua`, `?lang=es`, `?lang=ru`, `?lang=zh`
2. `localStorage` preference (`gp_lang`)
3. `navigator.language` autodetect
4. Fallback: English

---

## 🛠 Self-hosting

GridPulse is a **single `index.html` file**. No build tools, no npm dependencies, no server-side code.

    git clone https://github.com/pro100off/gridpulse.git
    cd gridpulse
    python3 -m http.server 8000           # Python 3
    php -S localhost:8000                 # PHP
    npx serve .                           # Node
    caddy file-server --listen :8000      # Caddy
    # Or just open index.html directly — file:// works too.

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

For improved Pionex / Binance reliability in restricted regions, you can deploy your own Cloudflare Worker proxy. The default deployment uses `https://gridpulse-proxy.pro100off.workers.dev/?url=` (a rate-limited shared instance).

If you fork GridPulse, please deploy your own and update the `CUSTOM_PROXY` constant in `index.html`: set `const CUSTOM_PROXY = 'https://YOUR-WORKER.workers.dev/?url=';`.

---

## 🗄 Storage keys

| Key | Contents |
|-----|----------|
| `gp_settings_v14_9_2` | UI settings (auto-migrates from older keys) |
| `gp_presets_v1` | Pair presets |
| `gp_preset_last` | ID of the last-applied preset |
| `gp_lang` | Language preference |
| `gp_mag` | Cell Magnifier state |
| `gp_scan_serial` | Daily scan serial counter |
| `gp_v11_alerts_v1` | Alerts + position-sizing config (v14.9.2) |
| `gp_v11_journal_v1` | Signal journal entries (v14.9.2) |
| `gp_v11_journal_v1_arch` | Pruned closed-trade stats archive (v14.9.2) |

All user-specific data stays in your browser and **never leaves your device** (except tokens/webhooks sent only to Telegram/Discord when you enable those alerts).

---

## 📁 Repository structure

    gridpulse/
    ├── index.html                       current release (v14.9.2)
    ├── LICENSE                          CC BY-NC-SA 4.0
    ├── README.md                        this file
    ├── CHANGELOG.md                     full version history
    ├── GitHub.USER_GUIDE.md             detailed user guide
    ├── docs/
    │   ├── screenshot.png               preview image (OG / social cards)
    │   └── RELEASE_NOTES_v14.9.2.md     short release notes
    └── legacy/                          archived previous versions
        ├── index-v14.7.6.html
        ├── index-v14.8.0.html
        ├── index-v14.8.1.html
        ├── index-v14.8.2.html
        ├── index-v14.9.0.html
        └── index-v14.9.1.html

---

## 📜 Version history (carried-over highlights)

Full history lives in [CHANGELOG.md](CHANGELOG.md).

### v14.9.1 — "ATR-Based R:R + Filter-Aware Classification"

- 🎯 ATR-based Take Profit — TF-adaptive TP targets (1m×2.0 → 1M×5.0 ATR)
- 🎯 Trade Plan v3 — TP1 (1R), TP2 (ATR×N), TP3 (3R+ trail), Chandelier ATR×3
- 🎯 Filter-Aware Classification — `decideMode()` respects filter checkboxes
- 📊 Reject-reason diagnostics with R:R counter; R:R tooltip shows TP / Risk / Reward
- `SET_KEY` → `gp_settings_v14_9_1`

### v14.9.0 — "Old School Wisdom"

- 🎯 MTF Trend Filter · 🤖 Donchian/Bollinger/ATR bot ranges · 🌏 Session Filter
- 💧 Liquidity Guard · 🏷 Symbol Unification · 🔍 Cell Magnifier
- ⚡ STRONG row highlighting · 📈 Freshness ranking bonus

### v14.8.2 — "Pair Presets"

- 💾 Pair Presets (save/load watchlists), 5 built-in starters, JSON import/export, shareable URLs

### v14.8.1 — "Setup geometry validation"

- 🐛 Stale setups (price already crossed entry/stop) no longer pass the filter

### v14.8.0 — "Pionex Companion"

- 🤝 Official Partner badge · Pionex default exchange · "Open in Pionex" CTA with UTM tags · larger QR codes

### v14.7.6 — "TF-adaptive thresholds"

- TF-adaptive Strictness · two paths to STRONG · classified SKIP reasons · dual TikTok PNG · custom domain

### v14.7.5 — "Directional Grid Modes"

- Directional Grid Modes · breakout entry logic · light-theme contrast · hotkeys panel

### v14.7 / v14.6

- 📱 TikTok Mode · ✨ Highlight Row · 🏷 Watermark serial · 🎬 Carousel · 🔊 Scan tick sound · Screenshot button · Binance→Bybit mirror fallback · Pionex PERP discovery

---

## ⚠ Disclaimer

GridPulse is an **analytical tool, NOT financial advice**.

Cryptocurrency trading involves substantial risk of loss. Always do your own research (DYOR).

The screener identifies *potential* setups based on technical indicators. It does not predict price movement and does not guarantee profitability. Past patterns do not guarantee future results. Backtest win-rates are historical and do not guarantee future performance.

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

### Forking

Forks with your own referral are welcome — please keep a visible link back to the original repository, the CC BY-NC-SA 4.0 license, and the transparency disclosure in the footer.

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

All user-specific settings, presets and journal data stay in your browser's `localStorage` and **never leave your device**.

---

## 🤝 Contributing

Issues and PRs are welcome. For major changes, please open an issue first.

### Especially appreciated

- **Translations** — adding new languages or improving existing ones.
- **Built-in presets** — curated starter presets for new themes (RWA, gaming, restaking, etc.).
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

**What's new in v14.9.2?**
The **Automation & Journaling suite**: Auto-refresh scanning, Desktop/Telegram/Discord alerts, Position Sizing calculator, Backtest engine, and a full Signal Journal with auto TP/SL resolution, Net R tracking and overflow-safe archiving — all localized across 5 languages. See the [What's new section](#-whats-new-in-v1492--alerts--backtest--journal).

**Will v14.9.2 break my saved presets, settings or journal?**
No. Presets live under `gp_presets_v1`, journal under `gp_v11_journal_v1`, and settings auto-migrate from `gp_settings_v14_9_1` (and all older keys) to `gp_settings_v14_9_2` on first load.

**Do alerts fire for every setup?**
No — alerts and journaling fire only for **STRONG_BUY / STRONG_SELL** setups, with a 30-second per-symbol cooldown, to avoid noise from GRID/SKIP rows.

**Are my Telegram token / Discord webhook safe?**
They're stored in your browser's `localStorage` and sent only directly to Telegram / Discord. Don't use alert credentials on a shared or public machine.

**How honest is the Backtest win-rate?**
It reproduces the **live signal pipeline** (MACD reversal + rc/cc), so it measures what the screener would actually have traded — not naive candle-pattern statistics. It's still historical and not a guarantee of future results.

**Why is MTF ON by default?**
It removes ~40% of signals — overwhelmingly counter-trend false positives. Uncheck **MTF TREND FILTER** to restore the old behaviour.

**Can I disable Liquidity Guard?**
No — it's always ON. Use GRID mode for low-liquidity pairs (it doesn't require STRONG classification).

**What is Net R in the Journal?**
Cumulative R across all closed trades: each TP adds +R:R of the trade, each SL subtracts −1R. It survives journal overflow via the persistent archive.

**Is my data sent anywhere?**
No. Indicators run client-side. Outbound calls are exchange APIs (direct or via proxy), TradingView (only when you open a chart), Cloudflare Web Analytics (anonymous), Pionex referral URL (only on "Open in Pionex"), and Telegram/Discord (only if you enable those alerts).

**Where do I report bugs?**
[GitHub Issues](https://github.com/pro100off/gridpulse/issues). Include exchange + market, TF list, Strictness, MTF filter state, Bot Range mode, and relevant Activity Log lines.

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
- 📝 Release notes v14.9.2: [docs/RELEASE_NOTES_v14.9.2.md](docs/RELEASE_NOTES_v14.9.2.md)
- 🚀 Latest release: [Releases](https://github.com/pro100off/gridpulse/releases/latest)
- 📜 License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

⚡ **GridPulse v14.9.2** · 🔔 **Alerts + Backtest + Journal** · 🎯 **MTF Trend Filter** · 🤝 **Pionex Partner** · Built with care · single-file · no build tools · runs everywhere · © 2026 GridPulse Project
