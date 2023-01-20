# Global Variables - Absorbing Boundary Condition

| Name    | Expression                                                   |
| ------- | ------------------------------------------------------------ |
| rx      | x / sqrt(x^2+y^2+z^2)                                        |
| ry      | y / sqrt(x^2+y^2+z^2)                                        |
| rz      | z / sqrt(x^2+y^2+z^2)                                        |
| rcurlMx | ry\*curlM2z - rz\*curlM2y                                    |
| rcurlMy | rz\*curlM2x - rx\*curlM2z                                    |
| rcurlMz | rx\*curlM2y - ry\*curlM2x                                    |
| Mtx     | comp1.M2x - (comp1.M2x\*rx + comp1.M2y\*ry + comp1.M2z\*rz)\*rx |
| Mty     | comp1.M2y - (comp1.M2x\*rx + comp1.M2y\*ry + comp1.M2z\*rz)\*ry |
| Mtz     | comp1.M2z - (comp1.M2x\*rx + comp1.M2y\*ry + comp1.M2z\*rz)\*rz |
| k       | omega_t / c_const                                            |