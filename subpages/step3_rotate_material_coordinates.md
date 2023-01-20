# Step 3: Rotate Material Coordinates

[← back](../README.md)

In the simulations, the direction of the material coordinates decides the results. Usually, one-time rotation is adequate. This method includes several lists of Parameters and Variables, which can help users to rotate the material coordinates easily. Note that this rotation will be around one of the three spatial coordinates.

## Definitions

Note that the list ***Reduced Coefficients*** doesn’t do any rotation. It just reduces the prefix `root.material.StressCharge.`, so that the other lists will not be too cumbersome.

[Global Parameters - Reduced Coefficients](../global_variables/reduced_coefficient.md)

[Global Variables - Rotate around x-axis](../global_variables/rotate_around_x.md)

[Global Variables - Rotate around y-axis](../global_variables/rotate_around_y.md)

[Global Variables - Rotate around z-axis](../global_variables/rotate_around_z.md)

Their corresponding “.txt” files are here:

[Reduced Coefficients.txt](../global_variables/Reduced Coefficients.txt)

[Rotate around x-axis.txt](../global_variables/Rotate around x-axis.txt)

[Rotate around y-axis.txt](../global_variables/Rotate around y-axis.txt)

[Rotate around z-axis.txt](../global_variables/rotate_around_z.md)

## How to use them

The list ***Reduced Coefficients*** is always necessary. Please do not ***disable*** it after importing it.

### Select Materials

Right-click ***Comp1*** → ***Materials***, then use ***Add Material from Library*** and select what you need.

Please remember to select Domains for each material.

The default ***Relative permeability*** in this model is 1 and the default ***Electrical conductivity*** is 0.

### Set the Angle of Rotation

This angle is the parameter `q`, which can be found in the list ***Global Parameters***.

### Choose an axis

Any rotation needs an axis. In this model, the axis can only be the x, y or z axis in the spatial coordinates. They corresponds to three different lists: ***Rotate around x-axis***, ***Rotate around y-axis*** and ***Rotate around z-axis***. ***Enable*** one list means the model will rotate the corresponding axis.

Note that enabling more than one lists is forbidden in this mode. Remember to ***disable*** the other two.

## Example

When simulating the phase velocity of different propagating direction in Lithium Niobate. Select ***128°Y-cut***, then enable ***Rotate around z-axis*** and input an angle in the expression of `q` in Global Parameters.