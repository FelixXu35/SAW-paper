# Step 5: Set Weak Forms & Boundary Conditions

[⇦ back](../README.md)

Weak forms and boundary conditions are the soul of a COMSOL model. The weak forms tell FEM softwares the general rule of these physical fields, while a suitable boundary condition can help to find eigenmodes more quickly and more accurately, since It can filter trivial results. It is crucial to define them correctly. This definition is in each ***Weak Form PDE*** interface.

## Acoustic Field

### Weak Forms: Mechanic Term

The following two expressions correspond to elastic energy and kinetic energy, respectively. They need to be input into the node ***Weak Form PDE*** of your acoustic field interface.

```
%% 1st line:
-(test(S1)*T1+test(S2)*T2+test(S3)*T3+test(S4)*T4+test(S5)*T5+test(S6)*T6)

%% 2nd line:
rho*(omega)^2*(test(u)*u+test(v)*v+test(w)*w)
```

### Weak Forms: Coupling Term

This term set the influence of electromagnetic fields on the acoustic fields. It need to be input into a separate ***Weak Contribution*** node, by which the model can be easily transformed into a purely acoustic simulation (simply ***Disable*** electromagnetic fields and this ***Weak Contribution*** node).

```
%% The coupling term:
(test(S1)*eE1+test(S2)*eE2+test(S3)*eE3+test(S4)*eE4+test(S5)*eE5+test(S6)*eE6)
```

### Boundary Condition: Free Boundary Condition

The free boundary condition is applied to the interface between piezoelectric devices and the air/vacuum. This boundary condition is accomplished by the default ***Zero Flux*** node without any extra input.

Note that, for now, the free boundary condition can only be used on the acoustic field. I am not sure what's the influence of a ***Zero Flux*** node on the electromagnetic fields.

### Boundary Condition: Fixed Boundary Condition

The Fixed Boundary Condition is applied on boundaries that waves cannot (or merely) reach, the fixed boundary condition is a simple choice. This boundary condition is realized using ***Dirichlet Boundary Condition*** node, where all three input boxes are filled with zeros. 

Right click on the ***Weak Form PDE*** node and create a ***Dirichlet Boundary Condition*** node, then type three `0` in three input boxes.

### Boundary Condition: Periodic Boundary Condition

The Periodic Boundary Condition can truncate acoustic waves that are periodically propagating, or identical on one direction. 

Right click on the ***Weak Form PDE*** node, then create ***Period Boundary Condition***s and then select the correct boundaries in the ***Boundary Selection*** box. We suggest that only one pair of boundaries are selected in each ***Period Boundary Condition*** node.

## Electromagnetic Field

### Weak Forms: Electric Energy Term

The electric energy is different between internal field and external field, since there is coupling term in the internal field but not in the external field. This discrepancy shows on the definition of the electric displacement, instead of the weak forms.

##### Internal field:

```
-(D1x*test(E1x)+D1y*test(E1y)+D1z*test(E1z))
```

##### External field:

```
-(D2x*test(E2x)+D2y*test(E2y)+D2z*test(E2z))
```

### Weak Forms: Magnetic Energy Term

##### Internal field:

```
(curlM1x*test(curlM1x)+curlM1y*test(curlM1y)+curlM1z*test(curlM1z)) / mu0_const
```

##### External field:

```
(curlM2x*test(curlM2x)+curlM2y*test(curlM2y)+curlM2z*test(curlM2z)) / mu0_const
```

### Boundary Condition: Fixed Constraint

Similar to the fixed boundary condition in acoustic fields, this constraint is applied to boundaries that electromagnetic waves cannot (or merely) reach. The procedures of defining this constraint is also similar to the one of the fixed boundary condition.

### Boundary Condition: Electric-wall Boundary Condition

The electric-wall boundary condition can easily simulate the surface of a metal wall, for example, the inner surface of a metal cavity.

Right click the ***Weak Form PDE*** node and created three ***Pointwise Constraint*** nodes. Then manually select the boundaries where the metal exist and input the following three ***Constraint expression*** in three nodes.

##### If the constraint is on the internal surface:

```
tM1x
tM1y
tM1z
```

##### If the constraint in on the external surface:

```
tM2x
tM2y
tM2z
```

### Boundary Condition: Continuity Boundary Condition

This Boundary Condition is used to connect the internal field and the external field. Its mathematical expression is:

$$
\hat{n}\times(\underline{E}_2-\underline{E}_1)
$$
where $\hat{n}$ is the norm on the interface between internal and external fields.

To use this boundary condition, right click the ***Weak Form PDE*** nodes of internal and external fields and created three ***Pointwise Constraint*** nodes. Then manually select the interface and input the following three ***Constraint expression*** in six nodes.

##### Internal Field:

```
M1x - M2x
M1y - M2y
M1z - M2z
```

##### External Field:

```
M1x - M2x
M1y - M2y
M1z - M2z
```

### Boundary Condition: Absorbing Boundary Condition

This boundary condition is applied on the external surface of radiating devices, like antennas. The absorbing boundary condition can effectively truncate the calculation domain while maintain a high accuracy.

This boundary condition must be in a Weak Constraint. Right click the ***Weak Form PDE*** nodes of the external field and create three ***Weak Constraint*** nodes, then select the outer surface of the mode and input the following three ***Constraint expression***s in three nodes.

```
rcurlMx - i*k*Mtx
rcurlMy - i*k*Mty
rcurlMz - i*k*Mtz
```