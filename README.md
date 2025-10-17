# GTSF IC Quant Mentorship — Python for Quantitative Finance Fundamentals

## Project Overview

This project demonstrates the application of quantitative finance fundamentals using Python. Over the course of six sections, I explored topics such as probability and statistics, time value of money, basic portfolio theory, and financial data analysis.

By analyzing real market data, I applied these core quantitative concepts to evaluate risk, return, diversification, and market relationships — culminating in a complete investment summary and recommendation.

## Setup and Dependencies
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
import yfinance as yf
```
**Configuration**
```python
pd.set_option('display.max_columns', 10)
pd.set_option('display.precision', 4)
plt.style.use('default')
plt.rcParams['figure.figsize'] = (10, 6)
```
## Project Structure
### Part 1 — Data Collection & Basic Analysis
- Downloaded 3 years (2021–2024) of data for AAPL, JNJ, and SPY
- Cleaned datasets and computed both simple and log returns
- Explained the importance of adjusted close prices in financial analysis

**Result**
- 753 trading days of data
- AAPL’s largest simple return: 0.08897 | log return: 0.08523
- Difference: 0.00374

### Part 2 - Risk and Return Analysis
- Calculated mean returns, volatility, and Sharpe ratios
- Visualized the risk-return relationship

**Result**
| Stock | Annualized Return | Annualized Volatility | Sharpe Ratio |
| :--- | :--- | :--- | :--- |
| AAPL | 17.76% | 0.2780 | 0.5668 |
| JNJ | 4.06% | 0.1619 | 0.1274 |
| SPY | 11.54% | 0.1760 | 0.5422 |

### Part 3 — Correlation and Diversification
- Created a correlation matrix and heatmap
- Constructed an equal-weighted portfolio of AAPL and JNJ

**Result**
- Correlation (AAPL–JNJ): 0.2396 → Good diversification potential
- Portfolio volatility: 17.68%, lower than the average individual volatility (22%)
- Diversification benefit: 0.0432

### Part 4 — Market Relationships (Beta Analysis)
- Calculated betas using covariance and regression
- Visualized the stock–market relationship with regression lines

**Result**
| Stock | Beta | 
| :--- | :--- |
| AAPL | 1.272 |
| JNJ | 0.326 |

- AAPL: Aggressive stock — more sensitive to market fluctuations
- JNJ: Defensive stock — less affected by market volatility

### Part 5 — Time Series Analysis
- Plotted cumulative returns and rolling volatility over time

**Result**
| Asset | Total Return (2021–2024) | 
| :--- | :--- |
| AAPL | 51.40% |
| JNJ | 8.57% |
| SPY | 34.74% |

- Highest volatility observed between May 2022 – March 2023, likely due to geopolitical and market uncertainty (e.g., Russia default risks, EU antitrust cases).
- Rolling volatility reveals dynamic risk levels and changing investor sentiment over time.

### Part 6 — Summary Analysis & Investment Recommendation
- AAPL exhibited the best risk-adjusted return but also the highest beta.
- AAPL–JNJ portfolio provided significant diversification benefits, reducing volatility.
- Beta analysis confirmed intuitive expectations: tech stocks are more market-sensitive than defensive healthcare stocks.
- Volatility spiked in mid-2022 due to macroeconomic and geopolitical shocks.

Recommendation:
A diversified portfolio of AAPL and JNJ is superior to holding either stock individually. Balancing AAPL’s high-growth potential with JNJ’s defensive characteristics yields better stability and improved Sharpe ratio performance.
