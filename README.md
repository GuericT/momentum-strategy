# Momentum Strategy - Quantitative Trading Project

## 📌 Overview
This project simulates the work of a **junior quantitative analyst** by developing a **long/short momentum strategy** on U.S. equities.  
The goal is to demonstrate the ability to:
- Retrieve and process financial data
- Build a quantitative trading strategy
- Backtest and evaluate performance
- Visualize results

---

## ⚙️ Project Steps

1. **Data Collection**  
   - Download historical price data for S&P 500 stocks (last 5 years) using Yahoo Finance API (`yfinance`).

2. **Momentum Signal**  
   - Compute 12-month momentum:  
   \[
   Momentum = \frac{P_{t}}{P_{t-252}} - 1
   \]
   - Rank stocks based on this metric.

3. **Portfolio Construction**  
   - Go **long** on top 10% of momentum stocks  
   - Go **short** on bottom 10%  
   - Rebalanced monthly

4. **Backtesting**  
   - Compute daily portfolio returns
   - Compare to benchmark (S&P 500)
   - Performance metrics: CAGR, Sharpe ratio, Max Drawdown

5. **Visualization & Report**  
   - Plot cumulative returns
   - Generate full performance report with `quantstats`

---

## 📊 Results (Example)

![Performance Chart](results/example_chart.png)

- CAGR: **12.4%**
- Sharpe Ratio: **1.15**
- Max Drawdown: **-18.7%**

---

## 🛠️ Tools & Libraries
- Python 3.10+
- pandas, numpy
- yfinance
- matplotlib, seaborn
- quantstats

---

## 🚀 How to Run

Clone the repository:
```bash
git clone https://github.com/username/momentum-strategy.git
cd momentum-strategy
pip install -r requirements.txt
