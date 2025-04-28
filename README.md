# 📈 Momentum and Hurst-Based Trading Strategy (10d Momentum, 30d Hurst)

This project implements a **momentum-based trading strategy** enhanced by **Hurst Exponent analysis** to generate **long and short trading signals** on **Apple (AAPL)** stock.

The system uses fixed analysis windows — **10-day momentum** and **30-day Hurst exponent** — to adaptively position trades based on market conditions between **December 2024 and April 2025**.

---

## 📋 Project Overview

- **Asset Traded**: Apple Inc. (AAPL)
- **Period**: December 2024 to April 2025
- **Data Source**: Yahoo Finance (`yfinance`)
- **Strategy Concept**:
  - Calculate **10-day momentum** (percentage price change over the last 10 days)
  - Calculate **30-day Hurst exponent** (trend strength)
  - Generate signals:
    - **Long** (`Signal = 1`) when `Momentum > 0` and `Hurst_30d > 0.3`
    - **Short** (`Signal = -1`) when `Momentum < 0` and `Hurst_30d > 0.3`
    - **No position** (`Signal = 0`) otherwise
- **Backtesting**:
  - Cumulative strategy returns vs Buy & Hold returns
  - Sharpe Ratio calculation
  - Visualization of cumulative returns over time

---

## 🛠️ Technologies Used

- Python 3.x
- Jupyter Notebook
- `numpy`
- `pandas`
- `matplotlib`
- `scipy`
- `yfinance`
- `statsmodels`

---
## 📈 Results

- During the selected testing period (**December 2024 to April 2025**),  
  no trades (long or short) were triggered by the strategy.
- As a result:
  - Final cumulative return = 0%
  - Final strategy value remained flat
  - Sharpe Ratio was undefined (no variability in returns)
- The strict filtering conditions (10-day momentum and 30-day Hurst exponent thresholds) combined with a short testing window led to no trading signals.

> ⚠️ **Note**: Adjusting the strategy thresholds (for example, using Hurst > 0.25) or expanding the backtest period could generate active signals and meaningful performance analysis.

