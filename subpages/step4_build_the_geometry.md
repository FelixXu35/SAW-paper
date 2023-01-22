# Step 4: Build the Geometry

[⇦ back](../README.md)

Directly importing from CAD model is supported (although we didn’t use it).

***Booleans*** operations (***Union***, ***Intersection*** and ***Difference***) is usually useful, especially the models with absorbing boundary condition (the environment is obtained by differentiating the antenna from a sphere) or holes.

## Warning❗️❗️❗️

1. Remember to select the unit!

   Selection of the unit can be found at the settings of ***Comp1*** → ***Geometry1***.

2. When building more than one objects, remember to check their relative positions.

   The ***Base***s of some objects are at their geometric centre, some are at corners.

   Their position can be set at the settings of ***Comp1*** → ***Geometry1***.

3. When using ***Booleans***, you can choose ***Keep objects to add*** or ***Keep objects to subtract***.