<!-- Badges: -->
[![License](https://img.shields.io/github/license/QuCAI-Lab/ibm2022-quantum-spring-challenge.svg?logo=CreativeCommons&style=flat-square)](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/blob/dev/LICENSE.md)
[![Contributions](https://img.shields.io/badge/contributions-welcome-orange?style=flat-square)](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/pulls)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/graphs/commit-activity)
[![Release](https://img.shields.io/github/release/QuCAI-Lab/ibm2022-quantum-spring-challenge.svg)](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/releases)

<!-- Logo: -->
<div align="center">
  <a href="https://qucai-lab.github.io/"><img src="https://github.com/QuCAI-Lab/qucai-lab.github.io/blob/main/assets/QuCAI-Lab.png" height="500" width="500" /></a>
</div>

<!-- Title: -->
<div align="center">
  <h1> <a href="https://challenges.quantum-computing.ibm.com/spring-2022"> IBM Quantum Spring Challenge 2022 </a></h1>
  <h2> Solutions to the IBM Quantum Spring Challenge 2022
</div>
<br>

<!-- Author: -->
<div align="center">
  <b>Developer: <a target="_blank" href="https://github.com/camponogaraviera">¹Lucas Camponogara Viera</a></b>
<br>
<b><a target="_blank" href="https://en.ntnu.edu.tw/">¹National Taiwan Normal University - NTNU, Taipei, Taiwan</a></b>.
<br>
</div>


<!-- Dependencies: -->
# Dependencies
<a href="https://www.python.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://www.python.org/static/img/python-logo.png"></a>
<a href="https://matplotlib.org" target="_blank" rel="noopener noreferrer"><img height="27" src="https://matplotlib.org/_static/images/logo2.svg"></a>
<a href="https://numpy.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://numpy.org/images/logo.svg"></a>
<a href="https://www.sympy.org/en/index.html" target="_blank" rel="noopener noreferrer"><img height="27" src="https://www.sympy.org/static/images/logo.png"></a>
<a href="https://scipy.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://scipy.org/images/logo.svg"></a>
<a href="https://pyscf.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://pyscf.org/_images/pyscf-logo.png"></a>
<a href="https://qiskit.org/" target="_blank" rel="noopener noreferrer">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://qiskit.org/documentation/stable/0.19/_static/logo.png">
    <img alt="Shows Qiskit logo for light color mode and dark color mode." src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Qiskit-Logo.svg/1200px-Qiskit-Logo.svg.png" height="27">
  </picture>
</a>
<br>
<br>
  

# Project Description

The IBM Quantum Spring Challenge provided an opportunity for interested parties to learn more about quantum computing and quantum chemistry simulations. This repository presents the solutions to the challenge and a dedicated [supplementary.ipynb](supplementary.ipynb) material with a skill-reaffirming background covering the step-by-step derivations of the quantum circuits provided as solutions to the first challenge. In addition, useful linear algebra identities were verified using matrix representation, index notation, NumPy, SymPy and Qiskit SDK. If there is a blunder, do not hesitate to open an issue in the [issue tracker](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/issues).
  
  
# Table of Contents

- **[Tight-binding Model](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/blob/dev/exercise1/solution1.ipynb)**
  - Trotter-Suzuki decomposition of the Unitary time evolution operator under the tight-binding model Hamiltonian for a 3 site tight-binding **uniform lattice** (**on-site energy $\epsilon_i = 0$**).
- **[Quantum Random Walks and Localization](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/blob/dev/exercise2/solution2.ipynb)**
  - Simulating the electron **linear propagation** under the tight-binding model Hamiltonian for a 5 site tight-binding lattice by a continuous-time quantum random walk (**on-site energy $\epsilon_i = 0$**). 
  - Simulating **Anderson localization** phenomenon due to the inhomogeneity of the Lattice that causes multiple scattering of the electron introducing disorder in the on-site energies $\epsilon_i \neq 0$, and consequently **localizing the electronic wavefunction**.
- **[Many-body Quantum Dynamics](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/blob/dev/exercise3/solution3.ipynb)**
  - Simulating many-body localization (interplay between lattice disorder and particle-particle interaction) under the tight-binding model Hamiltonian for a 5 site tight-binding lattice in a 12 qubit chain.
- **[Using VQE On a Water Molecule](https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge/blob/dev/exercise4/solution4.ipynb)**
  - Applying the Variational Quantum Eigensolver (VQE) to compute the electronic ground state energy and electronic excited state energies of a water molecule.
  
  
# First steps to run locally

- Note1: Windows users should replace "python3" with "python".
- Note2: install the [IBM grading client](https://github.com/qiskit-community/Quantum-Challenge-Grader#run-locally) to run all notebooks successfully.
  
<br>
  
Clone this repository:
```bash
git clone https://github.com/QuCAI-Lab/ibm2022-quantum-spring-challenge.git && cd ibm2022-quantum-spring-challenge
```
Create a conda environment with the required dependencies:
```bash
conda env create -n quantumspring environment.yml && conda activate quantumspring
```
Don't forget to install qiskit, qiskit-nature and PySCF via pip. 

Install pip first:
```bash
conda install -yc conda-forge pip==22.1.2 && python3 -m pip install -U --upgrade pip
```
Installing qiskit[all] including qiskit-nature:
```bash
python3 -m pip install -U qiskit[all]
```
To check if qiskit-nature is installed, run `$ conda list qiskit` or `$ pip show qiskit-nature`. 
  
Manually installing qiskit-nature should return:
```bash
python3 -m pip install -U qiskit[nature] >>> Requirement already satisfied
```
Final step, installing PySCF (no support for native Windows platform, see [issue #750](https://github.com/pyscf/pyscf/issues/750)):
```bash
python3 -m pip install -U qiskit-nature[pyscf]
```

  
<br>
  
Alternatively, one can install the required dependencies via the [requirements.txt](requirements.txt) file:
```bash
conda create -yn quantumspring python==3.9.11 && conda activate quantumspring
```
```bash
conda update -yn base -c defaults conda && conda install -yc conda-forge pip==22.1.2
```
```bash
python3 -m pip install --user --upgrade pip && python3 -m pip install -r requirements.txt
```

  
# References
  
\[1] [IBM Quantum Spring Challenge 2022 - Problemset templates](https://github.com/qiskit-community/ibm-quantum-spring-challenge-2022).
  
  
# License

This work is licensed under a [Creative Commons Zero v1.0 Universal](LICENSE) license.

<hr>

Created and maintained by [@camponogaraviera][1].

[1]: https://github.com/camponogaraviera
