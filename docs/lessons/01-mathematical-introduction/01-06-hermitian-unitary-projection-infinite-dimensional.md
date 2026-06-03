# 第 1 章第 6 讲：厄米、幺正、投影和无限维推广

本讲收束第 1 章。前面已经有态、基底、内积、算符、本征值。现在要认识三类特别重要的算符：

- 厄米算符：适合表示可观测量。
- 幺正算符：适合表示保持概率的变换。
- 投影算符：适合提取某个方向的成分。

最后再说明有限维公式怎样推广到波函数的无限维情形。

## 1. 本讲要解决的问题

量子力学中不是任何矩阵都有直接物理意义。我们需要知道：

1. 哪些算符适合表示测量量？
2. 哪些算符适合表示时间演化？
3. 怎样用算符提取一个态的某个分量？
4. 前面二维、三维的公式怎样变成 $`\psi(x)`$ 和积分？

## 2. 厄米算符：可观测量的数学形式

复矩阵的 dagger 操作定义为：

> 先转置，再复共轭。

如果：

$$
A^\dagger=A
$$

则 $`A`$ 叫厄米算符。

例子：

$$
A=
\begin{pmatrix}
2&0\\
0&5
\end{pmatrix}
$$

显然：

$$
A^\dagger=A
$$

再看：

$$
C=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix}
$$

转置：

$$
C^T=
\begin{pmatrix}
0&i\\
-i&0
\end{pmatrix}
$$

再复共轭：

$$
C^\dagger=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix}
=C
$$

所以 $`C`$ 也是厄米矩阵。

## 3. 为什么厄米算符表示可观测量

物理测量结果必须是实数。厄米算符有两个关键性质：

1. 本征值是实数。
2. 不同本征值对应的本征向量正交。

因此，如果可观测量由厄米算符 $`A`$ 表示：

$$
A\lvert a_n\rangle=a_n\lvert a_n\rangle
$$

那么本征值 $`a_n`$ 可以作为真实测量读数。

这就是第 4 章测量公设的数学基础。

## 4. 幺正算符：保持概率的变换

如果：

$$
U^\dagger U=I
$$

则 $`U`$ 是幺正算符。

它的核心性质是保持内积。设：

$$
\lvert \psi'\rangle=U\lvert\psi\rangle
$$

则：

$$
\begin{gathered}
\langle \psi'\mid\psi'\rangle \\
=\langle U\psi\mid U\psi\rangle \\
=\langle \psi\mid U^\dagger U\mid\psi\rangle \\
=\langle \psi\mid\psi\rangle
\end{gathered}
$$

所以如果原来：

$$
\langle \psi\mid\psi\rangle=1
$$

变换后仍然：

$$
\langle \psi'\mid\psi'\rangle=1
$$

物理意义：

> 幺正变换不破坏总概率。

时间演化必须保持总概率，所以孤立量子系统的时间演化由幺正算符描述。

## 5. 投影算符：取出某个方向的分量

设 $`\lvert n\rangle`$ 是归一化向量。投影到这个方向的算符定义为：

$$
P_n=\lvert n\rangle\langle n\rvert
$$

对任意态：

$$
\begin{gathered}
P_n\lvert\psi\rangle \\
=\lvert n\rangle\langle n\mid\psi\rangle
\end{gathered}
$$

这里：

$$
\langle n\mid\psi\rangle
$$

是 $`\lvert\psi\rangle`$ 在 $`\lvert n\rangle`$ 方向上的概率振幅。

所以投影算符做的事是：

> 只保留态在某个方向上的成分，丢掉其它方向。

例子：

$$
\begin{gathered}
\lvert n\rangle=(1,0),\quad \\
\lvert\psi\rangle=(a,b)
\end{gathered}
$$

则：

$$
P_n\lvert\psi\rangle=(a,0)
$$

## 6. 完备性

如果一组正交归一基底覆盖整个空间：

$$
\lvert 1\rangle,\lvert 2\rangle,\dots,\lvert n\rangle
$$

那么：

$$
\sum_i \lvert i\rangle\langle i\rvert=I
$$

这叫完备性关系。

普通语言：

> 把所有基底方向的投影加起来，就等于完整保留原向量。

对任意态：

$$
\begin{gathered}
\lvert\psi\rangle=I\lvert\psi\rangle \\
=\sum_i \lvert i\rangle\langle i\mid\psi\rangle
\end{gathered}
$$

因为：

$$
c_i=\langle i\mid\psi\rangle
$$

所以这就是展开公式：

$$
\lvert\psi\rangle=\sum_i c_i\lvert i\rangle
$$

的算符写法。

## 7. 从有限维到无限维

前面我们用有限维向量：

$$
\lvert\psi\rangle=\sum_n c_n\lvert n\rangle
$$

但位置 $`x`$ 是连续变量。连续位置基底写成：

$$
\lvert x\rangle
$$

态在位置基底下展开为：

$$
\lvert\psi\rangle=\int dx\,\psi(x)\lvert x\rangle
$$

这里：

$$
\psi(x)=\langle x\mid\psi\rangle
$$

是态在位置基底下的展开系数，也就是波函数。

有限维归一化：

$$
\sum_n |c_n|^2=1
$$

连续位置归一化：

$$
\int dx\,|\psi(x)|^2=1
$$

有限维内积：

$$
\langle\phi\mid\psi\rangle=\sum_n \phi_n^\ast\psi_n
$$

连续位置内积：

$$
\langle\phi\mid\psi\rangle=\int dx\,\phi^\ast(x)\psi(x)
$$

所以积分不是新魔法，只是“连续无穷多个分量求和”。

## 8. 物理意义

本讲把第 1 章的数学工具连到物理解释：

| 数学对象 | 物理意义 |
| --- | --- |
| 厄米算符 | 可观测量 |
| 厄米算符本征值 | 可能测量结果 |
| 幺正算符 | 保持概率的变换 |
| 投影算符 | 提取某个测量结果方向 |
| 完备性关系 | 所有可能结果覆盖整个态空间 |
| 波函数 $`\psi(x)`$ | 态在位置基底下的展开系数 |

## 9. 它和经典力学、数学、历史、后续章节的关系

经典力学中，物理量是实函数，时间演化保持相空间结构。量子力学中，可观测量变成厄米算符，时间演化变成幺正变换。

数学上，本讲涉及内积空间上的特殊线性算符：自伴算符、酉算符、投影算符。

历史上，Dirac 的统一语言让矩阵力学和波动力学成为同一个框架的不同表示。有限维求和和连续积分的对应，正是这种统一的核心。

后续关系：

- 第 4 章：厄米算符、投影、测量概率正式成为公设。
- 第 5 章：波函数归一化和边界条件会大量使用积分内积。
- 第 7 章：谐振子能量本征态构成完备基底。
- 第 8 章：路径积分会从传播算符和连续变量基底出发。
- 第 11 章：对称变换通常由幺正算符表示。

## 10. 练习

### 练习 1

判断下面矩阵是否厄米：

$$
A=
\begin{pmatrix}
1&i\\
-i&2
\end{pmatrix}
$$

### 练习 2

判断下面矩阵是否幺正：

$$
U=
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1&1\\
1&-1
\end{pmatrix}
$$

### 练习 3

设：

$$
\begin{gathered}
\lvert n\rangle=(1,0),\quad \\
\lvert\psi\rangle=\left(\frac35,\frac45\right)
\end{gathered}
$$

求：

$$
P_n\lvert\psi\rangle
$$

其中 $`P_n=\lvert n\rangle\langle n\rvert`$。

### 练习 4

把有限维公式：

$$
\langle\phi\mid\psi\rangle=\sum_n \phi_n^\ast\psi_n
$$

翻译成连续位置基底下的公式。

### 练习 5

用普通语言解释：

$$
\sum_n \lvert n\rangle\langle n\rvert=I
$$

## 11. 解答

### 解答 1

转置：

$$
A^T=
\begin{pmatrix}
1&-i\\
i&2
\end{pmatrix}
$$

复共轭：

$$
A^\dagger=
\begin{pmatrix}
1&i\\
-i&2
\end{pmatrix}
=A
$$

所以 $`A`$ 是厄米矩阵。

### 解答 2

这个矩阵是实矩阵，所以 $`U^\dagger=U^T`$。又因为它对称，$`U^\dagger=U`$。

计算：

$$
U^\dagger U=U^2
=\frac12
\begin{pmatrix}
1&1\\
1&-1
\end{pmatrix}
\begin{pmatrix}
1&1\\
1&-1
\end{pmatrix}
$$

$$
=\frac12
\begin{pmatrix}
2&0\\
0&2
\end{pmatrix}
=I
$$

所以 $`U`$ 是幺正矩阵。

### 解答 3

因为：

$$
\langle n\mid\psi\rangle=\frac35
$$

所以：

$$
\begin{gathered}
P_n\lvert\psi\rangle \\
=\lvert n\rangle\langle n\mid\psi\rangle \\
=\frac35(1,0) \\
=\left(\frac35,0\right)
\end{gathered}
$$

它只保留了 $`\lvert\psi\rangle`$ 在 $`\lvert n\rangle`$ 方向上的分量。

### 解答 4

连续位置基底下，离散求和变为积分，分量 $`\psi_n`$ 变为函数 $`\psi(x)`$。所以：

$$
\begin{gathered}
\langle\phi\mid\psi\rangle= \\
\int dx\,\phi^\ast(x)\psi(x)
\end{gathered}
$$

### 解答 5

这句话表示：所有正交归一基底方向的投影加起来，等于恒等算符。也就是说，任意态都可以被完整拆成这些基底方向上的分量，没有遗漏，也没有重复。

## 12. 第 1 章总复习

你现在应该能读懂：

$$
\lvert\psi\rangle=\sum_n c_n\lvert n\rangle
$$

态在基底上的展开。

$$
\langle\psi\mid\psi\rangle=1
$$

态已归一化。

$$
A\lvert a_n\rangle=a_n\lvert a_n\rangle
$$

$`\lvert a_n\rangle`$ 是算符 $`A`$ 的本征态，$`a_n`$ 是本征值。

$$
P_n=\lvert n\rangle\langle n\rvert
$$

投影到 $`\lvert n\rangle`$ 方向的算符。

$$
U^\dagger U=I
$$

$`U`$ 是幺正算符，保持内积和归一化。

## 13. 本讲必须记住的三句话

1. 厄米算符适合表示可观测量，因为它的本征值是实数。
2. 幺正算符保持内积和归一化，因此适合表示时间演化。
3. 无限维公式只是把离散求和推广为连续积分，波函数是态在位置基底下的坐标函数。
