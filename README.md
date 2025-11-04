# Quantitative & Behavioral Analysis — S&P 500  
**Report ID:** BTCQ-2025-3484  
**Date:** 3 November 2025  
**© 2025 Beyond the Chart | Proprietary Quantitative & Behavioral Research**

---

## Abstract

This report delivers a full quantitative and behavioral assessment of an S&P 500 trading account.  
We combine classical risk–return diagnostics with structural and behavioral indicators to evaluate the internal stability of the trading edge over 500 discrete trades.  
Findings point to structural decay manifested by volatility amplification, clustered drawdowns, and declining risk-adjusted returns despite a high win rate.  
Monte Carlo stress tests and regime diagnostics indicate that positive expectancy is undermined by asymmetric downside tails and unstable payoff ratios.

---

## Dataset & Methodology

- **Instrument:** S&P 500  
- **Sample:** 500 executed trades  
- **Data Frequency:** Trade-by-trade (aggregated from tick-level execution logs)  
- **Period Covered:** Up to 3 November 2025  
- **Framework:** Hybrid quantitative–behavioral model covering volatility response, frequency drift, and edge-decay dynamics  
- **Analytical Modules:**
  - Equity curve and drawdown decomposition  
  - Return distribution and QQ-plot validation  
  - Historical VaR/CVaR simulation (95–99%)  
  - Rolling Sharpe & Sortino (100-trade windows)  
  - Hurst exponent and ADF stationarity testing  
  - Edge-decay modeling (rolling mean P/L trend)  
  - Monte Carlo stress testing (500 reshuffled paths)  
  - Cumulative survival probability estimation  

All computations were executed in Python (NumPy, SciPy, pandas, statsmodels, matplotlib).  
The analysis blends classical statistics with non-linear stochastic diagnostics to capture drift, persistence, and tail asymmetries.

---

## Visual Results

### Equity & Drawdown
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/equity_drawdown.png?raw=true)

### Drawdown Profile
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/drawdown_profile.png?raw=true)

### Drawdown Duration
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/drawdown_duration.png?raw=true)

### Recovery Time Drawdown
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/recovery_time_drawdown.png?raw=true)

### Rolling Sharpe & Sortino
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/rolling_sharpe_sortino.png?raw=true)

### Rolling Win Rate / Payoff Ratio
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/rolling_winrate_payoff_ratio.png?raw=true)

### Payoff Stability
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/payoff_stability.png?raw=true)

### Risk Curve Cumulative
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/risk_curve_cumulative.png?raw=true)

### Cumulative Survival Curve
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/survival_probability.png?raw=true)

### Expected Annual Outcome
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/expected_annual_outcome.png?raw=true)

### Final Equity Distribution
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/final_equity_distribution.png?raw=true)

### Monte Carlo Simulation
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/montecarlo_simulation.png?raw=true)

### Monte Carlo Fan Chart
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/montecarlo_fan_chart.png?raw=true)

### Change Point Equity
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/change_point_equity.png?raw=true)

### Edge Decay Trend
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/edge_decay_trend.png?raw=true)

### Edge Decay Trend (Rolling Avg P/L – 30)
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/edge_decay_trend_rolling.png?raw=true)

### Edge Decay Timeline
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/edge_decay_timeline.png?raw=true)

### Edge Collapse Root Cause Matrix
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/edge_collapse_root_cause_matrix.png?raw=true)

### Edge Early-Warning Panel
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/edge_early_warning_panel.png?raw=true)

### Behavior-Structure Equilibrium Map
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/behavior_structure_equilibrium_map.png?raw=true)

### Behavior vs Structure — Enhanced Sensitivity
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/behavior_vs_structure_enhanced_sensitivity.png?raw=true)

### Behavior vs Structure — Stress Pressure
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/behavior_vs_structure_stress_pressure.png?raw=true)

### Behavior vs Structure — Timeline
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/behavior_vs_structure_timeline.png?raw=true)

### ACF Returns
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/acf_returns.png?raw=true)

### PACF Returns
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/pacf_returns.png?raw=true)

### Ulcer Index
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/ulcer_index.png?raw=true)

### Sortino Stress — Downside Risk
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/sortino_stress_downside_risk.png?raw=true)

### Beyond Risk Metrics — Table
![](https://github.com/BeyondTheChart/BTCQ-2025-SP500/blob/main/results/charts/beyond_risk_metrics_table.png?raw=true)

---

## Additional Metrics

### Return per Trade Distribution
![](results/charts/return_distribution.png)  
Skew and tail structure evidencing asymmetry and non-Gaussian single-trade returns.

---

### QQ-Plot
![](results/charts/qqplot_returns.png)  
Deviation from the Gaussian model highlighting excess kurtosis and fat-tail behavior.

---

### Tail Risk (VaR / CVaR)
![](results/charts/var_cvar.png)  
Historical loss simulation at 95–99% confirming clustered volatility and heavy downside tails.

---

### Rolling Win Rate / Payoff Ratio
![](results/charts/rolling_winrate_payoff_ratio.png)  
Behavioral consistency: joint evolution of win rate and payoff across volatility regimes.

---

### Hurst & ADF
![](results/charts/hurst_adf.png)  
Persistence and mean-reversion diagnostics of the equity process; lower values indicate edge decay.

---

### Edge Decay Trend (Rolling Avg P/L – 30)
![](results/charts/edge_decay_trend_rolling.png)  
Short-horizon rolling mean P/L capturing local decay within broader edge dynamics.

---

### Monte Carlo Simulation (500 runs)
![](results/charts/montecarlo_simulation.png)  
Final equity distribution from 500 randomized trade-order paths, validating robustness under re-sequencing.

---

### Survival Probability
![](results/charts/survival_probability.png)  
Cumulative likelihood of account persistence across the trade sequence horizon.

---

## Quantitative Performance Summary

| Metric | Value |
|:--|--:|
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

## Quantitative Interpretation

1. **Performance Instability** — Despite an 84% win rate, the profit factor (0.92) and negative Sharpe/Sortino confirm structural inefficiency. The equity path exhibits recurrent drawdowns >100%, consistent with tail clustering.  
2. **Volatility Response** — Expansions in realized volatility magnify drawdown depth and reduce payoff stability. Rolling risk-adjusted metrics remain negative across most observation windows.  
3. **Tail Risk Exposure** — Historical simulation shows extreme CVaR (−279.89% at 95% and −1,139.50% at 99%), indicating that infrequent but severe losses dominate the distribution.  
4. **Edge Persistence & Drift** — Edge-decay and Hurst (0.54) indicate mild persistence with structural deterioration. The ADF statistic (−3.23, p=0.0185) rejects pure randomness, implying mean-reverting noise around a declining mean expectancy.  
5. **Monte Carlo & Survival Modeling** — The fan chart and survival curve imply a 60–70% probability of capital impairment beyond ~300 trades, consistent with edge erosion under variance amplification.

---

### Equity & Drawdown (Narrative)

The equity curve alternates high-volatility clusters with deep drawdowns exceeding 100%, a signature of over-leveraged mean-reversion under adverse regimes.

### VaR / CVaR (Narrative)

Tail-risk simulation confirms disproportionate loss magnitude relative to trade frequency, revealing asymmetric downside dynamics.

### Edge Decay (Narrative)

The rolling mean P/L drifts downward after ~trade #300, signaling exhaustion of the initial structural advantage.

---

## Behavioral Layer

While the quantitative layer identifies edge decay, behavioral drift is visible in the frequency and amplitude of trade clustering.  
Periods of elevated trade density align with higher-volatility regimes and payoff asymmetry — a pattern consistent with overconfidence and latent FOMO bias.  
These behavioral signatures precede quantitative decay and can operate as early warnings of edge exhaustion.

---

## Conclusion

The examined S&P 500 account exhibits **measurable performance decay** and **behavioral instability**.  
An initially positive edge deteriorates under volatility expansion, driving weaker risk-adjusted outcomes and excessive drawdowns.  
Absent volatility normalization and tighter risk controls, long-horizon expectancy remains statistically negative.

---

## Appendix

- **Tests executed:** Historical VaR/CVaR, ADF, Hurst R/S, CUSUM change-points, Monte Carlo (500 runs)  
- **Environment:** Python 3.12 — NumPy 2.1, SciPy 1.13, pandas 2.2, statsmodels 0.14  
- **Reproducibility:** All figures generated via reproducible scripts under `/src/`  
- **Metrics file:** `results/metrics_summary.csv`

---

## Legal Notice

© 2025 Beyond the Chart — All rights reserved.  
This repository and its contents (data, code, and visual materials) are proprietary.  
No part of this report may be copied, redistributed, or used commercially without explicit written permission from Beyond the Chart.  
For institutional collaboration or partnership inquiries, contact: **[add your professional email or LinkedIn link]**

