# DAE Solver for Constrained Pendulum

This project implements a differential-algebraic equation (DAE) solver for a constrained pendulum in Cartesian coordinates using SciPy’s Radau method.

## Description
- Models a pendulum with length \( L = 1.0 \) meter, constrained to move on a circle (\( x^2 + y^2 = 1 \)).
- Solves the DAE system with initial conditions ensuring constraint consistency.
- Includes stationary (zero velocity) and dynamic (non-zero velocity) cases.
- Visualizes results using Matplotlib.

## Results
### Stationary Case
- Initial conditions: \( x=0, y=-1, v_x=0, v_y=0, \lambda=4.905 \).
- Constraint check: `Mean = 1.000000, Std = 0.000000` (for \( L^2 = 1 \)).
- Constraint derivative check: `Mean = 0.000000, Std = 0.000000`.
- Second derivative constraint check: `Mean = 0.000000, Std = 0.000000`.
- Plots: `pendulum_trajectory.png`, `pendulum_path.png` (stationary point).

### Dynamic Case
- Initial conditions: \( x=0, y=-1, v_x=0.1, v_y=0, \lambda=4.9105 \).
- Constraint check: `Mean = 1.000000, Std = 0.000000`.
- Constraint derivative check: `Mean = -0.000003, Std = 0.000004`.
- Second derivative constraint check: `Mean = -0.000245, Std = 0.000220`.
- Plots: `pendulum_trajectory_dynamic.png` (oscillatory), `pendulum_path_dynamic.png` (circular arc).

## Files
- `pendulum_dae_solver.py`: Stationary case script (Radau).
- `pendulum_dae_solver_dynamic.py`: Dynamic case script (Radau).
- `pendulum_trajectory.png`, `pendulum_path.png`: Stationary case plots.
- `pendulum_trajectory_dynamic.png`, `pendulum_path_dynamic.png`: Dynamic case plots.
