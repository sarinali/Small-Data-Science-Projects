# Simple Linear Regression

##Equation

Let $\hat{y}$ be the dependant variable, what we are trying to predict.
Let $b_0$ be the y-intercept.
Let $b_1$ be the slope coefficient.
Let $X_1$ be the independant variable, what we use to predict.

$$\hat{y} = b_0+b_1X_1$$

## Example Scenario

Suppose we are trying to predict number of potatoes on a farm by the amount of fertiliser we use in kgs. 

Let $t$ be tonnes, let $kg$ be kilograms.

$$Potatoes[t] = b_0 + b_1(Fertiliser[kg])$$

![img](https://i.ibb.co/CVfvYrx/Screenshot-2023-05-14-at-08-48-43.png)

Let the x axis be tonnes of fertiliser and y axis be the amount of potatoes in tonnes. This line is a prediction made from a series of many different points.

## Ordinary Least Squares

![img1](https://i.ibb.co/ZhZt6mz/Screenshot-2023-05-14-at-09-03-43.png)

Let $v$ be the set of points 

You want to minimize the following to decide on the line:

$$\sum_{i=0}^{n\in v} (y_i-\hat{y})^2$$

