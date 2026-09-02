# Portfolio Analytics & Risk-Return Optimization System

A Python-based project that analyzes a 14-stock portfolio across multiple sectors,
calculates risk and return metrics, and applies Modern Portfolio Theory to find an
optimal asset allocation.

## Status
🚧 In progress — Weeks 1–3 complete (data pipeline, risk/return metrics, portfolio
optimization via Monte Carlo simulation). 

## What This Project Does
- Pulls historical stock price data for 14 stocks across 5 sectors (Banking, IT, FMCG,
  Auto, Pharma) plus the Nifty 50 benchmark
- Stores and queries the data using SQLite
- Calculates annualized return, volatility, Sharpe ratio, and beta for each stock
- Builds a correlation matrix to understand how stocks move together
- Runs a Monte Carlo simulation (50,000 portfolios) to find the optimal
  risk-return allocation using Modern Portfolio Theory
- *(Coming next)* Backtests the optimized portfolio against the Nifty 50 benchmark
- *(Coming next)* Visualizes results in an interactive Power BI dashboard

## Tools Used
- Python (pandas, numpy, yfinance, matplotlib, seaborn)
- SQLite (data storage and querying)
- Power BI *(planned)*

## Key Findings
- M&M had the strongest individual risk-adjusted performance (Sharpe ratio: 1.09),
  followed by SBI (0.88), Sun Pharma (0.85), and ICICI Bank (0.70) — all
  outperforming the Nifty 50 benchmark (0.55) on a risk-adjusted basis.
- The three IT stocks (TCS, Infosys, Wipro) showed the highest correlation in the
  portfolio (~0.70), indicating limited diversification benefit from holding all three
- An equal-weighted baseline portfolio returned 15.71% annually at 12.75% volatility,
  with diversification alone cutting risk by ~9.5 percentage points versus holding
  the stocks independently.
- The optimized (max Sharpe) portfolio from a 50,000-portfolio Monte Carlo simulation
  achieved a 26.14% return at 16.30% volatility (Sharpe ratio: 1.20).
- The optimizer concentrated weight in SBI (28%), Eicher Motors (25%), and Maruti
  (24%), favoring Auto and Banking sector exposure over an even spread.
