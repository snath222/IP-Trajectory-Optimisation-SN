# Trajectory Optimisation for Voyager I & II Missions

This repository explores and implements three trajectory optimisation strategies for the Voyager I and II interplanetary missions using the Patched Conics approximation.

## Algorithms Implemented

- **Brute Force Grid Search**  
  Provides a comprehensive visual sweep of the problem space across fixed mission constraints (e.g., fixed departure or flyby dates).

- **Local Optimisation (`scipy.optimize.fmin`)**  
  Utilises the Nelder-Mead Simplex Algorithm to refine initial solutions and converge towards local minima of delta-v.

- **Genetic Algorithm**  
  Implements evolutionary search with elitism and tournament selection. Suitable for large, high-dimensional solution spaces where brute force becomes inefficient.

## Features

- Visual comparison of trajectories optimised using each method  
- Contour plots of delta-v landscapes across multiple constraints  
- Generational analysis of genetic algorithm performance  
- Designed for multi-body flyby trajectories with adjustable constraint configurations

---

Developed by Shubham Nath as part of an individual project on interplanetary trajectory optimisation.
