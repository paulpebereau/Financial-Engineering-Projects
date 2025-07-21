# Limit Order Cost Study — Quantitative Trading Project

This notebook investigates the **cost and effectiveness of a buy limit order** using a simple price model based on **random walks**. It simulates asset price paths and computes the probability of execution, the conditional expectation of final price, and the total cost associated with placing a limit order instead of a market order.

---

## Objective

To model and quantify the **cost of a limit order** by studying:

- The probability that the limit order is executed
- The expected final price of the asset given that the limit order is **not** executed
- The **expected cost** of using a limit order instead of executing at the initial price

---

## Methodology

1. **Price Simulation**:
   - Simulate thousands of random walk trajectories to model asset price evolution.
   - Each walk starts at 0 and moves ±1 at each step to approximate symmetric price movements.

2. **Limit Order Execution Analysis**:
   - A buy limit order is placed at a **negative threshold** (e.g. -10).
   - For each simulated path, determine whether the threshold was ever reached (i.e. whether the order would be executed).

3. **Expected Final Price**:
   - For all paths where the limit order is **not executed**, compute the average final price — this is what the trader would pay if the order failed and the asset was bought at the end.

4. **Cost Calculation**:
   - Use the **law of total expectation** to compute the expected price paid when using a limit order.
   - Compare this to a direct purchase at the initial price (which is 0) to measure the **cost** or **savings**.

5. **Parameter Sensitivity**:
   - Analyze how execution probability, expected final price, and order cost vary with the threshold level.

---

## Outputs

- Plot of multiple simulated price paths
- Execution probability vs. threshold
- Expected price (given no execution) vs. threshold
- Expected cost of using a limit order vs. threshold

---

## Requirements

Install the required libraries via pip:

```bash
pip install numpy matplotlib
```

---

## Context

This analysis forms part of a **Quantitative Trading course project**, focused on understanding market microstructure mechanics, order placement strategies, and trade-offs between execution certainty and price improvement.