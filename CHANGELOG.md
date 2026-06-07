# Changelog

All notable changes to GridPulse are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
versioning based on [Semantic Versioning](https://semver.org/).

---

## [14.3] — 2026-06-06 — Launch Card Hotfix

### Fixed
- 🐛 **Launch Card → «Copy all» button**: the button silently failed on click
  due to quote and newline escaping inside the inline
  `onclick="copyText(${JSON.stringify(allText)})"`. The attribute string broke,
  and the browser threw a silent syntax error.
- ✅ Replaced the inline `onclick` with `addEventListener('click', …)` attached
  **after** the HTML is mounted into the DOM. The handler now closes over the
  local `allText` variable — no escaping, no global buffers.

### Changed
- 🔖 `softwareVersion` in JSON-LD bumped: `14.2` → `14.3`.
- 🏷 Canary tag in HTML comment: `GRDPLS-V14-3-RELEASE-2026`.
- 📁 CSV export filename pattern: `gridpulse_v14_3_YYYY-MM-DD.csv`.
- 🔑 `localStorage` settings key: `gp_settings_v14_3`
  (legacy v14.2 settings auto-migrate on first launch).
- 🏷 Open-Graph / Twitter-card meta and the visible version label in the UI
  header updated to **v14.3**.

### Migration
- ✅ No action required for end users — a hard reload (`Ctrl+Shift+R`) is
  enough to flush the browser cache.
- 🗂 v14.2 is preserved at `/legacy/index-v14.2.html` for historical reference.


---

## [14.2] — 2026-06-04 — Open Edition

### Added
- 🌍 Full i18n: Ukrainian, English, Spanish, Russian, Chinese — auto-detected
  from `navigator.language`, switchable at runtime, persisted in `localStorage`.
- 🌗 Light / dark theme toggle with persistence.
- 💾 All UI settings (timeframes, depth, filters, exchange, market) persist
  across sessions via `localStorage`.
- 🔗 Social bar: Telegram / GitHub / Twitter / native Share API.
- 📱 Native `navigator.share()` support on mobile browsers.
- 🏷 Open-Graph meta tags for richer link previews.
- 📜 Lineage comment block in `index.html` referencing both v13.2 and v14.2
  canary markers (passive proof-of-authorship via git blame; no runtime checks).
- 💡 Transparent affiliate-disclosure block in the footer (FTC/EU compliant).

### Changed
- 📄 Re-licensed footer with a calm, community-first tone instead of legal threats.
- 📚 README rewritten from scratch (UA + EN). CHANGELOG and CONTRIBUTING added.
- 🗂 Repo restructured: `LICENSE`, `README.md`, `CHANGELOG.md`, `CONTRIBUTING.md`,
  `docs/screenshot.png` and `legacy/` directory.

### Removed
- 🚫 Anti-tamper watchdog (MutationObserver hijack detection).
- 🚫 Base64-XOR obfuscation of the referral URL.
- 🚫 Aggressive license modal with DMCA / civil-liability language.

### Reasoning
The protection layer in v13.2 was optimized for per-user retention of the
referral link. Empirically, this trade-off is wrong for an open-source project:
it kills GitHub stars, scares away forks, and prevents the community feedback
loop that ultimately drives adoption. v14.2 reverses the trade-off — community
growth > per-fork retention. Honest disclosure + a clear, single-line fork
instruction (`const REF_URL = '...'`) is the new social contract.

### Migration
- No action required for end users — the URL is identical.
- v13.2 remains permanently available at `/legacy/v13.2.html` and as
  the `v13.2` git tag for historical reference.

---

## [13.2] — 2026-05-30 — Initial Release · archived

### Added
- 🚀 Initial public release on GitHub Pages.
- 📊 Multi-exchange scanner: Bybit, Binance, KuCoin, OKX, Pionex.
- 🔍 MACD reversal detector with extremum / depth controls.
- 💧 VWAP + ±1σ / ±2σ bands.
- 🌪 ATR-14 candle-size filter.
- 📐 ADX-14 trend-strength filter (DMI+ / DMI-).
- 🎯 R:R filter.
- 🪪 Launch Card per setup (Pionex Smart Trade / Reverse Grid Bot params).
- 📈 Inline TradingView chart with MACD + VWAP overlays.
- 📥 CSV export.

### Notes
- v13.2 shipped with an anti-tamper protection layer; deprecated and removed
  in v14.2 in favour of community openness. See v14.2 reasoning above.
- Archived URL: `/legacy/v13.2.html`. Git tag: `v13.2`.
