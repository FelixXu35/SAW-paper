# Step 5: Set Weak Forms & Boundary Conditions

[⇦ back](../README.md)

The weak forms and boundary conditions are the backbone of a COMSOL model.  Therefore, it is crucial to define them correctly. This definition is in ***Weak Form PDE*** interface.

A suitable boundary condition can help to find eigenmodes more quickly and more accurately, since It can filter trivial results.

选取一个好的边界条件，不仅可以帮助我们更准确得找到想要的振动模式，更有利于筛掉不需要的振动模式。在选择的时候要考虑到所求振动模式的独特之处并利用好他们。

## Acoustic Field

### Weak Form: Mechanic Term

These two lines correspond to elastic energy and kinetic energy.

```
%% 1st line:
-(test(S1)*T1+test(S2)*T2+test(S3)*T3+test(S4)*T4+test(S5)*T5+test(S6)*T6)

%% 2nd line:
rho*(omega)^2*(test(u)*u+test(v)*v+test(w)*w)
```

### Weak From: Coupling Term

耦合项定义在一个单独的节点的意义在于，想要模拟纯声场的时候，只需要***禁用*** 耦合项和电磁场对应的***弱形式偏微分方程*** 接口即可。

```
%% The coupling term:
(test(S1)*eE1+test(S2)*eE2+test(S3)*eE3+test(S4)*eE4+test(S5)*eE5+test(S6)*eE6)
```

### Boundary Condition: Free Boundary Condition

适用于器件与空气/真空的交界面。

自由边界条件其实不需要额外输入，使用默认的***零通量*** 即可。

使用别的边界条件的时候把自由的边界空出来，默认的***零通量*** 会自动应用在这个边界上，这个边界就会成为自由边界。

Note that, for now, the free boundary condition can only be used on the acoustic field. I am not sure

注意：目前自由边界条件只能应用在声场上，暂不清楚***零通量*** 在电磁场的弱形式中意味着什么。

### Boundary Condition: Fixed Boundary Condition

固定约束适用于声波传播不到的边界，或者被牢固固定的边界。

固定约束可以通过***狄利克雷边界条件*** 实现。在***弱形式偏微分方程*** 节点上单击右键，可以找到并添加***狄利克雷边界条件*** 。***狄利克雷边界条件*** 限制的就是我们之前设置过的三个因变量，需要把三个对勾都勾上，然后在三个输入框中都输入`0`。

### Boundary Condition: Periodic Boundary Condition

周期性边界条件可以截断在某一方向上周期性传播的声波，或者在某一方向上完全相同的波。

直接在***弱形式偏微分方程*** 接口上单击右键，选择***周期性条件*** 节点，然后选择对应的边界即可。建议每个***周期性条件*** 节点只选择一对对应的边界。

## Electromagnetic Field

### Weak Form: Electric Energy Term

内外场在电场能量上确实有所不同，内电场能量包括耦合能量，但是外电场不包括。这个不同点不体现在弱形式上，而是体现在内外场对于电位移的不同定义上。

##### Internal field:

```
-(D1x*test(E1x)+D1y*test(E1y)+D1z*test(E1z))
```

##### External field:

```
-(D2x*test(E2x)+D2y*test(E2y)+D2z*test(E2z))
```

### Weak Form: Magnetic Energy Term

##### Internal field:

```
(curlM1x*test(curlM1x)+curlM1y*test(curlM1y)+curlM1z*test(curlM1z)) / mu0_const
```

##### External field:

```
(curlM2x*test(curlM2x)+curlM2y*test(curlM2y)+curlM2z*test(curlM2z)) / mu0_const
```

### Boundary Condition: Fixed Constraint

电磁场的固定约束适用于电磁波（几乎）传播不到的边界。

右键点击***弱形式偏微分方程*** 接口，选择创建***狄利克雷边界条件*** 节点。将三个“制定xxx值”勾选框全部勾选，并在三个输入框中都输入0。

### Boundary Condition: Electric-wall Boundary Condition

这个边界条件可以很方便地模拟任何金属的表面，比如金属腔的内壁。

右键单击右键点击边界所在的***弱形式偏微分方程*** 接口，选择创建三个***逐点约束*** 节点，手动选择理想电导体所在的边界，然后在三个节点的***约束表达式*** 输入框中分别输入以下内容：

如果约束位于内场的边界：

```
tM1x
tM1y
tM1z
```

如果约束位于外场的边界：

```
tM2x
tM2y
tM2z
```

### Boundary Condition: Continuity Boundary Condition

This Boundary Condition is used to connect the internal field and the external field. Its mathematical expression is:

$$ \hat{n}\times(\underline{E}_2-\underline{E}_1) $$

其中 $\hat{n}$ 是内外电磁场交界面上的法向单位矢量。

使用这个边界条件时，需要在内外电场对应的***弱形式偏微分方程*** 接口上单击右键，分别新建三个***逐点约束*** 节点，手动选择内外电场的交界面，然后在共计六个节点的***约束表达式*** 输入框中分别输入以下内容：

内场：

```
M1x - M2x
M1y - M2y
M1z - M2z
```

外场：

```
M1x - M2x
M1y - M2y
M1z - M2z
```

### Boundary Condition: Absorbing Boundary Condition

This boundary condition is applied on the external surface of radiating devices, like antennas. The absorbing boundary condition can effectively truncate the calculation domain while maintain a high accuracy.

这个边界条件适用于天线等向外辐射电磁场的模型的外表面，***吸收边界条件*** 在截断计算空间的同时可以有效地保证电磁波不会反射回来。

这个边界条件必须位于***弱约束*** 中。由于***吸收边界条件*** 只会出现在外电磁场中，所以只需右键单击外电磁场的***弱形式偏微分方程*** 接口，创建三个***弱约束***  ，选择整个模型的最外表面，并在***约束表达式*** 输入框输入以下三个表达式：

```
rcurlMx - i*k*Mtx
rcurlMy - i*k*Mty
rcurlMz - i*k*Mtz
```