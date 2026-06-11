# Linear Regression From Scratch

This project implements Linear Regression from scratch using NumPy and basic linear algebra concepts.

The notebook covers both:

- Simple Linear Regression
- Multiple Linear Regression

The implementation includes:

- Prediction
- Mean Squared Error (MSE) cost function
- Gradient computation
- Gradient Descent optimization
- Newton's Method optimization
- Normal Equation solution
- Model evaluation using the coefficient of determination ($R^2$)

## Linear Model

Simple Linear Regression:

$$
\hat{y} = \beta_0 + \beta_1 x
$$

Multiple Linear Regression:

$$
\hat{y} = X\beta
$$

## Cost Function

The model parameters are estimated by minimizing the Mean Squared Error:

$$
J(\beta)=\frac{1}{2n}\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
$$

## Normal Equation

The closed-form solution is given by:

$$
\beta=(X^TX)^{-1}X^Ty
$$

## Model Evaluation

The coefficient of determination is used to evaluate performance:

$$
R^2 =
1 -
\frac{\sum (y_i-\hat{y}_i)^2}
{\sum (y_i-\bar{y})^2}
$$

## Validation

Synthetic datasets are generated to test the implementation.

The results are compared with scikit-learn's `LinearRegression` model to verify correctness.

## Technologies

- Python
- NumPy
- Matplotlib
- scikit-learn (for validation only)