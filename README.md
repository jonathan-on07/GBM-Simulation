# Geometric Brownian Motion & Monte Carlo Option Pricing

A Python implementation of **Geometric Brownian Motion (GBM)** for simulating stock price paths using Monte Carlo methods. The project also includes risk analysis through **Value at Risk (VaR)** and **Conditional Value at Risk (CVaR)**, as well as pricing a European call option and comparing the result to the analytical **Black–Scholes** solution.

---

## Features

- Simulate stock prices using Geometric Brownian Motion
- Fully vectorized NumPy implementation
- Monte Carlo simulation of thousands of price paths
- Distribution of simulated returns
- Value at Risk (90%, 95%, 99%)
- Conditional Value at Risk (CVaR)
- European call option pricing using Monte Carlo
- Analytical Black–Scholes option pricing
- Confidence interval for Monte Carlo estimate

---

## Mathematical Model

The stock price follows the stochastic differential equation

\[
dS_t=\mu S_t\,dt+\sigma S_t\,dW_t
\]

whose exact solution is

\[
S_t=S_0\exp\left[\left(\mu-\frac12\sigma^2\right)t+\sigma W_t\right].
\]

Each simulation evolves according to

\[
S_{t+1}
=
S_t
\exp\left(
\left(\mu-\frac12\sigma^2\right)\Delta t
+
\sigma\sqrt{\Delta t}\,Z
\right),
\]

where

- \(Z\sim N(0,1)\)
- \(\mu\) is the expected annual return
- \(\sigma\) is the annual volatility

---

## European Call Option Pricing

The option price is estimated using Monte Carlo simulation

\[
C=e^{-rT}\mathbb{E}[\max(S_T-K,0)]
\]

and compared with the analytical Black–Scholes solution.

Example output

```
European Call Option

Monte Carlo Price : 8.17
Black-Scholes     : 8.02

Absolute Error    : 0.15
Relative Error    : 1.87%

95% Confidence Interval
[8.03, 8.31]
```

---

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib

## Future Improvements

- Asian option pricing
- Barrier option pricing
- Variance reduction techniques
- Delta, Gamma and Vega estimation
- Calibration using historical market data
- Performance benchmarking

