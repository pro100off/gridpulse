# ⚡ GridPulse

**Multi-Exchange Crypto Reversal Screener · Pionex Grid Bot Ready**

Real-time MACD-розворотний скринер для 5 бірж з готовими **Launch Cards** для Pionex Grid / Smart Trade ботів.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-blue.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
![Version](https://img.shields.io/badge/version-13.2-green.svg)
![Exchanges](https://img.shields.io/badge/exchanges-5-orange.svg)
![No Backend](https://img.shields.io/badge/backend-none-brightgreen.svg)
![Open Source](https://img.shields.io/badge/open%20source-yes-success.svg)

🌐 **Спробувати онлайн (без реєстрації):** [pro100off.github.io/gridpulse](https://pro100off.github.io/gridpulse/)

📢 **Telegram-канал:** [@tradescoutfree](https://t.me/tradescoutfree)

---

## 🎯 Що це?

**GridPulse** сканує крипторинок на 5 біржах одночасно, шукає **MACD-розвороти** з підтвердженням реверсної свічки, аналізує VWAP / ATR / ADX і генерує **готові параметри** для запуску Pionex Grid Bot, Smart Trade, Reverse Grid.

### 🔑 Ключові фішки

- 🔄 **Реальні MACD-розвороти** з аналізом глибини імпульсу
- 📊 **Launch Cards** — готові параметри (Buy/Sell/SL/TP) для одного кліку на Pionex
- 🤖 **3 режими рекомендацій**: Grid Bot / Grid Buy / Grid Sell / Skip
- 📐 **Автодіапазони** для Grid Bot на основі ATR і ADX
- ⭐ **VWAP Confluence** — пошук злиття ціни з ключовими рівнями
- 📈 **TradingView графіки** одним кліком
- 🌐 **5 бірж**: Bybit · Binance · KuCoin · OKX · **Pionex** (пріоритет)
- 📥 **CSV-експорт** з повною атрибуцією
- 💯 **Без backend** — все працює в браузері

---

## 🚀 Швидкий старт

### Варіант 1: Онлайн (рекомендовано)
👉 Просто відкрийте: **https://pro100off.github.io/gridpulse/**

### Варіант 2: Локально
1. Скачайте `index.html` (Code → Download ZIP, або з вкладки Releases)
2. Відкрийте файл у будь-якому сучасному браузері (Chrome / Edge / Firefox)
3. Натисніть **▶ Сканувати**

### Варіант 3: Свій форк на GitHub Pages
1. Натисніть **Fork** угорі цієї сторінки
2. У вашій копії: Settings → Pages → Branch `main` → Save
3. Через хвилину доступно за `https://<your-user>.github.io/gridpulse/`

---

## 📊 Підтримувані біржі та ринки

| Біржа | Спот | Ф'ючерси USDT | Особливості |
|---|---|---|---|
| **Pionex** ⭐ | ✅ | ⚠️ обмежено | Пріоритет — Launch Cards оптимізовані під Grid Bots |
| Bybit | ✅ | ✅ | Прямий API |
| Binance | ✅ | ✅ | Через CORS-проксі |
| KuCoin | ✅ | ✅ | Через CORS-проксі |
| OKX | ✅ | ✅ | Через CORS-проксі |

---

## 🧠 Алгоритм пошуку сетапів

1. **MACD Reversal** — пошук перших ознак розвороту гістограми (бичачий / ведмежий)
2. **Reversal Candle** — перевірка реверсної свічки на екстремумі (3–10 баров lookback)
3. **Confirmation Candle** — наступна свічка підтверджує патерн
4. **VWAP + Bands** — конфлюенс з ключовими рівнями (σ, 2σ)
5. **ATR** — мінімальний розмір свічки × 0.8
6. **Volume** — об'єм реверсної свічки × 1.1 від середнього
7. **ADX** — сила тренду (≥ 18)
8. **R:R** — мінімум 1.5 для входу
9. **decideMode()** — фінальна рекомендація: **BOT / BUY / SELL / SKIP**

---

## 📋 Launch Card — що це?

Натиснувши **📋** біля будь-якого результату, ви отримаєте інтерактивну картку з:

- 📊 **Параметрами для Pionex**: Buy Price, Stop Loss, Take Profit, Trailing
- 📈 **Підтвердженням індикаторів**: ADX, Volume, VWAP%, R:R
- 📝 **Покроковою інструкцією** для запуску бота
- 🚀 **QR-кодом** реєстрації на Pionex
- 📋 Кнопкою **"Копіювати все"** — текстова версія для блокноту/Telegram

---

## 🎨 Скриншоти

> 💡 *Після першого скріншоту видаліть цей блок і додайте `![GridPulse Screenshot](docs/screenshot.png)`*

---

## 🛠️ Технології

- **Pure HTML/CSS/JS** — без фреймворків, без збірки
- **TradingView Widget** — для інтерактивних графіків
- **QRCode.js** — для генерації QR-кодів реферального посилання
- **CoinGecko API** — для ринкової капіталізації
- **CORS-проксі**: codetabs.com / allorigins.win — для обходу обмежень бірж

---

## 🛡️ Ліцензія

[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/) (CC BY-NC-SA 4.0)

**✓ Дозволено:** особисте використання, модифікація, поширення зі збереженням атрибуції.

**✗ Заборонено:** комерційне використання, перепродаж, видалення авторської інформації та реферальних посилань.

Для комерційної ліцензії: [@tradescoutfree](https://t.me/tradescoutfree)

---

## 💚 Підтримати проєкт

GridPulse безкоштовний і завжди буде open source. Якщо інструмент допоміг — підтримайте автора, зареєструвавшись на **Pionex** за реферальним посиланням у скринері. Це єдина форма монетизації проєкту.

- 📢 **Telegram-канал:** [@tradescoutfree](https://t.me/tradescoutfree)
- 🐙 **GitHub:** [github.com/pro100off/gridpulse](https://github.com/pro100off/gridpulse)
- ⭐ Поставте зірочку, якщо корисно!

---

## ⚠️ Дисклеймер

GridPulse надається **«як є»** (as-is), без жодних гарантій. Автор не несе відповідальності за фінансові втрати, торгові рішення або іншу шкоду, що виникла внаслідок використання інструменту. Криптотрейдинг пов'язаний з високими ризиками — завжди робіть власний аналіз.

---

**⚡ Made with ❤️ for crypto traders · © 2026 GridPulse Project**
