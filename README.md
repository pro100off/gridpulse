# ⚡ GridPulse v14.7.6

Free open-source **multi-exchange crypto reversal screener** with directional **STRONG / GRID BUY/SELL** modes, **TF-adaptive Strictness**, MACD + VWAP + ATR + ADX + Funding-aware setups across Bybit, Binance, KuCoin, OKX, and Pionex. Includes one-click **Launch Cards** with ready-to-use parameters for Pionex Grid Bots.

**Live demo:** [https://tradescout.trade/](https://tradescout.trade/)  
**GitHub Pages mirror:** [https://pro100off.github.io/gridpulse/](https://pro100off.github.io/gridpulse/)  
**GitHub:** [https://github.com/pro100off/gridpulse](https://github.com/pro100off/gridpulse)  
**Telegram:** [https://t.me/tradescoutfree](https://t.me/tradescoutfree)  
**Twitter / X:** [https://x.com/tradeaiscout](https://x.com/tradeaiscout)  
**License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

[![GridPulse Screenshot](docs/screenshot.png)](docs/screenshot.png)

---

## ✨ Features

* **5 exchanges:** Bybit, Binance, KuCoin, OKX, Pionex (**Spot + USDT Futures**)
* **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, Volume ratio, R:R
* **TF-adaptive Strictness** — thresholds scale automatically by timeframe (**1m softer → 1W stricter**) with a global selector: **soft / normal / strict**
* **Two paths to STRONG setups**:
  * **Exhaustion** — blow-off trend + reversal candle
  * **Quality** — moderate trend + ⭐ VWAP confluence + strong R:R
* **Classified SKIP reasons** with exact per-row tooltip thresholds:
  * ⚡ **WATCH** — good reversal candle, but reward too low
  * 🌊 **TREND** — trend still too strong, no valid reversal yet
  * ⚖ **LOW R:R** — poor reward relative to risk
* **Funding-aware setups** for perpetual contracts — current rate, 7-day average, daily / annual cost, hold-period projection, LONG/SHORT bias
* **5 languages:** English · Українська · Español · Русский · 中文
* **Launch Cards** with copy-paste-ready Grid Bot parameters — directional modes:
  * **STRONG BUY**
  * **GRID BUY**
  * **STRONG SELL**
  * **GRID SELL**
  * **SKIP**
* **Breakout entry logic** — `limL` is placed at the opposite extreme of the reversal candle
  * bearish reversal → candle **low**
  * bullish reversal → candle **high**
* **TradingView integration** — open chart for any setup in one click
* **CSV export** of all scan results
* **Daily screenshot / vertical PNG / 5-slide carousel** export — accessible via hotkeys
* **No signup, no cookies, no individual user tracking** — anonymous traffic analytics only
* **Light / Dark theme** with full localization and high-contrast rows
* **Auto-fallback proxies** — scan still completes even when one exchange API is blocked in your region
* **Custom domain support** — canonical URL: [https://tradescout.trade/](https://tradescout.trade/)

---

## ⌨ Hotkeys

Floating `⌨` button in the bottom-left corner lists all shortcuts:

| Key               | Action                            |
| ----------------- | --------------------------------- |
| `Shift + T`       | Vertical / TikTok-friendly layout |
| `Shift + P`       | Export PNG Cards (top 5)          |
| `Shift + Alt + P` | Export PNG Table (top 15)         |
| `Shift + C`       | Generate 5-slide carousel         |
| `Esc`             | Close modals                      |
| Double-click row  | Highlight / dim others            |

---

## 🚀 Quick start

1. Open [https://tradescout.trade/](https://tradescout.trade/)
2. Choose exchange and market (**Spot** or **USDT Futures**)
3. Select timeframes and, if needed, adjust **Strictness** (`soft / normal / strict`)
4. Click **▶ Scan** — results usually appear in ~30 seconds
5. Click `📋` next to any symbol to open the **Launch Card** with copy-paste-ready parameters
6. Open Pionex (or your preferred exchange), paste parameters into a Grid Bot, and manage the trade manually

---

## 🧠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for restricted regions). It calculates MACD, VWAP, ATR, ADX, Volume ratio, and funding rates **client-side in your browser**.

No personal data is sent to any server. Your preferences are stored locally in `localStorage`.

For users behind GeoIP restrictions (for example, Binance Futures HTTP 451), GridPulse transparently falls back to alternative market-data routes so scans can still complete.

---

## 📈 Directional modes (v14.7.6)

Each setup is classified into one of five modes:

| Mode              | Direction | Logic summary | Launch Card layout |
| ----------------- | --------- | ------------- | ------------------ |
| **STRONG BUY**    | bullish   | Two routes: **Exhaustion** (strong blow-off trend + reversal candle + high confirmation) or **Quality** (moderate trend + ⭐ VWAP confluence + solid R:R). Thresholds are **TF-adaptive** and affected by **Strictness**. | Limit buy + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID BUY**      | bullish   | Relaxed directional grid conditions with moderate trend, controlled VWAP distance, and acceptable reward/risk. Thresholds scale by TF / Strictness. | Grid lower / upper / width / lines + SL + TP |
| **STRONG SELL**   | bearish   | Mirror logic of **STRONG BUY** | Limit sell + Stop loss + Conservative SL + fixed TP + trailing trigger |
| **GRID SELL**     | bearish   | Mirror logic of **GRID BUY** | Grid lower / upper / width / lines + SL + TP |
| **SKIP**          | any       | Setup does not qualify; now classified into **WATCH / TREND / LOW R:R** with tooltip explanation showing exact current thresholds | Reference price + warning |

### TF-adaptive thresholds

Unlike previous versions with static cutoffs, v14.7.6 scales thresholds by timeframe:

* **Lower TFs** (`1m`, `5m`) are more permissive
* **Higher TFs** (`1D`, `1W`) are stricter
* A single **Strictness** selector applies a global multiplier:
  * **Soft**
  * **Normal**
  * **Strict**

This affects:

* STRONG / GRID qualification
* ADX filter thresholds
* VWAP distance sensitivity
* minimum R:R
* depth requirements
* filter logic in the right-side panel

---

## 📝 What's new in v14.7.6

* **TF-adaptive thresholds** — STRONG / GRID / SKIP cutoffs now scale by timeframe (**1m softer → 1W stricter**) through a single **Strictness** selector
* **Two paths to STRONG** — added **Quality** route (moderate trend + ⭐ VWAP confluence + R:R ≥ 2) alongside the existing **Exhaustion** logic
* **Classified SKIP reasons** — setups now show:
  * ⚡ **WATCH**
  * 🌊 **TREND**
  * ⚖ **LOW R:R**
  with exact thresholds in per-row tooltips
* **Filter ADX / R:R thresholds now scale by timeframe** instead of using fixed global values
* **Mode sort priority fixed** — now:
  * `STRONG > GRID > SKIP`
* **Bot Range / B/S Range cell colours** and Launch Card sections now follow the new directional mode naming
* **Full i18n coverage** for new labels and SKIP categories across:
  * English
  * Ukrainian
  * Spanish
  * Russian
  * Chinese
* **Custom domain support** — canonical URL now points to:
  * [https://tradescout.trade/](https://tradescout.trade/)
* **Settings migration**
  * `SET_KEY → gp_settings_v14_7_6`

---

## 🧾 Previous major changes carried into v14.7.6

### v14.7.5

* **Directional Grid Modes** — replaced unified `BOT` mode with:
  * `STRONG_BUY`
  * `GRID_BUY`
  * `STRONG_SELL`
  * `GRID_SELL`
  * `SKIP`
* **Breakout entry logic** — `limL` now points to the opposite extreme of the reversal candle
* **Light-theme contrast boost** — zebra-striped rows, accent-coloured badges with visible borders, no text-shadow blur
* **Light TikTok mode** — vertical layout no longer forces a black background when light theme is active
* **Hotkeys panel** — floating `⌨` button with quick shortcut reference
* **TikTok-branded UI hidden** — export functions retained and accessible via hotkeys
* **STRONG SELL Launch Card fix** — resolved silent failure caused by a stray Cyrillic character
* **Carousel parsing issue fixed**
* **Stable row interaction for Pionex `_PERP` and OKX `-SWAP` symbols**

### v14.7.4 / v14.7.2 / v14.7

* Dark-theme contrast boost
* Restored localization blocks
* TikTok watermark fixes
* Highlight row mode
* Vertical TikTok layout
* PNG export and carousel generation
* Screenshot and watermark tools
* Binance Futures fallback improvements
* Pionex PERP discovery improvements

See [CHANGELOG.md](CHANGELOG.md) for full history.

