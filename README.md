# Linear Regression 🤖🤩

## Univariate Linear Regression

**Applications**
— Heart rate vs life expectancy
— running time vs cholesterol
— GDP vs Happiness rate

**Hypothesis h(x)**
h(x) = θ0 + θ1x     (or)  θTx
θ0 — Intercept Parameter
θ1— Cost function of x

**Compute Cost:**

J = (1 / (2*m) ) * sum(((X * theta)-y).^2)
 Gradient descend 
Gradient descend algorithm’s job is to find the right parameter theta0 and theta1 which causes the very less J (compute cost) , in other words, global minimum optima.
Update rule as follows,
for iter = 1:num_iters
     error = (X * theta) - y; 
    temp0 = theta(1) - ( alpha /m ) * sum(error.* X(:,1));
    temp1 = theta(2) - ( alpha /m ) * sum(error.* X(:,2));
    theta = [temp0; temp1];
End

## Multivariate Linear Regression

 **Hypothesis h(x)**
 h(x) = θ0 + θ1x + θ2x + θ3x +………. θnx

Everything is more or less similar , but we will need to modify the update rule for adding few parameters based on number of the feature( x1,x2,x3..).

**Feature Normalisation**
It is a technique to make all the features in to similar magnitude to make the gradient descend more efficient . Few technique below
Feature value / max value 
Feature value - mean of all feature / max value
Feature value - mean of all feature / std.dev

**How to make sure gradient descend working fine?**

We can plot J(θ) and number of iteration , if J(θ) reduces significantly for each iteration then it’s a positive signal that it’s covering as expected.
If gradient descent not working then we may need to use smaller learning rate 𝛼 to avoid the overshooting .
 𝛼 should be much smaller if iteration we using is huge number.







  
