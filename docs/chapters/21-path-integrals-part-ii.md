# 21. Path Integrals: Part II

本章继续发展路径积分。第 8 章已经给出核心图像：传播振幅等于所有路径的相位加权求和。本章进一步回答：路径积分怎样实际计算？为什么高斯积分如此核心？相互作用怎样变成微扰展开？为什么这套语言能自然通向统计物理和量子场论？

路径积分不是薛定谔方程的竞争者，而是同一量子理论的另一种组织方式。它特别擅长处理传播子、对称性、微扰展开、经典极限和场的量子化。

## 本章逐讲

| 讲义 | 主题 |
| --- | --- |
| [第 1 讲：从传播子重新理解路径积分](../lessons/21-path-integrals-part-ii/21-01-propagator-review.md) | 传播子、路径求和、边界条件 |
| [第 2 讲：离散化、测度和为什么路径积分不是普通积分](../lessons/21-path-integrals-part-ii/21-02-discretization-measure.md) | 时间切片、测度、极限过程 |
| [第 3 讲：高斯路径积分和二次型作用量](../lessons/21-path-integrals-part-ii/21-03-gaussian-path-integrals.md) | 高斯积分、自由理论、行列式 |
| [第 4 讲：含源路径积分和生成泛函](../lessons/21-path-integrals-part-ii/21-04-sources-generating-functionals.md) | 源、关联函数、函数求导 |
| [第 5 讲：路径积分中的微扰展开](../lessons/21-path-integrals-part-ii/21-05-perturbation-expansion.md) | 相互作用、级数、图像化组织 |
| [第 6 讲：Euclidean 路径积分、统计物理和场论入口](../lessons/21-path-integrals-part-ii/21-06-euclidean-statistical-field-entry.md) | Wick 转动、配分函数、场论语言 |

## 21.1 为什么还要继续路径积分

第 8 章给出路径积分公式：

$$
K(x_f,t_f;x_i,t_i)
=
\int_{x(t_i)=x_i}^{x(t_f)=x_f}\mathcal D x(t)\,
\exp\left(\frac{i}{\hbar}S[x]\right).
$$

它说明传播子是所有路径的振幅和。经典路径不是唯一真实路径，而是在 \(\hbar\) 很小时相位最稳定、贡献最相干的路径。

本章要把这个图像变成更可计算的工具：

- 如何定义 \(\mathcal D x(t)\)；
- 哪些路径积分可以精确算；
- 相互作用如何做微扰展开；
- 如何从路径积分读出关联函数；
- 为什么它适合推广到场论。

## 21.2 离散化和测度

路径积分不是普通有限维积分。一个路径 \(x(t)\) 是连续函数，积分对象是无限多个自由度。

实际定义常从时间切片开始。把时间区间切成 \(N\) 小段：

$$
t_i=t_0<t_1<\cdots<t_N=t_f.
$$

路径由中间点

$$
x_1,x_2,\ldots,x_{N-1}
$$

近似表示。于是路径积分先变成多重积分：

$$
\int \mathcal D x(t)
\quad\Longleftrightarrow\quad
\lim_{N\to\infty}
\mathcal N_N
\int dx_1\cdots dx_{N-1}.
$$

其中 \(\mathcal N_N\) 是归一化因子，保证传播子满足正确的短时极限和组合律。

路径积分的测度不是随便写的符号；它包含了如何切片、如何归一化、如何取连续极限。

## 21.3 高斯路径积分为什么核心

普通高斯积分：

$$
\int_{-\infty}^{\infty} dx\,e^{-ax^2}
=
\sqrt{\frac{\pi}{a}}
\qquad
(a>0).
$$

多维高斯积分推广为：

$$
\int d^n x\,\exp\left(-\frac12 x^T A x+J^T x\right)
\propto
(\det A)^{-1/2}
\exp\left(\frac12 J^T A^{-1}J\right).
$$

自由粒子、谐振子、自由场的作用量都是二次型，因此路径积分本质上是无限维高斯积分。二次型作用量可以精确处理；非二次相互作用通常以二次部分为基础做微扰。

这就是为什么谐振子和自由理论在路径积分中地位特殊：它们不是简单例子，而是所有微扰计算的零阶基准。

## 21.4 含源路径积分和生成泛函

为了系统计算期望值和关联函数，引入外源 \(J(t)\)：

$$
Z[J]
=
\int \mathcal D x\,
\exp\left[
\frac{i}{\hbar}
\left(
S[x]+\int dt\,J(t)x(t)
\right)
\right].
$$

对 \(J(t)\) 做函数求导，可以把 \(x(t)\) 从积分中“拉下来”。例如：

$$
\left.
\frac{\delta Z[J]}{\delta J(t)}
\right|_{J=0}
\propto
\langle x(t)\rangle.
$$

二阶求导给出两点关联函数：

$$
\left.
\frac{\delta^2 Z[J]}{\delta J(t_1)\delta J(t_2)}
\right|_{J=0}
\propto
\langle x(t_1)x(t_2)\rangle.
$$

这套语言在量子场论中极其重要，因为场论真正关心的常常不是某个单一路径，而是场的关联函数和散射振幅。

## 21.5 路径积分中的微扰展开

把作用量写成：

$$
S[x]=S_0[x]+S_{\text{int}}[x].
$$

其中 \(S_0\) 是二次型，可精确做高斯积分；\(S_{\text{int}}\) 是相互作用。

路径积分为：

$$
Z
=
\int\mathcal D x\,
e^{\frac{i}{\hbar}S_0[x]}
e^{\frac{i}{\hbar}S_{\text{int}}[x]}.
$$

若相互作用小，可展开：

$$
e^{\frac{i}{\hbar}S_{\text{int}}}
=
1+\frac{i}{\hbar}S_{\text{int}}
+\frac{1}{2!}\left(\frac{i}{\hbar}S_{\text{int}}\right)^2+\cdots.
$$

这样相互作用问题变成一串自由高斯平均。量子场论中的 Feynman 图，本质上就是这种展开的图像化记账方式：线来自自由传播子，顶点来自相互作用项。

## 21.6 Euclidean 路径积分和统计物理入口

实时间路径积分含有振荡因子：

$$
e^{iS/\hbar}.
$$

它物理意义清楚，但数学上高度振荡。做 Wick 转动：

$$
t=-i\tau,
$$

可以把相位权重变成类似 Boltzmann 权重：

$$
e^{iS/\hbar}
\longrightarrow
e^{-S_E/\hbar}.
$$

这里 \(S_E\) 是 Euclidean 作用量。形式上它很像统计物理中的配分函数：

$$
Z_{\text{stat}}
=
\int \mathcal D x\,e^{-\beta E[x]}.
$$

这揭示了量子力学、统计物理和场论之间的深层联系。许多现代方法，例如格点场论、瞬子、重整化群，都依赖 Euclidean 路径积分思想。

## 21.7 与经典力学、数学、历史和后续方向的关系

**与经典力学的关系：** 路径积分直接使用作用量 \(S\)。经典轨道来自驻相条件 \(\delta S=0\)，这把 Hamilton 最小作用量原理和量子相位求和联系起来。

**与数学的关系：** 本章涉及无限维积分、高斯泛函积分、Green 函数、函数求导和渐近展开。严格数学定义并不总是简单，但物理计算结构非常强大。

**与历史的关系：** Feynman 把量子振幅组织成路径求和，使作用量成为量子理论中心语言之一。后来它成为量子场论、统计物理和凝聚态理论的标准工具。

**与全书关系：** 本章回收了第 2 章作用量、第 4 章时间演化、第 8 章路径积分、第 16-19 章近似与散射、第 20 章相对论量子理论。它也是走向量子场论的自然出口。

## 本章学习检查

1. 路径积分中的 \(\mathcal D x(t)\) 为什么需要离散化来理解？
2. 为什么二次型作用量对应高斯路径积分？
3. 含源生成泛函 \(Z[J]\) 解决什么问题？
4. 路径积分中的微扰展开为什么以自由理论为零阶？
5. Wick 转动为什么能把振荡权重变成衰减权重？
6. 为什么路径积分适合推广到场论？

## 练习和解答

### 练习 1：高斯积分中的源

设一维高斯积分：

$$
Z(J)=\int_{-\infty}^{\infty}dx\,
\exp\left(-\frac12 ax^2+Jx\right),
\qquad a>0.
$$

求 \(Z(J)\) 与 \(Z(0)\) 的关系。

**解答：**

配方：

$$
-\frac12 ax^2+Jx
=
-\frac12 a\left(x-\frac{J}{a}\right)^2
+\frac{J^2}{2a}.
$$

所以：

$$
Z(J)=Z(0)\exp\left(\frac{J^2}{2a}\right).
$$

这就是生成泛函中 \(A^{-1}\) 出现的最小版本。

### 练习 2：为什么自由理论容易算

为什么自由粒子、谐振子或自由场是路径积分微扰的零阶基础？

**解答：**

它们的作用量是二次型。二次型路径积分是高斯积分，可以精确计算传播子和关联函数。相互作用项再围绕这个可解基础展开。

### 练习 3：关联函数从哪里来

如果

$$
Z[J]=\int \mathcal D x\,
e^{\frac{i}{\hbar}(S[x]+\int Jx\,dt)},
$$

对 \(J(t_1)\) 求导会带出什么？

**解答：**

形式上：

$$
\frac{\delta Z[J]}{\delta J(t_1)}
=
\frac{i}{\hbar}
\int\mathcal D x\,x(t_1)
e^{\frac{i}{\hbar}(S+\int Jx\,dt)}.
$$

令 \(J=0\) 后，它与 \(\langle x(t_1)\rangle\) 成正比。

### 练习 4：Wick 转动的意义

为什么 \(e^{iS/\hbar}\) 在计算上比 \(e^{-S_E/\hbar}\) 更难处理？

**解答：**

\(e^{iS/\hbar}\) 是纯相位振荡，很多路径贡献通过快速振荡抵消，积分数值和数学控制都困难。\(e^{-S_E/\hbar}\) 是衰减权重，更像统计物理的 Boltzmann 因子，通常更适合定义和计算。
