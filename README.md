# Primetrade.ai-Assignment

# Market Sentiment and Trading Behavior Analysis

Project Overview
This repository contains the analysis for the Web3 Trading Team data science assignment, exploring the relationship between trade execution data and the Bitcoin Fear & Greed Index.

The primary objective was to derive actionable, risk-adjusted trading strategies by quantifying how market sentiment influences trader profitability, risk-taking, and volume.


# Technical Workflow Highlights 

Data Cleaning & Merging: 
Column names were standardized using str.strip().str.replace(' ', '_').str.lower().
Datasets were merged using a Left Join on a normalized daily date key ($\text{timestamp.dt.normalize()}$) to align granular trades with the daily sentiment.
Missing sentiment values were imputed using Forward Fill ($\text{ffill}$).

Feature Engineering:
Normalized PnL ($\frac{\text{Closed PnL}}{\text{Size USD}}$) was created as the key metric for risk-adjusted performance.
Lagged Sentiment ($\text{value.shift(1 day)}$) was calculated to test for a 'hidden signal'.
Risk Proxy: Due to the absence of the explicit leverage column, $\text{Size USD}$ was used as the professional proxy for trade exposure/risk magnitude.

# Tools 

Python (Pandas, NumPy, Seaborn, Matplotlib)
Google Colab
GitHub
