
# Monte Carlo Option Pricing & Risk Analysis

A Python-based quantitative finance project that prices a European call option using Monte Carlo simulation, validates the results against the Black-Scholes model, and evaluates option sensitivities and risk.

## Project Overview

This project combines stochastic simulation, derivative pricing, numerical analysis, and risk measurement.

### Key Features

- Geometric Brownian Motion (GBM) stock price simulation
- Risk-neutral Monte Carlo pricing of a European call option
- Monte Carlo convergence analysis (100–50,000 simulations)
- Black-Scholes analytical benchmark
- Sensitivity analysis of volatility, strike price, and stock price
- Option Greeks: Delta, Gamma, Vega, Theta, and Rho
- Value at Risk (VaR) and Conditional Value at Risk (CVaR)
- Profit/loss distribution visualization

## Model Parameters

| Parameter | Value |
|---|---|
| Initial stock price | EUR 100 |
| Strike price | EUR 110 |
| Time to maturity | 1 year |
| Volatility | 20% |
| Risk-free interest rate | 3% |
| Assumed real-world expected return | 8% |

## Selected Results

| Metric | Result |
|---|---|
| Monte Carlo option price (50,000 simulations) | EUR 5.33 |
| Black-Scholes option price | EUR 5.29 |
| Delta | 0.4104 |
| Gamma | 0.0194 |
| Vega (1 percentage point) | 0.3888 |
| Daily Theta | -0.0136 |
| Rho (1 percentage point) | 0.3575 |
| 95% VaR | EUR 5.2934 |
| 95% CVaR | EUR 5.2934 |

## Technologies

- Python
- NumPy
- SciPy
- Pandas
- Matplotlib
- Jupyter Notebook

## How to Run

1. Install the required libraries:

   `pip install numpy scipy pandas matplotlib notebook`

2. Open `Monte_Carlo_Options_Pricing.ipynb` in Jupyter Notebook or JupyterLab.
3. Run all cells from top to bottom.

## Key Findings

The Monte Carlo pricing estimate is close to the Black-Scholes analytical benchmark. Sensitivity analysis demonstrates how call option values respond to market parameters, while the Greeks quantify the local effects of these changes.

The risk analysis illustrates the asymmetric profit/loss profile of a purchased call option: downside is limited to the initial premium, while upside is theoretically unlimited.

## Limitations

The analysis uses a simplified GBM model with constant volatility and interest rates. Real-world risk estimates depend on the assumed expected return and volatility. Transaction costs, market frictions, and early liquidation are not modeled.

This project is intended for educational and quantitative research purposes, not as an investment recommendation.
