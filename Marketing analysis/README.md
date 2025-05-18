# Marketing Campaign Analysis: Predicting Sales from Advertising Channels
## Overview
This project analyzes the relationship between various marketing campaign types—TV, radio, and social media—and revenue generated. The dataset includes campaign spending and sales performance, and our objective is to help company leadership allocate marketing resources more effectively.

## Dataset Overview
The data consists of 569 observations with five variables:

- TV (categorical: Low, Medium, High)
- Radio (continuous)
- Social Media (continuous)
- Influencer (categorical: Micro, Macro, Mega, Nano)
- Sales (continuous)

## Exploratory Analysis & Feature Selection

- **TV promotions** show a strong association with sales, with high-budget campaigns averaging over $300M in sales.
- **Radio spending** demonstrates a clear linear relationship with sales.
- **Social Media** spending appears correlated with Radio and was excluded due to multicollinearity (VIF ≈ 5).
- **Influencer** category showed minor variation across average sales, making it a weak predictor.

## Modeling Approach
We constructed a multiple linear regression model using TV (as a categorical variable) and Radio (continuous) as predictors:

ols_formula = 'Sales ~ C(TV) + Radio'

## Regression Results

- R² = 0.904, indicating the model explains 90.4% of the variation in sales.
- All predictors are statistically significant (p < 0.001).
- Residuals appear normally distributed and satisfy assumptions of linearity, homoscedasticity, and independence.

## Model Equation:

Sales = 218.53 − 154.30⋅TV (low) - 75.31⋅TV(medium) + 2.97⋅Radio

- **Baseline**: High TV promotions.
- **Interpretation**: A Low TV campaign is associated with $154.30M less in sales than a High TV campaign, holding Radio constant.
- Each additional unit in Radio spending corresponds to a $2.97M increase in sales (95% CI: [2.46, 3.31]).

## Model Diagnostics

- Residual plots and Q-Q plots support the assumptions of normality and constant variance.
- No multicollinearity was present in the final model (only one continuous predictor).
- The influence of TV spending dominates, causing discrete groupings in the fitted values.

## Conclusion
High TV advertising budgets and radio promotions are strong predictors of sales performance. This model can guide strategic decisions on media allocation, suggesting that cutting back on high-tier TV campaigns may significantly reduce revenue. Future enhancements could include interaction terms or nonlinear transformations and exploration of influencer performance within subgroups.
