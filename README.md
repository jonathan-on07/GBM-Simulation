# Geometric Brownian Motion & Monte Carlo Option Pricing

A Python implementation of Geometric Brownian Motion (GBM) used to simulate stock price movements with Monte Carlo methods. The project includes risk analysis using Value at Risk (VaR) and Conditional Value at Risk (CVaR), as well as pricing European call options and validating the Monte Carlo estimate against the Black–Scholes analytical solution.

---

## Features

- Simulates thousands of stock price paths using Geometric Brownian Motion
- Fully vectorized implementation using NumPy
- Calculates Value at Risk (90%, 95%, and 99%)
- Calculates Conditional Value at Risk (CVaR)
- Prices European call options using Monte Carlo simulation
- Compares Monte Carlo results with the Black–Scholes formula
- Visualizes simulated price paths and return distributions

---

## Mathematical Model

The stock price evolves according to the Geometric Brownian Motion model

```
dS = μS dt + σS dW
```

which has the analytical solution

```
S(t) = S₀ exp[(μ − ½σ²)t + σW(t)]
```

Each simulated time step is generated using

```
S(t+Δt) = S(t) × exp[(μ − ½σ²)Δt + σ√Δt Z]
```

where `Z ~ N(0,1)`.

---

## Example Output

### Simulated Stock Price Paths

![GBM Simulation](figures\gbm_paths.png)

### Distribution of Simulated Returns

![Return Distribution](figures\return_distribution.png)

---

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- SciPy

---

## Future Improvements

- Asian option pricing
- Barrier option pricing
- Greeks (Delta, Gamma, Vega)
- Variance reduction techniques
- Historical parameter calibration
- Performance benchmarking

---

## Author

Jonathan Nkana

Bachelor of Science in Actuarial and Financial Mathematics
