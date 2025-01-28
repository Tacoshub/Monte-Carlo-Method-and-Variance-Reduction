# Option Pricing Models and Simulations

This repository provides Python implementations of various financial models for option pricing and simulations of stochastic processes. The models include classic Black-Scholes pricing, Monte Carlo simulations, and exotic options such as Asian and Barrier options. The repository is designed to demonstrate the flexibility and power of numerical methods in option pricing.

## Features

### Implemented Models:
- **Brownian Motion**:
  - Simulates standard Brownian motion paths.
  - Visualization of paths.

- **Geometric Brownian Motion**:
  - Simulates paths for assets following a Geometric Brownian Motion process.
  - Visualization of stock price dynamics.

- **European Options**:
  - Black-Scholes closed-form solution for pricing, Delta, Gamma, and Vega.
  - Monte Carlo pricing with:
    - Antithetic variates.
    - Importance sampling.
    - Put-call parity.
  - Greeks computation methods:
    - Bump method for Delta and Gamma.
    - Pathwise method for Delta.
    - Likelihood ratio method for Delta and Gamma.
    - Hybrid methods combining Pathwise and Likelihood for Gamma.

- **Asian Options**:
  - Pricing using Monte Carlo methods with various integration techniques:
    - Riemann Sum.
    - Trapezoidal Rule.
    - Simpson’s Rule.

- **Barrier Options**:
  - Pricing up-and-out barrier options using Monte Carlo methods.

## Classes and Methods

### 1. `Brownian_Motion`
- Simulates standard Brownian motion paths.
- Methods:
  - `Brownian_Path()`: Simulates paths.
  - `Plot_Path()`: Visualizes paths.

### 2. `Geometric_Brownian_Motion`
- Simulates stock price dynamics using Geometric Brownian Motion.
- Methods:
  - `Geometric_Brownian_Path()`: Simulates paths.
  - `Plot_Path()`: Visualizes paths.

### 3. `European_Option`
- Prices European call and put options.
- Monte Carlo methods include:
  - `Monte_Carlo_Price()`: Standard Monte Carlo pricing.
  - `Antithetic_Monte_Carlo_Price()`: Variance reduction using antithetic variates.
  - `Importance_Sampling_Monte_Carlo_Price()`: Variance reduction using importance sampling.
  - `Put_Call_Parity_Price()`: Pricing using put-call parity.
- Greeks computation:
  - **Delta**:
    - `Black_Sholes_Delta()`: Closed-form Delta.
    - `Bump_Delta()`: Delta using finite-difference (bump) method.
    - `Pathwise_Delta()`: Delta using the pathwise method.
    - `Likelihood_Delta()`: Delta using the likelihood ratio method.
  - **Gamma**:
    - `Black_Sholes_Gamma()`: Closed-form Gamma.
    - `Bump_Gamma()`: Gamma using finite-difference (bump) method.
    - `Likelihood_Gamma()`: Gamma using the likelihood ratio method.
    - `Pathwise_Likelihood_Gamma()`: Hybrid method combining pathwise and likelihood for Gamma.
    - `Likelihood_Pathwise_Gamma()`: Alternative hybrid method for Gamma.

### 4. `Asian_Option`
- Prices Asian options using Monte Carlo simulations.
- Supports Riemann, Trapezoidal, and Simpson integration methods.
- Method:
  - `Monte_Carlo_Price()`: Calculates price with integration methods for averaging.

### 5. `Barrier_Option`
- Prices barrier options using Monte Carlo simulations.
- Simulates up-and-out barrier conditions.
- Method:
  - `Monte_Carlo_Price()`: Determines the payoff considering the barrier.

## Contact

For questions or suggestions, please contact **Ludovico Costa** at ludocosta2002@gmail.com.
