# 14. Spin

自旋是量子力学中最重要、也最容易被误解的概念之一。

它叫“spin”，但不能理解成电子这个小球真的在自转。更准确地说：

> 自旋是粒子内禀的角动量，是量子态在空间转动下如何变换的内部自由度。

第 12 章的轨道角动量来自：

$$
\mathbf L=\mathbf r\times\mathbf p
$$

但自旋不是 $`\mathbf r\times\mathbf p`$。它不来自粒子绕某点运动，而是粒子本身携带的角动量。

对自旋 $`1/2`$ 粒子，态空间是二维的：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

其中：

$$
|a|^2+|b|^2=1
$$

本章的关键是理解：量子态空间可以有“内部维度”，不一定来自普通空间坐标。

## 本章学习路线

建议分 6 次学习：

1. [第 1 讲：为什么需要自旋，它不是经典小球自转](../lessons/14-spin/14-01-why-spin-is-needed.md)
2. [第 2 讲：自旋 $`1/2`$ 的二维态空间](../lessons/14-spin/14-02-spin-half-state-space.md)
3. [第 3 讲：Pauli 矩阵和自旋算符](../lessons/14-spin/14-03-pauli-matrices-spin-operators.md)
4. [第 4 讲：不同方向自旋测量和概率](../lessons/14-spin/14-04-spin-measurements-directions.md)
5. [第 5 讲：Stern-Gerlach 实验和态制备](../lessons/14-spin/14-05-stern-gerlach-state-preparation.md)
6. [第 6 讲：磁矩、自旋进动和后续角动量耦合入口](../lessons/14-spin/14-06-magnetic-moment-precession-coupling-entry.md)

## 第 1 讲：为什么需要自旋

轨道角动量不能解释所有实验事实。

例如电子在磁场中的能级分裂、Stern-Gerlach 型实验、原子光谱精细结构，都说明粒子还有一种内禀角动量。

这个角动量不是由位置和动量产生的。电子即使没有轨道角动量，也可以有自旋。

自旋满足角动量代数：

$$
[S_i,S_j]=i\hbar\epsilon_{ijk}S_k
$$

但它作用在内部态空间，而不是直接作用在 $`\psi(x,y,z)`$ 的坐标变量上。

## 第 2 讲：自旋 $`1/2`$ 态空间

自旋 $`1/2`$ 系统沿 $`z`$ 方向测量只有两个可能结果：

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

因此可以用两个基矢：

$$
|\uparrow\rangle,\quad |\downarrow\rangle
$$

任意自旋态写成：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

用列向量表示：

$$
|\uparrow\rangle=
\begin{pmatrix}
1\\
0
\end{pmatrix},
\quad
|\downarrow\rangle=
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

于是：

$$
|\psi\rangle=
\begin{pmatrix}
a\\
b
\end{pmatrix}
$$

归一化：

$$
|a|^2+|b|^2=1
$$

## 第 3 讲：Pauli 矩阵

自旋 $`1/2`$ 的三个方向算符可写成：

$$
S_x=\frac{\hbar}{2}\sigma_x,\quad
S_y=\frac{\hbar}{2}\sigma_y,\quad
S_z=\frac{\hbar}{2}\sigma_z
$$

其中 Pauli 矩阵为：

$$
\sigma_x=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
$$

$$
\sigma_y=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix}
$$

$$
\sigma_z=
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}
$$

它们是厄米矩阵，所以对应可观测量。

它们满足：

$$
[\sigma_x,\sigma_y]=2i\sigma_z
$$

因此：

$$
[S_x,S_y]=i\hbar S_z
$$

这正是角动量代数。

## 第 4 讲：不同方向的自旋测量

沿 $`z`$ 方向测量时，$`|\uparrow\rangle`$、$`|\downarrow\rangle`$ 是 $`S_z`$ 的本征态：

$$
S_z|\uparrow\rangle=\frac{\hbar}{2}|\uparrow\rangle
$$

$$
S_z|\downarrow\rangle=-\frac{\hbar}{2}|\downarrow\rangle
$$

若：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

则测得 $`+\hbar/2`$ 的概率是：

$$
|a|^2
$$

测得 $`-\hbar/2`$ 的概率是：

$$
|b|^2
$$

但沿 $`x`$ 方向测量时，要用 $`S_x`$ 的本征态：

$$
|\uparrow_x\rangle=\frac{1}{\sqrt2}(|\uparrow\rangle+|\downarrow\rangle)
$$

$$
|\downarrow_x\rangle=\frac{1}{\sqrt2}(|\uparrow\rangle-|\downarrow\rangle)
$$

所以同一个态在不同方向下会有不同概率分布。

## 第 5 讲：Stern-Gerlach 实验

Stern-Gerlach 实验把粒子束通过非均匀磁场。

如果自旋投影连续，屏幕上应出现连续分布。

但自旋 $`1/2`$ 系统沿某方向只分成两束，对应：

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

这说明自旋分量量子化。

更重要的是，如果先筛选出 $`S_z=+\hbar/2`$ 的粒子，再测 $`S_x`$，会再次分成两束。这说明：

> 沿 $`z`$ 方向确定，不代表沿 $`x`$ 方向也确定。

这是非对易算符和测量投影的直接实验图像。

## 第 6 讲：磁矩和后续章节入口

带电粒子的自旋通常伴随磁矩。

电子自旋磁矩可写成：

$$
\boldsymbol\mu_s=-g\frac{e}{2m_e}\mathbf S
$$

其中电子的 $`g`$ 因子近似为 2。

磁场中的相互作用能量：

$$
H=-\boldsymbol\mu_s\cdot\mathbf B
$$

这会导致自旋进动和能级分裂。

本章之后，第 15 章会研究如何把不同角动量加起来，例如轨道角动量 $`\mathbf L`$ 和自旋 $`\mathbf S`$ 组合成总角动量：

$$
\mathbf J=\mathbf L+\mathbf S
$$

这是理解精细结构、自旋-轨道耦合和原子态标记的基础。

## 本章总复习

自旋 $`1/2`$ 态：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

归一化：

$$
|a|^2+|b|^2=1
$$

自旋算符：

$$
S_i=\frac{\hbar}{2}\sigma_i
$$

Pauli 矩阵对易关系：

$$
[\sigma_i,\sigma_j]=2i\epsilon_{ijk}\sigma_k
$$

自旋角动量代数：

$$
[S_i,S_j]=i\hbar\epsilon_{ijk}S_k
$$

自旋 $`z`$ 分量本征值：

$$
\pm\frac{\hbar}{2}
$$

总角动量入口：

$$
\mathbf J=\mathbf L+\mathbf S
$$

## 本章作业

### A. 自旋态归一化

若：

$$
|\psi\rangle=\frac{1}{2}|\uparrow\rangle+\frac{\sqrt3}{2}|\downarrow\rangle
$$

求测量 $`S_z`$ 得到 $`+\hbar/2`$ 和 $`-\hbar/2`$ 的概率。

### B. Pauli 矩阵

写出 $`\sigma_z`$ 的两个本征值。

### C. 换方向测量

如果态是 $`|\uparrow\rangle`$，测量 $`S_x`$ 得到 $`+\hbar/2`$ 的概率是多少？

### D. 非对易

为什么不能同时确定 $`S_x`$ 和 $`S_z`$？

### E. 磁场

磁场为什么会影响自旋能级？

## 参考答案

### A

概率为系数模平方：

$$
P(+)=\left|\frac12\right|^2=\frac14
$$

$$
P(-)=\left|\frac{\sqrt3}{2}\right|^2=\frac34
$$

### B

$$
\sigma_z=
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}
$$

所以本征值是：

$$
+1,\quad -1
$$

对应 $`S_z`$ 本征值：

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

### C

因为：

$$
|\uparrow_x\rangle=\frac{1}{\sqrt2}(|\uparrow\rangle+|\downarrow\rangle)
$$

所以：

$$
\langle \uparrow_x|\uparrow\rangle=\frac{1}{\sqrt2}
$$

概率为：

$$
\frac12
$$

### D

因为：

$$
[S_x,S_z]\ne0
$$

非对易观测量不能在一般态中同时确定。

### E

自旋带有磁矩，磁矩和外磁场有相互作用：

$$
H=-\boldsymbol\mu_s\cdot\mathbf B
$$

不同自旋投影对应不同能量，因此磁场会造成能级分裂。
