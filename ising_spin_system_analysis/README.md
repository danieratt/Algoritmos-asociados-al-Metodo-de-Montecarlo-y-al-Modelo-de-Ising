# Ising Model Spin Configuration Enumeration and Analysis

## Overview

This repository contains Python code for enumerating spin configurations in the 2D Ising model using the **gray-flip** algorithm. The implementation allows for the calculation of energy, magnetization, and the Binder cumulant for square lattices with periodic boundary conditions. 

The current code supports lattice sizes of \(2 \times 2\), \(4 \times 4\), and allows for analysis of the probability distributions and temperature-dependent behavior in these systems. Due to computational constraints, the \(6 \times 6\) lattice size was not processed.

## Functionality

### 1. Spin Configuration Enumeration

The **gray-flip** algorithm is implemented to efficiently generate all possible spin configurations for Ising lattices. The code calculates the energy \(E\) and magnetization \(M\) for each configuration in lattices of size \(2 \times 2\) and \(4 \times 4\). Each spin configuration is stored and its properties are compared to known exact solutions for validation.

### 2. Energy and Magnetization Distribution

Once the configurations are generated, the code computes the distribution of configurations based on their energy \(E\) and magnetization \(M\). These distributions are visualized to examine the behavior of the system under different temperature regimes.

### 3. Binder Cumulant Analysis

The code calculates the Binder cumulant \(B(T)\) as a function of temperature for each lattice size. The Binder cumulant is a key quantity used to distinguish between different phases of the system and to identify the critical temperature. The analysis is performed for lattices of size \(2 \times 2\) and \(4 \times 4\). The expected intersection of Binder cumulants at the critical temperature is explored.

### 4. Limitations

The enumeration for larger lattice sizes (e.g., \(6 \times 6\)) is computationally expensive and was not completed due to the time and resource limitations. Further optimization or access to more computational resources would be required to handle these larger systems.

## How to Run the Code

### Requirements

The following Python libraries are required:
- `numpy`
- `matplotlib`

### Running the Notebook

1. Download or clone the repository.
2. Open the Jupyter notebook `ising_spin_system_analysis.ipynb` in JupyterLab or Jupyter Notebook.
3. Run the cells to execute the **gray-flip** algorithm, generate spin configurations, and compute physical properties such as energy, magnetization, and Binder cumulant.

### Output

- **Spin Configuration Enumeration**: The notebook outputs the full enumeration of configurations for lattices of size \(2 \times 2\) and \(4 \times 4\), with their associated energy and magnetization values.
- **Histograms**: The code generates histograms of energy and magnetization for each lattice size, showing the distribution of states.
- **Binder Cumulant Plots**: The Binder cumulant is plotted as a function of temperature for each lattice size. These plots are used to analyze the phase transitions and identify the critical temperature.

### Limitations and Future Work

- **Larger Lattice Sizes**: Due to the computational complexity of enumerating spin configurations for lattices larger than \(4 \times 4\), the \(6 \times 6\) lattice was not processed. Future work could focus on optimizing the algorithm or leveraging more powerful computational resources to extend the analysis to larger lattice sizes.
- **Comparison with Exact Results**: The results obtained for \(2 \times 2\) and \(4 \times 4\) lattices are compared to known exact solutions, ensuring the correctness of the algorithm.

### Conclusion

This implementation provides an efficient enumeration of spin configurations for small Ising models and performs a detailed analysis of the energy, magnetization, and Binder cumulants. Although limited by computational resources for larger systems, it offers a solid foundation for studying phase transitions in the Ising model.

