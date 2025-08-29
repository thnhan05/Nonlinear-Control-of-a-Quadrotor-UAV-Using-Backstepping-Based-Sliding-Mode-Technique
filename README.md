# Nonlinear Control of a Quadrotor UAV Using Backstepping-Based Sliding Mode Technique  

📌 **Paper:** [arXiv:2506.14195](https://arxiv.org/abs/2506.14195)  

## Overview  

This repository contains MATLAB and Python implementations for simulating and optimizing the dynamics of a quadrotor UAV under a **Backstepping-Based Sliding Mode Controller (BSMC)**.  

- **MATLAB code**: Models the nonlinear quadrotor dynamics and applies BSMC for trajectory tracking.  
- **Python code**: Extends the controller with parameter optimization to minimize tracking error.  

---

## MATLAB Implementation  

### Files  
- **`QRBS.m`** – Quadrotor dynamics and controller equations.  
- **`run_file.m`** – Runs simulations and generates 3D trajectory plots.  
- **`R_P_Y_traj.m`** – Plots roll, pitch, yaw trajectories and tracking errors.  
- **`x_y_z_traj.m`** – Plots x, y, z translational trajectories and errors.  

### Usage  
1. Open all MATLAB files in the same workspace.  
2. Run `run_file.m` to simulate and visualize the 3D trajectory.  
3. Run `R_P_Y_traj.m` and `x_y_z_traj.m` for 2D trajectory tracking plots.  

### Key Variables in `QRBS.m`  
- **System parameters:** `m`, `Ix`, `Iy`, `Iz`, `Jr`, `g`, aerodynamic coefficients.  
- **Desired trajectory:** `xd`, `xdd`.  
- **Errors:** `z`.  
- **Controller tuning:** `alpha`, gains `q1...`, `k1...`.  
- **Control inputs:** `U1 … Uy`.  
- **State derivatives:** `dx1 … dx16`.  

---

## Python Implementation  

### File  
- **`Controls_Optimization.py`** – Contains dynamics, controller, optimization, and visualization.  

### Dependencies  
Install requirements with:  
```bash
pip install numpy scipy matplotlib
