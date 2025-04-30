# Trajectory Optimisation for Voyager I & II Missions

This repository explores and implements three trajectory optimisation methods for Voyager I and II interplanetary missions (minimise $\Delta V$) using the procedure developed in my Individual Project.

## Algorithms Implemented

- **Brute Force Search**  
  Provides a comprehensive brute force approach of the problem space across fixed mission constraints.

- **Nelder-Mead Simplex Algorithm (`scipy.optimize.fmin`)**  
  Utilises the Nelder-Mead Simplex Algorithm to refine initial solutions and converge towards the minima of $\Delta V$.

- **Genetic Algorithm**  
  Implements a metaheuristic optimisation method based on the principles of natural selection, employing both parallel and global search techniques – generating a global optimal solution, minimising $\Delta V$.

- **Hybrid Genetic Algorithm**  
  Combines the global search capabilities of the Genetic Algorithm with the local refinement precision of the Nelder-Mead Simplex Algorithm, providing a robust approach that leverages the strengths of both methods to efficiently locate and refine the global optimum $\Delta V$.

> **Note:** Jupyter notebooks for both Voyager I and II missions are available in `.html` format for convenient viewing without executing the code.

## How to Run the Code

### Using Binder

Click the following Binder button to run the notebooks in your browser without any local installation:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/snath222/IP-Trajectory-Optimisation-SN/HEAD)

> **Note:** Takes around 3-4 minutes to load into the Jupyter environment.

(Last updated: 30th April 2025)

### Using Pixi

**Prerequisites:** For LaTeX rendering in plots, you will need either one of these TeX distributions installed:
- Windows/macOS/Linux: [MiKTeX](https://miktex.org/download)
- macOS: [MacTeX](https://tug.org/mactex/)

[Pixi](https://pixi.sh) provides a reproducible environment with exact package versions, ensuring consistent results across different systems.

1. Install Pixi if you haven't already:
   ```bash
   curl -fsSL https://pixi.sh/install.sh | bash  # For macOS/Linux
   iwr -useb https://pixi.sh/install.ps1 | iex   # For Windows
   ```

3. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/snath222/IP-Trajectory-Optimisation-SN.git
   ```
    ```bash
   cd ~/IP-Trajectory-Optimisation-SN
   ```
   
4. Run the Jupyter notebooks:
   
   a) For Voyager I analysis:
   ```bash
   pixi run voyager1
   ```
   
   b) For Voyager II analysis:
   ```bash
   pixi run voyager2
   ```

### Alternative: Using pip
If you prefer not to use Pixi, you can install dependencies with pip:
```bash
pip install -r requirements.txt
jupyter lab "Voyager I - Optimisation Algo.ipynb"
jupyter lab "Voyager II - Optimisation Algo.ipynb"
```

The development environment used the following package versions:
```
# Environment Report
Python: 3.9.18 | packaged by conda-forge | (main, Dec 23 2023, 16:35:41) 
[Clang 16.0.6 ]
Platform: macOS-15.3.2-arm64-arm-64bit

## Package Versions
- numpy: 1.26.4
- matplotlib: 3.9.4
- pandas: 2.0.3
- scipy: 1.13.1
- tqdm: 4.66.5
- pickle: Built-in
- astropy: 5.3.4
- poliastro: 0.17.0
- seaborn: 0.13.2
- IPython: 8.15.0
```
---

Developed by Shubham Nath (under the supervision of [Hans Fangohr](https://github.com/fangohr)) as part of my Individual Project (IP) on interplanetary trajectory optimisation.
