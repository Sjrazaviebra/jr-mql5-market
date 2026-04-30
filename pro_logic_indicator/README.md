# ProLogic Indicator

**AI-Powered Multi-Indicator Signal Engine for MetaTrader 5**

[![Version](https://img.shields.io/badge/version-1.00-blue.svg)](https://github.com/Sjrazaviebra/jr-mql5-market)
[![Platform](https://img.shields.io/badge/platform-MetaTrader%205-orange.svg)](https://www.metatrader5.com)
[![License](https://img.shields.io/badge/license-Commercial-green.svg)](#license)

---

## Description

**ProLogic Indicator** combines RSI, MACD, Moving Averages, Bollinger Bands, ATR, and Heikin Ashi into a single weighted AI score from **-100** (Strong Sell) to **+100** (Strong Buy). Displays buy/sell arrows on the chart and a rich interactive dashboard with lot size calculator, commission filter, and strategy toggles.

---

## Key Features

**AI Scoring Engine**
- Weighted combination of 6 configurable indicators
- Score: -100 (Strong Sell) → 0 (Neutral) → +100 (Strong Buy)
- Confidence % based on inter-indicator agreement
- Recommended labels: STRONG BUY / BUY / NEUTRAL / SELL / STRONG SELL

**Visual Signals**
- Buy/Sell arrows plotted directly on price bars (strong signals only)
- Consecutive same-direction signals filtered automatically
- Commission-aware filter: signals ignored when potential profit ≤ commission cost

**Interactive Dashboard**
- Real-time score, confidence, and signal label
- Lot size selector (mouse wheel scroll)
- Commission per lot input
- Symbol switcher (search and change symbol)
- Minimize/maximize button
- Manual Buy/Sell buttons

**Strategy Toggles** (enable/disable per indicator)
- RSI (14)
- MACD (12/26/9)
- Moving Averages EMA20 / SMA50
- Bollinger Bands (20, 2σ)
- Trend (EMA/SMA gap)
- Heikin Ashi candle direction

**Alerts**
- Sound alerts (configurable .wav files)
- Popup alerts
- Configurable delay between alerts

---

## Indicator Parameters

### Analysis

| Parameter | Default | Description |
|-----------|---------|-------------|
| `RSI_Period` | 14 | RSI period |
| `MACD_Fast` | 12 | MACD fast EMA |
| `MACD_Slow` | 26 | MACD slow EMA |
| `MACD_Signal` | 9 | MACD signal period |
| `MA_Fast_Period` | 20 | Fast EMA period |
| `MA_Slow_Period` | 50 | Slow SMA period |
| `ATR_Period` | 14 | ATR period (for SL/TP) |
| `BB_Period` | 20 | Bollinger Bands period |

### Display

| Parameter | Default | Description |
|-----------|---------|-------------|
| `ShowArrows` | true | Display arrows on chart |
| `ShowLabels` | true | Display signal text labels |
| `ShowGraphicalPanel` | true | Display interactive dashboard |
| `ShowBuySellButtons` | true | Show manual trade buttons |
| `ArrowSize` | 3 | Arrow size |
| `BuyArrowColor` | Lime | Buy arrow color |
| `SellArrowColor` | Red | Sell arrow color |

### Alerts

| Parameter | Default | Description |
|-----------|---------|-------------|
| `EnableSoundAlerts` | true | Sound on new signal |
| `EnablePopupAlerts` | true | Popup on new signal |
| `AlertDelay` | 300 | Min seconds between alerts |

---

## Signal Logic

The score is computed as a weighted average:

| Indicator | Weight |
|-----------|--------|
| RSI | 25% |
| MACD | 25% |
| Moving Averages | 20% |
| Bollinger Bands | 15% |
| Trend | 10% |
| Heikin Ashi | 5% |

Disabled strategies are automatically excluded and weights are renormalized.

SL is placed at **2× ATR** from entry; TP at **3× ATR** from entry.

---

## Use Cases

**Confluence Confirmation** — Use the score to confirm setups from your primary strategy. Enter only when score > 60 or < -60.

**Session-Based Scalping** — Combine with ProSessionBox Premium to trade during London/NY sessions when score is strong.

**Signal Filtering** — Commission filter prevents taking signals where potential profit is too small to cover fees.

---

## System Requirements

- MetaTrader 5 (build 2200+)
- Windows 7/8/10/11 or macOS
- Any broker, any symbol

---

## Download / Request

**To receive the `.ex5` compiled file:**

1. Open a [Request Issue](../../issues/new?template=request_executable.md)
2. Fill in your MT5 account number, broker, and contact email
3. Receive the file within 24-48h

---

## Disclaimer

Trading Forex/CFDs involves significant risk of loss. This tool is for analysis assistance only. Always test on a demo account first. Past performance is not indicative of future results.

---

## Changelog

- **v1.00** (2025-11-22): Initial release — 6-indicator AI engine, interactive dashboard, commission filter, strategy toggles

---

## License

Commercial License — use on unlimited accounts and charts, no redistribution.

© 2025 Javad RAZAVI — S.javad_rz@yahoo.com
