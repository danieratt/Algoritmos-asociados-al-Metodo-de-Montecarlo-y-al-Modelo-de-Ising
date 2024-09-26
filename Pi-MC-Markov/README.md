# Pi Approximation using Monte Carlo and Markov Chains

## Description

This repository contains a Python implementation for approximating the value of \(\pi\) using two algorithms:
- **direct-pi**: A direct Monte Carlo method 
- **markov-pi**: A Markov Chain Monte Carlo (MCMC) method 



### a) Monte Carlo Simulation: `direct-pi`
Using the **direct-pi** algorithm, we approximate \(\pi\) by simulating random points inside a unit square and counting the fraction of points that lie inside the unit circle. This is done for increasing values of \(N\), the number of random trials. The code estimates the Mean Squared Error (MSE) between the computed fraction \(N_{\text{hits}}/N\) and \(\pi/4\), and plots how the MSE scales with \(N\).

### b) Markov Chain Monte Carlo: `markov-pi`
Using the **markov-pi** algorithm, we start at a point \((x_0, y_0) = (1,1)\) and generate new points within a step size \(\delta = 0.3\). The fraction of points that land inside the unit circle is calculated, and its convergence to \(\pi/4\) is analyzed. We also investigate how the MSE and the rejection rate depend on the choice of \(\delta\). A range of \(\delta\) values is used to study the effect on precision and rejection rate.

## Files

- `Pi-MC-Markov.ipynb`: Jupyter notebook containing the Python implementation of the two algorithms: **direct-pi** and **markov-pi**.
- `README.md`: This file, explaining the purpose and functionality of the notebook.

## Problem Description

### a) Direct Monte Carlo Approximation
- Run the **direct-pi** algorithm with \(N = 10, 100, \dots, 10^8\), repeating each experiment 20 times.
- Compute and plot the Mean Squared Error (MSE) between the computed fraction \(N_{\text{hits}} / N\) and \(\pi / 4\).
- Analyze how the MSE scales with \(N\).

### b) Markov Chain Monte Carlo Approximation
- Implement and run the **markov-pi** algorithm with an initial point \((x_0, y_0) = (1,1)\) and step size \(\delta = 0.3\).
- Show that \(N_{\text{hits}} / N\) converges to \(\pi / 4\).
- Investigate how precision depends on \(\delta\), verifying the "one-half" rule.
- Graph the rejection rate as a function of \(\delta\) in the range \([0, 0.3]\).
- Identify which values of the rejection rate yield the highest precision.

## Requirements

The following Python libraries are required to run the notebook:
- `numpy`
- `matplotlib`

### Running the Notebook

1. Clone the repository or download the notebook.
2. Install the dependencies listed above.
3. Open the notebook `Pi-MC-Markov.ipynb` using Jupyter Notebook or JupyterLab.
4. Run the cells to reproduce the results and plots for both the `direct-pi` and `markov-pi` methods.

### Output

- **Direct-pi method**: The MSE as a function of \(N\), showing the scaling of the error.
- **Markov-pi method**:
  - Convergence of \(N_{\text{hits}} / N\) to \(\pi / 4\) as a function of the number of iterations.
  - The MSE as a function of \(\delta\), demonstrating the rule of "one-half".
  - The rejection rate as a function of \(\delta\), with an analysis of how it affects the precision.

