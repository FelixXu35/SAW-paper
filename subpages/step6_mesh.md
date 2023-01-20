# Step 6: Mesh

[⇦ back](../README.md)

## Tricks

***Swept*** mesh is the first choice of column-shape objects.

The ***Free Triangular*** or  ***Free Quad*** meshes are recommended at the ***Source Surface***. They can be found at ***Boundary Generators***, which is in the setting menu when right-click the ***Mesh1*** node. These two meshes have their own advantages in different models. We recommend to try both of them in your simulation.

“Multilayers” are required in ***Swept***, especially on thin devices, like a thin disk. Controlling the number of layers can be done by ***Distribution*** node, which can be found when right-click the ***Swept1*** node. Input the number of layers at ***Number of elements***.

The external field is usually meshed with Free Tetrahedral, which doesn’t need to be very fine. Coarse is usually fine enough for the external field.

The size of each mesh can be defined individually. Right-click the mesh node you want to set, then choose ***Size***.

## Examples:

- a Piezoelectric Waveguide
- a Cylinder Antenna
- The External Field of the Cylinder Antenna