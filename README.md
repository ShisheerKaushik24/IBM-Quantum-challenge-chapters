<!-- Badges: -->
[![License](https://img.shields.io/github/license/ShisheerKaushik24/IBM-Quantum-challenge-chapters.svg?logo=CreativeCommons&style=flat-square)](https://github.com/ShisheerKaushik24/IBM-Quantum-challenge-chapters/blob/master/LICENSE.md)
[![Contributions](https://img.shields.io/badge/contributions-welcome-orange?style=flat-square)](https://github.com/ShisheerKaushik24/IBM-Quantum-challenge-chapters/pulls)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ShisheerKaushik24/IBM-Quantum-challenge-chapters/graphs/commit-activity)

<!-- Logo: -->
<div align="center">
  <a href="https://github.com/ShisheerKaushik24/IBM-Quantum-challenge-chapters"><img src="https://github.com/ShisheerKaushik24/IBM-Quantum-challenge-chapters/blob/master/asset/featured.png" height="500" width="700" /></a>
</div>

*<p align="center"><small>Source: IBM Quantum</small></p>*

<!-- Title: -->
<div align="center">
  <h1> <a href="https://challenges.quantum-computing.ibm.com/spring-2022"> IBM Quantum Challenge </a></h1>
  <h2> All my Solutions to the IBM Quantum Challenges
</div>
<br>

<!-- Author: -->
<div align="center">
  <b>Developer: <a target="_blank" href="https://github.com/ShisheerKaushik24">¹Shisheer S Kaushik</a></b>
<br>
</div>


<!-- Dependencies: -->
# Dependencies
<a href="https://www.python.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://www.python.org/static/img/python-logo.png"></a>
<a href="https://matplotlib.org" target="_blank" rel="noopener noreferrer"><img height="27" src="https://matplotlib.org/_static/images/logo2.svg"></a>
<a href="https://numpy.org/" target="_blank" rel="noopener noreferrer"><img height="27" src="https://numpy.org/images/logo.svg"></a>
<a href="https://www.sympy.org/en/index.html" target="_blank" rel="noopener noreferrer"><img height="27" src="https://www.sympy.org/static/images/logo.png"></a>
<a href="https://qiskit.org/" target="_blank" rel="noopener noreferrer">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://qiskit.org/documentation/stable/0.19/_static/logo.png">
    <img alt="Shows Qiskit logo for light color mode and dark color mode." src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Qiskit-Logo.svg/1200px-Qiskit-Logo.svg.png" height="27">
  </picture>
</a>
<br>
  
# Description

The IBM Quantum Challenge is an annual event where participants from all over the world solve a series of quantum computing programming challenges using IBM's quantum computing systems. The challenges are designed to test participants' knowledge and skills in various areas of quantum computing. These IBM Quantum challenges [2021,2022] provided me an ideal platform for me to explore various Quantum Computing Applications. This repository presents the solutions to my challenge. And I secured Advance Badge among the pool of 2000+ participants across the world, the Achieved badges can be accessed here<br>1.[2021](https://www.credly.com/badges/ee9d8117-1da4-40d1-bd89-c84693c33ee1/public_url)<br>2.[2022](https://www.credly.com/badges/bddc30d7-81a3-4b84-b403-c38f35b60b75/public_url)
  
# First steps to run locally

- Note1: Windows users should replace "python3" with "python".
- Note2: install the [IBM grading client](https://github.com/qiskit-community/Quantum-Challenge-Grader#run-locally) to run all notebooks successfully.
 
<br>
  
Create a conda environment with the required dependencies:
```bash
conda env create -n quantumchallenge environment.yml && conda activate quantumchallenge
```
Install qiskit, qiskit-nature and PySCF via pip. 

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
conda create -yn quantumchallenge python==3.9.11 && conda activate quantumchallenge
```
```bash
conda update -yn base -c defaults conda && conda install -yc conda-forge pip==22.1.2
```
```bash
python3 -m pip install --user --upgrade pip && python3 -m pip install -r requirements.txt
```

  
# References
  
\[1] [IBM Quantum Fall Challenge 2021](https://github.com/qiskit-community/ibm-quantum-challenge-2021)

\[2] [IBM Quantum Spring Challenge 2022](https://github.com/qiskit-community/ibm-quantum-spring-challenge-2022)
  
\[3] [IBM Quantum Spring Challenge 2023](https://github.com/qiskit-community/ibm-quantum-challenge-spring-2023)
  
  
# License

This work is licensed under a [Creative Commons Zero v1.0 Universal](LICENSE) license.

<hr>

Created and maintained by [@Shisheer S Kaushik][1].

[1]: https://github.com/ShisheerKauhik24
