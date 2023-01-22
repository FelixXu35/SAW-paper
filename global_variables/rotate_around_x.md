# Global Variables - Rotate around x-axis

[⇦ back](../subpages/step3_rotate_material_coordinates.md)

| Name       | Expression                                                   |
| ---------- | ------------------------------------------------------------ |
| cE11       | c11                                                          |
| cE12       | c13\*sin(q)^2 + c12\*cos(q)^2 + 2\*c14\*cos(q)\*sin(q)       |
| cE13       | c12\*sin(q)^2 + c13\*cos(q)^2 - 2\*c14\*cos(q)\*sin(q)       |
| cE14       | c14\*(cos(q)^2 - sin(q)^2) - c12\*cos(q)\*sin(q) + c13\*cos(q)\*sin(q) |
| cE15       | c15\*cos(q) - c16\*sin(q)                                    |
| cE16       | c16\*cos(q) + c15\*sin(q)                                    |
| cE21       | c31\*sin(q)^2 + c21\*cos(q)^2 + 2\*c41\*cos(q)\*sin(q)       |
| cE22       | cos(q)^2\*(c32\*sin(q)^2 + c22\*cos(q)^2 + 2\*c42\*cos(q)\*sin(q)) +  sin(q)^2\*(c33\*sin(q)^2 + c23\*cos(q)^2 + 2\*c43\*cos(q)\*sin(q)) +  2\*cos(q)\*sin(q)\*(c34\*sin(q)^2 + c24\*cos(q)^2 + 2\*c44\*cos(q)\*sin(q)) |
| cE23       | cos(q)^2\*(c33\*sin(q)^2 + c23\*cos(q)^2 + 2\*c43\*cos(q)\*sin(q)) +  sin(q)^2\*(c32\*sin(q)^2 + c22\*cos(q)^2 + 2\*c42\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c34\*sin(q)^2 + c24\*cos(q)^2 + 2\*c44\*cos(q)\*sin(q)) |
| cE24       | (cos(q)^2 - sin(q)^2)\*(c34\*sin(q)^2 + c24\*cos(q)^2 + 2\*c44\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c32\*sin(q)^2 + c22\*cos(q)^2 + 2\*c42\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c33\*sin(q)^2 + c23\*cos(q)^2 + 2\*c43\*cos(q)\*sin(q)) |
| cE25       | cos(q)\*(c35\*sin(q)^2 + c25\*cos(q)^2 + 2\*c45\*cos(q)\*sin(q)) -  sin(q)\*(c36\*sin(q)^2 + c26\*cos(q)^2 + 2\*c46\*cos(q)\*sin(q)) |
| cE26       | cos(q)\*(c36\*sin(q)^2 + c26\*cos(q)^2 + 2\*c46\*cos(q)\*sin(q)) +  sin(q)\*(c35\*sin(q)^2 + c25\*cos(q)^2 + 2\*c45\*cos(q)\*sin(q)) |
| cE31       | c21\*sin(q)^2 + c31\*cos(q)^2 - 2\*c41\*cos(q)\*sin(q)       |
| cE32       | cos(q)^2\*(c22\*sin(q)^2 + c32\*cos(q)^2 - 2\*c42\*cos(q)\*sin(q)) +  sin(q)^2\*(c23\*sin(q)^2 + c33\*cos(q)^2 - 2\*c43\*cos(q)\*sin(q)) +  2\*cos(q)\*sin(q)\*(c24\*sin(q)^2 + c34\*cos(q)^2 - 2\*c44\*cos(q)\*sin(q)) |
| cE33       | cos(q)^2\*(c23\*sin(q)^2 + c33\*cos(q)^2 - 2\*c43\*cos(q)\*sin(q)) +  sin(q)^2\*(c22\*sin(q)^2 + c32\*cos(q)^2 - 2\*c42\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c24\*sin(q)^2 + c34\*cos(q)^2 - 2\*c44\*cos(q)\*sin(q)) |
| cE34       | (cos(q)^2 - sin(q)^2)\*(c24\*sin(q)^2 + c34\*cos(q)^2 - 2\*c44\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c22\*sin(q)^2 + c32\*cos(q)^2 - 2\*c42\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c23\*sin(q)^2 + c33\*cos(q)^2 - 2\*c43\*cos(q)\*sin(q)) |
| cE35       | cos(q)\*(c25\*sin(q)^2 + c35\*cos(q)^2 - 2\*c45\*cos(q)\*sin(q)) -  sin(q)\*(c26\*sin(q)^2 + c36\*cos(q)^2 - 2\*c46\*cos(q)\*sin(q)) |
| cE36       | cos(q)\*(c26\*sin(q)^2 + c36\*cos(q)^2 - 2\*c46\*cos(q)\*sin(q)) +  sin(q)\*(c25\*sin(q)^2 + c35\*cos(q)^2 - 2\*c45\*cos(q)\*sin(q)) |
| cE41       | c41\*(cos(q)^2 - sin(q)^2) - c21\*cos(q)\*sin(q) + c31\*cos(q)\*sin(q) |
| cE42       | cos(q)^2\*(c42\*(cos(q)^2 - sin(q)^2) - c22\*cos(q)\*sin(q) + c32\*cos(q)\*sin(q)) + sin(q)^2\*(c43\*(cos(q)^2 - sin(q)^2) - c23\*cos(q)\*sin(q)  + c33\*cos(q)\*sin(q)) + 2\*cos(q)\*sin(q)\*(c44\*(cos(q)^2 - sin(q)^2) -  c24\*cos(q)\*sin(q) + c34\*cos(q)\*sin(q)) |
| cE43       | cos(q)^2\*(c43\*(cos(q)^2 - sin(q)^2) - c23\*cos(q)\*sin(q) +  c33\*cos(q)\*sin(q)) + sin(q)^2\*(c42\*(cos(q)^2 - sin(q)^2) - c22\*cos(q)\*sin(q)  + c32\*cos(q)\*sin(q)) - 2\*cos(q)\*sin(q)\*(c44\*(cos(q)^2 - sin(q)^2) -  c24\*cos(q)\*sin(q) + c34\*cos(q)\*sin(q)) |
| cE44       | (cos(q)^2 - sin(q)^2)\*(c44\*(cos(q)^2 - sin(q)^2) - c24\*cos(q)\*sin(q) +  c34\*cos(q)\*sin(q)) - cos(q)\*sin(q)\*(c42\*(cos(q)^2 - sin(q)^2) -  c22\*cos(q)\*sin(q) + c32\*cos(q)\*sin(q)) + cos(q)\*sin(q)\*(c43\*(cos(q)^2 -  sin(q)^2) - c23\*cos(q)\*sin(q) + c33\*cos(q)\*sin(q)) |
| cE45       | cos(q)\*(c45\*(cos(q)^2 - sin(q)^2) - c25\*cos(q)\*sin(q) +  c35\*cos(q)\*sin(q)) - sin(q)\*(c46\*(cos(q)^2 - sin(q)^2) - c26\*cos(q)\*sin(q) +  c36\*cos(q)\*sin(q)) |
| cE46       | cos(q)\*(c46\*(cos(q)^2 - sin(q)^2) - c26\*cos(q)\*sin(q) +  c36\*cos(q)\*sin(q)) + sin(q)\*(c45\*(cos(q)^2 - sin(q)^2) - c25\*cos(q)\*sin(q) +  c35\*cos(q)\*sin(q)) |
| cE51       | c51\*cos(q) - c61\*sin(q)                                    |
| cE52       | cos(q)^2\*(c52\*cos(q) - c62\*sin(q)) + sin(q)^2\*(c53\*cos(q) - c63\*sin(q)) +  2\*cos(q)\*sin(q)\*(c54\*cos(q) - c64\*sin(q)) |
| cE53       | cos(q)^2\*(c53\*cos(q) - c63\*sin(q)) + sin(q)^2\*(c52\*cos(q) - c62\*sin(q)) -  2\*cos(q)\*sin(q)\*(c54\*cos(q) - c64\*sin(q)) |
| cE54       | (cos(q)^2 - sin(q)^2)\*(c54\*cos(q) - c64\*sin(q)) -  cos(q)\*sin(q)\*(c52\*cos(q) - c62\*sin(q)) + cos(q)\*sin(q)\*(c53\*cos(q) -  c63\*sin(q)) |
| cE55       | cos(q)\*(c55\*cos(q) - c65\*sin(q)) - sin(q)\*(c56\*cos(q) - c66\*sin(q)) |
| cE56       | cos(q)\*(c56\*cos(q) - c66\*sin(q)) + sin(q)\*(c55\*cos(q) - c65\*sin(q)) |
| cE61       | c61\*cos(q) + c51\*sin(q)                                    |
| cE62       | cos(q)^2\*(c62\*cos(q) + c52\*sin(q)) + sin(q)^2\*(c63\*cos(q) + c53\*sin(q)) +  2\*cos(q)\*sin(q)\*(c64\*cos(q) + c54\*sin(q)) |
| cE63       | cos(q)^2\*(c63\*cos(q) + c53\*sin(q)) + sin(q)^2\*(c62\*cos(q) + c52\*sin(q)) -  2\*cos(q)\*sin(q)\*(c64\*cos(q) + c54\*sin(q)) |
| cE64       | (cos(q)^2 - sin(q)^2)\*(c64\*cos(q) + c54\*sin(q)) -  cos(q)\*sin(q)\*(c62\*cos(q) + c52\*sin(q)) + cos(q)\*sin(q)\*(c63\*cos(q) +  c53\*sin(q)) |
| cE65       | cos(q)\*(c65\*cos(q) + c55\*sin(q)) - sin(q)\*(c66\*cos(q) + c56\*sin(q)) |
| cE66       | cos(q)\*(c66\*cos(q) + c56\*sin(q)) + sin(q)\*(c65\*cos(q) + c55\*sin(q)) |
| eES11      | e11                                                          |
| eES12      | e13\*sin(q)^2 + e12\*cos(q)^2 + 2\*e14\*cos(q)\*sin(q)       |
| eES13      | e12\*sin(q)^2 + e13\*cos(q)^2 - 2\*e14\*cos(q)\*sin(q)       |
| eES14      | e14\*(cos(q)^2 - sin(q)^2) - e12\*cos(q)\*sin(q) + e13\*cos(q)\*sin(q) |
| eES15      | e15\*cos(q) - e16\*sin(q)                                    |
| eES16      | e16\*cos(q) + e15\*sin(q)                                    |
| eES21      | e21\*cos(q) + e31\*sin(q)                                    |
| eES22      | cos(q)^2\*(e22\*cos(q) + e32\*sin(q)) + sin(q)^2\*(e23\*cos(q) + e33\*sin(q)) +  2\*cos(q)\*sin(q)\*(e24\*cos(q) + e34\*sin(q)) |
| eES23      | cos(q)^2\*(e23\*cos(q) + e33\*sin(q)) + sin(q)^2\*(e22\*cos(q) + e32\*sin(q)) -  2\*cos(q)\*sin(q)\*(e24\*cos(q) + e34\*sin(q)) |
| eES24      | (cos(q)^2 - sin(q)^2)\*(e24\*cos(q) + e34\*sin(q)) -  cos(q)\*sin(q)\*(e22\*cos(q) + e32\*sin(q)) + cos(q)\*sin(q)\*(e23\*cos(q) +  e33\*sin(q)) |
| eES25      | cos(q)\*(e25\*cos(q) + e35\*sin(q)) - sin(q)\*(e26\*cos(q) + e36\*sin(q)) |
| eES26      | cos(q)\*(e26\*cos(q) + e36\*sin(q)) + sin(q)\*(e25\*cos(q) + e35\*sin(q)) |
| eES31      | e31\*cos(q) - e21\*sin(q)                                    |
| eES32      | cos(q)^2\*(e32\*cos(q) - e22\*sin(q)) + sin(q)^2\*(e33\*cos(q) - e23\*sin(q)) +  2\*cos(q)\*sin(q)\*(e34\*cos(q) - e24\*sin(q)) |
| eES33      | cos(q)^2\*(e33\*cos(q) - e23\*sin(q)) + sin(q)^2\*(e32\*cos(q) - e22\*sin(q)) -  2\*cos(q)\*sin(q)\*(e34\*cos(q) - e24\*sin(q)) |
| eES34      | (cos(q)^2 - sin(q)^2)\*(e34\*cos(q) - e24\*sin(q)) -  cos(q)\*sin(q)\*(e32\*cos(q) - e22\*sin(q)) + cos(q)\*sin(q)\*(e33\*cos(q) -  e23\*sin(q)) |
| eES35      | cos(q)\*(e35\*cos(q) - e25\*sin(q)) - sin(q)\*(e36\*cos(q) - e26\*sin(q)) |
| eES36      | cos(q)\*(e36\*cos(q) - e26\*sin(q)) + sin(q)\*(e35\*cos(q) - e25\*sin(q)) |
| epsilon_xx | epsilon11                                                    |
| epsilon_xy | epsilon12\*cos(q) + epsilon13\*sin(q)                        |
| epsilon_xz | epsilon13\*cos(q) - epsilon12\*sin(q)                        |
| epsilon_yx | epsilon21\*cos(q) + epsilon31\*sin(q)                        |
| epsilon_yy | cos(q)\*(epsilon22\*cos(q) + epsilon32\*sin(q)) + sin(q)\*(epsilon23\*cos(q) +  epsilon33\*sin(q)) |
| epsilon_yz | cos(q)\*(epsilon23\*cos(q) + epsilon33\*sin(q)) - sin(q)\*(epsilon22\*cos(q) +  epsilon32\*sin(q)) |
| epsilon_zx | epsilon31\*cos(q) - epsilon21\*sin(q)                        |
| epsilon_zy | cos(q)\*(epsilon32\*cos(q) - epsilon22\*sin(q)) + sin(q)\*(epsilon33\*cos(q) -  epsilon23\*sin(q)) |
| epsilon_zz | cos(q)\*(epsilon33\*cos(q) - epsilon23\*sin(q)) - sin(q)\*(epsilon32\*cos(q) -  epsilon22\*sin(q)) |