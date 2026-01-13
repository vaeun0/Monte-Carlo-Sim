# Monte-Carlo-Simulation-StockPrice

**1. Project Overview**

This project applies quantitative finance techniques to model and analyze future asset price behavior under uncertainty. Using historical price data, log returns are computed and analyzed to understand return characteristics before simulating future price paths through Monte Carlo methods.

2. Objective

The objective of this project is to:

Analyze the historical return behavior of a financial asset

Estimate return distribution parameters

Build a foundation for probabilistic price forecasting using simulation

Rather than predicting a single future price, this approach focuses on understanding the range of possible outcomes and associated risks.

3. Asset and Data Description

The analysis is conducted on NVIDIA Corporation (NVDA) using daily closing price data from January 2019 to January 2026.

The dataset contains:

Date

Adjusted closing price

Adjusted prices are used to account for stock splits and corporate actions, ensuring that computed returns reflect true investor outcomes.

4. Data Preparation

Historical price data is cleaned and sorted chronologically. Logarithmic returns are computed using consecutive price observations.

Log returns are preferred because they are time additive and provide a more stable representation of price changes over time.

5. Return Distribution Analysis

The empirical distribution of daily log returns is examined using a histogram. A normal distribution with the same mean and standard deviation is overlaid to assess the suitability of a normality assumption.

The return distribution exhibits a roughly bell shaped structure centered near zero, with noticeable fat tails. This indicates that extreme price movements occur more frequently than predicted by a normal distribution.

Despite this limitation, the normal distribution serves as a reasonable baseline model for initial Monte Carlo simulations.


