# 📘 Project Title: Covered Call Strategy Backtesting with Greeks (NIFTY 50)
## 📌 Objective:
**Backtest a covered call strategy on the NIFTY 50 index using Black-Scholes option pricing and compute Greeks (Delta, Gamma, Vega) to enhance insight into the trade's risk exposure.**

## 📁 Data Source:
Symbol: ^NSEI (NIFTY 50 Index)

Data Provider: Yahoo Finance (via yfinance)

Period: 2010-01-01 to 2024-01-01

Frequency: Daily Close Prices

## ⚙️ Strategy Parameters:
Contract Frequency: Monthly (every 21 trading days)

Strike Price: At-the-Money (ATM) call (i.e., K = S0)

Risk-Free Rate: 7.5% annualized

Volatility: Annualized standard deviation of daily returns

Model Used: Black-Scholes formula

## 🧮 Option Pricing & Greeks:
For each interval (monthly):

Call Option Premium using Black-Scholes:

𝐶
=
𝑆
0
⋅
𝑁
(
𝑑
1
)
−
𝐾
⋅
𝑒
−
𝑟
𝑇
⋅
𝑁
(
𝑑
2
)
C=S 
0
​
 ⋅N(d 
1
​
 )−K⋅e 
−rT
 ⋅N(d 
2
​
 )
Greeks calculated:

Delta: 
𝑁
(
𝑑
1
)
N(d 
1
​
 )

Gamma: 
𝑁
′
(
𝑑
1
)
𝑆
0
⋅
𝜎
⋅
𝑇
S 
0
​
 ⋅σ⋅ 
T
​
 
N 
′
 (d 
1
​
 )
​
 

Vega: 
𝑆
0
⋅
𝑁
′
(
𝑑
1
)
⋅
𝑇
S 
0
​
 ⋅N 
′
 (d 
1
​
 )⋅ 
T
​
 

## 📊 Metrics Computed:
Index P&L = 
𝑆
𝑇
−
𝑆
0
S 
T
​
 −S 
0
​
 

Option P&L = Premium – Max(ST − K, 0)

Total P&L = Index P&L + Option P&L

## 📈 Strategy Performance:
Metric	Value\
Total Return= 258.16\
Annualized Return	= 9.77%\
Max Drawdown = 	₹4239.62\
Win Rate= 	77.91%

## 💡 Key Learnings:
Despite a high win rate (77.91%), the CAGR is modest (9.77%) — showing that consistent small wins do not always lead to high compounding returns.

The inclusion of Greeks gives deeper insights into risk exposure and can help build more adaptive strategies (e.g., based on Delta hedging or Vega exposure).

This backtest is static — it does not include adjustments or early exits. Dynamic strategies using Greeks could further improve performance.

