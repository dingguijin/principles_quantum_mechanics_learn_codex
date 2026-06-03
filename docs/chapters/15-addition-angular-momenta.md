# 15. Addition of Angular Momenta

第 12 章讲了单个角动量的代数，第 14 章讲了自旋。真实系统中，经常同时存在多个角动量。

最重要的例子是原子中的电子：

$$
\mathbf L
$$

是轨道角动量，

$$
\mathbf S
$$

是自旋角动量。

总角动量是：

$$
\mathbf J=\mathbf L+\mathbf S
$$

本章要解决的问题是：

> 已知两个角动量 \(j_1,j_2\)，总角动量 \(j\) 可以取哪些值？两套基底之间如何转换？

## 本章学习路线

建议分 6 次学习：

1. [第 1 讲：为什么需要角动量加法](../lessons/15-addition-angular-momenta/15-01-why-add-angular-momenta.md)
2. [第 2 讲：非耦合基底和耦合基底](../lessons/15-addition-angular-momenta/15-02-coupled-and-uncoupled-bases.md)
3. [第 3 讲：总角动量允许范围](../lessons/15-addition-angular-momenta/15-03-allowed-total-angular-momentum.md)
4. [第 4 讲：Clebsch-Gordan 系数是什么](../lessons/15-addition-angular-momenta/15-04-clebsch-gordan-coefficients.md)
5. [第 5 讲：两个自旋 \(1/2\) 的完整例子](../lessons/15-addition-angular-momenta/15-05-two-spin-half-example.md)
6. [第 6 讲：自旋-轨道耦合、选择规则和后续章节入口](../lessons/15-addition-angular-momenta/15-06-spin-orbit-selection-rules-entry.md)

## 第 1 讲：为什么需要角动量加法

如果系统只有一个角动量，可以用：

$$
|j,m\rangle
$$

标记。

但若系统有两个角动量：

$$
\mathbf J_1,\quad \mathbf J_2
$$

就要描述它们的组合。

总角动量定义为：

$$
\mathbf J=\mathbf J_1+\mathbf J_2
$$

总 \(z\) 分量为：

$$
J_z=J_{1z}+J_{2z}
$$

总角动量在转动对称系统中往往比单个角动量更自然。

例如自旋-轨道耦合中，哈密顿量含有：

$$
\mathbf L\cdot\mathbf S
$$

此时用总角动量 \(\mathbf J=\mathbf L+\mathbf S\) 分类能级更方便。

## 第 2 讲：两套基底

两个角动量可以先分别标记。

这叫非耦合基底：

$$
|j_1,m_1\rangle|j_2,m_2\rangle
$$

常简写为：

$$
|j_1,m_1;j_2,m_2\rangle
$$

它适合讨论两个角动量各自的投影。

也可以用总角动量标记。

这叫耦合基底：

$$
|j_1,j_2;j,m\rangle
$$

其中：

$$
\mathbf J=\mathbf J_1+\mathbf J_2
$$

且：

$$
J^2|j_1,j_2;j,m\rangle=\hbar^2j(j+1)|j_1,j_2;j,m\rangle
$$

$$
J_z|j_1,j_2;j,m\rangle=\hbar m|j_1,j_2;j,m\rangle
$$

两套基底描述同一个态空间，只是坐标不同。

## 第 3 讲：允许的总角动量

给定 \(j_1,j_2\)，总角动量 \(j\) 的允许值为：

$$
j=|j_1-j_2|,\ |j_1-j_2|+1,\ \cdots,\ j_1+j_2
$$

对每个 \(j\)，

$$
m=-j,-j+1,\cdots,j
$$

这和经典向量加法的三角形限制有关：两个向量相加，总大小不能超过两者之和，也不能小于两者差。

但量子中允许值是离散的。

维数检查也一致：

非耦合基底维数：

$$
(2j_1+1)(2j_2+1)
$$

耦合基底维数：

$$
\sum_{j=|j_1-j_2|}^{j_1+j_2}(2j+1)
$$

二者相等。

## 第 4 讲：Clebsch-Gordan 系数

非耦合基底和耦合基底之间的转换写成：

$$
|j_1,j_2;j,m\rangle
=\sum_{m_1,m_2}
|j_1,m_1;j_2,m_2\rangle
\langle j_1,m_1;j_2,m_2|j_1,j_2;j,m\rangle
$$

其中：

$$
\langle j_1,m_1;j_2,m_2|j_1,j_2;j,m\rangle
$$

叫 Clebsch-Gordan 系数。

它本质上就是换基底矩阵元。

重要选择规则：

$$
m=m_1+m_2
$$

如果这个条件不满足，对应系数为 0。

## 第 5 讲：两个自旋 \(1/2\)

两个自旋 \(1/2\) 的非耦合基底是四个态：

$$
|\uparrow\uparrow\rangle,\quad
|\uparrow\downarrow\rangle,\quad
|\downarrow\uparrow\rangle,\quad
|\downarrow\downarrow\rangle
$$

允许的总角动量：

$$
j=1,\quad j=0
$$

三重态：

$$
|1,1\rangle=|\uparrow\uparrow\rangle
$$

$$
|1,0\rangle=\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle+|\downarrow\uparrow\rangle\right)
$$

$$
|1,-1\rangle=|\downarrow\downarrow\rangle
$$

单重态：

$$
|0,0\rangle=\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle-|\downarrow\uparrow\rangle\right)
$$

这四个态构成同一个四维空间的另一组正交基底。

## 第 6 讲：物理应用

角动量加法是原子物理的核心工具。

电子的轨道角动量和自旋组合成：

$$
\mathbf J=\mathbf L+\mathbf S
$$

若 \(s=1/2\)，给定 \(l\) 时：

$$
j=l+\frac12,\quad j=l-\frac12
$$

其中 \(l=0\) 时只允许：

$$
j=\frac12
$$

自旋-轨道耦合常含：

$$
\mathbf L\cdot\mathbf S
$$

利用：

$$
\mathbf J^2=(\mathbf L+\mathbf S)^2
=L^2+S^2+2\mathbf L\cdot\mathbf S
$$

得到：

$$
\mathbf L\cdot\mathbf S
=\frac12(J^2-L^2-S^2)
$$

所以在耦合基底中，自旋-轨道耦合容易对角化。

## 本章总复习

总角动量：

$$
\mathbf J=\mathbf J_1+\mathbf J_2
$$

非耦合基底：

$$
|j_1,m_1;j_2,m_2\rangle
$$

耦合基底：

$$
|j_1,j_2;j,m\rangle
$$

允许范围：

$$
j=|j_1-j_2|,\cdots,j_1+j_2
$$

投影关系：

$$
m=m_1+m_2
$$

Clebsch-Gordan 系数是两套基底之间的换基底系数。

两个自旋 \(1/2\)：

$$
\frac12\otimes\frac12=1\oplus0
$$

自旋-轨道耦合：

$$
\mathbf L\cdot\mathbf S
=\frac12(J^2-L^2-S^2)
$$

## 本章作业

### A. 允许的 \(j\)

若 \(j_1=1\)，\(j_2=1/2\)，允许的总角动量 \(j\) 是哪些？

### B. 投影关系

若 \(m_1=1/2\)，\(m_2=-1\)，总 \(m\) 是多少？

### C. 维数检查

两个自旋 \(1/2\) 的非耦合空间维数是多少？耦合后各 \(j\) 子空间维数是多少？

### D. 单重态

写出两个自旋 \(1/2\) 的单重态。

### E. 自旋-轨道耦合

为什么 \(\mathbf L\cdot\mathbf S\) 在耦合基底中更容易处理？

## 参考答案

### A

允许：

$$
j=\left|1-\frac12\right|,\quad 1+\frac12
$$

即：

$$
j=\frac12,\quad \frac32
$$

### B

$$
m=m_1+m_2=\frac12-1=-\frac12
$$

### C

非耦合维数：

$$
2\times2=4
$$

耦合后：

- \(j=1\)：维数 \(2j+1=3\)。
- \(j=0\)：维数 \(1\)。

总维数：

$$
3+1=4
$$

### D

$$
|0,0\rangle=\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle-|\downarrow\uparrow\rangle\right)
$$

### E

因为：

$$
\mathbf L\cdot\mathbf S
=\frac12(J^2-L^2-S^2)
$$

耦合基底同时标记 \(J^2,L^2,S^2\)，因此该项容易用本征值计算。
