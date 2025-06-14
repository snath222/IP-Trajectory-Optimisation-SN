# Trajectory Optimisation for Voyager I & II Missions

This repository explores and implements four trajectory optimisation methods for Voyager I \& II interplanetary missions (minimise $\Delta V_\mathrm{mission}$) using the procedure developed in my Individual Project.

## Algorithms Implemented

- **Brute Force Search**  
  Implements a brute force approach to a set discretisation, exploring the problem space to minimise $\Delta V_\mathrm{mission}$.

- **Nelder-Mead Simplex Algorithm (`scipy.optimize.fmin`)**  
  Utilises the Nelder-Mead Simplex Algorithm, where the initial guess is set to be the historical mission epochs, to minimise $\Delta V_\mathrm{mission}$.

- **Genetic Algorithm**  
  Implements a metaheuristic optimisation method based on the principles of natural selection, employing both parallel and global search techniques – generating an optimal individual solution (of $\Delta V_\mathrm{mission}$).

- **Hybrid Genetic Algorithm**  
  Combines the global search capabilities of the Genetic Algorithm with the local refinement precision of the Nelder-Mead Simplex Algorithm, providing a robust approach that leverages the strengths of both methods to efficiently locate and refine the global optimum $\Delta V_\mathrm{mission}$.

### Results Preview

<div align="center">
  <table>
    <tr>
      <td align="center" width="50%">
        <img src="https://github.com/snath222/IP-Trajectory-Optimisation-SN/blob/82f66a08e21d56596c95d5ec8e7950dc50068e4b/Voyager%201%20-%20Figures/voyager_I_trajectory_km_AU.png" alt="Voyager I Trajectory" width="100%"/>
        <br>
        <b>Fig 1: Voyager I Optimised Trajectory Comparison</b>
        <br>
        <em>Earth → Jupiter → Saturn</em>
      </td>
      <td align="center" width="50%">
        <img src="https://github.com/snath222/IP-Trajectory-Optimisation-SN/blob/82f66a08e21d56596c95d5ec8e7950dc50068e4b/Voyager%202%20-%20Figures/voyager_II_trajectory_km_AU.png" alt="Voyager II Trajectory" width="100%"/>
        <br>
        <b>Fig 2: Voyager II Optimised Trajectory Comparison</b>
        <br>
        <em>Earth → Jupiter → Saturn → Uranus → Neptune</em>
      </td>
    </tr>
  </table>
</div>


> **Note:** Jupyter notebooks for both Voyager I and II missions are available in `.html` format for convenient viewing without executing the code.

## How to Run the Code

### Using Binder (Cloud)

Click the following Binder button to run the notebooks in your browser without any local installation:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/snath222/IP-Trajectory-Optimisation-SN/HEAD)

> **Note:** Takes around 5-10 minutes to load into the Jupyter environment.

(Last updated: 2nd May 2025)

### Using Pixi (Local)

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
## License \& Acknowledgements

This repository uses the [MIT](https://github.com/snath222/IP-Trajectory-Optimisation-SN/blob/32550e88cd8426dbb31d62e780e0c84489deedf5/LICENSE) license.

The code was formatted using [Black](https://black.readthedocs.io/en/stable/) (The uncompromising Python code formatter).

The [Poliastro](https://docs.poliastro.space/en/stable/) library was extensively used, allowing for seamless illustration of orbital trajectories.

---

Developed by Shubham Nath (under the supervision of [Hans Fangohr](https://github.com/fangohr)) as part of my Individual Project (IP) on interplanetary trajectory optimisation.
