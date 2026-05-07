# FFD Pro Signal

**Memory-Preserving Stationarity + Tradable Buy/Sell Signals**

The trading edition of [**FFD Pro**](../ffd_pro/) — same research-grade
Fixed-Width Fractional Differentiation engine, with on-chart Buy/Sell
arrows, three signal modes, and Popup / Sound / Email / **Telegram** alerts.

![FFD Pro Signal](FFD_Pro_Signal_V1.png)

---

## What you get on top of Core

| Capability                          | Core | **Signal** |
|-------------------------------------|:----:|:----------:|
| FFD line + ±2σ bands                | ✅   | ✅         |
| Glass UI panel with live stats      | ✅   | ✅         |
| Validated < 5e-13 vs Python         | ✅   | ✅         |
| **Buy / Sell arrows on chart**      | ❌   | ✅         |
| **3 signal modes** (Reversion / Momentum / Hybrid) | ❌ | ✅ |
| **Popup + Sound alerts**            | ❌   | ✅         |
| **Email alerts**                    | ❌   | ✅         |
| **Telegram alerts**                 | ❌   | ✅         |
| **24h signal counter** in panel     | ❌   | ✅         |
| Min-bars-between filter             | —    | ✅         |

---

## Three signal modes

- 🔵 **Reversion** — BUY at −2σ touch, SELL at +2σ touch (ranges).
- 🟣 **Momentum** — BUY on zero-cross up, SELL on zero-cross down (trends).
- 🌟 **Hybrid** *(default)* — reversion filtered by FFD slope. Best for both regimes.

Switch mode from the inputs — no recompile needed.

---

## Recommended presets

| Asset                       | `d`        | Mode      |
|-----------------------------|------------|-----------|
| EURUSD, GBPUSD (FX)         | 0.45–0.55  | Hybrid    |
| US30, NDX100                | 0.40–0.50  | Momentum  |
| JP225 (Nikkei)              | 0.45–0.55  | Hybrid    |
| XAUUSD (gold)               | 0.45–0.55  | Hybrid    |
| BCO (oil brent)             | 0.50–0.60  | Hybrid    |
| BTCUSD                      | 0.50–0.65  | Momentum  |

Watch the Stationarity Score in the panel — aim for **≥ 70 %**.

---

## Telegram in 90 seconds

1. Message `@BotFather` → `/newbot` → save the token.
2. Find your chat ID at `https://api.telegram.org/bot<TOKEN>/getUpdates`.
3. Paste both into the inputs.
4. In MT5: `Tools → Options → Expert Advisors` → whitelist `https://api.telegram.org`.

You'll start receiving messages like:

```
FFD Pro Signal — BUY on EURUSD PERIOD_H1 @ FFD=-0.012345 (2026.05.07 14:32)
```

---

## Get it

- 🛒 **MQL5 Market** — *coming soon*
- 🌐 **Author website** — <https://www.javadrazavi.fr>
- 👤 **MQL5 profile** — <https://www.mql5.com/en/users/monsieurseraj>

### Bundle deal *(site only)*

**FFD Pro + FFD Pro Signal** — single payment, both lifetime, both updates included.

---

## License

Proprietary, single-user. Use within your own **private** EAs (via `iCustom`)
is explicitly permitted. Redistribution and reverse engineering are not.

---

## Contact

- 📧 <S.javad_rz@yahoo.com>
- 🌐 <https://www.javadrazavi.fr>
