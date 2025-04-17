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

## How to run code?

### Using Pixi (Recommended)
[Pixi](https://pixi.sh) provides a reproducible environment with exact package versions.

1. Install Pixi if you haven't already:
   ```bash
   curl -fsSL https://pixi.sh/install.sh | bash  # For macOS/Linux
   # or
   iwr -useb https://pixi.sh/install.ps1 | iex   # For Windows
   ```

2. Clone the repository and navigate to the project directory:
   ```bash
   git clone (URL - TBC)
   cd YOUR_PATH/IP-Trajectory-Optimisation-SN
   ```

3. Run the Voyager I analysis:
   ```bash
   pixi run voyager1
   ```

   Or generate an HTML report without the interactive interface:
   ```bash
   pixi run voyager1-auto
   ```

### Alternative: Using pip
If you prefer not to use Pixi, you can install dependencies with pip:
```bash
pip install -r requirements.txt
jupyter lab "Voyager I - Optimisation Algo.ipynb"
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

**Note:** For LaTeX rendering in plots, you will need a TeX distribution installed:
- Windows: [MiKTeX](https://miktex.org/download)
- macOS: [MacTeX](https://tug.org/mactex/)


Developed by Shubham Nath as part of an individual project on interplanetary trajectory optimisation.
