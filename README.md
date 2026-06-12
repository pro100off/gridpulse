# ⚡ GridPulse v14.5

Free open-source **multi-exchange crypto reversal screener** with MACD + VWAP + ATR + ADX + Funding-aware setups across Bybit, Binance, KuCoin, OKX, Pionex. One-click **Launch Cards** with ready-to-use parameters for Pionex Grid Bots.

🌐 **Live demo:** https://pro100off.github.io/gridpulse/  
📢 **Telegram:** https://t.me/tradescoutfree  
🐦 **Twitter / X:** https://x.com/tradeaiscout  
📜 **License:** [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

![GridPulse Screenshot](docs/screenshot.png)

---

## ✨ Features

- **5 exchanges:** Bybit, Binance, KuCoin, OKX, Pionex (Spot + USDT Futures)
- **Indicators:** MACD divergence, VWAP confluence ⭐, ATR, ADX, Volume ratio, R:R
- **Funding-aware setups** for perpetual contracts — current rate, 7-day average, daily/annual cost, hold-period projection, LONG/SHORT bias
- **5 languages:** 🇬🇧 English · 🇺🇦 Українська · 🇪🇸 Español · 🇷🇺 Русский · 🇨🇳 中文
- **Launch Cards** with copy-paste-ready Grid Bot parameters (BUY / SELL / BOT / SKIP modes)
- **TradingView integration** — open chart for any setup in one click
- **CSV export** of all scan results
- **No signup, no cookies, no individual user tracking** — anonymous traffic analytics only
- **Light / Dark theme** with full localization
- **Auto-fallback proxies** — works even when one exchange API is blocked in your region

---

## 🚀 Quick start

1. Open https://pro100off.github.io/gridpulse/
2. Choose exchange and market (Spot or USDT Futures)
3. Click **▶ Scan** — results in ~30 seconds
4. Click 📋 next to any symbol to open Launch Card with copy-paste-ready parameters
5. Open Pionex (or your preferred exchange), paste parameters into Grid Bot — start trading

---

## 🛠 How it works

GridPulse fetches public market data directly from exchange APIs (with proxy fallbacks for blocked regions). It calculates MACD, VWAP, ATR, ADX, and funding rates **client-side in your browser**. No personal data is sent to any server — your settings stay in `localStorage`.

For users behind GeoIP restrictions (e.g., Binance Futures HTTP 451), GridPulse transparently falls back to Bybit market-data as a mirror, so scans complete regardless of your location.

---

## 🆕 What's new in v14.5

- ✅ **Binance Futures** GeoIP fallback via Bybit market-data mirror
- ✅ **Pionex Futures** PERP discovery + `/market/indexes` funding endpoint
- ✅ **Pionex 1M** interval explicitly disabled (was silently returning 1-minute candles)
- ✅ **KuCoin** restored in direct-fetch list (-200ms per request)
- ✅ **safeFetch** early-return on structured API errors (-30s on full GeoIP-bans)
- ✅ **Cloudflare Web Analytics** — anonymous traffic stats (no cookies, GDPR-friendly)

See [CHANGELOG.md](CHANGELOG.md) for full history.

---

## 🖥 Self-hosting

GridPulse is a **single `index.html` file**. No build tools, no npm dependencies. Clone the repo and serve it with any static host:

```bash
git clone https://github.com/pro100off/gridpulse.git
cd gridpulse
python3 -m http.server 8000
# Open http://localhost:8000 in your browser
```

Works out of the box with:

- ✅ GitHub Pages
- ✅ Cloudflare Pages
- ✅ Netlify / Vercel
- ✅ Any web server (Apache, nginx, Caddy)
- ✅ Even file:// (open `index.html` directly in browser)

---

## 🌐 Optional: Cloudflare Worker proxy

For improved Pionex/Binance reliability in restricted regions, you can deploy your own Cloudflare Worker proxy. The default deployment uses `https://gridpulse-proxy.pro100off.workers.dev/` (rate-limited shared instance).

---

## 📁 Repository structure

```
gridpulse/
├── index.html               ← current release (v14.5)
├── LICENSE                  ← CC BY-NC-SA 4.0
├── README.md                ← this file
├── CHANGELOG.md             ← version history
├── docs/
│   └── screenshot.png       ← preview image (OG/social cards)
└── legacy/                  ← archived previous versions
    ├── index-v14.2.html
    └── index-v14.3.html
```

---

## ⚠️ Disclaimer

**GridPulse is an analytical tool, NOT financial advice.** Cryptocurrency trading involves substantial risk of loss. Always do your own research (DYOR).

The screener identifies *potential* setups based on technical indicators — it does not predict price movement and does not guarantee profitability. Past patterns do not guarantee future results.

---

## 💡 Transparency

GridPulse is free and open-source. The author earns a referral commission from Pionex when users sign up via the referral link and trade — **this is the project's only monetization**. There are no ads, no paid tiers, no premium features locked behind paywalls.

**Forks with your own referral are welcome** — please keep a visible link back to the original repository and preserve the CC BY-NC-SA 4.0 license. Do not remove the transparency disclosure in the footer.

---

## 📊 Analytics

GridPulse uses **Cloudflare Web Analytics** for anonymous, aggregate traffic statistics (page views, country breakdown, referrers). 

- ❌ No cookies
- ❌ No personal data collection
- ❌ No individual user tracking
- ❌ No fingerprinting
- ✅ GDPR-compliant
- ✅ Open about what's tracked

---

## 🤝 Contributing

Issues and PRs are welcome. For major changes, please open an issue first to discuss.

Translation contributions for any of the 5 supported languages (or adding new ones) are especially appreciated.

---

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License** ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).

**Commercial resale is prohibited.** Forking and personal use are encouraged.

See [LICENSE](LICENSE) for full terms.

---

## 🔗 Links

- 🌐 [Live demo](https://pro100off.github.io/gridpulse/)
- 📢 [Telegram channel](https://t.me/tradescoutfree)
- 🐦 [Twitter / X](https://x.com/tradeaiscout)
- 📋 [GitHub Issues](https://github.com/pro100off/gridpulse/issues)
- 📝 [Changelog](CHANGELOG.md)
- 📦 [Latest release](https://github.com/pro100off/gridpulse/releases/latest)
