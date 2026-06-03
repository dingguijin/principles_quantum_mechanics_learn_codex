# 第 1 章第 4 讲：线性算符和矩阵

前面三讲建立了态、基底、坐标、内积。现在进入量子力学的另一个核心对象：

> 什么东西作用在态上，并改变态？

答案是：算符。有限维情况下，算符可以用矩阵表示。

## 1. 本讲要解决的问题

量子力学不仅要描述系统处在什么态：

$$
\lvert \psi\rangle
$$

还要描述：

- 一个态怎样变成另一个态。
- 一个测量问题怎样作用在态上。
- 两个操作的先后顺序是否重要。

这些都需要算符。

基本写法是：

$$
A\lvert \psi\rangle = \lvert \phi\rangle
$$

普通语言：

> 算符 $`A`$ 作用在态 $`\lvert \psi\rangle`$ 上，得到新态 $`\lvert \phi\rangle`$。

## 2. 为什么需要算符

### 2.1 只描述态不够

态告诉我们系统现在是什么样。但物理还要问：

- 如果系统随时间演化，态怎么变？
- 如果我们测量能量，应该怎样从态中读出可能结果？
- 如果做一次旋转、平移或投影，态怎样变化？

这些问题都不是单靠 $`\lvert\psi\rangle`$ 能回答的。我们需要“作用规则”，这就是算符。

### 2.2 叠加原理要求算符是线性的

如果：

$$
\lvert \psi\rangle = a\lvert v\rangle + b\lvert w\rangle
$$

那么一个物理操作 $`A`$ 对它的作用应当满足：

$$
\begin{gathered}
A\lvert \psi\rangle = \\
A(a\lvert v\rangle + b\lvert w\rangle) \\
= aA\lvert v\rangle + bA\lvert w\rangle
\end{gathered}
$$

这就是线性：

$$
\begin{gathered}
A(a\lvert v\rangle + b\lvert w\rangle) \\
= aA\lvert v\rangle + bA\lvert w\rangle
\end{gathered}
$$

线性保证叠加态的每一部分可以分别处理，再合成总结果。

## 3. 公式怎么来的

先看二维向量。设：

$$
A =
\begin{pmatrix}
1 & 2\\
3 & 4
\end{pmatrix},
\quad
v =
\begin{pmatrix}
5\\
6
\end{pmatrix}
$$

矩阵作用在向量上：

$$
Av =
\begin{pmatrix}
1\cdot 5+2\cdot 6\\
3\cdot 5+4\cdot 6
\end{pmatrix}
=
\begin{pmatrix}
17\\
39
\end{pmatrix}
$$

这不是随便定义的规则。矩阵的每一行告诉我们：新向量的某个分量怎样由旧向量分量线性组合得到。

一般写成：

$$
(Av)_i = \sum_j A_{ij}v_j
$$

这里：

- $`v_j`$ 是旧向量的第 $`j`$ 个分量。
- $`A_{ij}`$ 是矩阵第 $`i`$ 行第 $`j`$ 列的元素。
- $`(Av)_i`$ 是新向量的第 $`i`$ 个分量。

## 4. 算符和矩阵不是一回事

算符是抽象作用规则。矩阵是选定基底后对这个规则的数字表示。

这和前面“态”和“坐标”的关系完全平行：

| 抽象对象 | 选定基底后的表示 |
| --- | --- |
| 态 $`\lvert\psi\rangle`$ | 坐标列向量 |
| 算符 $`A`$ | 矩阵 |

同一个算符，换一组基底，矩阵可能变。但物理作用没有变。

这就是为什么后面会出现“位置表象下的算符”“动量表象下的算符”“能量表象下的算符”。它们不是不同物理对象，而是同一对象在不同基底下的表示。

## 5. 矩阵元

若基底为：

$$
\lvert 1\rangle,\lvert 2\rangle,\dots,\lvert n\rangle
$$

算符 $`A`$ 的矩阵元定义为：

$$
A_{ij} = \langle i\mid A\mid j\rangle
$$

普通语言：

> $`A`$ 先作用在第 $`j`$ 个基底态上，再看结果在第 $`i`$ 个基底方向上的分量。

这说明矩阵元素本质上是“作用后再投影”的结果。

例子：

$$
A =
\begin{pmatrix}
1 & 2\\
3 & 4
\end{pmatrix}
$$

第 1 列表示 $`A\lvert 1\rangle`$ 的坐标：

$$
A\lvert 1\rangle =
\begin{pmatrix}
1\\
3
\end{pmatrix}
= 1\lvert 1\rangle+3\lvert 2\rangle
$$

第 2 列表示 $`A\lvert 2\rangle`$ 的坐标：

$$
A\lvert 2\rangle =
\begin{pmatrix}
2\\
4
\end{pmatrix}
= 2\lvert 1\rangle+4\lvert 2\rangle
$$

## 6. 对易子

两个算符的先后顺序可能重要。定义对易子：

$$
[A,B] = AB - BA
$$

如果：

$$
[A,B]=0
$$

则称 $`A`$ 和 $`B`$ 对易。意思是先做 $`A`$ 再做 $`B`$，和先做 $`B`$ 再做 $`A`$，结果一样。

如果：

$$
[A,B]\ne 0
$$

则不对易，说明操作顺序会改变结果。

量子力学中，不对易是非常核心的。位置和动量算符满足：

$$
[X,P] = i\hbar I
$$

这最终导向 Heisenberg 不确定性关系。第 9 章会系统讨论。

## 7. 物理意义

算符在量子力学中有几类常见角色：

- 可观测量：能量、动量、角动量、自旋等由算符表示。
- 变换：平移、旋转、时间演化由算符表示。
- 投影：提取某个结果方向的成分。

所以算符不是普通计算工具，而是量子力学用来表达“我们对态做什么”以及“我们问系统什么问题”的语言。

## 8. 它和经典力学的关系

经典力学中，物理量常是相空间上的函数：

$$
f(q,p)
$$

例如能量：

$$
H(q,p)
$$

量子力学中，很多经典物理量会被提升为算符：

$$
q \to X,\quad p \to P,\quad H(q,p)\to H
$$

区别在于：经典函数相乘通常对易，而量子算符相乘一般不对易。

这正是量子力学和经典力学形式结构的重要差别之一。

## 9. 它和数学、历史、后续章节的关系

数学上，本讲是线性代数中的线性映射与矩阵表示。

历史上，Heisenberg 的矩阵力学正是把可观测量组织成矩阵，并发现它们的乘法不对易。后来 Dirac 把矩阵语言和 Schrodinger 的波函数语言统一到算符作用在态矢量上的形式。

后续关系：

- 第 5 讲：本征值问题就是研究 $`A\lvert v\rangle=\lambda\lvert v\rangle`$。
- 第 6 讲：厄米算符、幺正算符、投影算符都是特殊算符。
- 第 4 章：可观测量会正式由厄米算符表示。
- 第 7 章：谐振子会大量使用升降算符。
- 第 11-12 章：对称性和角动量的核心是算符代数。

## 10. 最小计算例子

设：

$$
A =
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix},
\quad
B =
\begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix}
$$

计算：

$$
AB =
\begin{pmatrix}
0 & 1\\
-1 & 0
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
$$

所以：

$$
[A,B]=AB-BA =
\begin{pmatrix}
0 & 2\\
-2 & 0
\end{pmatrix}
$$

它们不对易。

## 11. 练习

### 练习 1

设：

$$
A =
\begin{pmatrix}
2 & 1\\
0 & 3
\end{pmatrix},
\quad
v=
\begin{pmatrix}
1\\
2
\end{pmatrix}
$$

计算 $`Av`$。

### 练习 2

验证下面算符是线性的：

$$
A =
\begin{pmatrix}
2 & 0\\
0 & -1
\end{pmatrix}
$$

即验证：

$$
A(av+bw)=aAv+bAw
$$

对任意二维向量成立。

### 练习 3

设：

$$
A =
\begin{pmatrix}
0 & 1\\
1 & 0
\end{pmatrix},
\quad
B =
\begin{pmatrix}
1 & 0\\
0 & -1
\end{pmatrix}
$$

计算 $`[A,B]`$。

### 练习 4

用普通语言解释：

$$
A_{ij}=\langle i\mid A\mid j\rangle
$$

## 12. 解答

### 解答 1

$$
Av =
\begin{pmatrix}
2\cdot 1+1\cdot 2\\
0\cdot 1+3\cdot 2
\end{pmatrix}
=
\begin{pmatrix}
4\\
6
\end{pmatrix}
$$

### 解答 2

设：

$$
v=(v_1,v_2),\quad w=(w_1,w_2)
$$

则：

$$
av+bw=(av_1+bw_1,\;av_2+bw_2)
$$

作用 $`A`$：

$$
A(av+bw)=(2av_1+2bw_1,\;-av_2-bw_2)
$$

另一方面：

$$
aAv+bAw=a(2v_1,-v_2)+b(2w_1,-w_2)
$$

$$
=(2av_1+2bw_1,\;-av_2-bw_2)
$$

两边相同，所以 $`A`$ 线性。

### 解答 3

$$
AB =
\begin{pmatrix}
0 & -1\\
1 & 0
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
0 & 1\\
-1 & 0
\end{pmatrix}
$$

所以：

$$
[A,B]=AB-BA =
\begin{pmatrix}
0 & -2\\
2 & 0
\end{pmatrix}
$$

### 解答 4

它表示：先让算符 $`A`$ 作用在第 $`j`$ 个基底态 $`\lvert j\rangle`$ 上，再用 $`\langle i\rvert`$ 取出结果在第 $`i`$ 个基底方向上的分量。它就是算符 $`A`$ 在这组基底下矩阵的第 $`i`$ 行第 $`j`$ 列元素。

## 13. 本讲必须记住的三句话

1. 算符是作用在态上的规则；矩阵是选定基底后的表示。
2. 线性算符满足 $`A(a\lvert v\rangle+b\lvert w\rangle)=aA\lvert v\rangle+bA\lvert w\rangle`$。
3. 对易子 $`[A,B]`$ 衡量两个操作的先后顺序是否重要。
