# DAE Solver for Constrained Pendulum

This project implements a Python script to solve a differential-algebraic equation (DAE) system for a constrained pendulum using SciPy's `solve_ivp` with the Radau method. The pendulum is modeled in Cartesian coordinates with an algebraic constraint ensuring a fixed length (\(x^2 + y^2 = L^2\)). The project demonstrates proficiency in numerical methods for DAEs, relevant to research in port-Hamiltonian systems.

## Project Overview
- **Objective**: Solve a DAE system modeling a pendulum with a fixed length (\(L = 1 \, \text{m}\)) under gravity (\(g = 9.81 \, \text{m/s}^2\)).
- **Tools**: Python, SciPy (`solve_ivp`), NumPy, Matplotlib.
- **Equations**:
  - Differential: \(\dot{x} = v_x\), \(\dot{y} = v_y\), \(\dot{v_x} = -2 \lambda x\), \(\dot{v_y} = -2 \lambda y - g\).
  - Algebraic: \(x^2 + y^2 - L^2 = 0\).
- **Outputs**:
  - `pendulum_trajectory.png`: Plot of positions \(x(t)\) and \(y(t)\) vs. time.
  - `pendulum_path.png`: Plot of pendulum path (\(x\) vs. \(y\)), showing a circular arc.
  - Constraint check: Verifies \(x^2 + y^2 \approx L^2\).

## Files
- `pendulum_dae_solver.py`: Main script to solve the DAE and generate plots.
- `pendulum_trajectory.png`: Trajectory plot showing \(x(t)\) and \(y(t)\).
- `pendulum_path.png`: Path plot showing the pendulum’s motion in the \(x\)-\(y\) plane.

## Usage
1. Install dependencies: `pip install numpy scipy matplotlib`.
2. Run the script: `python pendulum_dae_solver.py`.
3. Outputs: Plots saved as PNG files and a console message verifying the constraint.

## Results
- The trajectory plot shows oscillatory motion of the pendulum.
- The path plot confirms the constraint, forming a circular arc.
- Constraint check (example): `Mean = 1.000000, Std = 0.000001` (for \(L^2 = 1\)).

## Author
Hassan Mahmood Yousafzai  
[GitHub Profile](https://github.com/HassanYousafzai)  
[Email](mailto:hassan.yousafzai@gmail.com)

This project was developed to enhance skills in numerical methods for DAEs, aligning with research interests in scientific machine learning and port-Hamiltonian systems.
