# ⚡ GridPulse v14.2

> Free open-source multi-exchange crypto reversal screener — MACD + VWAP + ATR + ADX setups across Bybit, Binance, KuCoin, OKX, Pionex. One-click Launch Cards for Pionex Grid Bots.

🔗 **Live demo:** https://pro100off.github.io/gridpulse/
📢 **Telegram:** https://t.me/tradescoutfree
🐦 **Twitter:** https://x.com/tradeaiscout

![GridPulse screenshot](docs/screenshot.png)

---

## ✨ Features

- 🔍 **5 exchanges**: Bybit, Binance, KuCoin, OKX, Pionex (Spot + USDT Futures)
- 📊 **MACD reversal detection** with configurable depth and extremum lookback
- 🎯 **Multi-filter booster pack**: VWAP direction, VWAP confluence, ATR size, volume spike, ADX trend, R:R ratio
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
```

## 🔧 Self-hosting & custom CORS proxy

For high-traffic deployments, set up your own Cloudflare Worker — see [worker/README.md](worker/README.md). Then edit `index.html`:

```js
const CUSTOM_PROXY = 'https://your-worker.your-name.workers.dev/?url=';
```

## 📋 Roadmap

- [ ] Heatmap view across all timeframes
- [ ] Telegram bot for push alerts
- [ ] Backtest mode with historical setups
- [ ] More exchanges (MEXC, Gate, BingX)

## 🤝 Contributing

PRs welcome. If you fork and replace the referral link with your own — please keep a visible link back to this repository.

## 📄 License

CC BY-NC-SA 4.0 — Free for personal use. Commercial resale prohibited.

## 💚 Support the project

GridPulse is free. The only monetization is the [Pionex referral link](https://bit.ly/43bkdc7) — if you sign up via it, you help fund development. Thank you!

---

**Disclaimer:** Crypto trading is risky. This tool is not financial advice. Always do your own research.
