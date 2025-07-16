# Twice-Exercisable Bermudan Put Option Pricing

This repository presents the pricing of a **twice-exercisable Bermudan put option** using various Monte Carlo techniques under a risk-neutral Geometric Brownian Motion (GBM) model. Developed as part of my MSc Quantitative Finance program at UCD Michael Smurfit Graduate Business School.

## 🧮 Objective

To value a Bermudan put option with early exercise allowed at:
- **T1 = 3/12 (0.25 years)**
- **T2 = 6/12 (0.5 years)**

The following pricing methods are implemented and compared:
- Standard Monte Carlo (MC)
- Conditional Monte Carlo (CMC)
- Least Squares Monte Carlo (LSMC)
- Binomial Tree (for benchmarking)

---

## 📌 Features

### ✅ Binomial Tree Pricing
- Provides a benchmark price.
- Price: **€10.49**

### ✅ Monte Carlo (MC) Simulation
- Simulates 10,000 paths.
- Uses GBM model to simulate asset price trajectories.
- Price: **€12.53**
- 95% Confidence Interval: [12.32, 12.74]
- Proportional Error: **3.35%**

### ✅ Conditional Monte Carlo (CMC)
- Improves on standard MC by conditioning on T1.
- Price: **€13.40**
- 95% Confidence Interval: [13.29, 13.51]
- Proportional Error: **1.60%**

### ✅ Least Squares Monte Carlo (LSMC)
- Implements Longstaff-Schwartz regression-based approach.
- Adapts to multiple exercise opportunities.
- Price: **€10.34**
- 95% Confidence Interval: [10.13, 10.55]
- Proportional Error: **2.01%**

---

## 📊 Results Summary

| Method         | Option Price (€) | 95% Confidence Interval     | Proportional Error |
|----------------|------------------|-----------------------------|--------------------|
| Binomial Tree  | 10.49            | –                           | –                  |
| Monte Carlo    | 12.53            | [12.32, 12.74]              | 3.35%              |
| Conditional MC | 13.40            | [13.29, 13.51]              | 1.60%              |
| LSMC           | 10.34            | [10.13, 10.55]              | 2.01%              |

---

## 🔍 Comparative Insights

- **CMC** yielded the highest price due to more accurate modeling of early exercise decision points.
- **LSMC** demonstrated greater flexibility, useful for multiple exercise dates.
- **Standard MC** is less precise but useful as a baseline.
- **Binomial Tree** remains a strong benchmark for discrete early exercise options.

---

## 📈 Visualizations

- Sample GBM paths showing exercise thresholds (T1 and T2)
- Bar chart comparing prices from MC, CMC, and LSMC

---

## 🛠️ Technologies Used

- **Python** (NumPy, Matplotlib)
- **Stochastic Simulations**
- **Polynomial Regression** (for LSMC)
- **Monte Carlo Frameworks** for option pricing

---


## 👨‍💻 Author

**Pranjal Kharbanda**  
MSc Quantitative Finance  
UCD Michael Smurfit Graduate Business School  


---

## 📎 Reference

Longstaff, F.A., & Schwartz, E.S. (2001). Valuing American Options by Simulation: A Simple Least-Squares Approach. *Review of Financial Studies*.
