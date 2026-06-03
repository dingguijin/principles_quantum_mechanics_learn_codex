# 第 14 章第 3 讲：Pauli 矩阵和自旋算符

本讲介绍自旋 \(1/2\) 的三个基本观测量。

## 1. 为什么有这个概念

要测量自旋在 \(x,y,z\) 方向的分量，就需要三个厄米算符：

$$
S_x,\quad S_y,\quad S_z
$$

对二维自旋态空间，这些算符可以用 \(2\times2\) 矩阵表示。

## 2. 它解决了什么问题

Pauli 矩阵给出自旋 \(1/2\) 的具体计算工具。

有了它们，可以计算：

- 本征值。
- 本征态。
- 测量概率。
- 对易关系。
- 磁场中的能量。

## 3. 公式怎么来的

定义 Pauli 矩阵：

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

自旋算符是：

$$
S_i=\frac{\hbar}{2}\sigma_i
$$

所以：

$$
S_z=\frac{\hbar}{2}
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}
$$

## 4. 物理意义

\(\sigma_z\) 的本征值是：

$$
+1,\quad -1
$$

所以 \(S_z\) 的本征值是：

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

这正是自旋 \(1/2\) 的两个测量结果。

## 5. 对易关系

Pauli 矩阵满足：

$$
[\sigma_i,\sigma_j]=2i\epsilon_{ijk}\sigma_k
$$

因此：

$$
[S_i,S_j]=i\hbar\epsilon_{ijk}S_k
$$

这说明自旋和轨道角动量满足同一套角动量代数。

## 6. 和数学的关系

Pauli 矩阵是厄米矩阵：

$$
\sigma_i^\dagger=\sigma_i
$$

所以它们可以表示观测量。

它们也是二维复 Hilbert 空间中最重要的一组矩阵基底。

## 7. 练习

### 练习 1

写出三个 Pauli 矩阵。

### 练习 2

求 \(S_z\) 的两个本征值。

### 练习 3

写出 \([S_x,S_y]\)。

## 8. 解答

### 解答 1

$$
\sigma_x=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix},
\quad
\sigma_y=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix},
\quad
\sigma_z=
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}
$$

### 解答 2

$$
+\frac{\hbar}{2},\quad -\frac{\hbar}{2}
$$

### 解答 3

$$
[S_x,S_y]=i\hbar S_z
$$

## 9. 本讲必须记住的三句话

1. 自旋算符是 \(S_i=\hbar\sigma_i/2\)。
2. Pauli 矩阵是自旋 \(1/2\) 的计算核心。
3. 自旋满足和角动量相同的对易关系。
