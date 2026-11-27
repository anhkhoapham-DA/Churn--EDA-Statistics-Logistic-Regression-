# Bank Customer Churn Analysis

Statistical analysis of customer churn in a public bank dataset (10,000 customers), using EDA and logistic regression.

## Question
Which customer characteristics are associated with churn, and how large are the differences between segments?

## Data
- Source: public `Churn_Modelling.csv`
- Target: `exited` (1 = churned); overall churn rate ≈ 20.4%
- Public dataset; may not reflect a real bank

## Methods
- Cleaning and EDA: churn rates by segment, pairplot, correlation heatmap
- Multicollinearity check (VIF)
- Logistic regression (`statsmodels`) with quadratic age and grouped number of products
- Interpretation with odds ratios (95% CI) and average marginal effects (AME)

## Key findings
- Age (non-monotonic): churn is 56.2% in the 51–60 group vs 24.8% in 61+; fitted peak ≈ 59 years
- Products (non-monotonic): 2 products show the lowest churn (7.6%); 3+ products show very high churn (small group, n = 326, less stable estimates)
- Germany vs France: OR ≈ 2.64 (95% CI 2.28–3.07), AME ≈ +12 percentage points
- Active vs inactive members: AME ≈ −11 percentage points
- Tenure, estimated salary and credit card ownership: no sufficient evidence of association

## Repository structure
- `churn_eda_statistics_logistic_regression.ipynb`: full analysis
- `dataset/`: place `Churn_Modelling.csv` here
- `requirements.txt`: pandas, numpy, matplotlib, seaborn, scipy, statsmodels

## Limitations
Cross-sectional data, associations only. No out-of-sample evaluation of predictive performance. Recommended actions are hypotheses to be validated.
