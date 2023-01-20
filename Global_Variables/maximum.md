# Global Variables - Maximum

This group of variables will be used in the normalization.

Please also define a node by right-clicking ***Definitions*** and select ***Nonlocal Couplings*** → ***Maximum*** under ***Component 1***.

| Name | Expression                                                   |
| ---- | ------------------------------------------------------------ |
| mE   | max(comp1.maxop1(sqrt(realdot(E1x,E1x) + realdot(E1y,E1y) + realdot(E1z,E1z))), comp1.maxop2(sqrt(realdot(E2x,E2x) + realdot(E2y,E2y) + realdot(E2z,E2z)))) |
| mEx  | max(comp1.maxop1(real(E1x)),comp1.maxop2(real(E2x)))         |
| mEy  | max(comp1.maxop1(real(E1y)),comp1.maxop2(real(E2y)))         |
| mEz  | max(comp1.maxop1(real(E1z)),comp1.maxop2(real(E2z)))         |
| mDx  | max(comp1.maxop1(real(D1x)),comp1.maxop2(real(D2x)))         |
| mDy  | max(comp1.maxop1(real(D1y)),comp1.maxop2(real(D2y)))         |
| mDz  | max(comp1.maxop1(real(D1z)),comp1.maxop2(real(D2z)))         |
| mH   | max(comp1.maxop1(sqrt(realdot(H1x,H1x) + realdot(H1y,H1y) + realdot(H1z,H1z))), comp1.maxop2(sqrt(realdot(H2x,H2x) + realdot(H2y,H2y) + realdot(H2z,H2z)))) |
| mHx  | max(comp1.maxop1(real(H1x)),comp1.maxop2(real(H2x)))         |
| mHy  | max(comp1.maxop1(real(H1y)),comp1.maxop2(real(H2y)))         |
| mHz  | max(comp1.maxop1(real(H1z)),comp1.maxop2(real(H2z)))         |
