# Global Parameters

[⇦ back](../subpages/step2_define_parameters_and_variables.md)

| Name    | Expression                  |
| ------- | --------------------------- |
| q       | (degree-0) / 180 * pi [rad] |
| degree  | 0                           |
| freq_t  | 0                           |
| omega_t | freq_t * 2 * pi[rad/s]      |

Note that “-0” in the `q` is for the beginning of the rotation. This “0” can be replaced with any number. For example, for an X-prop waveguide, the beginning of rotation is Z-cut when “-0”, the beginning is Y-cut when “-90”.

Besides, if needed, the dimensions of devices are also defined here.

`freq_t` and `omega_t` are prepared for the Absorbing Boundary Conditions. `freq_t` is the estimated frequency and `omega_t` is used to change the frequency into angular velocity.