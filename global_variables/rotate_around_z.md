# Global Variables - Rotate around z-axis

| Name       | Expression                                                   |
| ---------- | ------------------------------------------------------------ |
| cE11       | cos(q)^2\*(c21\*sin(q)^2 + c11\*cos(q)^2 +  2\*c61\*cos(q)\*sin(q)) + sin(q)^2\*(c22\*sin(q)^2 + c12\*cos(q)^2 +  2\*c62\*cos(q)\*sin(q)) + 2\*cos(q)\*sin(q)\*(c26\*sin(q)^2 + c16\*cos(q)^2 +  2\*c66\*cos(q)\*sin(q)) |
| cE12       | cos(q)^2\*(c22\*sin(q)^2 + c12\*cos(q)^2 + 2\*c62\*cos(q)\*sin(q)) +  sin(q)^2\*(c21\*sin(q)^2 + c11\*cos(q)^2 + 2\*c61\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c26\*sin(q)^2 + c16\*cos(q)^2 + 2\*c66\*cos(q)\*sin(q)) |
| cE13       | c23\*sin(q)^2 + c13\*cos(q)^2 + 2\*c63\*cos(q)\*sin(q)       |
| cE14       | cos(q)\*(c24\*sin(q)^2 + c14\*cos(q)^2 + 2\*c64\*cos(q)\*sin(q)) -  sin(q)\*(c25\*sin(q)^2 + c15\*cos(q)^2 + 2\*c65\*cos(q)\*sin(q)) |
| cE15       | cos(q)\*(c25\*sin(q)^2 + c15\*cos(q)^2 + 2\*c65\*cos(q)\*sin(q)) +  sin(q)\*(c24\*sin(q)^2 + c14\*cos(q)^2 + 2\*c64\*cos(q)\*sin(q)) |
| cE16       | (cos(q)^2 - sin(q)^2)\*(c26\*sin(q)^2 + c16\*cos(q)^2 + 2\*c66\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c21\*sin(q)^2 + c11\*cos(q)^2 + 2\*c61\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c22\*sin(q)^2 + c12\*cos(q)^2 + 2\*c62\*cos(q)\*sin(q)) |
| cE21       | cos(q)^2\*(c11\*sin(q)^2 + c21\*cos(q)^2 - 2\*c61\*cos(q)\*sin(q)) +  sin(q)^2\*(c12\*sin(q)^2 + c22\*cos(q)^2 - 2\*c62\*cos(q)\*sin(q)) +  2\*cos(q)\*sin(q)\*(c16\*sin(q)^2 + c26\*cos(q)^2 - 2\*c66\*cos(q)\*sin(q)) |
| cE22       | cos(q)^2\*(c12\*sin(q)^2 + c22\*cos(q)^2 - 2\*c62\*cos(q)\*sin(q)) +  sin(q)^2\*(c11\*sin(q)^2 + c21\*cos(q)^2 - 2\*c61\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c16\*sin(q)^2 + c26\*cos(q)^2 - 2\*c66\*cos(q)\*sin(q)) |
| cE23       | c13\*sin(q)^2 + c23\*cos(q)^2 - 2\*c63\*cos(q)\*sin(q)       |
| cE24       | cos(q)\*(c14\*sin(q)^2 + c24\*cos(q)^2 - 2\*c64\*cos(q)\*sin(q)) -  sin(q)\*(c15\*sin(q)^2 + c25\*cos(q)^2 - 2\*c65\*cos(q)\*sin(q)) |
| cE25       | cos(q)\*(c15\*sin(q)^2 + c25\*cos(q)^2 - 2\*c65\*cos(q)\*sin(q)) +  sin(q)\*(c14\*sin(q)^2 + c24\*cos(q)^2 - 2\*c64\*cos(q)\*sin(q)) |
| cE26       | (cos(q)^2 - sin(q)^2)\*(c16\*sin(q)^2 + c26\*cos(q)^2 - 2\*c66\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c11\*sin(q)^2 + c21\*cos(q)^2 - 2\*c61\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c12\*sin(q)^2 + c22\*cos(q)^2 - 2\*c62\*cos(q)\*sin(q)) |
| cE31       | c32\*sin(q)^2 + c31\*cos(q)^2 + 2\*c36\*cos(q)\*sin(q)       |
| cE32       | c31\*sin(q)^2 + c32\*cos(q)^2 - 2\*c36\*cos(q)\*sin(q)       |
| cE33       | c33                                                          |
| cE34       | c34\*cos(q) - c35\*sin(q)                                    |
| cE35       | c35\*cos(q) + c34\*sin(q)                                    |
| cE36       | c36\*(cos(q)^2 - sin(q)^2) - c31\*cos(q)\*sin(q) + c32\*cos(q)\*sin(q) |
| cE41       | cos(q)^2\*(c41\*cos(q) - c51\*sin(q)) + sin(q)^2\*(c42\*cos(q) - c52\*sin(q)) +  2\*cos(q)\*sin(q)\*(c46\*cos(q) - c56\*sin(q)) |
| cE42       | cos(q)^2\*(c42\*cos(q) - c52\*sin(q)) + sin(q)^2\*(c41\*cos(q) - c51\*sin(q)) -  2\*cos(q)\*sin(q)\*(c46\*cos(q) - c56\*sin(q)) |
| cE43       | c43\*cos(q) - c53\*sin(q)                                    |
| cE44       | cos(q)\*(c44\*cos(q) - c54\*sin(q)) - sin(q)\*(c45\*cos(q) - c55\*sin(q)) |
| cE45       | cos(q)\*(c45\*cos(q) - c55\*sin(q)) + sin(q)\*(c44\*cos(q) - c54\*sin(q)) |
| cE46       | (cos(q)^2 - sin(q)^2)\*(c46\*cos(q) - c56\*sin(q)) -  cos(q)\*sin(q)\*(c41\*cos(q) - c51\*sin(q)) + cos(q)\*sin(q)\*(c42\*cos(q) -  c52\*sin(q)) |
| cE51       | cos(q)^2\*(c51\*cos(q) + c41\*sin(q)) + sin(q)^2\*(c52\*cos(q) + c42\*sin(q)) +  2\*cos(q)\*sin(q)\*(c56\*cos(q) + c46\*sin(q)) |
| cE52       | cos(q)^2\*(c52\*cos(q) + c42\*sin(q)) + sin(q)^2\*(c51\*cos(q) + c41\*sin(q)) -  2\*cos(q)\*sin(q)\*(c56\*cos(q) + c46\*sin(q)) |
| cE53       | c53\*cos(q) + c43\*sin(q)                                    |
| cE54       | cos(q)\*(c54\*cos(q) + c44\*sin(q)) - sin(q)\*(c55\*cos(q) + c45\*sin(q)) |
| cE55       | cos(q)\*(c55\*cos(q) + c45\*sin(q)) + sin(q)\*(c54\*cos(q) + c44\*sin(q)) |
| cE56       | (cos(q)^2 - sin(q)^2)\*(c56\*cos(q) + c46\*sin(q)) -  cos(q)\*sin(q)\*(c51\*cos(q) + c41\*sin(q)) + cos(q)\*sin(q)\*(c52\*cos(q) +  c42\*sin(q)) |
| cE61       | cos(q)^2\*(c61\*(cos(q)^2 - sin(q)^2) - c11\*cos(q)\*sin(q) +  c21\*cos(q)\*sin(q)) + sin(q)^2\*(c62\*(cos(q)^2 - sin(q)^2) - c12\*cos(q)\*sin(q)  + c22\*cos(q)\*sin(q)) + 2\*cos(q)\*sin(q)\*(c66\*(cos(q)^2 - sin(q)^2) -  c16\*cos(q)\*sin(q) + c26\*cos(q)\*sin(q)) |
| cE62       | cos(q)^2\*(c62\*(cos(q)^2 - sin(q)^2) - c12\*cos(q)\*sin(q) +  c22\*cos(q)\*sin(q)) + sin(q)^2\*(c61\*(cos(q)^2 - sin(q)^2) - c11\*cos(q)\*sin(q)  + c21\*cos(q)\*sin(q)) - 2\*cos(q)\*sin(q)\*(c66\*(cos(q)^2 - sin(q)^2) -  c16\*cos(q)\*sin(q) + c26\*cos(q)\*sin(q)) |
| cE63       | c63\*(cos(q)^2 - sin(q)^2) - c13\*cos(q)\*sin(q) + c23\*cos(q)\*sin(q) |
| cE64       | cos(q)\*(c64\*(cos(q)^2 - sin(q)^2) - c14\*cos(q)\*sin(q) +  c24\*cos(q)\*sin(q)) - sin(q)\*(c65\*(cos(q)^2 - sin(q)^2) - c15\*cos(q)\*sin(q) +  c25\*cos(q)\*sin(q)) |
| cE65       | cos(q)\*(c65\*(cos(q)^2 - sin(q)^2) - c15\*cos(q)\*sin(q) +  c25\*cos(q)\*sin(q)) + sin(q)\*(c64\*(cos(q)^2 - sin(q)^2) - c14\*cos(q)\*sin(q) +  c24\*cos(q)\*sin(q)) |
| cE66       | (cos(q)^2 - sin(q)^2)\*(c66\*(cos(q)^2 - sin(q)^2) - c16\*cos(q)\*sin(q) +  c26\*cos(q)\*sin(q)) - cos(q)\*sin(q)\*(c61\*(cos(q)^2 - sin(q)^2) -  c11\*cos(q)\*sin(q) + c21\*cos(q)\*sin(q)) + cos(q)\*sin(q)\*(c62\*(cos(q)^2 -  sin(q)^2) - c12\*cos(q)\*sin(q) + c22\*cos(q)\*sin(q)) |
| eES11      | cos(q)^2\*(e11\*cos(q) + e21\*sin(q)) + sin(q)^2\*(e12\*cos(q) + e22\*sin(q)) +  2\*cos(q)\*sin(q)\*(e16\*cos(q) + e26\*sin(q)) |
| eES12      | cos(q)^2\*(e12\*cos(q) + e22\*sin(q)) + sin(q)^2\*(e11\*cos(q) + e21\*sin(q)) -  2\*cos(q)\*sin(q)\*(e16\*cos(q) + e26\*sin(q)) |
| eES13      | e13\*cos(q) + e23\*sin(q)                                    |
| eES14      | cos(q)\*(e14\*cos(q) + e24\*sin(q)) - sin(q)\*(e15\*cos(q) + e25\*sin(q)) |
| eES15      | cos(q)\*(e15\*cos(q) + e25\*sin(q)) + sin(q)\*(e14\*cos(q) + e24\*sin(q)) |
| eES16      | (cos(q)^2 - sin(q)^2)\*(e16\*cos(q) + e26\*sin(q)) -  cos(q)\*sin(q)\*(e11\*cos(q) + e21\*sin(q)) + cos(q)\*sin(q)\*(e12\*cos(q) +  e22\*sin(q)) |
| eES21      | cos(q)^2\*(e21\*cos(q) - e11\*sin(q)) + sin(q)^2\*(e22\*cos(q) - e12\*sin(q)) +  2\*cos(q)\*sin(q)\*(e26\*cos(q) - e16\*sin(q)) |
| eES22      | cos(q)^2\*(e22\*cos(q) - e12\*sin(q)) + sin(q)^2\*(e21\*cos(q) - e11\*sin(q)) -  2\*cos(q)\*sin(q)\*(e26\*cos(q) - e16\*sin(q)) |
| eES23      | e23\*cos(q) - e13\*sin(q)                                    |
| eES24      | cos(q)\*(e24\*cos(q) - e14\*sin(q)) - sin(q)\*(e25\*cos(q) - e15\*sin(q)) |
| eES25      | cos(q)\*(e25\*cos(q) - e15\*sin(q)) + sin(q)\*(e24\*cos(q) - e14\*sin(q)) |
| eES26      | (cos(q)^2 - sin(q)^2)\*(e26\*cos(q) - e16\*sin(q)) -  cos(q)\*sin(q)\*(e21\*cos(q) - e11\*sin(q)) + cos(q)\*sin(q)\*(e22\*cos(q) -  e12\*sin(q)) |
| eES31      | e32\*sin(q)^2 + e31\*cos(q)^2 + 2\*e36\*cos(q)\*sin(q)       |
| eES32      | e31\*sin(q)^2 + e32\*cos(q)^2 - 2\*e36\*cos(q)\*sin(q)       |
| eES33      | e33                                                          |
| eES34      | e34                                                          |
| eES35      | e35\*cos(q) + e34\*sin(q)                                    |
| eES36      | e36\*(cos(q)^2 - sin(q)^2) - e31\*cos(q)\*sin(q) + e32\*cos(q)\*sin(q) |
| epsilon_xx | cos(q)\*(epsilon11\*cos(q) + epsilon21\*sin(q)) + sin(q)\*(epsilon12\*cos(q) +  epsilon22\*sin(q)) |
| epsilon_xy | cos(q)\*(epsilon12\*cos(q) + epsilon22\*sin(q)) - sin(q)\*(epsilon11\*cos(q) +  epsilon21\*sin(q)) |
| epsilon_xz | epsilon13\*cos(q) + epsilon23\*sin(q)                        |
| epsilon_yx | cos(q)\*(epsilon21\*cos(q) - epsilon11\*sin(q)) + sin(q)\*(epsilon22\*cos(q) -  epsilon12\*sin(q)) |
| epsilon_yy | cos(q)\*(epsilon22\*cos(q) - epsilon12\*sin(q)) - sin(q)\*(epsilon21\*cos(q) -  epsilon11\*sin(q)) |
| epsilon_yz | epsilon23\*cos(q) - epsilon13\*sin(q)                        |
| epsilon_zx | epsilon31\*cos(q) + epsilon32\*sin(q)                        |
| epsilon_zy | epsilon32\*cos(q) - epsilon31\*sin(q)                        |
| epsilon_zz | epsilon33                                                    |
