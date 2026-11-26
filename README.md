# Bank Customer Churn Analysis

Statistical analysis of customer churn in a public bank customer dataset (10,000 customers), using exploratory analysis and logistic regression.

## Question
Which customer characteristics are associated with churn, and how large are the differences between segments?

## Data
Public bank customer churn dataset (`Churn_Modelling.csv`). Target variable: `exited` (1 = churned). Overall churn rate: about 20.4%.

## Methods
- Data cleaning and EDA (churn rates by segment, pairplot, correlation heatmap)
- Multicollinearity check (VIF)
- Logistic regression (`statsmodels`) with a quadratic age term and grouped number of products
- Interpretation with odds ratios and average marginal effects (AME)

## Key findings
- Churn is highest among customers aged 51-60, and the fitted age effect peaks at about 59 years
- Churn is non-monotonic in the number of products (lowest for 2 products, very high for 3 or more)
- Higher churn is associated with being in Germany (vs France) and with inactive membership
- Tenure, estimated salary and credit card ownership show no sufficient evidence of an association

## Limitations
Cross-sectional public data, associations only. The model was not evaluated on out-of-sample predictive performance. Recommended actions are hypotheses to be validated.