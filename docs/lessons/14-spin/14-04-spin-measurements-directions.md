# 第 14 章第 4 讲：不同方向自旋测量和概率

本讲解释为什么同一个自旋态，换方向测量会得到不同概率。

## 1. 为什么有这个概念

量子测量依赖观测量。

测 \(S_z\) 和测 \(S_x\) 是两个不同问题，对应不同本征基底。

## 2. 它解决了什么问题

它解决“为什么已经是 \(S_z\) 向上态，测 \(S_x\) 仍然会分成两个结果”的问题。

核心原因是：

$$
[S_z,S_x]\ne0
$$

## 3. \(S_z\) 基底

选：

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

若：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

测 \(S_z\) 得：

$$
P(+)=|a|^2,\quad P(-)=|b|^2
$$

## 4. \(S_x\) 基底怎么来

\(S_x\) 的本征态是：

$$
|\uparrow_x\rangle=\frac{1}{\sqrt2}
\left(|\uparrow\rangle+|\downarrow\rangle\right)
$$

$$
|\downarrow_x\rangle=\frac{1}{\sqrt2}
\left(|\uparrow\rangle-|\downarrow\rangle\right)
$$

所以：

$$
|\uparrow\rangle=
\frac{1}{\sqrt2}
\left(|\uparrow_x\rangle+|\downarrow_x\rangle\right)
$$

因此如果态是 \(|\uparrow\rangle\)，测量 \(S_x\) 时：

$$
P(S_x=+\hbar/2)=\frac12
$$

$$
P(S_x=-\hbar/2)=\frac12
$$

## 5. 物理意义

沿 \(z\) 方向确定，不等于沿 \(x\) 方向确定。

自旋态不是一个已经指向某个普通空间箭头的经典对象；它是一个量子态，测量方向决定使用哪个本征基底。

## 6. 和不确定性关系的关系

因为：

$$
[S_x,S_z]\ne0
$$

所以不同方向自旋分量不能一般地同时确定。

这和第 9 章、第 12 章的非对易结构完全一致。

## 7. 练习

### 练习 1

写出 \(|\uparrow_x\rangle\)。

### 练习 2

态为 \(|\uparrow\rangle\) 时，测 \(S_x\) 得到 \(+\hbar/2\) 的概率是多少？

### 练习 3

为什么 \(S_z\) 确定不意味着 \(S_x\) 确定？

## 8. 解答

### 解答 1

$$
|\uparrow_x\rangle=\frac{1}{\sqrt2}
(|\uparrow\rangle+|\downarrow\rangle)
$$

### 解答 2

$$
\frac12
$$

### 解答 3

因为 \(S_z\) 和 \(S_x\) 的本征基底不同，且二者不对易。

## 9. 本讲必须记住的三句话

1. 不同方向自旋测量对应不同本征基底。
2. \(|\uparrow\rangle\) 测 \(S_x\) 会有两个等概率结果。
3. 换测量方向就是换观测量，不是同一个问题。
