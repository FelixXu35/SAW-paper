# Can we use a 2D simulation?

[← back](../README.md)

## Question

Why don't the authors simply use a 2D simulation in Figure 1? Using a 3D geometry and then applying periodic boundary conditions on surfaces 4 and 5 will significantly increase the total DOFs and computational costs.

## Reply

It is true that using 3D geometry and periodic boundary conditions will increase the needed commutating recourses. There are three reasons for not using the 2D geometry.

1. Our aim is to develop a universal simulating program for all scenarios. Most users have 3D models. We don’t want the users to waste their time changing the settings for different dimensions.
2. There is a trick that can save time. If the models can be simplified to a 2D one, simply set the number of layers to 1 in the *Swept* node while meshing. It can reduce the calculating time to an affordable level.
3. Deriving the weak forms for 2D models (especially those with rotational symmetry) and testing will cost us too much time. We don’t have enough time.

My supervisor used this method to simulate the Whispering Gallery mode. If anybody has interest to realise this method on electromagnetic-acoustic coupling, please refer to this paper:

[Traceable 2-D Finite-Element Simulation of the Whispering-Gallery Modes of Axisymmetric Electromagnetic Resonators](https://ieeexplore.ieee.org/abstract/document/4230891)