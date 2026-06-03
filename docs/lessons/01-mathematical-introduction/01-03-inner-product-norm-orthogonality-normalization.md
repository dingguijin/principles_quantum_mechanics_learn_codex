# 第 1 章第 3 讲：内积、长度、正交和归一化

上一讲说：量子态要先选基底，才能写成坐标。本讲继续问：

> 有了态和基底以后，怎样判断两个态有多“接近”？怎样从态中取出某个基底方向的分量？怎样保证概率总和为 1？

答案是：引入内积。

## 1. 本讲要解决的问题

量子力学需要回答三类问题：

1. 一个态有多大，是否已经归一化？
2. 两个态是否可以清楚区分？
3. 一个态在某个基底方向上的概率振幅是多少？

这些问题都由同一个数学工具解决：

$$
\langle \phi \mid \psi \rangle
$$

它叫内积。可以先粗略读成：

> 态 $`\lvert \psi\rangle`$ 在态 $`\lvert \phi\rangle`$ 方向上的重合程度。

后面这句话会变成测量概率的基础。

## 2. 为什么需要内积这个概念

### 2.1 只知道坐标还不够

设：

$$
\lvert \psi\rangle = c_1\lvert 1\rangle + c_2\lvert 2\rangle
$$

如果基底是正交归一的，那么：

$$
|c_1|^2 + |c_2|^2
$$

就是总概率。一个合法态必须满足：

$$
|c_1|^2 + |c_2|^2 = 1
$$

但这句话其实依赖一个更深的结构：我们需要有办法定义“长度平方”。在量子力学中，长度平方写成：

$$
\langle \psi \mid \psi \rangle
$$

归一化条件就是：

$$
\langle \psi \mid \psi \rangle = 1
$$

### 2.2 测量概率需要“投影”

如果想知道 $`\lvert \psi\rangle`$ 有多少成分沿着 $`\lvert 1\rangle`$，直觉上要做“投影”。

在普通几何中，投影靠点积。在量子力学中，投影靠内积：

$$
c_1 = \langle 1 \mid \psi \rangle
$$

概率则是：

$$
P_1 = |\langle 1 \mid \psi \rangle|^2
$$

这就是内积的物理入口：它把“态的重合程度”变成“测量概率振幅”。

## 3. 公式怎么来的

### 3.1 从实向量点积开始

普通二维实向量：

$$
v = (v_1,v_2), \quad w = (w_1,w_2)
$$

点积定义为：

$$
v\cdot w = v_1w_1 + v_2w_2
$$

例子：

$$
v=(1,0),\quad w=(0,1)
$$

则：

$$
v\cdot w = 1\cdot 0 + 0\cdot 1 = 0
$$

这表示两个方向垂直。

如果：

$$
u=(1,0),\quad v=(3,0)
$$

则：

$$
u\cdot v = 3
$$

这表示 $`v`$ 在 $`u`$ 方向上有分量。

### 3.2 复向量为什么必须取复共轭

量子态的坐标通常是复数。若：

$$
\lvert v\rangle = (v_1,v_2,\dots,v_n)
$$

$$
\lvert w\rangle = (w_1,w_2,\dots,w_n)
$$

复向量内积定义为：

$$
\begin{gathered}
\langle v \mid w\rangle = \\
v_1^\ast w_1 + v_2^\ast w_2 + \cdots + v_n^\ast w_n
\end{gathered}
$$

也就是：

$$
\langle v \mid w\rangle = \sum_i v_i^\ast w_i
$$

为什么第一个向量的分量要取复共轭？

因为我们要求长度平方：

$$
\langle v\mid v\rangle
$$

必须是非负实数。否则“长度”和“概率”都无法解释。

看一个反例。设：

$$
\lvert v\rangle = (1,i)
$$

如果不用复共轭，直接算：

$$
1\cdot 1 + i\cdot i = 1 - 1 = 0
$$

这会荒谬地说一个非零向量长度为 0。

用复共轭后：

$$
\begin{gathered}
\langle v\mid v\rangle = \\
1^\ast\cdot 1 + i^\ast\cdot i \\
= 1 + (-i)i \\
= 2
\end{gathered}
$$

这才是合理的长度平方。

更一般地：

$$
\begin{gathered}
\langle v\mid v\rangle = \\
|v_1|^2 + |v_2|^2 + \cdots + |v_n|^2
\end{gathered}
$$

每一项都非负。

## 4. bra 和 ket 的关系

如果 ket 写作列向量：

$$
\lvert v\rangle =
\begin{pmatrix}
v_1\\
v_2
\end{pmatrix}
$$

那么对应 bra 写作：

$$
\langle v\rvert =
\begin{pmatrix}
v_1^\ast & v_2^\ast
\end{pmatrix}
$$

也就是：转置，再取复共轭。

于是：

$$
\langle v\mid w\rangle =
\begin{pmatrix}
v_1^\ast & v_2^\ast
\end{pmatrix}
\begin{pmatrix}
w_1\\
w_2
\end{pmatrix}
= v_1^\ast w_1 + v_2^\ast w_2
$$

这就是 Dirac 记号中 bra-ket 的计算含义。

## 5. 长度和归一化

态的长度定义为：

$$
\|\psi\| = \sqrt{\langle \psi\mid\psi\rangle}
$$

量子态要求归一化：

$$
\langle \psi\mid\psi\rangle = 1
$$

物理意义是：

> 所有可能测量结果的总概率必须等于 1。

例子：

$$
\lvert \psi\rangle = (2,i)
$$

则：

$$
\begin{gathered}
\langle \psi\mid\psi\rangle = \\
|2|^2 + |i|^2 = 4+1=5
\end{gathered}
$$

所以它还不是归一化态。长度是：

$$
\|\psi\| = \sqrt{5}
$$

归一化后：

$$
\begin{gathered}
\lvert \psi_{\text{norm}}\rangle = \\
\frac{1}{\sqrt{5}}(2,i)
\end{gathered}
$$

即：

$$
\begin{gathered}
\lvert \psi_{\text{norm}}\rangle = \\
\left(\frac{2}{\sqrt{5}},\frac{i}{\sqrt{5}}\right)
\end{gathered}
$$

检查：

$$
\begin{gathered}
\left|\frac{2}{\sqrt{5}}\right|^2 \\
{}+ \left|\frac{i}{\sqrt{5}}\right|^2 \\
= \frac45 + \frac15 = 1
\end{gathered}
$$

## 6. 正交的物理意义

如果：

$$
\langle \phi\mid\psi\rangle = 0
$$

就说 $`\lvert \phi\rangle`$ 和 $`\lvert \psi\rangle`$ 正交。

数学上，它们像几何中的垂直方向。

物理上，正交常常表示：

> 两个态可以被某个理想测量清楚地区分。

例如两个基底态：

$$
\lvert 1\rangle=(1,0),\quad \lvert 2\rangle=(0,1)
$$

内积为：

$$
\langle 1\mid 2\rangle =
(1,0)
\begin{pmatrix}
0\\
1
\end{pmatrix}
=0
$$

如果测量结果 1 和结果 2 是互斥的，它们对应的态就应当正交。第 4 章讲测量公设时，这一点会正式出现。

## 7. 正交归一基底

一组基底若满足：

$$
\langle i\mid j\rangle =
\begin{cases}
1, & i=j,\\
0, & i\ne j,
\end{cases}
$$

就叫正交归一基底。

可以用 Kronecker delta 简写：

$$
\langle i\mid j\rangle = \delta_{ij}
$$

其中：

$$
\delta_{ij} =
\begin{cases}
1, & i=j,\\
0, & i\ne j.
\end{cases}
$$

正交归一基底最大的好处是：可以直接用内积取出展开系数。

如果：

$$
\begin{gathered}
\lvert \psi\rangle = \\
c_1\lvert 1\rangle + c_2\lvert 2\rangle + \cdots + c_n\lvert n\rangle
\end{gathered}
$$

两边左乘 $`\langle k\rvert`$：

$$
\begin{gathered}
\langle k\mid\psi\rangle = \\
c_1\langle k\mid 1\rangle \\
{}+ c_2\langle k\mid 2\rangle \\
{}+ \cdots \\
{}+ c_n\langle k\mid n\rangle
\end{gathered}
$$

因为：

$$
\langle k\mid i\rangle = \delta_{ki}
$$

所以只有 $`i=k`$ 的那一项留下：

$$
\langle k\mid\psi\rangle = c_k
$$

这就是：

$$
c_k = \langle k\mid\psi\rangle
$$

它是量子力学中最常用的公式之一。

## 8. 物理意义

对于归一化态：

$$
\begin{gathered}
\lvert \psi\rangle = \\
\sum_i c_i\lvert i\rangle
\end{gathered}
$$

如果 $`\lvert i\rangle`$ 是某个测量的正交归一结果基底，那么：

$$
c_i = \langle i\mid\psi\rangle
$$

是得到第 $`i`$ 个结果的概率振幅，而：

$$
P_i = |c_i|^2 = |\langle i\mid\psi\rangle|^2
$$

是对应概率。

归一化：

$$
\langle \psi\mid\psi\rangle = 1
$$

等价于：

$$
\sum_i |c_i|^2 = 1
$$

这说明所有可能结果的概率加起来为 1。

## 9. 它和经典力学的关系

经典力学中，点积常用于计算投影、角度和功：

$$
W = \vec F\cdot \vec s
$$

这里点积告诉我们力在位移方向上的有效成分。

量子力学中的内积也像投影，但物理解释变了：

| 经典点积 | 量子内积 |
| --- | --- |
| 衡量几何方向重合 | 衡量态之间的重合 |
| 常用于长度、角度、功 | 用于概率振幅、归一化、正交 |
| 通常处理实向量 | 必须处理复向量 |
| 结果直接是几何量或物理量 | 模平方给出概率 |

所以内积是经典几何思想在量子态空间中的升级。

## 10. 它和数学的关系

本讲对应线性代数中的内积空间。一个向量空间如果配备了内积，就可以谈：

- 长度。
- 角度。
- 正交。
- 归一化。
- 投影。

量子态空间还要求复数内积满足几个关键性质：

1. $`\langle v\mid v\rangle\ge 0`$。
2. $`\langle v\mid v\rangle=0`$ 只在 $`v=0`$ 时成立。
3. $`\langle v\mid w\rangle = \langle w\mid v\rangle^\ast`$。
4. 对第二个位置线性：$`\langle v\mid aw+bz\rangle = a\langle v\mid w\rangle+b\langle v\mid z\rangle`$。

不同教材的约定可能把线性放在第一个位置，但物理教材使用 Dirac 记号时，通常对 ket 那一侧线性。

## 11. 历史关系

Schrodinger 形式中，态常写成波函数：

$$
\psi(x)
$$

两个波函数的内积写成积分：

$$
\begin{gathered}
\langle \phi\mid\psi\rangle = \\
\int \phi^\ast(x)\psi(x)\,dx
\end{gathered}
$$

这正是有限维公式：

$$
\sum_i \phi_i^\ast\psi_i
$$

的连续版本。

Dirac 记号的价值在于，它让有限维向量、无限维函数、离散基底、连续基底都能写成同一种结构：

$$
\langle \phi\mid\psi\rangle
$$

所以本讲虽然看起来是线性代数，实际上是在为波函数、算符、本征态、测量概率做统一准备。

## 12. 和后续章节的关系

本讲会在后面持续使用：

- 第 4 讲：算符的矩阵元写作 $`\langle i\mid A\mid j\rangle`$。
- 第 5 讲：本征向量正交性依赖内积。
- 第 4 章：测量概率公式会写成 $`|\langle a\mid\psi\rangle|^2`$。
- 第 5 章：波函数归一化会写成 $`\int |\psi(x)|^2dx=1`$。
- 第 9 章：不确定性关系的证明依赖内积和 Cauchy-Schwarz 不等式。
- 第 12-15 章：角动量和自旋态大量使用正交归一基底。

如果不熟悉内积，后面的“投影”“本征态展开”“概率振幅”都会变成死记硬背。

## 13. 最小计算例子

设：

$$
\lvert \psi\rangle =
\begin{pmatrix}
1/2\\
\sqrt{3}/2
\end{pmatrix}
$$

计算归一化：

$$
\begin{gathered}
\langle \psi\mid\psi\rangle = \\
\left|\frac12\right|^2 \\
{}+ \left|\frac{\sqrt{3}}{2}\right|^2 \\
= \frac14+\frac34=1
\end{gathered}
$$

所以它是归一化态。

再设：

$$
\lvert \phi\rangle =
\begin{pmatrix}
\sqrt{3}/2\\
-1/2
\end{pmatrix}
$$

计算内积：

$$
\begin{gathered}
\langle \phi\mid\psi\rangle = \\
\frac{\sqrt{3}}{2}\cdot \frac12 \\
{}+ \left(-\frac12\right)\cdot \frac{\sqrt{3}}{2} \\
=0
\end{gathered}
$$

所以 $`\lvert \phi\rangle`$ 和 $`\lvert \psi\rangle`$ 正交。

## 14. 常见误解

### 误解 1：内积就是普通乘法

不是。内积是两个向量之间的运算，结果是一个数。复向量内积还必须对 bra 一侧取复共轭。

### 误解 2：$`\langle \psi\mid\psi\rangle`$ 是态

不是。它是一个数，表示态的长度平方。归一化态满足它等于 1。

### 误解 3：正交只是数学垂直，没有物理意义

在量子力学中，正交通常意味着可以被理想测量区分。不同测量结果对应的态应当正交。

### 误解 4：归一化只是数学规定

归一化的物理意义是总概率为 1。如果态没有归一化，计算概率前必须先归一化。

## 15. 练习

### 练习 1

设：

$$
\lvert v\rangle = (1,i)
$$

计算 $`\langle v\mid v\rangle`$，并写出归一化后的向量。

### 练习 2

设：

$$
\begin{gathered}
\lvert a\rangle = \\
\frac{1}{\sqrt{2}}(1,1), \\
\quad \\
\lvert b\rangle = \\
\frac{1}{\sqrt{2}}(1,-1)
\end{gathered}
$$

判断它们是否归一化，是否正交。

### 练习 3

设正交归一基底为 $`\lvert 1\rangle,\lvert 2\rangle,\lvert 3\rangle`$，且：

$$
\begin{gathered}
\lvert \psi\rangle = \\
\frac12\lvert 1\rangle \\
{}+ \frac{i}{2}\lvert 2\rangle \\
{}+ \frac{1}{\sqrt{2}}\lvert 3\rangle
\end{gathered}
$$

求三个测量结果的概率，并判断该态是否归一化。

### 练习 4

解释为什么复内积不能简单定义为：

$$
v_1w_1+v_2w_2+\cdots+v_nw_n
$$

### 练习 5

设：

$$
\begin{gathered}
\lvert \psi\rangle = \\
\frac{3}{5}\lvert 1\rangle \\
{}+ \frac{4}{5}\lvert 2\rangle
\end{gathered}
$$

其中 $`\lvert 1\rangle,\lvert 2\rangle`$ 是正交归一基底。计算：

$$
\begin{gathered}
\langle 1\mid\psi\rangle,\quad \\
\langle 2\mid\psi\rangle
\end{gathered}
$$

并说明它们的物理意义。

## 16. 解答

### 解答 1

因为：

$$
\lvert v\rangle=(1,i)
$$

所以：

$$
\begin{gathered}
\langle v\mid v\rangle = \\
1^\ast\cdot 1+i^\ast\cdot i \\
=1+(-i)i \\
=2
\end{gathered}
$$

长度为：

$$
\sqrt{2}
$$

归一化后：

$$
\begin{gathered}
\lvert v_{\text{norm}}\rangle = \\
\frac{1}{\sqrt{2}}(1,i)
\end{gathered}
$$

### 解答 2

先算 $`\lvert a\rangle`$：

$$
\begin{gathered}
\langle a\mid a\rangle = \\
\frac12+\frac12=1
\end{gathered}
$$

再算 $`\lvert b\rangle`$：

$$
\begin{gathered}
\langle b\mid b\rangle = \\
\frac12+\frac12=1
\end{gathered}
$$

所以二者都归一化。

内积：

$$
\begin{gathered}
\langle a\mid b\rangle = \\
\frac{1}{\sqrt{2}}\frac{1}{\sqrt{2}} \\
{}+ \frac{1}{\sqrt{2}}\left(-\frac{1}{\sqrt{2}}\right) \\
=\frac12-\frac12=0
\end{gathered}
$$

所以它们正交。

### 解答 3

三个振幅分别为：

$$
c_1=\frac12,\quad c_2=\frac{i}{2},\quad c_3=\frac{1}{\sqrt{2}}
$$

概率为：

$$
P_1=\left|\frac12\right|^2=\frac14
$$

$$
P_2=\left|\frac{i}{2}\right|^2=\frac14
$$

$$
P_3=\left|\frac{1}{\sqrt{2}}\right|^2=\frac12
$$

总和：

$$
P_1+P_2+P_3=\frac14+\frac14+\frac12=1
$$

所以该态已经归一化。

### 解答 4

如果不取复共轭，非零复向量可能得到零长度平方。例如：

$$
v=(1,i)
$$

直接相乘会得到：

$$
1\cdot 1+i\cdot i=1-1=0
$$

这不可能作为长度平方，也不能作为概率总和。因此复内积必须取复共轭，使得：

$$
\langle v\mid v\rangle=\sum_i |v_i|^2\ge 0
$$

### 解答 5

因为基底正交归一：

$$
\langle 1\mid 1\rangle=1,\quad \langle 1\mid 2\rangle=0
$$

所以：

$$
\begin{gathered}
\langle 1\mid\psi\rangle = \\
\frac35\langle 1\mid 1\rangle \\
+\frac45\langle 1\mid 2\rangle \\
=\frac35
\end{gathered}
$$

同理：

$$
\begin{gathered}
\langle 2\mid\psi\rangle = \\
\frac35\langle 2\mid 1\rangle \\
+\frac45\langle 2\mid 2\rangle \\
=\frac45
\end{gathered}
$$

它们分别是态 $`\lvert \psi\rangle`$ 在 $`\lvert 1\rangle`$、$`\lvert 2\rangle`$ 方向上的概率振幅。对应概率为：

$$
P_1=\frac{9}{25},\quad P_2=\frac{16}{25}
$$

## 17. 本讲必须记住的三句话

1. 内积 $`\langle \phi\mid\psi\rangle`$ 衡量两个态的重合，并给出概率振幅。
2. 复内积必须取复共轭，否则长度平方不能保证非负。
3. 正交归一基底中，展开系数可以用 $`c_i=\langle i\mid\psi\rangle`$ 直接取出。
