# README 

## Overview
This project provides solutions to mathematical and programming exercises related to the Beta distribution and Monte Carlo simulation using R. The main topics covered include:

1. **Beta Distribution:**
   - Finding the constant \( c \) for a Beta distribution.
   - Calculating probabilities for given intervals.
   - Computing the expected value and variance.

2. **Simulation of Continuous Random Variables:**
   - Implementing a custom probability density function (PDF).
   - Calculating probabilities using simulation techniques.
   - Exploring the impact of sample size on simulation accuracy.

## Structure
### Sections

1. **Mathematical Derivations:**
   - Derivations for the Beta distribution constant \( c \) using the Beta and Gamma functions.
   - Formulas for probability, expectation, and variance.

2. **R Code Implementation:**
   - Functions to compute constants, probabilities, expectations, and variances.
   - Simulations to approximate integrals and probabilities.

3. **Monte Carlo Simulations:**
   - Custom function implementation for approximating integrals using random points.
   - Visualizations to demonstrate the accuracy of simulations.

### Key Functions
- **Beta Distribution:**
  - `constant_with_BETA(a, b)`: Calculates \( c \) using the Beta function.
  - `constant_with_GAMMA(a, b)`: Calculates \( c \) using the Gamma function.
  - `Expected_value_X(a, b)`: Computes the expectation \( E(X) \).
  - `var_X(a, b)`: Computes the variance \( \text{Var}(X) \).

- **Simulation:**
  - `FIND_MAXIMUN(fun, a, b, n)`: Finds the maximum value of a function over an interval.
  - `RANDOM_POINTS(fun, a, b, n, visualice)`: Implements Monte Carlo simulation for approximating integrals.
  - `EXPERIMENT(n, N, delta, integral, fun, a, b)`: Plots the error vs. number of points in the simulation.

### Example PDF
The example PDF used in the Monte Carlo simulation is defined as:
\[ f(x) = \frac{\sqrt{x}}{21.08185} \]
Its support is between \([0, 10]\), and it is normalized to ensure it is a valid PDF.

### Validity Checks
- Ensuring the PDF integrates to 1 over its support.
- Verifying non-negativity of the PDF.

## Instructions
### Prerequisites
- Install R and the required packages (`dplyr`).
- Ensure the LaTeX engine `xelatex` is available for rendering the PDF output.

### Execution
1. Open the `.Rmd` file in RStudio.
2. Render the file to generate a PDF document.
3. Run the R code chunks to:
   - Verify calculations for the Beta distribution.
   - Perform simulations and visualize results.
   - Validate the accuracy of the Monte Carlo method.

### Key Outputs
- Mathematical derivations and explanations.
- Visualizations of the PDF and random points within the function's domain.
- Error analysis for Monte Carlo simulation.

## Results and Observations
1. **Beta Distribution Calculations:**
   - The constants \( c \), expectation, and variance were calculated and verified.
   - Probabilities were computed using numerical integration.

2. **Simulation Accuracy:**
   - Increasing the number of random points improves the accuracy of the simulation.
   - Error analysis shows diminishing errors as the sample size increases.

3. **PDF Validity:**
   - The custom PDF \( f(x) \) is valid as it integrates to 1 over its support and remains non-negative.

## Notes
- The project demonstrates the application of R for statistical computations and simulations.
- Monte Carlo simulations are computationally intensive but highly effective for approximating probabilities and integrals for continuous random variables.

