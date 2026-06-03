# 12. Rotational Invariance and Angular Momentum

第 11 章说明：连续对称性有生成元，生成元若与哈密顿量对易，就给出守恒量。

本章把这个原则用于空间转动。

经典力学中，轨道角动量是：

$$
\mathbf L=\mathbf r\times\mathbf p
$$

量子力学中，$`\mathbf r`$ 和 $`\mathbf p`$ 变成算符，角动量也变成算符。更重要的是，三个分量之间不再彼此对易：

$$
[L_x,L_y]=i\hbar L_z
$$

循环置换得到另外两个关系。

这意味着角动量的三个分量不能同时任意确定。通常能同时讨论的是：

$$
L^2,\quad L_z
$$

它们有共同本征态，用量子数 $`l,m`$ 标记。

## 本章学习路线

建议分 6 次学习：

1. [第 1 讲：转动不变性，为什么角动量是转动生成元](../lessons/12-rotational-invariance-angular-momentum/12-01-rotations-and-generators.md)
2. [第 2 讲：轨道角动量算符从 $`\mathbf r\times\mathbf p`$ 来](../lessons/12-rotational-invariance-angular-momentum/12-02-orbital-angular-momentum-operator.md)
3. [第 3 讲：角动量对易关系和非同时确定性](../lessons/12-rotational-invariance-angular-momentum/12-03-angular-momentum-commutators.md)
4. [第 4 讲：$`L^2`$、$`L_z`$ 和角动量量子数](../lessons/12-rotational-invariance-angular-momentum/12-04-l2-lz-quantum-numbers.md)
5. [第 5 讲：升降算符 $`L_\pm`$ 和 $`m`$ 的阶梯结构](../lessons/12-rotational-invariance-angular-momentum/12-05-ladder-operators.md)
6. [第 6 讲：球谐函数、简并和后续章节入口](../lessons/12-rotational-invariance-angular-momentum/12-06-spherical-harmonics-degeneracy.md)

## 第 1 讲：转动和生成元

绕 $`z`$ 轴转动角度 $`\phi`$ 的量子变换写成：

$$
U_z(\phi)=e^{-i\phi L_z/\hbar}
$$

这里 $`L_z`$ 是绕 $`z`$ 轴转动的生成元。

这和第 11 章完全平行：

$$
U(a)=e^{-ia p/\hbar}
$$

平移由动量生成；转动由角动量生成。

若哈密顿量在转动下不变：

$$
U^\dagger H U=H
$$

则对应生成元与哈密顿量对易：

$$
[H,L_z]=0
$$

如果所有方向转动都不变，则：

$$
[H,L_x]=[H,L_y]=[H,L_z]=0
$$

角动量守恒。

## 第 2 讲：轨道角动量算符

经典轨道角动量：

$$
\mathbf L=\mathbf r\times\mathbf p
$$

分量为：

$$
L_x=yp_z-zp_y
$$

$$
L_y=zp_x-xp_z
$$

$$
L_z=xp_y-yp_x
$$

量子力学中：

$$
p_x=-i\hbar\frac{\partial}{\partial x},\quad
p_y=-i\hbar\frac{\partial}{\partial y},\quad
p_z=-i\hbar\frac{\partial}{\partial z}
$$

所以：

$$
L_z=-i\hbar\left(x\frac{\partial}{\partial y}-y\frac{\partial}{\partial x}\right)
$$

在球坐标中，绕 $`z`$ 轴转动就是改变方位角 $`\phi`$，因此：

$$
L_z=-i\hbar\frac{\partial}{\partial \phi}
$$

这个公式非常重要，因为它直接说明 $`m`$ 量子数来自方位角相位。

## 第 3 讲：角动量代数

角动量算符满足：

$$
[L_x,L_y]=i\hbar L_z
$$

$$
[L_y,L_z]=i\hbar L_x
$$

$$
[L_z,L_x]=i\hbar L_y
$$

紧凑写法：

$$
[L_i,L_j]=i\hbar\epsilon_{ijk}L_k
$$

其中 $`\epsilon_{ijk}`$ 是 Levi-Civita 符号。

这组关系说明角动量三个分量不能同时对角化。

例如：

$$
[L_x,L_y]\ne0
$$

所以 $`L_x`$ 和 $`L_y`$ 不能在一般态中同时确定。

但定义：

$$
L^2=L_x^2+L_y^2+L_z^2
$$

可以证明：

$$
[L^2,L_x]=[L^2,L_y]=[L^2,L_z]=0
$$

所以可以同时测量：

$$
L^2,\quad L_z
$$

## 第 4 讲：角动量量子数

共同本征态写作：

$$
|l,m\rangle
$$

满足：

$$
L^2|l,m\rangle=\hbar^2l(l+1)|l,m\rangle
$$

$$
L_z|l,m\rangle=\hbar m|l,m\rangle
$$

其中：

$$
l=0,1,2,\cdots
$$

对给定 $`l`$，

$$
m=-l,-l+1,\cdots,l-1,l
$$

因此每个 $`l`$ 有：

$$
2l+1
$$

个 $`m`$ 值。

物理意义：

- $`l`$ 描述角动量总大小。
- $`m`$ 描述角动量在选定 $`z`$ 轴上的分量。

注意 $`L^2`$ 的本征值不是 $`\hbar^2l^2`$，而是：

$$
\hbar^2l(l+1)
$$

这来自角动量代数的阶梯结构。

## 第 5 讲：升降算符

定义：

$$
L_+=L_x+iL_y
$$

$$
L_-=L_x-iL_y
$$

它们改变 $`m`$：

$$
L_+|l,m\rangle
=\hbar\sqrt{l(l+1)-m(m+1)}\,|l,m+1\rangle
$$

$$
L_-|l,m\rangle
=\hbar\sqrt{l(l+1)-m(m-1)}\,|l,m-1\rangle
$$

但它们不改变 $`l`$。

因为 $`m`$ 不能无限上升或下降，所以阶梯必须在某处停止。这迫使 $`m`$ 的取值是：

$$
-l,-l+1,\cdots,l
$$

也迫使 $`l`$ 是非负整数或半整数。对轨道角动量，单值波函数要求 $`l`$ 为非负整数。

## 第 6 讲：球谐函数和转动不变性

轨道角动量的共同本征函数是球谐函数：

$$
Y_l^m(\theta,\phi)
$$

它们满足：

$$
L^2Y_l^m=\hbar^2l(l+1)Y_l^m
$$

$$
L_zY_l^m=\hbar mY_l^m
$$

球谐函数是三维中心势问题的角向基底。

如果势能只依赖半径：

$$
V=V(r)
$$

则系统具有转动不变性。哈密顿量与角动量对易：

$$
[H,L^2]=0,\quad [H,L_z]=0
$$

因此能量本征态可以按 $`l,m`$ 分类。

在纯中心势中，能量通常不依赖 $`m`$，所以出现 $`2l+1`$ 重简并。

这直接进入第 13 章氢原子。

## 本章总复习

转动生成元：

$$
U_z(\phi)=e^{-i\phi L_z/\hbar}
$$

轨道角动量：

$$
\mathbf L=\mathbf r\times\mathbf p
$$

角动量代数：

$$
[L_i,L_j]=i\hbar\epsilon_{ijk}L_k
$$

总角动量平方：

$$
L^2=L_x^2+L_y^2+L_z^2
$$

共同本征值：

$$
L^2|l,m\rangle=\hbar^2l(l+1)|l,m\rangle
$$

$$
L_z|l,m\rangle=\hbar m|l,m\rangle
$$

升降算符：

$$
L_\pm=L_x\pm iL_y
$$

球谐函数：

$$
Y_l^m(\theta,\phi)
$$

是轨道角动量的角向本征函数。

## 本章作业

### A. 角动量分量

从 $`\mathbf L=\mathbf r\times\mathbf p`$ 写出 $`L_z`$。

### B. 对易关系

为什么 $`L_x`$ 和 $`L_y`$ 不能同时任意确定？

### C. 量子数

给定 $`l=2`$，允许的 $`m`$ 有哪些？共有几个？

### D. 升降算符

$`L_+`$ 对 $`|l,m\rangle`$ 做什么？

### E. 转动不变性

为什么中心势 $`V(r)`$ 的能量本征态可以按 $`l,m`$ 分类？

## 参考答案

### A

叉乘给出：

$$
L_z=xp_y-yp_x
$$

坐标表象中：

$$
L_z=-i\hbar\left(x\frac{\partial}{\partial y}-y\frac{\partial}{\partial x}\right)
$$

### B

因为：

$$
[L_x,L_y]=i\hbar L_z
$$

通常不为零。非对易观测量不能在一般态中同时有确定值。

### C

若 $`l=2`$，则：

$$
m=-2,-1,0,1,2
$$

共有：

$$
2l+1=5
$$

个。

### D

它把 $`m`$ 提高一格：

$$
L_+|l,m\rangle
\propto |l,m+1\rangle
$$

但不改变 $`l`$。

### E

中心势只依赖 $`r`$，空间转动不改变 $`r`$，所以哈密顿量与转动生成元对易。于是可以同时选取 $`H,L^2,L_z`$ 的共同本征态，用 $`l,m`$ 分类。
