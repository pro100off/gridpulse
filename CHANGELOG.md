# GridPulse Changelog

## [14.8.2] - 2026-06-27 — Pair Presets

### Added
- **💾 Pair Presets** — save / load named pair watchlists directly in
  `localStorage` (no backend required). One-click apply from a dropdown
  next to Custom Pairs.
- **5 built-in starter presets** (read-only): 💎 Majors, 🐸 Memes,
  🤖 AI Tokens, 🏛 Layer 1s, 💧 DeFi Blue Chips.
- **Save as…** button — persists the current Custom Pairs input as a
  named preset with a custom icon (20 pre-defined options).
- **Manage Presets modal** — apply / delete user presets in one place.
- **Import / Export JSON** — full backup or share between devices.
- **Shareable preset URL** — `tradescout.trade/?preset=<base64-json>`
  auto-imports a preset on page load (with consent prompt).
- **Last-used preset auto-restored** on next visit.
- Full i18n for the entire preset UI across EN / UA / ES / RU / ZH
  (~22 keys × 5 languages = 110 new translations).

### Changed
- `SET_KEY` → `gp_settings_v14_8_2` with migration from `v14_8_1` /
  `v14_8_0` / `v14_7_6` / … / `v14_5`.
- Welcome hint key → `gp_visited_v1482` (re-shown after upgrade).
- Storage namespace: `gp_presets_v1` (independent from settings;
  survives settings reset).
- Version markers updated everywhere: title, meta, JSON-LD,
  ready log, CSV filename, screenshot filename, watermark, lic-mark.

### Fixed
- Removed duplicate `"hdr.pionexOnly"` key in EN locale (was defined
  twice in the same object).
- Cleaned up changelog headers in `index.html` (previous v14.8.0 entry
  self-referenced itself; carried-over entries now correctly labelled).
- License mark in lic-bar updated from `GRDPLS-V14-7-6-RELEASE-2026`
  to `GRDPLS-V14-8-2-RELEASE-2026`.

### Storage footprint
- 5 built-in presets are not persisted (defined in code).
- User presets stored as `{version:1, presets:[…]}` in
  `localStorage['gp_presets_v1']`. ~50 KB per 500 pairs spread across
  10 presets — far below the 5 MB localStorage limit.

---

## [14.8.1] - 2026-06-26 — Setup geometry validation

### Fixed
- **🐛 BUGFIX**: Stale setups where price had already crossed entry or
  stop before scan no longer pass the filter. Strict geometry is now
  enforced for both directions:
  - **Bullish (LONG)** — requires `stopL < price < limL`
  - **Bearish (SHORT)** — requires `limL  < price < stopL`
  
  Fixes cases like CLANKER 1h where `stopL` (15.84) was reported above
  current price (15.77) for a GRID BUY — physically impossible to
  execute as a long-side limit/stop pair.

### Changed
- `SET_KEY` → `gp_settings_v14_8_1` with migration from `v14_8_0`.

---

> **Positioning release.** GridPulse is now explicitly framed as a **dedicated companion tool for Pionex Grid Bots**, with Pionex as the default exchange, an "Official Partner" badge throughout the UI, and a redesigned Launch Card focused on driving users straight into a trading-ready Pionex session.

### Added
- **🤝 Official Partner badge** — visible "Pionex Partner" marker next to GridPulse branding in the header, referral banner, footer, and Launch Card. Hover tooltip: *"Official Pionex Partner"*.
- **Pionex as default exchange** — new sessions open with **Pionex selected by default** (was Bybit). Bybit, Binance, KuCoin, and OKX remain fully supported via the exchange dropdown.
- **🤝 Pionex Only mode** — single header checkbox (stored in `localStorage` as `gp_pionex_only`) that locks the exchange dropdown to Pionex and visually de-emphasizes other exchanges for first-time users.
- **Prominent "Open in Pionex" CTA in Launch Card** — large, full-width gradient button (green → blue) with subtle shimmer animation. Includes **UTM tracking tags**:
  - `utm_source=gridpulse`
  - `utm_medium=launchcard`
  - `utm_campaign={mode}` (e.g. `strong_buy`, `grid_sell`)
  - `utm_content={symbol}_{tf}`
- **Larger, more visible referral QR codes**:
  - Top banner: 64 × 64 px → **96 × 96 px** (wrapper 72 → **108 px**)
  - Launch Card: 46 × 46 px → **84 × 84 px** in a dedicated bordered panel (`.lc-ref-block`)
- **Launch Card readability boost** — base font sizes increased across the board:
  - `.lc-label`: 10 px → **13 px**
  - `.lc-val`: 12 px → **16 px**
  - `.lc-ind-name`: 9 px → **12 px**
  - `.lc-ind-val`: 11 px → **16 px**
  - `.lc-sec-title`: 9 px → **12 px**
  - `.lc-row` padding: 5 px → **9 px**, gap 6 → **10 px**
  - Modal max-width: 560 px → **640 px**
  - Mode badge: 11 px → **14 px**, padding 3/8 → 5/12
  - Footer buttons (Copy all / Open chart / Share TG): 11 px → **13 px**, padding 9/12 → **12/16**

### Changed
- `SET_KEY` → **`gp_settings_v14_8_0`** with backward migration from `v14_7_6`, `v14_7_5`, `v14_7_4`, `v14_7_3`, `v14_7_2`, `v14_7`, `v14_6`, `v14_5`.
- Header now reads: **`⚡ GridPulse v14.8.0 🤝 Pionex Partner`**.
- Footer disclosure now explicitly includes the "Official Pionex Partner" badge inline.
- Welcome hint key bumped: `gp_visited_v1476` → `gp_visited_v1480`.
- All version markers updated: title, meta description, JSON-LD, ready log, CSV filename, screenshot filename, watermark, license bar (`GRDPLS-V14-8-0-RELEASE-2026`).

### Fixed
- N/A — this is a purely additive UX/positioning release. All v14.7.6 scanning logic, classification, and indicator behaviour is preserved unchanged.

### Migration notes
- **No breaking changes.** Settings are auto-migrated from any version back to v14.5.
- Users with **Bybit** previously selected as exchange will continue to see Bybit selected (their localStorage choice is preserved).
- New users land on **Pionex / Spot** by default.
- The Pionex Only toggle is **opt-in** and off by default.

---
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
