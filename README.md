# Financial Engineering Projects

This repository gathers a collection of academic and applied projects in quantitative finance, developed as part of a Master's program in Financial Engineering. The repository is structured into three major folders, each representing a distinct area of financial modeling or machine learning application.

---

## 1. Machine Learning

This project uses deep learning to estimate the price of arithmetic Asian call options, using synthetic datasets generated from Monte Carlo simulations under a log-normal price dynamic. The model is trained to approximate option prices using different market conditions.

**Contents:**
- `ML_Project.ipynb`: Main notebook for training the neural network.
- `checkpoint_i.csv`, `data_checkpoint_i.csv` (i = 0 to 9): Precomputed datasets and results to avoid repeating long simulations.
- `reg_10/`: Saved TensorFlow model, training history, and weights for reuse and evaluation.

---

## 2. Quantitative Trading

This section contains two notebooks that focus on the microstructure of financial markets. It explores how market orders propagate in the limit order book and analyzes price impacts based on order flow imbalance and execution strategies.

**Contents:**
- `Limit_Order_Study.ipynb`: Empirical study on how limit orders behave in the order book.
- `Propagation_Model_Mid_Point_Series.ipynb`: Simulation and modeling of mid-point price changes in response to market orders.

---

## 3. Empirical Methods in Finance

This project focuses on asset pricing, portfolio construction, and performance attribution. It applies econometric techniques to study real financial datasets, including factor regressions and portfolio optimization.

**Contents:**
- `final.ipynb`: The main notebook with the full analysis.
- `100_Portfolios_10x10_Daily.csv`: Daily returns of portfolios sorted on size and book-to-market.
- `funds.csv`: Dataset of mutual fund returns used in the empirical analysis.

---

## Tools & Libraries

All projects are implemented in Python using:
- `NumPy`, `Pandas`, `Matplotlib`
- `SciPy`, `Scikit-learn`, `TensorFlow` (for ML)
- `Tqdm`, `Seaborn`, `Statsmodels` (as needed)

---

## Notes

- The repository is structured for clarity and reproducibility.
- Precomputed datasets are included to reduce computational time.
- For each sub-project, more detailed documentation is included in their respective subfolders.

---

## Author

Paul Pébereau  
