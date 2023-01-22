# Step 2: Define Parameters and Variables

[⇦ back](../README.md)

In COMSOL, parameters are constants, which don't change with results or other variables. Their values are directly assigned by the user. For example, the diameters of a piezoelectric device are parameters. In contrast, variables are defined as a function, which may be different with time, position and/or results.

All definitions are accomplished within ***Global Definitions*** node.

Note that the ***Expression***s of some variables will be yellow when input, and show "Unknown variable lambda" when the cursor is placed on those ***Expression***s. Please ignore them, because they will not influence anything.

Note that ***Expression***s include `lambda` should not be in any Constraints.

There are two methods of including definitions:

1. Manually copt and paste
2. Automatically import

## Copy and paste manually

Please build a new node for each list of definition, then copy and paste all terms and their expressions. Note that some nodes are ***Parameter***s and some nodes are ***Variable***s.

[Global Parameters](../Global_Variables/parameters.md)

[Global Variables - Maximum](../Global_Variables/maximum.md)

[Global Variables - Acoustic Field](../Global_Variables/acoustic_field.md)

[Global Variables - Internal & External Electromagnetic Fields](../Global_Variables/EM_field.md)

[Global Variables - Absorbing Boundary Condition](../Global_Variables/absorbing_boundary_condition.md)

## Import Automatically

When define a new ***Parameters*** or ***Variables*** node, the corresponding list of terms can be imported using the following files.

How: Right-click the ***Global Definitions*** node and define a ***Parameters/Variables*** node. Select ***Label:*** in the setting area then input the name of the list. There is a “Load from File” icon below the empty list. Left-click this icon and choose the corresponding “.txt” file.

[Parameters.txt](../global_variables/Parameters.txt)

[Maximum.txt](../global_variables/Maximum.txt)

[Acoustic Field.txt](../global_variables/Acoustic_Field.txt)

[Internal EM field.txt](../global_variables/Internal_EM_field.txt)

[External EM Field.txt](../global_variables/External_EM_Field.txt)

[Absorbing Boundary Condition.txt](../global_variables/Absorbing_Boundary_Condition.txt)