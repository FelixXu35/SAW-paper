# Step 8: Results

[← back](../README.md)

## Visualisation

The internal field and external field are simulated in two different interfaces, so their value have different range and use different color bar, which

An normalization is employed to enable the internal field and external field to use the same colour-bar.

In this simulation, electromagnetic fields usually doesn’t concentrate on the surface of the device, so the ***Volume*** node is not adequate for observing the properties of electromagnetic fields. ***Slice*** node is often firstly considered, although this node requires to be built for three times on three directions. I recommend the ***Multislice*** node, which can be found in ***3D Plot Group*** → ***More Plots***.

Moreover, I recommend to use ***3D Plot Group*** → Arrow Volume to visualize the field lines.

Acoustic displacement field should be visualized using ***Volume*** with a ***Deformation***, which can be found when right-click ***Volume*** node.

For the visualisation of electromagnetic fields, I recommend inputing the following codes into ***Multislice*** node: (the variables of maximum values are defined in [Global Variables - Maximum](https://www.notion.so/Global-Variables-Maximum-fb4f8f5e6b914a70add36284e32a293a))

```
%% Internal electric field
sqrt(realdot(E1x,E1x)+realdot(E1y,E1y)+realdot(E1z,E1z)) / mE
 
%% External electric field
sqrt(realdot(E2x,E2x)+realdot(E2y,E2y)+realdot(E2z,E2z)) / mE

%% Internal magnetic field
sqrt(realdot(H1x,H1x)+realdot(H1y,H1y)+realdot(H1z,H1z)) / mH

%% External magneric field
sqrt(realdot(H2x,H2x)+realdot(H2y,H2y)+realdot(H2z,H2z)) / mH

%% The x component of internal electric field
real(E1x) / mEx

%% The x component of external electric field
real(E2x) / mEx

%% The y component of internal electric field
real(E1y) / mEy

%% The y component of external electric field
real(E2y) / mEy

%% The z component of internal electric field
real(E1z) / mEz

%% The z component of external electric field
real(E2z) / mEz

%% The x component of internal magnetic field
real(H1x) / mHx

%% The x component of external magnetic field
real(H2x) / mHx

%% The y component of internal magnetic field
real(H1y) / mHy

%% The y component of external magnetic field
real(H2y) / mHy

%% The z component of internal magnetic field
real(H1z) / mHz

%% The z component of external magnetic field
real(H2z) / mHz
```

# Magnetic Coupling Coefficient

Our model is better than others because it can simulate the magnetic fields in/around piezoelectric devices, especially the external fields. Therefore, we mainly focus on the magnetic coupling coefficient.

The magnetic coupling coefficient is defined as:
$$
\eta = \frac{E_{\text{mag}}^{\text{ext}}}{E_{\text{kin}}^{\text{int}}+E_{\text{ela}}^{\text{int}}+E_{\text{elec}}^{\text{int}}+E_{\text{mag}}^{\text{int}}+E_{\text{elec}}^{\text{ext}}+E_{\text{mag}}^{\text{ext}}}
$$
where “int” denotes fields in the piezoelectric devices (internal fields), “ext” denotes the fields around the devices (external fields). “kin”, “ela”, “elec” & “mag“ are abbreviations of kinetic energy, elastic potential energy, electric field energy and magnetic field energy, respectively. Those energy can be calculated in COMSOL, which uses two ***Volume integration*** nodes. The expression input into ***Volume integration*** nodes are listed here:

[Expressions of Field Energy ](./expressions_of_field_energy.md)

耦合效率的计算虽然简单，但是需要在其他的软件中进行，比如Excel。