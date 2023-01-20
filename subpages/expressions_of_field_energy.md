# Expressions of Field Energy

[← back](../README.md)

输入于***结果*** →***派生值*** 节点中创建的***积分*** →***体积分*** 节点内。内外场各需要创建一个节点。

Both internal fields and external fields need a ***Volume Integration*** node. To set them up, tight click ***Results*** → ***Derived Values*** and find ***Integration*** → ***Volume Integration***.

##### Internal Fields:

| Expression                                                   | Description     |
| ------------------------------------------------------------ | --------------- |
| realdot(S1,T1)+realdot(S2,T2)+realdot(S3,T3)+realdot(S4,T4)+realdot(S5,T5)+realdot(S6,T6) | Elastic energy  |
| rho\*omega^2\*(realdot(i\*u,i\*u)+realdot(i\*v,i\*v)+realdot(i\*w,i\*w)) | Kinetic energy  |
| realdot(D1xE,E1x)+realdot(D1yE,E1y)+realdot(D1zE,E1z)        | Electric energy |
| mu0_const\*(realdot(H1x,H1x)+realdot(H1y,H1y)+realdot(H1z,H1z)) | Magnetic energy |

##### External Field:

| Expression                                                   | Description     |
| ------------------------------------------------------------ | --------------- |
| (realdot(D2x,E2x)+realdot(D2y,E2y)+realdot(D2z,E2z))         | Electric energy |
| mu0_const\*(realdot(H2x,H2x)+realdot(H2y,H2y)+realdot(H2z,H2z)) | Magnetic energy |