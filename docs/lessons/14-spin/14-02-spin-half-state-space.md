# 第 14 章第 2 讲：自旋 1/2 的二维态空间

本讲建立自旋 \(1/2\) 系统的最小数学模型。

## 1. 为什么有这个概念

Stern-Gerlach 实验显示，自旋 \(1/2\) 粒子沿任意固定方向测量时只给出两个结果。

沿 \(z\) 方向：

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

两个结果意味着态空间至少需要两个基矢。

## 2. 它解决了什么问题

它解决“如何表示电子自旋态”的问题。

选 \(S_z\) 本征态作为基底：

$$
|\uparrow\rangle,\quad |\downarrow\rangle
$$

任意自旋态写成：

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

## 3. 公式怎么来的

用二维列向量表示：

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

所以：

$$
|\psi\rangle=
\begin{pmatrix}
a\\
b
\end{pmatrix}
$$

归一化要求：

$$
\langle\psi|\psi\rangle=1
$$

即：

$$
|a|^2+|b|^2=1
$$

## 4. 物理意义

如果测量 \(S_z\)，得到 \(+\hbar/2\) 的概率是：

$$
|a|^2
$$

得到 \(-\hbar/2\) 的概率是：

$$
|b|^2
$$

这和第 4 章 Born 规则完全一致。

## 5. 和第 1 章线性代数的关系

自旋 \(1/2\) 是最清楚的二维 Hilbert 空间例子。

这里没有位置变量，也能做完整量子力学：

- 态是向量。
- 观测量是厄米矩阵。
- 测量概率来自投影。

## 6. 和后续章节的关系

两个自旋 \(1/2\) 系统组合时，态空间会变成：

$$
\mathbb C^2\otimes\mathbb C^2
$$

这正是第 15 章角动量加法和纠缠态的重要例子。

## 7. 练习

### 练习 1

写出一般自旋 \(1/2\) 态。

### 练习 2

若 \(a=1/\sqrt3\)，归一化要求 \(|b|^2\) 是多少？

### 练习 3

为什么自旋 \(1/2\) 态空间是二维的？

## 8. 解答

### 解答 1

$$
|\psi\rangle=a|\uparrow\rangle+b|\downarrow\rangle
$$

且：

$$
|a|^2+|b|^2=1
$$

### 解答 2

$$
|b|^2=1-\frac13=\frac23
$$

### 解答 3

因为沿任意固定方向测量自旋只有两个本征结果，需要两个基矢描述。

## 9. 本讲必须记住的三句话

1. 自旋 \(1/2\) 态空间是二维 Hilbert 空间。
2. \(|\uparrow\rangle,|\downarrow\rangle\) 可作为 \(S_z\) 基底。
3. 系数模平方给出对应测量概率。
