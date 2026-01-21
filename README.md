# Monte-Carlo-Simulation-StockPrice

Monte Carlo simulation project to model future stock price behavior under uncertainty using historical data and probabilistic sampling of returns.

---

## Project Overview

This project applies quantitative finance techniques to analyze historical stock returns and simulate potential future price paths. Using daily adjusted closing prices, the notebook computes log returns, studies their distribution, and generates many simulated outcomes to understand risk and variability rather than producing a single point prediction.

---

## Objective

The goals of this project are to:

- Analyze historical return behavior of a financial asset
- Estimate return distribution parameters (mean and volatility)
- Build a foundation for probabilistic price forecasting using Monte Carlo simulation

Instead of predicting one future price, the project focuses on the range of possible outcomes and the uncertainty around them.

---

## Asset and Data Description

- **Asset:** NVIDIA Corporation (NVDA)
- **Frequency:** Daily
- **Time period:** January 2019 to January 2026
- **Price field used:** Adjusted Close

Adjusted prices are used to account for stock splits and corporate actions so that computed returns reflect investor level outcomes.

---

## Method Summary

### 1) Data Preparation
- Clean and sort the data chronologically
- Compute **log returns** from consecutive adjusted closing prices

Why log returns:
- They are **time additive**
- They often provide a more stable representation of relative price changes

### 2) Return Distribution Analysis
- Plot a histogram of daily log returns
- Overlay a normal distribution using the same mean and standard deviation
- Visually assess whether a normal assumption is reasonable

Observation:
- Returns are roughly bell shaped and centered near zero
- There are **fat tails**, meaning extreme moves happen more often than a normal model predicts

Even with this limitation, the normal distribution is used as a baseline for simulation because it is simple, interpretable, and commonly used as a first step.

### 3) Monte Carlo Simulation of Future Prices
- Estimate historical mean return and volatility
- Simulate many future return sequences by random sampling
- Convert simulated returns into simulated future price paths (compounding through time)
- Analyze the distribution of simulated outcomes

Key output:
- A **distribution** of possible future prices and paths, not a single forecast

---

## Results and Interpretation

What this project provides:
- An empirical view of historical return behavior
- A probabilistic range of future prices
- A clearer picture of uncertainty and downside risk

What it does not claim:
- Guaranteed prediction accuracy
- Perfect modeling of market crashes or regime shifts

---

## Limitations

- Assumes return behavior estimated from history remains stable
- Normal returns can underestimate extreme events (fat tails)
- Does not include time varying volatility, jumps, or macro regime changes





