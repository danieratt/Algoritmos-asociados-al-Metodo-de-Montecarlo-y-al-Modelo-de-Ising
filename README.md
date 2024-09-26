# Ising Model and Pi Approximation: Monte Carlo and Markov Chain Methods

## Overview

This repository contains a collection of Python implementations for solving problems related to the **2D Ising model** and the **approximation of \(\pi\)** using Monte Carlo and Markov Chain Monte Carlo methods. These implementations apply well-known algorithms to study statistical mechanics and phase transitions, as well as numerical techniques for approximating \(\pi\). Each problem includes detailed analysis and visualizations to better understand the underlying physics and computational methods.

## Problems

### 1. **Monte Carlo and Markov Chain Methods for Pi Approximation**

- **Algorithms**: Direct Monte Carlo simulation (`direct-pi`) and Markov Chain Monte Carlo (`markov-pi`).
- **Description**: 
  - The `direct-pi` algorithm uses random sampling to estimate the value of \(\pi\), with calculations of the mean squared error (MSE) for increasing numbers of trials.
  - The `markov-pi` algorithm applies a Markov Chain process to sample points from within the unit circle, analyzing the precision of the estimation as a function of step size (\(\delta\)).
- **Key Outputs**: MSE plots, rejection rate analysis, and convergence to \(\pi/4\).

### 2. **Gray-Flip and Enumerate-Ising for Spin Configuration Analysis**

- **Algorithms**: `gray-flip` for spin configuration enumeration and `enumerate-ising` for energy and magnetization distribution.
- **Description**:
  - The `gray-flip` algorithm efficiently enumerates all possible spin configurations in the 2D Ising model for small lattice sizes (\(2 \times 2\) and \(4 \times 4\)).
  - The energy and magnetization distributions are computed and visualized, along with Binder cumulant analysis for identifying phase transitions.
- **Key Outputs**: Histograms of energy and magnetization, Binder cumulant plots, and phase transition identification.

### 3. **Markov-Ising: Metropolis Algorithm for the Ising Model**

- **Algorithm**: Markov Chain Monte Carlo using the Metropolis algorithm (`markov-ising`).
- **Description**:
  - The `markov-ising` algorithm simulates the 2D Ising model on square lattices with periodic boundary conditions, calculating thermodynamic properties such as energy, specific heat, and magnetization as a function of temperature.
  - Comparisons are made with known exact results for validation.
- **Key Outputs**: Energy and specific heat plots, magnetization vs. temperature, and phase transition analysis.

### 4. **Cluster-Ising: Wolff Algorithm for the Ising Model**

- **Algorithm**: Wolff cluster algorithm (`cluster-ising`).
- **Description**:
  - The `cluster-ising` algorithm applies the Wolff algorithm to efficiently simulate the 2D Ising model, flipping entire spin clusters to speed up convergence near the critical temperature.
  - The energy, specific heat, and Binder cumulant are calculated for different lattice sizes, and the results are used to analyze phase transitions.
- **Key Outputs**: Energy and specific heat plots, magnetization plots, Binder cumulant plots, and phase transition identification.

## Requirements

Each problem requires the following Python libraries:
- `numpy`
- `matplotlib`



## How to Run

Each problem is implemented in a separate Jupyter notebook. Follow these steps to run the simulations:

1. **Clone or Download the Repository**: First, clone or download this repository to your local machine.

2. **Navigate to the Directory**: Move to the directory where the notebooks are located.

3. **Install Dependencies**: Ensure you have the required Python libraries, such as `numpy` and `matplotlib`. You can install them using your preferred package manager.

4. **Run the Notebooks**: Open the Jupyter notebooks and execute the cells to run the simulations.

Once the notebooks are open, you can follow the steps inside to simulate each problem.

## Conclusion

This repository provides a complete implementation of Monte Carlo simulations for the Ising model and the estimation of \(\pi\) using various methods. The results include analysis of energy, magnetization, specific heat, and phase transitions in 2D lattice systems.

