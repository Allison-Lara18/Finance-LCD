# Cost of Equity Analysis Project

## Overview

This repository contains the final project for the course **Introduction to Business and Finance** (Semester 2025-1) at Universidad Nacional Autónoma de México (UNAM, IIMAS). The project investigates the key determinants of the **Cost of Equity (CoE)** for a sample of 32 companies, using both linear and non-linear modeling approaches to assess relationships between CoE and a set of financial and operational indicators.

## Authors

* Jaime Rodrigo Lagunas Parra
* Allison Lara Nieva
* Diana Laura Salgado Tirado

## Methodology

The analysis is organized in two complementary approaches:

1. **Linear Approach**

   * Visualize pairwise relationships between CoE and each predictor via scatter plots.
   * Compute **Pearson correlation coefficients** to quantify linear associations.
   * Fit an **Ordinary Least Squares (OLS)** regression model:
     $$
       y = \beta_0 + \sum_{i=1}^p \beta_i X_i + \varepsilon
     $$
   * Evaluate model performance using R², adjusted R², and relative RMSE.
   * Identify statistically significant predictors based on p-values.

2. **Non-Linear Approach**

   * Train a **Random Forest Regressor** with Mean Squared Error (MSE) criterion.
   * Compute **feature importances** by aggregating variance reduction across splits.
   * Validate importances via permutation tests and bootstrap confidence intervals.
   * Compare predictive performance (RMSE, relative RMSE) against linear model.


## Key Results

* **Linear Model** explains \~52.8% of CoE variability (adjusted R² = 0.502), with significant predictors: leverage (Lev), book-to-market ratio (Ln B/M), return on assets (ROA), and income volatility (OIStd).
* **Random Forest** achieves a lower relative RMSE (21.69% vs 49%), highlighting non-linear patterns and confirming the prominence of Ln B/M and Lev, as well as additional influence from operational income stability.


