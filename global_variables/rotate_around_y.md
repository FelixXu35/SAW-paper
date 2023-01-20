# Global Variables - Rotate around y-axis

| Name       | Expression                                                   |
| ---------- | ------------------------------------------------------------ |
| cE11       | cos(q)^2\*(c31\*sin(q)^2 + c11\*cos(q)^2 +  2\*c51\*cos(q)\*sin(q)) + sin(q)^2\*(c33\*sin(q)^2 + c13\*cos(q)^2 +  2\*c53\*cos(q)\*sin(q)) + 2\*cos(q)\*sin(q)\*(c35\*sin(q)^2 + c15\*cos(q)^2 +  2\*c55\*cos(q)\*sin(q)) |
| cE12       | c32\*sin(q)^2 + c12\*cos(q)^2 + 2\*c52\*cos(q)\*sin(q)       |
| cE13       | cos(q)^2\*(c33\*sin(q)^2 + c13\*cos(q)^2 + 2\*c53\*cos(q)\*sin(q)) +  sin(q)^2\*(c31\*sin(q)^2 + c11\*cos(q)^2 + 2\*c51\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c35\*sin(q)^2 + c15\*cos(q)^2 + 2\*c55\*cos(q)\*sin(q)) |
| cE14       | cos(q)\*(c34\*sin(q)^2 + c14\*cos(q)^2 + 2\*c54\*cos(q)\*sin(q)) -  sin(q)\*(c36\*sin(q)^2 + c16\*cos(q)^2 + 2\*c56\*cos(q)\*sin(q)) |
| cE15       | (cos(q)^2 - sin(q)^2)\*(c35\*sin(q)^2 + c15\*cos(q)^2 + 2\*c55\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c31\*sin(q)^2 + c11\*cos(q)^2 + 2\*c51\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c33\*sin(q)^2 + c13\*cos(q)^2 + 2\*c53\*cos(q)\*sin(q)) |
| cE16       | cos(q)\*(c36\*sin(q)^2 + c16\*cos(q)^2 + 2\*c56\*cos(q)\*sin(q)) +  sin(q)\*(c34\*sin(q)^2 + c14\*cos(q)^2 + 2\*c54\*cos(q)\*sin(q)) |
| cE21       | c23\*sin(q)^2 + c21\*cos(q)^2 + 2\*c25\*cos(q)\*sin(q)       |
| cE22       | c22                                                          |
| cE23       | c21\*sin(q)^2 + c23\*cos(q)^2 - 2\*c25\*cos(q)\*sin(q)       |
| cE24       | c24\*cos(q) - c26\*sin(q)                                    |
| cE25       | c25\*(cos(q)^2 - sin(q)^2) - c21\*cos(q)\*sin(q) + c23\*cos(q)\*sin(q) |
| cE26       | c26\*cos(q) + c24\*sin(q)                                    |
| cE31       | cos(q)^2\*(c11\*sin(q)^2 + c31\*cos(q)^2 - 2\*c51\*cos(q)\*sin(q)) +  sin(q)^2\*(c13\*sin(q)^2 + c33\*cos(q)^2 - 2\*c53\*cos(q)\*sin(q)) +  2\*cos(q)\*sin(q)\*(c15\*sin(q)^2 + c35\*cos(q)^2 - 2\*c55\*cos(q)\*sin(q)) |
| cE32       | c12\*sin(q)^2 + c32\*cos(q)^2 - 2\*c52\*cos(q)\*sin(q)       |
| cE33       | cos(q)^2\*(c13\*sin(q)^2 + c33\*cos(q)^2 - 2\*c53\*cos(q)\*sin(q)) +  sin(q)^2\*(c11\*sin(q)^2 + c31\*cos(q)^2 - 2\*c51\*cos(q)\*sin(q)) -  2\*cos(q)\*sin(q)\*(c15\*sin(q)^2 + c35\*cos(q)^2 - 2\*c55\*cos(q)\*sin(q)) |
| cE34       | cos(q)\*(c14\*sin(q)^2 + c34\*cos(q)^2 - 2\*c54\*cos(q)\*sin(q)) -  sin(q)\*(c16\*sin(q)^2 + c36\*cos(q)^2 - 2\*c56\*cos(q)\*sin(q)) |
| cE35       | (cos(q)^2 - sin(q)^2)\*(c15\*sin(q)^2 + c35\*cos(q)^2 - 2\*c55\*cos(q)\*sin(q))  - cos(q)\*sin(q)\*(c11\*sin(q)^2 + c31\*cos(q)^2 - 2\*c51\*cos(q)\*sin(q)) +  cos(q)\*sin(q)\*(c13\*sin(q)^2 + c33\*cos(q)^2 - 2\*c53\*cos(q)\*sin(q)) |
| cE36       | cos(q)\*(c16\*sin(q)^2 + c36\*cos(q)^2 - 2\*c56\*cos(q)\*sin(q)) +  sin(q)\*(c14\*sin(q)^2 + c34\*cos(q)^2 - 2\*c54\*cos(q)\*sin(q)) |
| cE41       | cos(q)^2\*(c41\*cos(q) - c61\*sin(q)) + sin(q)^2\*(c43\*cos(q) - c63\*sin(q)) +  2\*cos(q)\*sin(q)\*(c45\*cos(q) - c65\*sin(q)) |
| cE42       | c42\*cos(q) - c62\*sin(q)                                    |
| cE43       | cos(q)^2\*(c43\*cos(q) - c63\*sin(q)) + sin(q)^2\*(c41\*cos(q) - c61\*sin(q)) -  2\*cos(q)\*sin(q)\*(c45\*cos(q) - c65\*sin(q)) |
| cE44       | cos(q)\*(c44\*cos(q) - c64\*sin(q)) - sin(q)\*(c46\*cos(q) - c66\*sin(q)) |
| cE45       | (cos(q)^2 - sin(q)^2)\*(c45\*cos(q) - c65\*sin(q)) -  cos(q)\*sin(q)\*(c41\*cos(q) - c61\*sin(q)) + cos(q)\*sin(q)\*(c43\*cos(q) -  c63\*sin(q)) |
| cE46       | cos(q)\*(c46\*cos(q) - c66\*sin(q)) + sin(q)\*(c44\*cos(q) - c64\*sin(q)) |
| cE51       | cos(q)^2\*(c51\*(cos(q)^2 - sin(q)^2) - c11\*cos(q)\*sin(q) +  c31\*cos(q)\*sin(q)) + sin(q)^2\*(c53\*(cos(q)^2 - sin(q)^2) - c13\*cos(q)\*sin(q)  + c33\*cos(q)\*sin(q)) + 2\*cos(q)\*sin(q)\*(c55\*(cos(q)^2 - sin(q)^2) -  c15\*cos(q)\*sin(q) + c35\*cos(q)\*sin(q)) |
| cE52       | c52\*(cos(q)^2 - sin(q)^2) - c12\*cos(q)\*sin(q) + c32\*cos(q)\*sin(q) |
| cE53       | cos(q)^2\*(c53\*(cos(q)^2 - sin(q)^2) - c13\*cos(q)\*sin(q) +  c33\*cos(q)\*sin(q)) + sin(q)^2\*(c51\*(cos(q)^2 - sin(q)^2) - c11\*cos(q)\*sin(q)  + c31\*cos(q)\*sin(q)) - 2\*cos(q)\*sin(q)\*(c55\*(cos(q)^2 - sin(q)^2) -  c15\*cos(q)\*sin(q) + c35\*cos(q)\*sin(q)) |
| cE54       | cos(q)\*(c54\*(cos(q)^2 - sin(q)^2) - c14\*cos(q)\*sin(q) +  c34\*cos(q)\*sin(q)) - sin(q)\*(c56\*(cos(q)^2 - sin(q)^2) - c16\*cos(q)\*sin(q) +  c36\*cos(q)\*sin(q)) |
| cE55       | (cos(q)^2 - sin(q)^2)\*(c55\*(cos(q)^2 - sin(q)^2) - c15\*cos(q)\*sin(q) +  c35\*cos(q)\*sin(q)) - cos(q)\*sin(q)\*(c51\*(cos(q)^2 - sin(q)^2) -  c11\*cos(q)\*sin(q) + c31\*cos(q)\*sin(q)) + cos(q)\*sin(q)\*(c53\*(cos(q)^2 -  sin(q)^2) - c13\*cos(q)\*sin(q) + c33\*cos(q)\*sin(q)) |
| cE56       | cos(q)\*(c56\*(cos(q)^2 - sin(q)^2) - c16\*cos(q)\*sin(q) +  c36\*cos(q)\*sin(q)) + sin(q)\*(c54\*(cos(q)^2 - sin(q)^2) - c14\*cos(q)\*sin(q) +  c34\*cos(q)\*sin(q)) |
| cE61       | cos(q)^2\*(c61\*cos(q) + c41\*sin(q)) + sin(q)^2\*(c63\*cos(q) + c43\*sin(q)) +  2\*cos(q)\*sin(q)\*(c65\*cos(q) + c45\*sin(q)) |
| cE62       | c62\*cos(q) + c42\*sin(q)                                    |
| cE63       | cos(q)^2\*(c63\*cos(q) + c43\*sin(q)) + sin(q)^2\*(c61\*cos(q) + c41\*sin(q)) -  2\*cos(q)\*sin(q)\*(c65\*cos(q) + c45\*sin(q)) |
| cE64       | cos(q)\*(c64\*cos(q) + c44\*sin(q)) - sin(q)\*(c66\*cos(q) + c46\*sin(q)) |
| cE65       | (cos(q)^2 - sin(q)^2)\*(c65\*cos(q) + c45\*sin(q)) -  cos(q)\*sin(q)\*(c61\*cos(q) + c41\*sin(q)) + cos(q)\*sin(q)\*(c63\*cos(q) +  c43\*sin(q)) |
| cE66       | cos(q)\*(c66\*cos(q) + c46\*sin(q)) + sin(q)\*(c64\*cos(q) + c44\*sin(q)) |
| eES11      | cos(q)^2\*(e11\*cos(q) + e31\*sin(q)) + sin(q)^2\*(e13\*cos(q) + e33\*sin(q)) +  2\*cos(q)\*sin(q)\*(e15\*cos(q) + e35\*sin(q)) |
| eES12      | e12\*cos(q) + e32\*sin(q)                                    |
| eES13      | cos(q)^2\*(e13\*cos(q) + e33\*sin(q)) + sin(q)^2\*(e11\*cos(q) + e31\*sin(q)) -  2\*cos(q)\*sin(q)\*(e15\*cos(q) + e35\*sin(q)) |
| eES14      | cos(q)\*(e14\*cos(q) + e34\*sin(q)) - sin(q)\*(e16\*cos(q) + e36\*sin(q)) |
| eES15      | (cos(q)^2 - sin(q)^2)\*(e15\*cos(q) + e35\*sin(q)) -  cos(q)\*sin(q)\*(e11\*cos(q) + e31\*sin(q)) + cos(q)\*sin(q)\*(e13\*cos(q) +  e33\*sin(q)) |
| eES16      | cos(q)\*(e16\*cos(q) + e36\*sin(q)) + sin(q)\*(e14\*cos(q) + e34\*sin(q)) |
| eES21      | cos(q)\*(e16\*cos(q) + e36\*sin(q)) + sin(q)\*(e14\*cos(q) + e34\*sin(q)) |
| eES22      | e22                                                          |
| eES23      | e21\*sin(q)^2 + e23\*cos(q)^2 - 2\*e25\*cos(q)\*sin(q)       |
| eES24      | e24\*cos(q) - e26\*sin(q)                                    |
| eES25      | e25\*(cos(q)^2 - sin(q)^2) - e21\*cos(q)\*sin(q) + e23\*cos(q)\*sin(q) |
| eES26      | e26\*cos(q) + e24\*sin(q)                                    |
| eES31      | cos(q)^2\*(e31\*cos(q) - e11\*sin(q)) + sin(q)^2\*(e33\*cos(q) - e13\*sin(q)) +  2\*cos(q)\*sin(q)\*(e35\*cos(q) - e15\*sin(q)) |
| eES32      | e32\*cos(q) - e12\*sin(q)                                    |
| eES33      | cos(q)^2\*(e33\*cos(q) - e13\*sin(q)) + sin(q)^2\*(e31\*cos(q) - e11\*sin(q)) -  2\*cos(q)\*sin(q)\*(e35\*cos(q) - e15\*sin(q)) |
| eES34      | cos(q)\*(e34\*cos(q) - e14\*sin(q)) - sin(q)\*(e36\*cos(q) - e16\*sin(q)) |
| eES35      | (cos(q)^2 - sin(q)^2)\*(e35\*cos(q) - e15\*sin(q)) -  cos(q)\*sin(q)\*(e31\*cos(q) - e11\*sin(q)) + cos(q)\*sin(q)\*(e33\*cos(q) -  e13\*sin(q)) |
| eES36      | cos(q)\*(e36\*cos(q) - e16\*sin(q)) + sin(q)\*(e34\*cos(q) - e14\*sin(q)) |
| epsilon_xx | cos(q)\*(epsilon11\*cos(q) + epsilon31\*sin(q)) + sin(q)\*(epsilon13\*cos(q) +  epsilon33\*sin(q)) |
| epsilon_xy | epsilon12\*cos(q) + epsilon32\*sin(q)                        |
| epsilon_xz | cos(q)\*(epsilon13\*cos(q) + epsilon33\*sin(q)) - sin(q)\*(epsilon11\*cos(q) +  epsilon31\*sin(q)) |
| epsilon_yx | epsilon21\*cos(q) + epsilon23\*sin(q)                        |
| epsilon_yy | epsilon22                                                    |
| epsilon_yz | epsilon23\*cos(q) - epsilon21\*sin(q)                        |
| epsilon_zx | cos(q)\*(epsilon31\*cos(q) - epsilon11\*sin(q)) + sin(q)\*(epsilon33\*cos(q) -  epsilon13\*sin(q)) |
| epsilon_zy | epsilon32\*cos(q) - epsilon12\*sin(q)                        |
| epsilon_zz | cos(q)\*(epsilon33\*cos(q) - epsilon13\*sin(q)) - sin(q)\*(epsilon31\*cos(q) -  epsilon11\*sin(q)) |