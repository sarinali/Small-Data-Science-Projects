# Multiple Linear Regression

Let $\hat{y}$ be the dependant variable (what you want to predict)
Let $b_0$ be the y-intercept
Let $b_1, b_2, b_3... b_n$ be the coefficients for each of the independant variables

The equation is:

$$\hat{y} = b_0 + b_1X_1 + b_2X_2 + ... +b_nX_n$$

## Assumptions of Linear Regression

1. Linearity: There should be a linear relationship between x and y
2. Homoscedasticity: There should not be a cone shape 
3. Multivaraite Normality: Normality of error distribution (there shouldn't be many data points away from the line or clustered in one place)
4. Independence: Don't want to see patterns in the data 
5. Lack of Multicollinearity: when predictors do not have a relationship

## Creating Dummy Variables

| State |
| --- | 
| California |
| New York | 

becomes 

| New York | California |
| --- | ----------- |
| 1 | 0 |
| 0 | 1 |

Since you cannot quantify "California" or "New York" as part of your mulitple linear regression formula

You should only include the coefficient for one dummy variable in your mutiple linear regression equation because it will affect the model, cannot have $b_0, b_{dummy1}$ and $b_{dummy2}$ at the same time in our case. 

So, if there are 2 dummy variables, include 1 if there are 99 dummy variables include 98 etc.

## P Values

Suppose the following:

$H_0$: a universe where flipping a coin is fair 
$H_1$: a universe where flipping a coin is unfair

We can assume the null hypothesis ($H_0$) and then try to disprove it with statistical signifigance when we see that the outcome heavily favours $H_1$ at $\alpha=0.05$ or when the outcome of something is $5\%$ which is highly unlikely

## Steps of Building a Model

1. All-in
2. Backward Elimination
3. Forward Selection
4. Bidirectional Elimination
5. Score Comparison

### All in

- Prior knowledge 
- You have to use all the varaibles
- Preparing for backward elimination

### Backward Elimination

**Step 1**: select a significance level in the model (e.g $\alpha = 0.05$) 
**Step 2**: Fit the full model with all possible predictors
**Step 3**: Take the predictor with the highest P-value and if P>$\alpha$ then 
**Step 4**: Remove the variable and refit the model, repeat step 3 until all variables P<=$\alpha$

### Forward Selection

**Step 1**: select a significance level in the model (e.g $\alpha = 0.05$) 
**Step 2**: Fit the model with that variable, pick the one with the lowest P value
**Step 3**: Pick the next variable with the lowest P value and refit
**Step 4**: If the predictor P value is greater than $\alpha$ then stop

### Bidirectional Elimination

**Step 1**: select a significance level for entering and staying the model $\alpha_1$ and $\alpha_2$
**Step 2**: Perform steps of Forward Selection (new variables must have P < $\alpha_1$ to be added)
**Step 3**: Perform steps of Backward Elimination (old variables must have P < $\alpha_2$ to stay)
**Step 4**: Once nothing can be added or eliminated, the model is ready

### All Possible Models

All possible regression models: $2^n-1$, select the one with best criterion