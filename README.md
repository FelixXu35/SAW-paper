This is the detailed supplementary information for the paper <Simulating the magnetic fields generated by piezoelectric devices using FEM software: Beyond the quasi-static approximation> .

In this paper, we developed a method to simulate the magnetic field in/around a piezoelectric material. Which means, <u>there is no quasi-static approximation involved</u>. This method in principle can be applied to any finite-element method softwares, as long as they are based on weak forms. We use <u>COMSOL</u> as an example.

If you are interested in this method and decide to use our method in your research, please cite our paper using the link below:

https://aip.scitation.org/doi/abs/10.1063/5.0120630

# Instructions

We wrote a step-by-step instruction about how to build such a simulation from zero (or from a template), and it can be found in the links below ⬇️

中文版教程请点击以下链接🔗：

https://www.notion.so/xiaotianxu/86ff1b4e7153402a98b3e525ab1b28c6

English version can be found in the following link:

https://www.notion.so/xiaotianxu/Simulation-Instruction-58353f73e47e4aa5b184d3bc13bbe8f4

# Basic Information

[Terminologies](https://www.notion.so/Terminologies-b30bb2eb6d1f4131a64b2b8b8238a162)

# Start from an empty model

[Step 1: Build a new mode]()

[Step 2: Define Parameters and Variables](./subpages/step2_define_parameters_and_variables.md)

[Step 3: Rotate Material Coordinates](https://www.notion.so/Step-3-Rotate-Material-Coordinates-57ce01bb563b48019e43bf2bdbcb0b23)

[Step 4: Building Geometry](https://www.notion.so/Step-4-Building-Geometry-46e23617e36145cc89de67833bd84470)

# Templates

*Requires COMSOL 6.0 or later.*

[empty_60.mph](./mph_files/empty_60.mph)

# Start form a template

[Step 5: Set Weak Forms & Boundary Conditions](https://www.notion.so/Step-5-Set-Weak-Forms-Boundary-Conditions-d19a9dca844a419e8117f88b62d09253)

[Step 6: Mesh](https://www.notion.so/Step-6-Mesh-94056d3f86d548549f4cedd020a26e46)

[Step 7: Search for Eigenvalues](https://www.notion.so/Step-7-Search-for-Eigenvalues-aa7af67bde9944c7b3cdd0359677be4c)

[Step 8: Results](https://www.notion.so/Step-8-Results-405ee117511d4805bf3f6d0fe01b9773)

# Cases

*Requires COMSOL 6.0 or later.*

[Rayleigh_mode_60.mph](./mph_files/Rayleigh_mode_60.mph)

[disk_antenna_60.mph](./mph_files/disk_antenna_60.mph)

# Discussion

# Templates

Templates (.mph files) are available from the folder *templates*.

### 

# Contribution

Authors of the paper: Xiaotian (Felix) Xu, Michael Newns, Mark Oxborrow.

Author of this website: Xiaotian (Felix) Xu
