# Optimization with Linear Regression, SVM, and COBYLA
This project demonstrates an optimization workflow involving multiple linear regression, polynomial regression using Support Vector Machines (SVM), and optimization techniques including Simplex and COBYLA.

Project Overview
The project is divided into the following steps:

Multiple Linear Regression:

Perform multiple linear regression on the provided data to obtain coefficients and construct the regression equation.
Simplex Method for Linear Optimization:

Use the Simplex method to maximize the linear objective function derived from the coefficients obtained in Step 1. The constraints are included in the optimization process.

SVM for Polynomial Regression:

Fit an SVM model with polynomial features to the data. This step also extracts the polynomial coefficients and intercept needed for further optimization.

COBYLA Optimization:

Utilize the COBYLA method to maximize the polynomial function derived from the SVM model. The bounds and constraints are included in this optimization step.

Counterexample Demonstrating COBYLA Failure with a Random Initial Guess:

This section demonstrates a scenario where the COBYLA optimization method fails to converge when starting from an arbitrary initial guess. However, COBYLA successfully converges when using the initial guess derived from the Simplex method solution.
Example Usage

The notebook includes code to demonstrate the usage of these functions with a sample CSV file. The process involves performing linear regression, optimizing with Simplex and COBYLA, and printing the polynomial equation.
Running the Code
To run the code, ensure you have the necessary dependencies installed:

pip install pandas statsmodels scikit-learn

Sample Workflow

Linear Regression:

coefficients, regression_equation = linear_regression_summary('data.csv')

print(regression_equation)

Simplex Optimization:

x1, x2, z = simplex_optimization(coefficients)

print(f"Optimal values - x1: {x1}, x2: {x2}, z: {z}")

SVM Polynomial Regression and COBYLA Optimization:

polynomial_equation = fit_svm_polynomial('data.csv')

print(polynomial_equation)

result = cobyla_maximization(coefficients, bounds, constraints)

print(result)
# Files in This Repository

Optimisation Project.ipynb: The main Jupyter notebook containing the implementation of the optimization process.
README.md: This file, providing an overview and instructions for the project.

#Additional Resources

This repository also includes the following files:

Hybrid-Price-Optimisation.pdf: A detailed document outlining the need for the project, its future scope, and a comprehensive description of the course. This file provides essential context and direction for the ongoing and future development of the project.
data.csv: A CSV file containing pseudo data for the objective function. This file is used in the optimization process and serves as a sample dataset for demonstrating the methods implemented in the project.
