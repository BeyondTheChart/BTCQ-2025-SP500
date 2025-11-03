# Quantitative & Behavioral Analysis — S&P 500  
**Report ID:** BTCQ-2025-3484  
**Date:** 3 November 2025  
**© 2025 Beyond the Chart | Proprietary Quantitative & Behavioral Research**

---

## Abstract

This document presents a full quantitative and behavioral performance analysis on an S&P 500 trading account.  
The study integrates classical risk–return metrics with structural and behavioral indicators to assess the internal stability of the trading edge across 500 discrete trades.  
The results highlight an apparent structural decay characterized by volatility amplification, drawdown clustering, and diminishing risk-adjusted returns despite a high win rate.  
Monte Carlo simulations and regime diagnostics confirm that the strategy’s positive expectancy is compromised by asymmetric tail exposure and unstable payoff ratios.

---

## Dataset & Methodology

- **Instrument:** S&P 500  
- **Sample:** 500 executed trades  
- **Data Frequency:** Trade-by-trade (aggregated from tick-level execution logs)  
- **Period Covered:** Up to 3 November 2025  
- **Framework:** Hybrid quantitative–behavioral model integrating volatility response, frequency drift, and edge decay analysis.  
- **Analytical Modules:**
  - Equity curve and drawdown decomposition  
  - Return distribution and QQ-plot validation  
  - Historical VaR/CVaR simulation (95–99 %)  
  - Rolling Sharpe & Sortino (100-trade windows)  
  - Hurst exponent and ADF stationarity test  
  - Edge Decay model (rolling mean P/L trend)  
  - Monte Carlo stress testing (500 reshuffled paths)  
  - Cumulative survival probability estimation  

All computations were executed using Python (NumPy, SciPy, pandas, statsmodels, matplotlib).  
The analysis applies both classical statistics and non-linear stochastic diagnostics to capture drift, persistence, and tail asymmetries.

---

## Visual Results

### ACF
![](results/charts/acf.png)

### PACF
![](results/charts/pacf.png)

### Sharpe Proxy
![](results/charts/sharpe_proxy.png)

### Ulcer Index
![](results/charts/ulcer_index.png)

### Sortino Stress Downside Risk
![](results/charts/sortino_stress_downside_risk.png)

### Drawdown
![](results/charts/drawdown.png)

### Drawdown Duration
![](results/charts/drawdown_duration.png)

### Recovery Time Drawdown
![](results/charts/recovery_time_drawdown.png)

### Risk Metric
![](results/charts/risk_metric.png)

### Risk Curve Cumulative
![](results/charts/risk_curve_cumulative.png)

### Expected Annual Outcome
![](results/charts/expected_annual_outcome.png)

### Final Equity
![](results/charts/final_equity.png)

### Change Point Equity
![](results/charts/change_point_equity.png)

### Change Point Analysis
![](results/charts/change_point_analysis.png)

### Montecarlo Simulation
![](results/charts/montecarlo_simulation.png)

### Montecarlo Fan Chart
![](results/charts/montecarlo_fan_chart.png)

### Edge Decay Trend
![](results/charts/edge_decay_trend.png)

### Forecast Edge Decay
![](results/charts/forecast_edge_decay.png)

### Edge Decay Timeline
![](results/charts/edge_decay_timeline.png)

### Edge Decay Timeline 2
![](results/charts/edge_decay_timeline_2.png)

### Edge Collapse Root Cause Matrix
![](results/charts/edge_collapse_root_cause_matrix.png)

### Edge Early-Warning Panel
![](results/charts/edge_early_warning_panel.png)

### Edge Correlation Matrix
![](results/charts/edge_correlation_matrix.png)

### Behavior Structure Equilibrium Map
![](results/charts/behavior_structure_equilibrium_map.png)

### Behavior vs Structure Enhanced Sensitivity
![](results/charts/behavior_vs_structure_enhanced_sensitivity.png)

### Behavior vs Structure Stress Pressure
![](results/charts/behavior_vs_structure_stress_pressure.png)

### Behavior vs Structure Timeline
![](results/charts/behavior_vs_structure_timeline.png)

### Rolling Win Rate
![](results/charts/rolling_win_rate.png)

### Rolling Payoff Ratio
![](results/charts/rolling_payoff_ratio.png)

### Rolling Payoff
![](results/charts/rolling_payoff.png)

### Payoff Stability
![](results/charts/payoff_stability.png)

### Consistency Panel
![](results/charts/consistency_panel.png)

---

## Quantitative Performance Summary

| Metric | Value |
|--------|-------:|
| **Total Net Profit** | −11,112.20 |
| **Win Rate (%)** | 84.21 |
| **Profit Factor** | 0.92 |
| **Average Win** | 305.74 |
| **Average Loss** | −1,767.81 |
| **CAGR (%)** | 86.38 |
| **Sharpe Ratio** | −0.13 |
| **Sortino Ratio** | −0.07 |
| **Calmar Ratio** | 0.80 |
| **Gain-to-Pain Ratio** | 0.94 |
| **Max Drawdown (%)** | 107.86 |
| **Edge Health (%)** | 87.63 |

---

## Visual Results

| Chart | Description |
|-------|--------------|
| ![](results/charts/equity_drawdown.png) | **Equity & Drawdown Profile** — total return and cumulative losses. |
| ![](results/charts/return_distribution.png) | **Return per Trade Distribution** — skew and tail structure. |
| ![](results/charts/qqplot_returns.png) | **QQ-Plot** — deviation from Gaussian return model. |
| ![](results/charts/var_cvar.png) | **Tail Risk (VaR / CVaR)** — historical simulation 95–99 %. |
| ![](results/charts/rolling_sharpe_sortino.png) | **Rolling Sharpe & Sortino** — 100-trade window risk-adjusted performance. |
| ![](results/charts/drawdown_profile.png) | **Drawdown Dynamics (%)** — clustering and depth analysis. |
| ![](results/charts/winrate_payoff.png) | **Rolling Win Rate / Payoff Ratio** — behavioral consistency. |
| ![](results/charts/hurst_adf.png) | **Hurst & ADF** — persistence and mean-reversion characteristics. |
| ![](results/charts/edge_decay.png) | **Edge Decay Trend** — rolling mean P/L trajectory. |
| ![](results/charts/montecarlo_equity.png) | **Monte Carlo Simulation (500 runs)** — final equity distribution. |
| ![](results/charts/survival_curve.png) | **Survival Probability** — cumulative likelihood of account persistence. |

---

## Quantitative Interpretation

1. **Performance Instability:**  
   Despite an 84 % win rate, the profit factor (0.92) and negative Sharpe/Sortino confirm structural inefficiency. The equity curve shows recurrent drawdown cycles exceeding 100 %, consistent with tail clustering.

2. **Volatility Response:**  
   Expansion in realized volatility directly amplifies drawdown depth and reduces payoff stability. The rolling risk-adjusted metrics remain negative across most observation windows.

3. **Tail Risk Exposure:**  
   Historical simulation reveals extreme CVaR values (−279.89 % at 95 % and −1,139.50 % at 99 %), indicating that rare but severe losses dominate the distribution.

4. **Edge Persistence & Drift:**  
   Edge Decay and Hurst (0.54) confirm mild persistence but with structural degradation over time. The ADF statistic (−3.23, p = 0.0185) rejects pure randomness, implying mean-reverting noise around a decaying mean expectancy.

5. **Monte Carlo & Survival Modeling:**  
   The forecast fan chart and survival curve demonstrate a 60–70 % probability of capital impairment beyond 300 trades, confirming edge erosion under variance amplification.

---
#### Equity & Drawdown
The equity curve reveals alternating high-volatility clusters and deep drawdowns exceeding 100%,
confirming tail clustering typical of over-leveraged mean-reverting exposure.

#### VaR / CVaR
Historical simulation of tail risk confirms disproportionate loss magnitude relative to trade frequency,
indicating structural asymmetry within negative outcomes.

#### Edge Decay
Rolling average P/L demonstrates a downward bias after trade #300,
signaling exhaustion of the initial structural advantage.

## Behavioral Layer

While the quantitative framework identifies structural decay, behavioral drift is observable in the frequency and amplitude of trade clustering.  
Periods of elevated trade density correlate with higher volatility regimes and payoff asymmetry — a pattern consistent with overconfidence and latent FOMO bias.  
These behavioral signatures precede quantitative decay and can thus act as early indicators of edge exhaustion.

---

## Conclusion

The analysis confirms that the examined S&P 500 trading account exhibits **quantitatively measurable performance decay** and **behavioral instability**.  
The strategy’s edge, while initially positive, deteriorates under volatility expansion, resulting in declining risk-adjusted performance and excessive drawdowns.  
Without volatility normalization and stricter risk control, expectancy remains statistically negative on a long-term basis.

---

## Appendix

- **Tests executed:** VaR/CVaR (historical), ADF, Hurst R/S, CUSUM change-points, Monte Carlo 500 runs  
- **Environment:** Python 3.12, NumPy 2.1, SciPy 1.13, pandas 2.2, statsmodels 0.14  
- **Reproducibility:** All figures generated via reproducible scripts under `/src/`  
- **Metrics file:** `results/metrics_summary.csv`

---

## Legal Notice

© 2025 Beyond the Chart — All Rights Reserved.  
This repository and its contents (including data, code, and visual materials) are proprietary.  
No part of this report may be copied, redistributed, or used commercially without explicit written permission from Beyond the Chart.  
For institutional collaboration or partnership inquiries, contact: **[add your professional email or LinkedIn link]**

---
