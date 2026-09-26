# Black-Scholes Option Pricing: Analytical vs Monte Carlo

## Overview

This project explores European call option pricing using two approaches:

1. The analytical Black-Scholes pricing model
2. Monte Carlo simulation

The project was implemented in Python to compare the numerical Monte Carlo estimate against the analytical Black-Scholes benchmark.

The analysis also examines Monte Carlo convergence, statistical uncertainty, option Greeks, and sensitivity to changes in the underlying stock price.

## Project Objectives

- Implement the Black-Scholes analytical pricing model
- Implement Monte Carlo simulation for European call option pricing
- Compare Monte Carlo estimates with the analytical benchmark
- Analyse Monte Carlo convergence and pricing error
- Calculate a 95% confidence interval
- Calculate the main Black-Scholes Greeks
- Perform stock-price sensitivity analysis
- Examine model assumptions and limitations

## Model Parameters

| Parameter | Value |
|---|---:|
| Initial Stock Price | $100 |
| Strike Price | $100 |
| Time to Maturity | 1 year |
| Risk-Free Rate | 5% |
| Volatility | 20% |
| Monte Carlo Simulations | 1,000,000 |

## Key Results

| Metric | Result |
|---|---:|
| Black-Scholes Price | $10.4506 |
| Monte Carlo Price | $10.4342 |
| Absolute Error | $0.0164 |
| Relative Error | 0.1572% |
| Standard Error | $0.0147 |
| 95% Confidence Interval | $10.4053 – $10.4630 |

## Option Greeks

| Greek | Value |
|---|---:|
| Delta | 0.6368 |
| Gamma | 0.01876 |
| Vega | 0.3752 |
| Theta | -6.4140 |
| Rho | 0.5323 |

## Methods

### Black-Scholes

The Black-Scholes model provides an analytical benchmark for the theoretical value of a European call option.

### Monte Carlo Simulation

Monte Carlo simulation generates random stock-price outcomes under geometric Brownian motion and estimates the option price from the discounted average payoff.

The simulation was tested using different numbers of simulations to examine convergence towards the Black-Scholes benchmark.

## Sensitivity Analysis

The project examines how:

- Call option price changes with the underlying stock price
- Delta changes with the underlying stock price
- Gamma changes with the underlying stock price

The analysis demonstrates the nonlinear relationship between the underlying stock price and the value of the option.

## Model Assumptions

The implementation assumes:

- Constant volatility
- Constant risk-free interest rate
- Log-normal stock prices
- No transaction costs
- Continuous trading
- European exercise
- No dividends

## Limitations

The assumptions of the Black-Scholes model simplify real financial markets. In practice, volatility and interest rates can change over time, transaction costs exist, and asset-price behaviour may differ from geometric Brownian motion.

Monte Carlo simulation also introduces sampling error, with greater numbers of simulations generally reducing statistical uncertainty at increased computational cost.

## Technologies

- Python
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

## Project Files

- `Black_Scholes_Monte_Carlo.ipynb` — Complete Python implementation, analysis and visualisations
