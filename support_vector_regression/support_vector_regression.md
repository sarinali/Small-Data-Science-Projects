# Support Vector Regression

![img](https://i.ibb.co/y0Jy93g/Screenshot-2023-05-17-at-15-45-07.png)

The $\xi$ are the points of data outside of the tube, $\xi_i$ is above the tube, $\xi^*_i$ are below the tube. 

The line is modelled by the formula $y=wx+b$, $w$ is dependant, it is our slope coefficient and you want to use it to minimize the following formula:

$$\frac{1}{2}||w||^2+C\sum_{i=1}^{N}(\xi_i+\xi^*_i)$$

*There are other types of SVR as well*

## Feature Scaling

With other types of linear regression there are coefficients to balance out large values but since SVR doesn't have an explicit formula, you need to scale the features in order to make it make sense