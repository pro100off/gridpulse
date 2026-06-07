# ⚡ GridPulse v14.3

> Free open-source multi-exchange crypto reversal screener — MACD + VWAP + ATR + ADX setups across Bybit, Binance, KuCoin, OKX, Pionex. One-click Launch Cards for Pionex Grid Bots.

🔗 **Live demo:** https://pro100off.github.io/gridpulse/
📢 **Telegram:** https://t.me/tradescoutfree
🐦 **Twitter:** https://x.com/tradeaiscout

![GridPulse screenshot](docs/screenshot.png)

---

## 🆕 What's new in v14.3

- 🐛 **Fixed**: «Copy all» button in Launch Card now works correctly
  (was silently failing due to `onclick` attribute escaping).
- 🔖 Bumped metadata: `softwareVersion`, canary tag, CSV filename pattern,
  `localStorage` key.

See full history in [CHANGELOG.md](./CHANGELOG.md).
Previous stable version archived at [`legacy/index-v14.2.html`](./legacy/index-v14.2.html).

---

## ✨ Features

- 🔍 **5 exchanges**: Bybit, Binance, KuCoin, OKX, Pionex (Spot + USDT Futures)
- 📊 **MACD reversal detection** with configurable depth and extremum lookback
- 🎯 **Multi-filter booster pack**: VWAP direction, VWAP confluence, ATR size, volume spike, ADX trend, R:R ratio
- 💰 **Funding-rate awareness** for perpetual futures (current + 7-day history, holding-cost calculator, auto-SKIP on threshold)
- 🤖 **Pionex Launch Cards** — auto-calculated parameters for Grid Bot, Smart Trade BUY/SELL with copy-to-clipboard
- 🌐 **5 languages**: English, Ukrainian, Spanish, Russian, Chinese
- 🌙 **Dark/Light themes** with persistent settings
- 📈 **Embedded TradingView charts** with MACD + VWAP studies
- 💾 **CSV export** of all signals
- 🔄 **Multi-proxy rotation** for reliability under load
- 💨 **Smart caching** — no API spam on page reload

## 🚀 Quick start

Just open https://pro100off.github.io/gridpulse/ — no signup, no install.

Or clone and serve locally:

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse
python3 -m http.server 8080
# open http://localhost:8080
