# Trajectory Optimisation for Voyager I & II Missions

This repository explores and implements three trajectory optimisation methods for Voyager I and II interplanetary missions (minimise $\Delta V$) using the procedure developed in my Individual Project.

## Algorithms Implemented

- **Brute Force Search**  
  Provides a comprehensive brute force approach of the problem space across fixed mission constraints.

- **Nelder-Mead Simplex Algorithm (`scipy.optimize.fmin`)**  
  Utilises the Nelder-Mead Simplex Algorithm to refine initial solutions and converge towards the minima of $\Delta V$.

- **Genetic Algorithm**  
  Implements a metaheuristic optimisation method based on the principles of
natural selection, employing both parallel and global search techniques – generating a global optimal solution, minimising $\Delta V$.

## Python Version & Install Packages

The supported Python version is between Python 3.8 and Python 3.10. The code was written in Python 3.9.

To install the required packages, run the following command:

```bash
pip install -r requirements.txt
```
---

Developed by Shubham Nath as part of an individual project on interplanetary trajectory optimisation.
