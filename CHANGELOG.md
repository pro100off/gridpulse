# Changelog

All notable changes to GridPulse are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [14.5] — 2026-06-11

Major stability release fixing critical issues with Binance Futures and Pionex Futures support, plus anonymous traffic analytics integration.

### Fixed

- **Binance Futures 451 / GeoIP restriction** — explicit detection of "restricted location" payloads via `isBinanceBlockedPayload()`. On block, transparently falls back to Bybit linear market-data as a mirror so the scan still completes for users behind GeoIP restrictions.
- **Pionex Futures PERP discovery** — switched to `/common/symbols?type=PERP&status=TRADING` with correct filtering by `s.type==='PERP' || s.contractType==='PERPETUAL'`. Previously returned 0 pairs.
- **Pionex Funding** — now uses `/market/indexes` (nextFundingRate) for current rate and `/market/fundingRates` for 7-day history. Bybit fallback retained when Pionex returns null.
- **Pionex 1M interval** explicitly mapped to `null` — Pionex public API does not expose monthly candles. The TF button now auto-disables via `refreshTFAvail()` instead of silently returning 1-minute candles (v14.4 misbehavior, silent data corruption).
- **KuCoin restored** in `safeFetch` direct-fetch list — has working CORS headers, routing through proxies in v14.4-hotfix added unnecessary 100-300ms per request.
- **safeFetch early-return** when first proxy loop produces a valid API-error payload — no point retrying 4 more proxies when the upstream API has already given us a structured error (saves up to 30 seconds on full GeoIP-bans).

### Added

- `readJsonResponse` + `isApiErrorPayload` — extracted as single source of truth for parsing and error detection across all exchange calls.
- **Cloudflare Web Analytics** integration for anonymous traffic statistics (page views, countries, referrers). No cookies, no individual user tracking, GDPR-friendly.
- `log.binFutMirror` i18n key in all 5 languages.
- Project infrastructure files: `LICENSE`, expanded `README.md`, `legacy/README.md`.
- Proxy log throttling — `shouldLogProxy()` limits noise to 1 message per proxy per 5 seconds.

### Changed

- `SET_KEY` bumped to `gp_settings_v14_5` (old v14.4 user settings will be re-initialized to defaults — clean migration).
- All version markers updated: JSON-LD `softwareVersion` → 14.5, lic-bar canary → `GRDPLS-V14-5-RELEASE-2026`, `og:title`, `twitter:title`, CSV filename (`gridpulse_v14_5_*.csv`), footer badge, header version display.
- Binance warning banner text refined — now mentions auto-fallback to Bybit instead of just warning about scan failures.

### Removed

- Accidental duplicate `<!DOCTYPE>` block from v14.4-hotfix scratch file.

### Migration notes

- Previous v14.3 archived to [`legacy/index-v14.3.html`](legacy/index-v14.3.html) alongside the existing v14.2 archive.
- **v14.4 was an internal intermediate revision and was never publicly released.** Its fixes are consolidated into v14.5. If you see references to v14.4 in commit history, they refer to development snapshots, not deployed versions.

---

## [14.3] — 2026-06-09

### Fixed

- **Launch Card "📋 Copy all"** now works reliably — switched from inline `onclick` to `addEventListener` mount to avoid HTML-attribute escaping collisions with complex multi-line text containing quotes and backslashes.

---

## [14.2] — 2026-06-08

### Fixed

- `render()` function syntax error that broke result table generation.
- `fPairs()` hardened with `Array.isArray()` guards — previously could throw `TypeError: not iterable` on unexpected API responses.
- **Binance Futures** ticker/price fallback when `exchangeInfo` endpoint is rate-limited or blocked.
- `fundingBias()` SHORT-direction labels and logic — previously showed misleading labels for short setups with positive funding.

### Added

- SHORT funding-bias i18n strings for all 5 languages (`lc.fundBiasShortOk`, `lc.fundBiasShortBad`).
- Full Launch-Card translation for Spanish, Russian, Chinese (previously partial fallback to English).
- Footer/disclosure translated for all 5 languages.
- Dated-contract filter (`_isDatedContract()`) — excludes expiring futures like `BTC-26DEC25` from scan results.
- Binance IP-ban notice banner — visible warning when Binance is selected as exchange.

### Changed

- `ua` (Ukrainian) locale now inherits full EN base for any missing keys.

---

## [14.1] — 2026-06-05

### Added

- VWAP confluence detection (⭐ marker for setups where entry aligns with VWAP or its standard-deviation bands).
- ATR-based grid range calculation for Bot Range and Buy/Sell Range columns.
- Mode classification (BUY / SELL / BOT / SKIP) with reasoning tooltip.
- R:R ratio calculation and filter (≥ 1.5 or ≥ 2.0).
- ADX trend strength filter and column.

---

## [14.0] — 2026-06-01

### Added

- Multi-exchange support: Bybit, Binance, KuCoin, OKX, Pionex.
- USDT Futures market type with funding rate awareness.
- 5-language i18n (en, ua, es, ru, zh).
- Launch Card modal with copy-paste-ready Grid Bot parameters.
- TradingView chart integration.
- CSV export.
- Light/Dark theme.

---

## [13.x] — 2026-05

Initial public releases. MACD divergence screener for Bybit Spot only.

For versions before v13.2, see git commit history.

---

## Conventions

This changelog follows these conventions:

- **Fixed** — bug fixes that resolve incorrect behavior
- **Added** — new features or capabilities
- **Changed** — modifications to existing behavior (potentially breaking)
- **Removed** — features that were deleted
- **Deprecated** — features marked for future removal but still functional
- **Security** — fixes related to security vulnerabilities

Version numbers follow [Semantic Versioning](https://semver.org/):
- **MAJOR** version for incompatible changes
- **MINOR** version for new functionality (backwards-compatible)
- **PATCH** version for backwards-compatible bug fixes

---

## Links

- [Live demo](https://pro100off.github.io/gridpulse/)
- [GitHub repository](https://github.com/pro100off/gridpulse)
- [Latest release](https://github.com/pro100off/gridpulse/releases/latest)
- [All releases](https://github.com/pro100off/gridpulse/releases)
