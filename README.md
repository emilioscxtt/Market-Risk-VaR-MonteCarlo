# Market Risk Engine: VaR & Monte Carlo Simulation 📉

![Python](https://img.shields.io/badge/Python-3.9%2B-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Status](https://img.shields.io/badge/Status-Active-success)

## 📌 Project Overview
This repository hosts a robust **Market Risk Engine** designed to quantify the potential loss of an equity portfolio under extreme market conditions. The model calculates **Value at Risk (VaR)** and **Expected Shortfall (CVaR)** using three industry-standard methodologies, applied specifically to Mexican Stock Exchange (BMV) assets (e.g., CEMEX, WALMEX, GFNORTE).

The core implementation focuses on overcoming the limitations of Normal Distribution assumptions by introducing **Heavy-Tailed simulations** via Monte Carlo methods.

## 🛠️ Methodologies Implemented
1.  **Parametric VaR (Variance-Covariance):** Assumes normality (Gaussian) of returns.
2.  **Historical Simulation:** Non-parametric approach using empirical data distributions.
3.  **Monte Carlo Simulation (Brownian Motion):**
    * Generates 10,000+ stochastic price paths.
    * Models drift and volatility based on historical parameters.
    * *Key Feature:* Stress testing for "Black Swan" events.

## 💻 Tech Stack & Libraries
* **Core:** `Python`, `NumPy`, `Pandas`
* **Statistical Modeling:** `SciPy.stats` (Norm, T-Student distributions)
* **Data Acquisition:** `yfinance` (Real-time market data)
* **Visualization:** `Matplotlib`, `Seaborn`

## 📊 Key Results (Example)
> *Comparing 1-Day 95% VaR for a generic BMV Portfolio:*

| Method | Estimated Max Loss (VaR) | Accuracy (Backtest) |
| :--- | :--- | :--- |
| **Parametric** | $12,450 MXN | Underestimates Risk ⚠️ |
| **Historical** | $14,200 MXN | Robust |
| **Monte Carlo** | **$14,850 MXN** | **Most Conservative & Realistic** |

## 🚀 How to Run
```bash
# Clone the repository
git clone [https://github.com/emilioscxtt/Market-Risk-VaR-MonteCarlo.git](https://github.com/emilioscxtt/Market-Risk-VaR-MonteCarlo.git)

# Install dependencies
pip install -r requirements.txt

# Run the analysis notebook
jupyter notebook notebooks/01_Risk_Analysis.ipynb
