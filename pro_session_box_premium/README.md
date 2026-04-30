# ProSessionBox Premium

**Professional Daily Box + Multi-Session Tracker for MetaTrader 5**

[![Version](https://img.shields.io/badge/version-1.00-blue.svg)](https://github.com/Sjrazaviebra/jr-mql5-market)
[![Platform](https://img.shields.io/badge/platform-MetaTrader%205-orange.svg)](https://www.metatrader5.com)
[![License](https://img.shields.io/badge/license-Commercial-green.svg)](#license)

---

## Description

**ProSessionBox Premium** displays **Daily price boxes** combined with **4 major trading sessions** and a **smart time bar**. Designed for day traders, scalpers, and swing traders who need to visualize market structure and session activity.

---

## Key Features

**Daily Box Visualization**
- High-Low range displayed as a colored candle (bullish/bearish/neutral)
- Today's Box + optional Yesterday's Box (J-1)
- Profit calculation for 0.01 lot displayed on chart

**4 Major Trading Sessions with DST Support**
- Sydney (UTC+10/+11)
- Tokyo (UTC+9)
- London (UTC+0/+1)
- New York (UTC-5/-4)
- Automatic Daylight Saving Time adjustment for all sessions

**Smart Time Bar**
- Visual progress bar showing current time relative to the trading day
- Positioned between Daily Box and session bars
- Hour markers for easy reference

**Interactive Control Panel**
- Toggle sessions ON/OFF instantly
- Toggle Yesterday Box
- Minimize button for compact view
- Click the Daily Box itself to show/hide the panel

**Performance**
- CPU usage: < 1%
- Memory: < 5 MB
- No chart lag

---

## Parameters

### Daily Box

| Parameter | Default | Description |
|-----------|---------|-------------|
| `ShowOnlyBoxFrame` | true | Show border only (no fill) |
| `ShowYesterdayBox` | false | Show Yesterday's Box (J-1) |
| `BoxBullishColor` | SteelBlue | Bullish day color |
| `BoxBearishColor` | PaleVioletRed | Bearish day color |
| `BoxCandleShift` | 5 | Shift box right (candles) |
| `ShowBoxLabels` | true | Show range/profit labels |

### Sessions

| Parameter | Default | Description |
|-----------|---------|-------------|
| `ShowSydney` | true | Sydney session bar |
| `ShowTokyo` | true | Tokyo session bar |
| `ShowLondon` | true | London session bar |
| `ShowNewYork` | true | New York session bar |
| `SessionLineHeight` | 5 | Session bar height (px) |
| `SessionTransparent` | true | Transparent colors |

### Control Panel

| Parameter | Default | Description |
|-----------|---------|-------------|
| `ShowControlPanel` | false | Display control panel |
| `PanelXOffset` | 10 | Distance from left edge |
| `PanelYOffset` | 10 | Distance from top edge |
| `PanelButtonColor` | Windows 11 blue | Button color |

---

## Use Cases

**Day Trading** — Visualize session opens/closes, identify London/NY overlap for high volatility.

**Scalping** — Sessions drawn below price action keep your chart clean. Toggle visibility instantly.

**Swing Trading** — Daily box shows the day's range and trend. Compare today vs yesterday (J-1).

---

## System Requirements

- MetaTrader 5 (build 2200+)
- Windows 7/8/10/11 or macOS
- Any broker, any symbol, any timeframe

---

## Download / Request

**To receive the `.ex5` compiled file:**

1. Open a [Request Issue](../../issues/new?template=request_executable.md)
2. Fill in your MT5 account number, broker, and contact email
3. Receive the file within 24-48h

---

## Changelog

- **v1.00** (2025-11-21): Initial release — 4 sessions, daily box, time bar, control panel, DST support

---

## License

Commercial License — use on unlimited accounts and charts, no redistribution.

© 2025 Javad RAZAVI — S.javad_rz@yahoo.com
