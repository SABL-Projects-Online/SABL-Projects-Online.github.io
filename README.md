###### *GPU Posterior Simulation - Bayesian Simulated Annealing - Quantum Annealing*
# SABL-Projects
#### Quickstart
[Download SABL](https://www.uts.edu.au/about/faculty-science/what-we-do/our-research-areas/sequentially-adaptive-bayesian-learning-resear-1)

Installation instructions are contained in the archive .zip that you downloaded at the above link.

#### GitHub
A more streamlined code base with recent bug-fixes is now on GitHub.  See here for details.

#### About SABL: Sequentially Adaptive Bayesian Learning
SABL was the output resulting from Australian Research Council Grant DP130103356 (Massively parallel algorithms for Bayesian inference and decision making).  Details of the research project and the original team are [here](https://www.uts.edu.au/about/faculty-science/what-we-do/our-research-areas/sequentially-adaptive-bayesian-learning-research).

## The aim of SABL-Projects
The aim of this site is simple:

> To collect real-use examples of SABL from all application domains
> for the benefit of new users

These examples supplement the [original guide](https://www.uts.edu.au/sites/default/files/article/downloads/SABL_handbook_2015a.pdf) written by Professor John Geweke in 2015.  A new SABL user (with a moderate Matlab programming background) can then learn by example, taking code snippets that will be useful in their own application for such tasks as:
- [x] Setting up the Matlab global variables required by SABL
- [x] Importing .CSV data
- [x] Setting locations to store results from SABL, including saving the posterior sampling distribution of model parameters to .CSV
- [x] Leaving a randomly selected held-out sample from the estimation
- [x] Applying adjustments to data
- [x] Setting up simple prior distributions of model parameters
- [x] Calculating log-likelihood using [n-dimensional (tensor) arrays and arithmetic](/TensorMath/Tutorial)
- [x] Generating summary tables and plots
- [x] Trading off execution time in return for lower memory usage

## Projects
### Simple generic SABL project

| Concepts covered | 
| ---------------- |
| - [x] Setting up the Matlab global variables required by SABL  |
| - [x] Setting up simple prior distributions of model parameters |

| Download |
| -------- |
 
Installation |
------------ |
Expand the .zip contents to a new subdirectory under the "Projects" directory of your SABL installation. |

### The Impact of Confirmation Bias on Willingness To Pay for Financial Advice
[View output](/20170420 - Improved documentation after code cleanup/run.html)

Concepts covered | Download | Installation
---------------- | -------- | ------------
All items listed above | | Expand the .zip contents to a new subdirectory under the "Projects" directory of your SABL installation.


## Roadmap to Quantum Computing
An early implementation of quantum computing is underway thanks to [D-Wave](http://www.dwavesys.com).  Where SABL performs unconstrained optimisation on GPUs for real-valued problems, D-Wave performs unconstrained optimisation on qubit hardware for (quadratic) integer-valued problems.  Future SABL projects will look to bridge these two through the [qbsolv software](https://github.com/dwavesystems/qbsolv) released by D-Wave.

## Contact Us
Please submit your thoughts and suggestions as [Issues](https://github.com/SABL-Projects-Online/SABL-Projects-Online.github.io/issues) at this GitHub site.
