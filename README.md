# ⚡ GridPulse v14.7.5

Free open-source **multi-exchange crypto reversal screener** with directional **STRONG / GRID BUY/SELL** modes, MACD + VWAP + ATR + ADX + Funding-aware setups across Bybit, Binance, KuCoin, OKX, Pionex. One-click **Launch Cards** with ready-to-use parameters for Pionex Grid Bots.

**Live demo:** [https://pro100off.github.io/gridpulse/](https://pro100off.github.io/gridpulse/)
**Telegram:** [https://t.me/tradescoutfree](https://t.me/tradescoutfree)
**Twitter / X:** [https://x.com/tradeaiscout](https://x.com/tradeaiscout)
**License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

[![GridPulse Screenshot](docs/screenshot.png)](docs/screenshot.png)

---

## ✨ Features

* **5 exchanges:** Bybit, Binance, KuCoin, OKX, Pionex (Spot + USDT Futures)
* **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, Volume ratio, R:R
* **Funding-aware setups** for perpetual contracts — current rate, 7-day average, daily / annual cost, hold-period projection, LONG/SHORT bias
* **5 languages:** English · Українська · Español · Русский · 中文
* **Launch Cards** with copy-paste-ready Grid Bot parameters — directional modes:
  **STRONG BUY** / **GRID BUY** / **STRONG SELL** / **GRID SELL** / **SKIP**
* **Breakout entry logic** — `limL` placed at the opposite extreme of the reversal candle (bearish: low, bullish: high)
* **TradingView integration** — open chart for any setup in one click
* **CSV export** of all scan results
* **Daily screenshot / vertical PNG / 5-slide carousel** export — accessible via hotkeys for content creators
* **No signup, no cookies, no individual user tracking** — anonymous traffic analytics only
* **Light / Dark theme** with full localization and high-contrast rows
* **Auto-fallback proxies** — works even when one exchange API is blocked in your region

---

## ⌨ Hotkeys

Floating `⌨` button in the bottom-left corner lists all shortcuts:

| Key | Action |
|---|---|
| `Shift + T` | Vertical / TikTok-friendly layout |
| `Shift + P` | Export PNG 1080×1350 |
| `Shift + C` | Generate 5-slide carousel |
| `Esc` | Close modals |
| Double-click row | Highlight / dim others |

---

## 🚀 Quick start

1. Open [https://pro100off.github.io/gridpulse/](https://pro100off.github.io/gridpulse/)
2. Choose exchange and market (Spot or USDT Futures)
3. Click **▶ Scan** — results in ~30 seconds
4. Click 📋 next to any symbol to open the Launch Card with copy-paste-ready parameters
5. Open Pionex (or your preferred exchange), paste parameters into a Grid Bot — start trading

---

## 🧠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for blocked regions). It calculates MACD, VWAP, ATR, ADX, and funding rates **client-side in your browser**. No personal data is sent to any server — your settings stay in `localStorage`.

For users behind GeoIP restrictions (e.g., Binance Futures HTTP 451), GridPulse transparently falls back to Bybit market-data as a mirror, so scans complete regardless of your location.

### Directional modes (v14.7.5)

Each setup is classified into one of five modes:

| Mode | Direction | Rules | Launch Card layout |
|---|---|---|---|
| **STRONG BUY** | bullish | Strict: ADX ≥ 25, VWAP < −5 %, Vol ≥ 1.5×, depth ≥ 5, R:R ≥ 2.0, reversal candle present | Limit buy + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID BUY** | bullish | Relaxed: ADX < 28, \|VWAP\| ≤ 5 %, R:R ≥ 1.5 | Grid lower / upper / width / lines + SL + TP |
| **STRONG SELL** | bearish | Mirror of STRONG BUY | Limit sell + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID SELL** | bearish | Mirror of GRID BUY | Same as GRID BUY |
| **SKIP** | any | Trend too strong (ADX ≥ 28 & \|VWAP\| > 7 %) or low R:R | Reference price + warning |

---

## 📝 What's new in v14.7.5

* **Directional Grid Modes** — replaced unified `BOT` mode with `STRONG_BUY` / `GRID_BUY` / `STRONG_SELL` / `GRID_SELL` / `SKIP`, with mirrored strict / relaxed entry rules and per-mode Launch Card layouts.
* **Breakout entry logic** — `limL` placed at the opposite extreme of the reversal candle (bearish: low, bullish: high).
* **Light-theme contrast boost** — zebra-striped rows, accent-coloured badges with visible borders, no text-shadow blur.
* **Light TikTok mode** — vertical layout no longer forces black background when light theme is active.
* **Hotkeys panel** — floating `⌨` button (bottom-left) with `Shift+T` / `Shift+P` / `Shift+C` / `Esc` / double-click row.
* **TikTok-branded UI hidden** — TikTok PNG button, Carousel button, vertical-mode toggle, and Launch Card "Export for TikTok" no longer visible. All functions retained and accessible via hotkeys.
* **STRONG SELL Launch Card fix** — was silently failing due to a stray Cyrillic character; now opens consistently.
* **Carousel `indicators` array fix** — duplicate VWAP% fragment broke `<script>` parsing; restored.
* **Pionex `_PERP` / OKX `-SWAP` symbols** in row handlers — migrated to `data-*` attributes for stable interactivity.

See [CHANGELOG.md](CHANGELOG.md) for full history.

---

## 🛠 Self-hosting

GridPulse is a **single `index.html` file**. No build tools, no npm dependencies. Clone the repo and serve it with any static host:

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
