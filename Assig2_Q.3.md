
    
Sklearn's LinearRegression class by default uses the Ordinary Least Squares (OLS) method for solving
linear regression problems. The OLS method estimates the parameters in a linear regression model by minimizing the 
sum of the squared differences between the observed and predicted values(mean squared error). This method is mathematically
robust and efficient for solving linear regression, even in the presence of multicollinearity.

The formula for computing theta is:

theta=np.linalg.inv(X.T @ X) @X.T @ y

Where:

theta is the vector of coefficients

X is the design matrix (features)

y is the vector of target values

This formula involves the matrix inversion of X.T @ X.In the presence of multicollinearity, where two or more features are
highly correlated, X.T @ X becomes nearly singular (having determinant close to zero), leading to numerical instability when 
computing the inverse. This is what happened in the initial part of the provided code when attempting to directly invert the 
matrix  X.T @ X resulting in a singular matrix error.

However, Sklearn's implementation is robust against this issue. Instead of directly computing the matrix inverse,Sklearn uses 
more numerically stable methods to solve the least squares problem. Sklearn internally handles the computation of X.T @ X
using efficient numerical methods such as  Singular Value Decomposition (SVD).By avoiding explicit matrix inversion,It can
handle multicollinearity gracefully, ensuring stable and reliable results even in the presence of highly correlated features.
These methods are numerically stable and can handle multicollinearity well.
    
    
Also,Sklearn provides regularization options like Ridge Regression (L2 regularization) and Lasso Regression 
(L1 regularization), which can further enhance the robustness of the linear regression model by penalizing large 
coefficients and reducing overfitting, especially in scenarios with multicollinearity. These regularization techniques 
help in stabilizing the coefficients and improving the generalization performance of the model.

Overall, scikit-learn's LinearRegression class is able to solve linear regression problems effectively and efficiently 
by leveraging a combination of mathematical algorithms, optimization techniques, and robustness checks.



