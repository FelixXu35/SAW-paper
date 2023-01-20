# Global Variables - Acoustic Field

| Name  | Expression                                                   |
| ----- | ------------------------------------------------------------ |
| S1    | comp1.ux                                                     |
| S2    | comp1.vy                                                     |
| S3    | comp1.wz                                                     |
| S4    | comp1.vz+comp1.wy                                            |
| S5    | comp1.uz+comp1.wx                                            |
| S6    | comp1.uy+comp1.vx                                            |
| T1    | cE11 * S1+cE12 * S2+cE13 * S3+cE14 * S4+cE15 * S5+cE16 * S6  |
| T2    | cE21 * S1+cE22 * S2+cE23 * S3+cE24 * S4+cE25 * S5+cE26 * S6  |
| T3    | cE31 * S1+cE32 * S2+cE33 * S3+cE34 * S4+cE35 * S5+cE36 * S6  |
| T4    | cE41 * S1+cE42 * S2+cE43 * S3+cE44 * S4+cE45 * S5+cE46 * S6  |
| T5    | cE51 * S1+cE52 * S2+cE53 * S3+cE54 * S4+cE55 * S5+cE56 * S6  |
| T6    | cE61 * S1+cE62 * S2+cE63 * S3+cE64 * S4+cE65 * S5+cE66 * S6  |
| rho   | root.material.rho                                            |
| mu    | 1                                                            |
| omega | 2 * pi * lambda [rad/s]                                      |
| eSx   | eES11 * S1+eES12 * S2+eES13 * S3+eES14 * S4+eES15 * S5+eES16 * S6 |
| eSy   | eES21 * S1+eES22 * S2+eES23 * S3+eES24 * S4+eES25 * S5+eES26 * S6 |
| eSz   | eES31 * S1+eES32 * S2+eES33 * S3+eES34 * S4+eES35 * S5+eES36 * S6 |