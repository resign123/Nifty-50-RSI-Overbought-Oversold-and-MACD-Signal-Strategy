# **Nifty-50-RSI-Overbought-Oversold-and-MACD-Signal-Strategy**

This repository contains a trading strategy that combines the **Relative Strength Index (RSI)** and **Moving Average Convergence Divergence (MACD)** indicators to generate robust buy and sell signals for more effective trading. The strategy has been thoroughly backtested and optimized for performance across a multi-year period on the NIFTY50 index.

## **Strategy Overview**

This strategy uses **RSI** to detect potential buy and sell opportunities and relies on **MACD** to confirm these signals, reducing the likelihood of false entries and exits.

### **Indicators Used**

1. **RSI (Relative Strength Index)**:
   - **Buy Signal**: RSI drops below 30 (oversold) and crosses back above 30.
   - **Sell Signal**: RSI rises above 70 (overbought).
   
   **Settings**:
   - Length: 10
   - Source: Closed values

2. **MACD (Moving Average Convergence Divergence)**:
   - Confirms buy and sell signals triggered by RSI.
   
   **Settings**:
   - Fast Length: 8
   - Slow Length: 21
   - Signal Smoothing: 5
   - Source: Closed values
   - Oscillator MA Type: EMA
   - Signal Line MA Type: EMA

### **Trading Logic**

- **Buy Signal**:
  - RSI drops below 30, then crosses back above 30.
  - Confirmation: MACD line crosses above the signal line after the RSI buy signal.
  
- **Sell Signal**:
  - RSI crosses above 70.
  - Confirmation: MACD line crosses below the signal line after the RSI sell signal.

This combination allows the strategy to filter out false signals, entering trades when both RSI and MACD align for maximum trend-following efficiency.

## **Backtest Results**

The strategy has been rigorously backtested over 5.5 years to evaluate its performance. Below are the key metrics:

| **Backtest Metric**                     | **Value**        |
|-----------------------------------------|------------------|
| **Backtest Start Date**                 | 2017-07-17       |
| **Backtest End Date**                   | 2022-12-20       |
| **Number of Trades**                    | 10,025           |
| **Number of Wins**                      | 8,506            |
| **Number of Losses**                    | 1,516            |
| **Average Profit**                      | 1,119.93 points  |
| **Average Loss**                        | -1,352.02 points |
| **Maximum Profit Points**               | 50,012.5 points  |
| **Maximum Loss Points**                 | -29,987.5 points |
| **Median Trade**                        | 637.5 points     |
| **Win Rate**                            | 85%              |
| **Expectancy**                          | 0.55             |
| **Sharpe Ratio**                        | 2.71             |
| **Sortino Ratio**                       | 2.17             |
| **Max Drawdown**                        | -33,867.5 points |
| **Max Drawdown Percent**                | -1.22%           |
| **Days Taken to Recover from Drawdown** | 10 days          |
| **Number of Trades to Recover**         | 38 trades        |
| **Calmar Ratio**                        | 78.49            |
| **CAGR (Compound Annual Growth Rate)**  | 95.76%           |
| **Consecutive Wins**                    | 56               |
| **Consecutive Losses**                  | 5                |
| **Profit Factor**                       | 4.65             |
| **Outlier Adjusted Profit Factor**      | 4.62             |

### **Key Takeaways**:
- With an impressive **win rate of 85%**, this strategy captures the majority of trades successfully.
- The **Profit Factor of 4.65** indicates that for every unit of loss, the strategy generates 4.65 units of profit.
- **Sharpe** and **Sortino Ratios** reflect strong risk-adjusted returns, while the **CAGR of 95.76%** shows remarkable annual growth.
