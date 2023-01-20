# Global Variables - Internal & External Electromagnetic Fields

There is no electromagnetic-acoustic coupling existing in the external EM field, which leads to a lack of `eSx`, `eSy` and `eSz` in the definition of external D field.

### Internal EM field:

| Name    | Experssion                                                   |
| ------- | ------------------------------------------------------------ |
| H1x     | curlM1x / (-i * mu0_const)                                   |
| H1y     | curlM1y / (-i * mu0_const)                                   |
| H1z     | curlM1z / (-i * mu0_const)                                   |
| eE1     | eES11 * E1x + eES21 * E1y + eES31 * E1z                      |
| eE2     | eES12 * E1x + eES22 * E1y + eES32 * E1z                      |
| eE3     | eES13 * E1x + eES23 * E1y + eES33 * E1z                      |
| eE4     | eES14 * E1x + eES24 * E1y + eES34 * E1z                      |
| eE5     | eES15 * E1x + eES25 * E1y + eES35 * E1z                      |
| eE6     | eES16 * E1x + eES26 * E1y + eES36 * E1z                      |
| B1z     | H1z * mu0_const                                              |
| B1x     | H1x * mu0_const                                              |
| B1y     | H1y * mu0_const                                              |
| D1x     | epsilon_xx * E1x + epsilon_xy * E1y + epsilon_xz * E1z + eSx |
| D1y     | epsilon_yx * E1x + epsilon_yy * E1y + epsilon_yz * E1z + eSy |
| D1z     | epsilon_zx * E1x + epsilon_zy * E1y + epsilon_zz * E1z + eSz |
| curlM1x | comp1.M1zy - comp1.M1yz                                      |
| curlM1y | comp1.M1xz - comp1.M1zx                                      |
| curlM1z | comp1.M1yx - comp1.M1xy                                      |
| E1x     | comp1.M1x * omega                                            |
| E1y     | comp1.M1y * omega                                            |
| E1z     | comp1.M1z * omega                                            |
| tM1x    | comp1.M1x-(comp1.w2.nx * comp1.M1x+comp1.w2.ny * comp1.M1y+comp1.w2.nz * comp1.M1z) * comp1.w2.nx |
| tM1y    | comp1.M1y-(comp1.w2.nx * comp1.M1x+comp1.w2.ny * comp1.M1y+comp1.w2.nz * comp1.M1z) * comp1.w2.ny |
| tM1z    | comp1.M1z-(comp1.w2.nx * comp1.M1x+comp1.w2.ny * comp1.M1y+comp1.w2.nz * comp1.M1z)*comp1.w2.nz |

### External EM field:

| Name    | Expression                                                   |
| ------- | ------------------------------------------------------------ |
| H2x     | curlM2x / (-i * mu0_const)                                   |
| H2y     | curlM2y / (-i * mu0_const)                                   |
| H2z     | curlM2z / (-i * mu0_const)                                   |
| B2z     | H2z * mu0_const                                              |
| B2x     | H2x * mu0_const                                              |
| B2y     | H2y * mu0_const                                              |
| D2x     | epsilon_xx * E2x + epsilon_xy * E2y + epsilon_xz * E2z       |
| D2y     | epsilon_yx * E2x + epsilon_yy * E2y + epsilon_yz * E2z       |
| D2z     | epsilon_zx * E2x + epsilon_zy * E2y + epsilon_zz * E2z       |
| E2x     | comp1.M2x * omega                                            |
| E2y     | comp1.M2y * omega                                            |
| E2z     | comp1.M2z * omega                                            |
| curlM2x | comp1.M2zy - comp1.M2yz                                      |
| curlM2y | comp1.M2xz - comp1.M2zx                                      |
| curlM2z | comp1.M2yx - comp1.M2xy                                      |
| tM2x    | comp1.M2x-(comp1.w3.nx * comp1.M2x+comp1.w3.ny * comp1.M2y+comp1.w3.nz * comp1.M2z) * comp1.w3.nx |
| tM2y    | comp1.M2y-(comp1.w3.nx * comp1.M2x+comp1.w3.ny * comp1.M2y+comp1.w3.nz * comp1.M2z) * comp1.w3.ny |
| tM2z    | comp1.M2z-(comp1.w3.nx * comp1.M2x+comp1.w3.ny * comp1.M2y+comp1.w3.nz * comp1.M2z) * comp1.w3.nz |
