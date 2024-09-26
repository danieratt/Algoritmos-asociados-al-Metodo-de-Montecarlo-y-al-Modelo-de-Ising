# Wolff Algorithm for the Ising Model: Cluster-Based Simulation

## Overview

This repository contains a Python implementation of the **Wolff algorithm** for simulating the 2D Ising model on square lattices with periodic boundary conditions. The code computes the energy, specific heat, and magnetization of the system as a function of temperature. Additionally, the Binder cumulant is calculated to analyze phase transitions. Simulations are performed for different lattice sizes, including \(6 \times 6\), \(16 \times 16\), \(32 \times 32\), and \(64 \times 64\).

## Functionality

### 1. Wolff Algorithm for Spin Clusters

The **Wolff algorithm** is a cluster-based Monte Carlo method used to simulate spin systems, particularly suited for studying phase transitions. Unlike the local Metropolis algorithm, Wolff's method flips entire clusters of spins at once, leading to faster convergence near the critical temperature.

The code initializes a random spin configuration and iteratively applies the Wolff algorithm to update the system for various temperatures, enabling the calculation of:

- **Energy per spin**: The average energy of the system at each temperature.
- **Specific heat**: Derived from the fluctuations in energy.
- **Magnetization**: The average magnetization per spin as a function of temperature.
- **Binder cumulant**: A dimensionless quantity used to identify phase transitions.

### 2. Calculation of Thermodynamic Properties

For each lattice size and temperature, the following thermodynamic properties are calculated:
- **Energy per spin**: Monitored to study how the system's energy changes as the temperature varies.
- **Specific heat**: Computed from the variance of the energy and used to identify the critical temperature \(T_c\).
- **Magnetization**: Both the average absolute magnetization and its distribution are analyzed to study the behavior of the system across different phases.

### 3. Binder Cumulant and Phase Transitions

The **Binder cumulant** \(B(T)\) is calculated for each lattice size, providing a reliable indicator of phase transitions. By plotting the Binder cumulant for different lattice sizes, the code verifies the intersection point at the critical temperature \(T_c\). This is a key characteristic of second-order phase transitions in the Ising model.

### 4. Lattice Sizes and Temperature Range

Simulations are performed for the following lattice sizes:
- \(6 \times 6\)
- \(16 \times 16\)
- \(32 \times 32\)
- \(64 \times 64\)

The temperature range is chosen to capture the behavior of the system both above and below the critical temperature \(T_c \approx 2.269\), ensuring that the phase transition is adequately covered.

## Results

The following outputs are generated:
- **Energy vs. Temperature**: A plot showing the energy per spin as a function of temperature.
- **Specific Heat vs. Temperature**: A plot displaying the specific heat per spin, with a peak near the critical temperature.
- **Magnetization vs. Temperature**: A plot of the average absolute magnetization, showing how the system transitions from an ordered (magnetized) phase to a disordered phase as the temperature increases.
- **Binder Cumulant**: A plot of the Binder cumulant for each lattice size, showing the expected intersection near the critical temperature \(T_c\).

### Comparison with Exact Results

For small lattice sizes (e.g., \(6 \times 6\)), the results are compared with known exact solutions for the Ising model. The energy and specific heat are printed with at least 4 significant digits for validation.

## How to Run the Code

### Requirements

The following Python libraries are required:
- `numpy`
- `matplotlib`

### Running the Notebook

1. Clone or download the repository.
2. Open the Jupyter notebook `cluster_ising_wolff.ipynb` using Jupyter Notebook or JupyterLab.
3. Run the cells to execute the Wolff algorithm and compute the thermodynamic properties for different lattice sizes and temperatures.

### Output

- **Energy vs. Temperature**: Plots for each lattice size.
- **Specific Heat vs. Temperature**: Plots showing the behavior of specific heat across the phase transition.
- **Magnetization vs. Temperature**: Plots of magnetization as the system is heated.
- **Binder Cumulant**: Plots of the Binder cumulant for each lattice size, identifying the critical temperature.

### Limitations and Future Work

- **Larger Lattice Sizes**: The \(64 \times 64\) lattice simulations are computationally intensive and could be further optimized. Larger lattices would provide even more accurate results for studying critical phenomena.
- **Precision in Results**: While results for smaller lattice sizes match exact solutions, the precision for larger sizes can be improved by running the simulation for a greater number of Monte Carlo steps.

### Conclusion

This implementation provides an efficient simulation of the Ising model using the Wolff algorithm. The Binder cumulant and other thermodynamic properties are computed for multiple lattice sizes, and the critical temperature is identified through their analysis. This notebook is a powerful tool for studying phase transitions in 2D spin systems.


