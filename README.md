# Linear-Regression Study Notes
x - training dataset
y - target dataset
m - number of training same
theta's - parameter of model

hypothesis : h(x) = thet0 * x0 + theta1 * x1 

Compute cost:
J = (1 / (2*m) ) * sum(((X * theta)-y).^2)

Gradient Descend Algorithm:
J_history = zeros(num_iters, 1);

for iter = 1:num_iters
     error = (X * theta) - y; 
    temp0 = theta(1) - ( alpha /m ) * sum(error.* X(:,1));
    temp1 = theta(2) - ( alpha /m ) * sum(error.* X(:,2));
    theta = [temp0; temp1];
    
   J_history(iter) = computeCost(X, y, theta);

end

linear fit --> plot( x , x *(theta) )
