# Fund Analytics, Strategy Implementation & Derivatives Modeling – Python Notebook

## Overview

This project is a collection of **three independent exercises** focused on advanced financial analysis and quantitative modeling. It covers fund performance diagnostics, portfolio allocation using factor models, and derivative pricing via Monte Carlo simulation.

---

## Contents

- `final.ipynb`: Notebook structured around three main exercises.
- `funds.csv`: Time series data of various funds, used in Exercises 1 and 2.
- `100_Portfolios_10x10_Daily.csv`: Fama-French factor data used in Exercise 2.

---

## Exercises Breakdown

### **Exercise 1 – Maximum Time Under Water**
> *Goal*: Compare the **Maximum Time Under Water (MTUW)** across 6 funds.  
> MTUW measures the longest duration a fund takes to recover from a drawdown — critical for understanding fund resilience and risk.

- Implements a rolling max-tracking logic to compute drawdowns.
- Visualizes drawdown trajectories.
- Outputs the maximum recovery time for each fund.

---

### **Exercise 2 – Factor-Based Covariance & Portfolio Allocation**
> *Goal*: Use **factor models** to estimate the covariance matrix of fund returns and optimize asset allocation.

- Uses Fama-French data (`100_Portfolios_10x10_Daily.csv`) as explanatory factors.
- Computes **factor exposures** and **residual covariance**.
- Performs portfolio optimization based on:
  - Factor model covariance
  - Sample covariance
- Compares resulting portfolio allocations and performances.

---

### **Exercise 3 – Asian Option Pricing with Monte Carlo**
> *Goal*: Price an **Asian Call Option** using Monte Carlo simulations.

- Simulates Geometric Brownian Motion for the underlying asset.
- Estimates the price of an Asian call option (average-based payoff).
- Compares convergence across different numbers of simulations.

---

## Technologies Used

- Python (Jupyter Notebook)
- Pandas, NumPy
- Matplotlib
- `statsmodels.api` for regressions
- Monte Carlo simulation (from scratch)

---

## Getting Started

1. Place all files (`final.ipynb`, `funds.csv`, `100_Portfolios_10x10_Daily.csv`) in the same folder.
2. Open the notebook in Jupyter.
3. Run exercises one by one – they are self-contained.

---

## Notes

- Exercise 1 and 2 rely on historical fund performance.
- Exercise 2 requires understanding of **multivariate regression** and **risk modeling**.
- Exercise 3 is suitable as an introduction to **derivatives pricing** using simulation.