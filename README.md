# Marketing ROI: Evaluating Simple Linear Regression Analysis

## 📌 Project Overview

This repository contains a data analytics project that models and evaluates the relationship between marketing campaign budgets and revenue. Working as part of an analytics team, the primary objective is to investigate the directional impact and magnitude of different Promotion methods on cross-company Sales revenue.

Using an exploratory data analysis (EDA) and ordinary least squares (OLS) regression framework, this project provides data-driven insights to help company executives strategically allocate future marketing resources across TV, radio, and social media.

---

## 📉 Core Objective & Modeling Framework

* **Business Problem:** Determine if increasing investment in any of the advertising methods yields a statistically significant increase in sales, and quantify that return.
* **Dependent Variable (Y):** `Sales` (expressed in millions of dollars)
* **Independent Variable (X):** `TV Budget` (expressed in millions of dollars) - The one variable that has the strongest positive linear relationship with Sales.

---

## 📐 Regression Assumptions Evaluated

Before finalizing predictions, the model verifies the core OLS linear regression assumptions:
* **Linearity:** Linear relationship between the independent and dependent variables (assessed via scatter plot).
* **Independence:** Observations are independent of one another.
* **Homoscedasticity:** Residuals maintain constant variance across all levels of the independent variable.
* **Normality:** Residuals are normally distributed (assessed via histogram and Q-Q plot).

---

## 🛠️ Tech Stack & Libraries

* **Python 3**
* **Pandas:** Data loading, inspection, and missing value cleanup.
* **Matplotlib & Seaborn:** Exploratory scatter plots, residual distribution plotting, and trend line visualization.
* **Statsmodels:** Fitting the OLS simple linear regression model and extracting detailed summary coefficients.

---

## 📊 Methodology & Analytical Steps

### 1. Data Cleaning & Exploration
The initial fictional dataset (`marketing_sales_data.csv`) contains promotional information across media streams. Missing rows were isolated and handled using `.isna()` structures to ensure data consistency. Descriptive analytics and scatter plots were used during EDA to verify a strong, positive monotone relationship between TV spending and revenue.

### 2. Model Estimation (OLS)
The regression model was constructed using the formula interface:

OLS_model = ols(formula="Sales ~ TV", data=data)
model_results = OLS_model.fit()

## 📈 Key Findings & Statistical Results

The Ordinary Least Squares (OLS) regression model yielded definitive metrics regarding the impact of TV advertising on commercial revenue:

* **Statistical Significance:** The relationship between the TV promotion budget and sales is highly statistically significant, underscored by an exceptional p-value of **0.000**.
* **Model Precision:** The model demonstrated exceptionally high fit, estimating that **99.9% of the variation in sales** is explained by the TV promotional budget alone. The slope coefficient has a tight 95% confidence interval of `[3.558, 3.565]`.
* **Y-Intercept ($\beta_0$):** Baseline constant calculated from data.
* **Slope/TV Coefficient ($\beta_1$):** `3.5614`

### 📝 Mathematical Equation
$$\text{Sales (in Millions)} = \beta_0 + 3.5614 \times \text{TV Budget (in Millions)}$$

### 💡 Interpretation of Coefficients
* **Baseline Sales ($\beta_0$):** Represent the estimated average sales when the TV promotional budget is set to \$0.
* **Marginal Return ($\beta_1$):** For every \$1 million increase in the TV promotional budget, sales revenue is expected to increase by an average of **\$3.5614 million**.

---

## 🎯 Strategic Business Recommendations

Based on the statistical strength of the OLS model, the following insights are presented to stakeholders and company leadership to guide future marketing resource allocation:

1. **Prioritize TV Campaigns:** Among TV, social media, and radio, TV had the strongest positive linear relationship with sales. Because nearly all variation in sales is explained by this single channel, TV is an excellent and highly confident predictor of commercial growth.
2. **Targeted Budget Decisions:** If company leaders seek to accurately scale revenue, they can safely propose a budget expansion for TV promotions, expecting an estimated return of **\$3.5614 million more dollars** in sales for every additional million invested.
3. **Data-Driven Resource Optimization:** Executive teams should utilize the derived linear formula to forecast returns and prioritize TV expenditures above other channels with weaker or less certain linear fits.
