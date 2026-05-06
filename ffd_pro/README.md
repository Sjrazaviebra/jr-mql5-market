# FFD Pro

**Memory-Preserving Stationarity Transform for Quantitative Trading**

A research-grade MetaTrader 5 indicator that turns non-stationary price series
into stationary ones — **without destroying the memory** that ML models need.

![FFD Pro](FFD_Pro_V1.png)

---

## The problem

Every machine-learning model applied to price data needs **stationary inputs**
to give reliable predictions. The classical fix — first-difference (`d = 1`) —
turns price levels into returns and **destroys all memory** of the past in
the process. That memory is precisely what your model needs.

## The solution

**Fractional differentiation** with `0 < d < 1`, popularised by Marcos
López de Prado in *Advances in Financial Machine Learning*, interpolates
smoothly between raw price and first-difference. Pick `d = 0.4` and you
typically get stationarity with **over 90 % of memory preserved**.

| Method                     | Stationary?       | Memory preserved? |
|----------------------------|-------------------|-------------------|
| Raw price (`d = 0`)        | No                | 100 %             |
| **FFD (`d = 0.4`)**        | **Yes**           | **High**          |
| First difference (`d = 1`) | Yes               | None              |

---

## What's inside

- A polished MetaTrader 5 indicator with a **futuristic glass UI panel**
  showing live statistics — current FFD value, mean, σ, range, lag-1 ρ
  and a real-time stationarity score.
- Optional rolling **±2σ statistical bands** for outlier detection.
- A reusable **header-only engine** (`CFFDEngine.mqh`) you can include
  in your own private EAs to use FFD as a feature.
- A **validation script** that exports CSVs for cross-checking against
  the Python reference (`afml.frac_diff_ffd`) — verified to better
  than `1e-12` precision.

---

## Highlights

- 🧠 **Memory-preserving stationarity** — bridge Python research and MQL5 production
- 💎 **Glass / cyber-pro UI** — live stats overlay, color-coded values
- ⚡ **Zero per-tick allocation** — `O(width)` per new bar, ~ 8 KB footprint
- 🔬 **Validated < 1e-12** vs Python reference
- 🧰 **Reusable engine** — one library, infinite ML pipelines
- 🛡️ **Article 2555 stress-guard compliant** — production-grade

---

## Get it

- 🛒 **MQL5 Market** — TBD (link will be added at launch)
- 🌐 **Author website** — <https://www.javadrazavi.fr>
- 👤 **MQL5 profile** — <https://www.mql5.com/en/users/monsieurseraj>

---

## License

Proprietary, single-user. Personal trading and integration into your own
**private** EAs is explicitly permitted. Redistribution, reverse engineering
and derivative works are not.

---

## Contact

- 📧 <S.javad_rz@yahoo.com>
- 🌐 <https://www.javadrazavi.fr>
