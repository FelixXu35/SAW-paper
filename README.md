# Simulation Instruction 

This is step-by-step instruction of how to build a similar simulation as the one in this paper:

 ***\<Simulating the magnetic fields generated by piezoelectric devices using FEM software: Beyond the quasi-static approximation\>*** 

In this paper, we developed a method to simulate the magnetic field in/around a piezoelectric material. Which means, <u>there is no quasi-static approximation involved</u>. This method in principle can be applied to any finite-element method softwares, as long as they are based on weak forms. We use <u>COMSOL</u> as an example.

If you are interested in this method and decide to use our method in your research, please cite our paper using the link below:

https://aip.scitation.org/doi/abs/10.1063/5.0120630

中文版教程请点击以下链接🔗：

https://www.notion.so/xiaotianxu/86ff1b4e7153402a98b3e525ab1b28c6

## Basic Information

[Terminologies](https://www.notion.so/Terminologies-b30bb2eb6d1f4131a64b2b8b8238a162)

## Start from an empty model

[Step 1: Build a new mode](./subpages/step1_build_a_new_mode.md)

[Step 2: Define Parameters and Variables](./subpages/step2_define_parameters_and_variables.md)

[Step 3: Rotate Material Coordinates](./subpages/step3_rotate_material_coordinates.md)

[Step 4: Building Geometry](./subpages/step4_build_the_geometry.md)

## Templates

*Requires COMSOL 6.0 or later.*

[empty_60.mph](./mph_files/empty_60.mph)

## Start form a template

[Step 5: Set Weak Forms & Boundary Conditions](./subpages/step5_set_weak_forms_&_boundary_conditions.md)

[Step 6: Mesh](./subpages/step6_mesh.md)

[Step 7: Search for Eigenvalues](./subpages/step7_search_for_eigenvalues.md)

[Step 8: Results](./subpages/step8_result.md)

## Cases

*Requires COMSOL 6.0 or later.*

[Rayleigh_mode_60.mph](./mph_files/Rayleigh_mode_60.mph)

[disk_antenna_60.mph](./mph_files/disk_antenna_60.mph)

## Discussion

*Those are topics included in the response letter.*

[Why not using the AC/DC module?](./subpages/why_not_AC_DC_module.md)

[Can we use a 2D simulation?](./subpages/why_not_2D.md)

[The performance of COMSOL on Apple silicon (Chinese)](https://quan.ithome.com/content/sharedetail?id=79461)

## Help

[Common error message](./subpages/error_message.md)

[FAQ](./subpages/FAQ.md)

## Contribution

Authors of the paper: Xiaotian (Felix) Xu, Michael Newns, Mark Oxborrow.

Author of this website: Xiaotian (Felix) Xu [(xiaotian.xu19@imperial.ac.uk)](mailto:xiaotian.xu19@imperial.ac.uk)

Author’s personal page: [Xiaotian Xu](https://www.notion.so/Xiaotian-Xu-192edc330fb94e3fab12bf7c879832e7)

