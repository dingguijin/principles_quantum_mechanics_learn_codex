# 20. The Dirac Equation

Dirac 方程把量子力学和狭义相对论放到同一个框架中。它解决的问题不是“再找一个更复杂的波动方程”这么简单，而是：怎样写出一个既符合相对论能量关系、又像薛定谔方程那样一阶时间演化、并且有合理概率解释的量子方程？

这章最重要的结果有三个：波函数必须变成多分量旋量；自旋 \(1/2\) 自然出现；负能量解迫使我们走向反粒子和量子场论。

## 本章逐讲

| 讲义 | 主题 |
| --- | --- |
| [第 1 讲：为什么薛定谔方程不够相对论](../lessons/20-dirac-equation/20-01-why-relativistic-quantum.md) | 非相对论能量、Lorentz 对称、光速尺度 |
| [第 2 讲：Klein-Gordon 方程和它的困难](../lessons/20-dirac-equation/20-02-klein-gordon-difficulty.md) | 二阶时间导数、概率密度问题 |
| [第 3 讲：Dirac 的线性化思路](../lessons/20-dirac-equation/20-03-dirac-linearization.md) | 一阶方程、alpha beta 矩阵、反对易关系 |
| [第 4 讲：矩阵、旋量和自旋的出现](../lessons/20-dirac-equation/20-04-matrices-spinors-spin.md) | 多分量波函数、Clifford 代数、自旋 |
| [第 5 讲：非相对论极限和 Pauli 方程入口](../lessons/20-dirac-equation/20-05-nonrelativistic-limit-pauli.md) | 大小分量、磁矩、自旋-磁场耦合 |
| [第 6 讲：负能量、反粒子和后续入口](../lessons/20-dirac-equation/20-06-negative-energy-antiparticles-next.md) | 负能量解、正电子、量子场论 |

## 20.1 为什么需要相对论量子方程

非相对论薛定谔方程基于：

$$
E=\frac{p^2}{2m}+V.
$$

自由粒子时：

$$
i\hbar\frac{\partial\psi}{\partial t}
=
-\frac{\hbar^2}{2m}\nabla^2\psi.
$$

它对时间是一阶导数，对空间是二阶导数。这适合 Galilean 对称的非相对论世界，但不适合狭义相对论。相对论中时间和空间应以 Lorentz 方式统一，能量和动量满足：

$$
E^2=p^2c^2+m^2c^4.
$$

当粒子速度接近 \(c\)、能量接近或超过 \(mc^2\)、或者涉及粒子产生湮灭时，非相对论方程就不够。

## 20.2 先尝试 Klein-Gordon 方程

直接把

$$
E^2=p^2c^2+m^2c^4
$$

量子化：

$$
E\to i\hbar\frac{\partial}{\partial t},
\qquad
\mathbf p\to -i\hbar\nabla,
$$

得到：

$$
-\hbar^2\frac{\partial^2\psi}{\partial t^2}
=
-\hbar^2c^2\nabla^2\psi+m^2c^4\psi.
$$

这就是 Klein-Gordon 方程的形式。它确实相对论协变，但对时间是二阶导数，导致概率解释不像薛定谔方程那样直接。对应的“密度”不一定正定，不能简单解释为粒子概率密度。

这不是说 Klein-Gordon 方程没用；它适合描述自旋 0 场。但如果我们想描述电子，并保留一阶时间演化和正定概率密度，Dirac 的方案更合适。

## 20.3 Dirac 的线性化

Dirac 希望方程对时间和空间导数都一阶：

$$
i\hbar\frac{\partial\psi}{\partial t}
=
\left(c\,\boldsymbol{\alpha}\cdot\mathbf p+\beta mc^2\right)\psi.
$$

记

$$
H_D=c\,\boldsymbol{\alpha}\cdot\mathbf p+\beta mc^2.
$$

为了让这个方程仍满足相对论能量关系，要求：

$$
H_D^2=p^2c^2+m^2c^4.
$$

展开平方：

$$
H_D^2
=
c^2\sum_{i,j}\alpha_i\alpha_jp_ip_j
+mc^3\sum_i(\alpha_i\beta+\beta\alpha_i)p_i
+\beta^2m^2c^4.
$$

要让交叉项消失，并让 \(p_i^2\) 的系数正确，矩阵必须满足反对易关系：

$$
\{\alpha_i,\alpha_j\}=2\delta_{ij}I,
\qquad
\{\alpha_i,\beta\}=0,
\qquad
\beta^2=I.
$$

这些 \(\alpha_i,\beta\) 不可能都是普通数，必须是矩阵。因此波函数 \(\psi\) 也不能只有一个复数分量，而必须是多分量对象。

## 20.4 旋量和自旋

最小可行矩阵是 \(4\times4\)，所以 Dirac 波函数是四分量旋量：

$$
\psi=
\begin{pmatrix}
\psi_1\\
\psi_2\\
\psi_3\\
\psi_4
\end{pmatrix}.
$$

这四个分量不是四个普通空间方向，而是内部自由度。它们编码粒子/反粒子和自旋自由度。

Dirac 方程的一个重大成功是：自旋 \(1/2\) 不是额外硬加进去的标签，而是相对论一阶方程和矩阵代数自然带来的结构。进一步把电磁场耦合进去，会出现正确的电子磁矩结构，并导向 Pauli 方程。

## 20.5 非相对论极限

在低速极限 \(p\ll mc\) 下，总能量包含很大的静止能：

$$
E\approx mc^2+\frac{p^2}{2m}.
$$

把快速相位 \(e^{-imc^2t/\hbar}\) 提出来后，Dirac 方程可约化为非相对论形式。若有电磁场，进一步得到包含自旋-磁场耦合的 Pauli 方程：

$$
H_{\text{Pauli}}
=
\frac{1}{2m}(\mathbf p-q\mathbf A)^2
+q\phi
-\frac{q\hbar}{2m}\boldsymbol{\sigma}\cdot\mathbf B
$$

在适当符号约定下表示自旋磁矩与磁场耦合。也就是说，Dirac 方程在低速下不会推翻前面的量子力学，而是还原出薛定谔/Pauli 理论，并给出相对论修正。

## 20.6 负能量和反粒子

相对论能量关系有两个分支：

$$
E=\pm\sqrt{p^2c^2+m^2c^4}.
$$

Dirac 方程也有负能量解。最初这带来严重解释困难：如果电子可以不断落入负能量态，就会释放无限能量。

Dirac 的历史性解释引向“空穴”和反粒子思想。现代观点更清楚：单粒子相对论量子力学不是最终框架，必须进入量子场论。负能量解在场论中重新解释为反粒子自由度。正电子的发现成为 Dirac 理论的重要胜利。

## 20.7 与经典力学、数学、历史和后续章节的关系

**与经典力学的关系：** Dirac 方程建立在相对论能量动量关系上，而不是非相对论 \(p^2/2m\)。它是经典相对论和量子力学结合的结果。

**与数学的关系：** 关键数学结构是反对易代数、矩阵表示和旋量。它不是普通向量，而是在 Lorentz 变换下按旋量表示变换。

**与历史的关系：** Dirac 方程解释了电子自旋和磁矩结构，并预言了反粒子。正电子的发现使它成为 20 世纪理论物理的经典成功。

**与后续章节的关系：** 第 21 章路径积分会从传播子和作用量角度重新理解量子振幅。更远处，Dirac 方程自然通向量子场论，而不是停留在单粒子波函数。

## 本章学习检查

1. 薛定谔方程为什么不是相对论方程？
2. Klein-Gordon 方程为什么会有概率解释困难？
3. Dirac 为什么要求方程对时间和空间导数都一阶？
4. \(\alpha_i,\beta\) 为什么必须是矩阵？
5. Dirac 波函数为什么是多分量旋量？
6. 负能量解为什么引出反粒子和量子场论？

## 练习和解答

### 练习 1：检查 Dirac 矩阵条件的作用

说明为什么要求 \(\{\alpha_i,\beta\}=0\)。

**解答：**

Dirac Hamiltonian 为

$$
H_D=c\boldsymbol{\alpha}\cdot\mathbf p+\beta mc^2.
$$

平方时会出现交叉项：

$$
mc^3\sum_i(\alpha_i\beta+\beta\alpha_i)p_i.
$$

相对论能量关系中没有与 \(p_i\) 一次成正比的项，因此交叉项必须消失。这要求：

$$
\alpha_i\beta+\beta\alpha_i=0.
$$

也就是 \(\{\alpha_i,\beta\}=0\)。

### 练习 2：为什么不能用普通数代替矩阵

若 \(\alpha_i,\beta\) 都是普通数，是否能满足 \(\alpha_i^2=1\) 且 \(\alpha_i\beta+\beta\alpha_i=0\)？

**解答：**

普通数彼此交换，所以

$$
\alpha_i\beta+\beta\alpha_i=2\alpha_i\beta.
$$

若 \(\alpha_i^2=1,\beta^2=1\)，则 \(\alpha_i,\beta\) 都非零，\(2\alpha_i\beta\neq0\)。因此不能满足反对易要求，必须用矩阵。

### 练习 3：非相对论极限

从

$$
E=\sqrt{p^2c^2+m^2c^4}
$$

在 \(p\ll mc\) 下展开到 \(p^2\) 阶。

**解答：**

写成：

$$
E=mc^2\sqrt{1+\frac{p^2}{m^2c^2}}.
$$

用 \(\sqrt{1+x}\approx1+x/2\)，得：

$$
E\approx mc^2+\frac{p^2}{2m}.
$$

第一项是静止能，第二项是非相对论动能。

### 练习 4：负能量分支

为什么 \(E^2=p^2c^2+m^2c^4\) 自然有正负两个能量分支？

**解答：**

因为它是关于 \(E\) 的二次方程：

$$
E=\pm\sqrt{p^2c^2+m^2c^4}.
$$

这不是 Dirac 方程独有的问题，而是相对论能量关系本身的结构。Dirac 方程让这个结构以一阶时间演化形式出现，并最终引向反粒子的解释。
