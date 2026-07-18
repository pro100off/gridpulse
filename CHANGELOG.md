# Changelog

All notable changes to **GridPulse** are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/).
License: CC BY-NC-SA 4.0 · © 2026 GridPulse Project

---

## [14.9.2] — 2026-07 — "Alerts + Backtest + Journal"

### Added
- 🔔 **Auto-refresh scanning** — configurable interval (1–1440 min). Re-runs
  the scan automatically and highlights new setups since the last run.
- 🔔 **Desktop notifications** — browser push alerts for STRONG_BUY / STRONG_SELL
  setups (30 s cooldown per symbol to prevent spam).
- ✈️ **Telegram alerts** — send STRONG setups to a Telegram chat via bot token
  + chat_id. Includes entry, SL, TP, R:R, position size and risk. Test button.
- 🎮 **Discord alerts** — send STRONG setups to a Discord channel via webhook.
  Test button and webhook-URL validation.
- 💰 **Position Sizing calculator** — set account balance + risk %. Computes
  units, position value, % of balance, leverage-equivalent, reward/loss in USDT.
  Injected as a dedicated section into every Launch Card.
- 📊 **Backtest engine** — historical win-rate per setup, reproducing the live
  `findSetup` MACD-reversal + rc/cc pipeline over the last N bars. Win-rate
  badge (BT xx%) appears in the Mode column; Expected Value shown in Launch Card.
- 📓 **Signal Journal** — every new STRONG setup is auto-logged with entry/SL/TP.
  Auto-resolves status (TP / SL / Expired) on open by walking forward candles.
  Stats: Total, TP Hit, SL Hit, Win Rate, **Net R (closed)**. CSV export.
- 🧮 **Net R metric** — cumulative R over all closed journal trades
  (TP → +R:R of the trade, SL → −1R).
- 🗄 **Journal overflow protection** — 200-entry cap prunes *expired → closed →
  pending last*, so pending trades are never lost. Pruned closed-trade stats are
  folded into a persistent archive (`gp_v11_journal_v1_arch`) so Win Rate /
  Net R never reset on overflow. "Clear Journal" also clears the archive.

### Changed
- 🏷 Version markers bumped to v14.9.2 (title, meta, JSON-LD, footer, lic-mark).
- 💾 `SET_KEY → gp_settings_v14_9_2` with migration from v14_9_1 … v14_5.
- 🌐 Full EN + UA i18n for all new panel labels, statuses and journal columns.
  ES / RU / ZH fall back to English for v1.1-specific keys.

### Fixed
- 🐛 Auto-refresh minutes now stay in sync between the input field and the
  active timer (live restart on change).
- 🐛 Journal dedup: skips the same sym+tf+pattern logged within the last 4 h.

### Notes
- Alerts fire only for STRONG_BUY / STRONG_SELL (to avoid noise from GRID/SKIP).
- Backtest reproduces the live signal pipeline, so its win-rate reflects what
  the screener would actually have traded (not raw candle patterns).

---

## [14.9.1] — 2026-07-09 — "ATR-Based R:R + Filter-Aware Classification"

### Added
- 🎯 ATR-based Take Profit — TF-adaptive TP targets (1m×2.0 → 1M×5.0 ATR),
  replacing the fixed ±5% extremum model. Fair R:R across all timeframes.
- 🎯 Trade Plan v3 in Launch Card — TP1 (1R), TP2 (ATR×N), TP3 (3R+ trail),
  Chandelier ATR×3 trailing stop.
- 🎯 Filter-Aware Classification — `decideMode()` respects user filter
  checkboxes; OFF filters no longer block STRONG/GRID classification.
- 📊 Reject-reason diagnostics with R:R counter; R:R cell tooltip shows
  TP, Risk, Reward.

### Changed
- 🏷 Column header R:R → "R:R 🎯"; VWAP distance no longer blocks classification.
- 📥 CSV export includes TP_ATR + TP_Mult columns.
- 💾 `SET_KEY → gp_settings_v14_9_1`.

---

## [14.9.0] — "Old School Wisdom"
- 🎯 MTF Trend Filter (ON by default) · 🤖 Bot Range modes (Donchian / Bollinger
  / ATR) · 🌏 Session Filter · 💧 Liquidity Guard · 🏷 Symbol Unification ·
  🔍 Cell Magnifier · ⚡ STRONG row highlighting · 📈 Freshness ranking bonus.

## [14.8.2] — "Presets"
- 💾 Pair Presets (save/load watchlists), built-in starters, import/export JSON,
  shareable preset URL, Pionex Only mode, Launch Card readability boost.

## [14.8.1] — "Setup geometry validation"
- 🐛 Stale setups (price already crossed entry/stop) no longer pass the filter.

## [14.8.0] — "Pionex Companion"
- 🤝 Official Partner badge · Pionex default exchange · "Open in Pionex" CTA with
  UTM tags · larger QR codes.

## [14.7.6] — TF-adaptive thresholds, Strictness selector, two STRONG paths,
classified SKIP reasons.

## [14.7.5] — Directional Grid Modes (STRONG/GRID BUY/SELL/SKIP), breakout entry,
light-theme contrast, hotkeys panel.

## [14.7.x] — TikTok Mode, Highlight Row, watermark serial, carousel export,
scan-tick sound, bold SKIP.

## [14.6] — Screenshot button, Binance→Bybit mirror fallback, Pionex PERP
discovery, safeFetch error handling.

---

_This tool is an analytical aid, NOT financial advice. Crypto trading is risky. DYOR._
