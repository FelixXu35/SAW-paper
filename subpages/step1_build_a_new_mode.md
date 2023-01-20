# Step 1: Build a new mode

[← back](../README.md)

The number of dimensions and the category of simulation will be decided in this step. Huge problem will occur if they cannot be correctly selected. Fortunately,  in our simulation, this selection is not complicated.

In most instances, the environment (the external field) needs to be considered. So we need to consider a truncated environment and using proper boundary conditions on it. In our simulation, the internal field and the external field are simulated in two physics interfaces.

## Select physics interfaces

Select ***Model Wizard*** → ***3D*** → (add the following interfaces⬇️) → ***General Studies*** → ***Eigenvalue*** → ***Done*** → replace the name of the acoustic field as `w1`.

1. Weak Form PDE(w): Field name `u`, Number of dependent variables `3`, Dependent variables `u`, `v`, `w`, Dependent variable quantity unit `m`.
2. Weak Form PDE(w2): Field name `EM1`, Number of dependent variables `3`, Dependent variables `M1x`, `M1y`, `M1z`, Dependent variable quantity unit `V/m / (rad/s)`.
3. Weak Form PDE(w3): Field name `EM2`, Number of dependent variables `3`, Dependent variables `M2x`, `M2y`, `M2z`, Dependent variable quantity unit `V/m / (rad/s)`.