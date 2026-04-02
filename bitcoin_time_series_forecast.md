# Bitcoin Time-Series Forecast (as of 2026-03-28)

## Objective
Provide a practical forecast for BTC/USD using available historical data and a scenario overlay for current geopolitical stress.

## Data Used
- **Primary price series:** FRED `CBBTCUSD` (Coinbase Bitcoin, daily, USD).
- **Observed series range:** 2014-12-01 to 2026-03-27.
- **Most recent close:** 66,390.02 on 2026-03-27.
- **Recent closes used for short-horizon momentum check:**
  - 2026-03-23: 70,906.00
  - 2026-03-24: 70,555.44
  - 2026-03-25: 71,277.56
  - 2026-03-26: 68,762.20
  - 2026-03-27: 66,390.02

## Method (Lightweight due environment constraints)
I used a **hybrid signal approach** rather than a full ARIMA/Prophet fit:

1. **Structural trend signal (long-term):**
   - From 370 (2014-12-01) to 66,390.02 (2026-03-27), implied long-run annualized growth is ~58.2% CAGR.
   - This supports the thesis that Bitcoin remains in a long-term secular uptrend regime.

2. **Short-term momentum signal (last 5 sessions):**
   - 5-session move: **-6.37%**.
   - Mean daily return over those 4 intervals: **-1.61%**.
   - Daily volatility estimate: **~2.25%**.
   - This indicates near-term downside pressure / risk-off behavior.

3. **Geopolitical risk overlay:**
   - In stress episodes, BTC can behave in two opposite ways:
     - **Risk asset mode** (drops with equities/liquidity tightening).
     - **Alternative-asset mode** (holds up if fiat/system stress dominates narrative).
   - Current tape (recent 5-day slide) is more consistent with **risk-asset mode** in the immediate term.

## Forecast (Scenario-Based)
Starting point: **66,390**.

### 1) Base Case (most likely)
- Assumption: geopolitical tensions stay elevated but do not materially escalate; liquidity conditions stay mixed.
- Direction: **choppy to slightly down in the short term**, then stabilization.
- Range:
  - **2 weeks:** 62,000 to 69,000
  - **1-3 months:** 58,000 to 74,000

### 2) Bear Case (drop scenario)
- Assumption: tensions escalate + broad risk-off move + tighter global liquidity.
- Direction: **downside continuation**.
- Range:
  - **2-6 weeks:** 54,000 to 62,000

### 3) Bull Case (upside scenario)
- Assumption: tensions cool, ETF/institutional demand absorbs supply, and macro risk premium compresses.
- Direction: **rebound and trend resumption**.
- Range:
  - **1-3 months:** 72,000 to 82,000

## Bottom-Line View
- **Near-term (days to a few weeks):** higher probability of volatility and downside spikes than a clean breakout.
- **Medium-term (1-3 months):** bias turns constructive if geopolitical risk cools and flows remain supportive.
- So: **a drop is plausible first, then recovery potential remains meaningful**.

## Risk Notes
- This is a probabilistic market view, **not financial advice**.
- BTC can invalidate any model quickly during regime shifts (policy shock, exchange events, conflict escalation).
