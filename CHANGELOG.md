# GridPulse Changelog

## [14.7.6] - 2026-06-23 — TF-adaptive Strictness + Classified SKIP

### Added
- **TF-adaptive thresholds**: STRONG/GRID/SKIP cutoffs now scale per timeframe
  (1m softer ... 1W stricter) via a single **Strictness** selector
  (soft / normal / strict) in the right control panel.
- **Two paths to STRONG**:
  - **Exhaustion** — strong trend + extreme reversal candle (blow-off top/bottom)
  - **Quality** — moderate trend + ⭐ VWAP confluence + R:R ≥ 2
- **Classified SKIP reasons** with per-row tooltip showing exact thresholds:
  - `⚡ WATCH` — strong reversal candle but R:R too low → watch for re-entry
  - `🌊 TREND` — trending market, no reversal yet → wait for reversal candle
  - `⚖ LOW R:R` — poor reward/risk ratio → skip
- **Dual TikTok PNG export**: Cards (top 5, mobile-readable) and Table (top 15, analytical).
  Hotkeys: `Shift+P` for Cards, `Shift+Alt+P` for Table.
- **ATR-based SL/TP** for GRID bots (replaces fixed −20%/+15% with TF-adaptive ATR multipliers).
- **i18n** for all new mode labels, SKIP categories, and card layout: EN, UA, ES, RU, ZH.
- **Custom domain**: canonical URL changed to https://tradescout.trade/
  (still served from `pro100off.github.io/gridpulse/`).
- **SEO hreflang tags** for all 5 languages.
- **?lang=xx URL param** for direct language link entries (used by sitemap).

### Fixed
- `findSetup()` ADX≥18 and R:R≥1.5 checkbox thresholds now scale with TF/strictness
  instead of being hardcoded.
- Mode-column sort priority corrected: STRONG > GRID > SKIP (was alphabetical).
- Bot Range / B/S Range cell highlight colour now uses STRONG_*/GRID_* names.
- Launch Card section title colour follows new mode names.
- `countSetupsByMode()` now maps new mode names to BUY/SELL/BOT/SKIP buckets.
- Carousel ranking and slide rendering updated for new mode names.

### Changed
- `SET_KEY` → `gp_settings_v14_7_6` with migration from v14_7_5...v14_5.
- Welcome hint localStorage key → `gp_visited_v1476`.
- All version markers updated: title, meta, JSON-LD, ready log,
  CSV filename, screenshot filename, watermark, license mark.

---

## [14.7.5] - 2026-06-17 — Directional Grid Modes + UX polish

### Added
- Directional Grid Modes — replaced unified BOT mode with STRONG_BUY /
  GRID_BUY / STRONG_SELL / GRID_SELL / SKIP.
- Breakout entry logic — limL now points at the opposite extreme of the
  reversal candle (bearish: rc.l, bullish: rc.h).
- Light theme contrast boost.
- Hotkeys panel (Shift+T/P/C).

### Fixed
- STRONG SELL Launch Card silently failing (stray Cyrillic char).
- Carousel `indicators` array (duplicate VWAP% fragment).

---

## [14.7.4] - 2026-XX-XX
- Dark theme contrast boost.
- Restored full referral banner UA i18n keys.

## [14.7.2] - 2026-XX-XX
- TikTok watermark hidden by default.
- Highlight Row uses double-click.

## [14.7] - 2026-XX-XX
- TikTok Mode (Shift+T).
- Highlight Row.
- Auto-watermark with daily scan serial.
- Auto-Carousel — 5-slide pack.
- Scan tick sound.
- Bold SKIP visual.

## [14.6] - 2026-XX-XX
- Screenshot button.
- Binance Futures 451 → Bybit mirror fallback.
- Pionex PERP discovery.

---

License: CC BY-NC-SA 4.0 · © 2026 GridPulse Project
