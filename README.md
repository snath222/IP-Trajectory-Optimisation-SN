# Trajectory Optimisation for Voyager I & II Missions

This repository explores and implements three trajectory optimisation strategies for the Voyager I and II interplanetary missions using the procedure to minimise $\Delta V$ developed in my Individual Project.

## Algorithms Implemented

- **Brute Force Search**  
  Provides a comprehensive brute force approach of the problem space across fixed mission constraints.

- **Nelder-Mead Simplex Algorithm (`scipy.optimize.fmin`)**  
  Utilises the Nelder-Mead Simplex Algorithm to refine initial solutions and converge towards local minima of delta-V.

- **Genetic Algorithm**  
  Implements a metaheuristic optimisation method based on the principles of
natural selection, employing both parallel and global search techniques – generating a global optimal solution, minimising delta-V.

## Install Packages

To install the required packages, run the following command:

```bash
pip install -r requirements.txt
```
---

Developed by Shubham Nath as part of an individual project on interplanetary trajectory optimisation.
