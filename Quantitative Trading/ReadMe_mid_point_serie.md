# Propagation Model and Mid-Point Series — Quantitative Trading Project

This notebook explores a **market microstructure model** by simulating a **mid-point price series** using long-memory order flow and a **propagation kernel**. The goal is to analyze how persistent order flow impacts price formation and to study the resulting price process focusing on the **Hurst exponent**.

---

## Objective

To model and analyze how correlated order flow can lead to persistent or mean-reverting price dynamics, using:

- A **long-memory process** for order signs
- A **propagation model** to construct mid-point prices
- Estimation of the **Hurst exponent** as a measure of memory in the resulting price series

---

## Methodology

1. **Order Flow Generation**:
   - Simulate a **fractional Brownian motion (FBM)** with Hurst exponent \( H = 0.75 \)
   - Compute the **sign of increments** to obtain a binary long-memory order flow series (εₜ)
   - Estimate the **decay exponent \gamma** of the autocorrelation of εₜ, fitted to a power law \( C(l) \sim l^{-\gamma} \)

2. **Mid-Point Price Construction**:
   - Use a **propagator model** to generate the mid-point series:
     $$
     m_t = m_0 + \sum_{n=0}^{t-1} G(t - n) \cdot \varepsilon_n + \sum_{n=0}^{t-1} \xi_n
     $$
   - \( G(t) = (t + 1)^{-\beta} \) is the **impact kernel**
   - \( \xi_n \) is a white noise process

3. **Memory Estimation in Prices**:
   - Repeat the procedure for different values of the kernel exponent:  
     \( \beta = 0.2,\ 0.25,\ 0.3 \)
   - Estimate the **Hurst exponent** of the resulting mid-point series using the **variogram** method in log-log scale
   - Observe how the value of β affects price persistence

---

## Outputs

- Autocorrelation function of the order sign process and fitted power law
- Mid-point price series for different kernel exponents
- Hurst exponent values for each case to assess memory and roughness of the price paths

---

## Requirements

Install the required packages using:

```bash
pip install numpy scipy matplotlib fbm
```

---

## Context

This notebook is part of a **Quantitative Trading course project** exploring how microstructural phenomena — such as long-memory in order flow and transient impact — can give rise to empirically observed market behaviors like price persistence or mean reversion.