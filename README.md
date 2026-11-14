# quant-risk-metrics-python
Risk metrics in Python using real SPY and NVDA prices from Yahoo Finance. Calculates skewness, Sortino ratio, kurtosis, 95% Value at Risk (VaR), 95% Conditional VaR (CVaR), and expectancy for a Micro Gold +75/-25 tick bracket. SPY: excess kurtosis 3.06, VaR -1.42%, CVaR -1.91%. Expectancy +$15 per trade at a 40% win rate, breakeven 25%.

# Risk Metrics in Python — SPY & NVDA

Applied quant work in Python, using real daily prices for SPY and NVDA from Yahoo Finance (yfinance), run in Google Colab.

## What it calculates

- **Skewness** — which side hurts, up or down
- **Sortino ratio** — return per unit of downside risk only
- **Kurtosis** — how often extreme days happen
- **95% Value at Risk (VaR)** — how bad a bad day is
- **95% Conditional VaR (CVaR)** — average loss on the worst days
- **Expectancy** — average profit or loss per trade

## Results (13 Nov 2026, 1-year window)

| Metric | SPY | NVDA |
|---|---|---|
| Mean daily return | +0.045% | -0.038% |
| Volatility | 0.867% | 2.458% |
| Skewness | -0.46 | -0.02 |
| Sortino (annualised) | 1.16 | -0.34 |
| Sharpe (annualised) | 0.82 | -0.24 |
| Excess kurtosis | 3.06 | 1.07 |
| 95% VaR | -1.42% | — |
| 95% CVaR | -1.91% | — |

Expectancy for a Micro Gold +75 / -25 tick bracket (+$75 / -$25 per contract):
+$15 per trade at a 40% win rate, +$5 at 30%, -$5 at 20%. Breakeven win rate is 25%.

## How to run it

Open the notebook in Google Colab and run all cells. Re-running later will give slightly different numbers, because the 1-year window moves.
