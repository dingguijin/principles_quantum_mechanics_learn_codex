# 第 10 章第 2 讲：多维位置、动量和对易关系

本讲把第 5 章的一维位置、动量算符推广到 \(N\) 个自由度。

## 1. 为什么有这个概念

一维中，动量算符是：

$$
\hat p=-i\hbar\frac{d}{dx}
$$

多自由度中，每个坐标方向都有自己的动量。

如果坐标是：

$$
q_1,q_2,\cdots,q_N
$$

对应动量是：

$$
p_1,p_2,\cdots,p_N
$$

## 2. 它解决了什么问题

它告诉我们：多维系统中如何计算每个方向的运动、能量和不确定性。

例如三维自由粒子的动能是：

$$
T=\frac{p_x^2+p_y^2+p_z^2}{2m}
$$

所以量子哈密顿量必须知道 \(\hat p_x,\hat p_y,\hat p_z\) 怎么作用。

## 3. 公式怎么来的

在 \(N\) 维坐标表象中：

$$
\hat q_i\psi(q_1,\cdots,q_N)=q_i\psi(q_1,\cdots,q_N)
$$

动量算符是：

$$
\hat p_i=-i\hbar\frac{\partial}{\partial q_i}
$$

注意这里是偏导数。因为 \(p_i\) 只关心第 \(i\) 个坐标方向的变化。

## 4. 基本对易关系

一维中：

$$
[\hat x,\hat p]=i\hbar
$$

多维中：

$$
[\hat q_i,\hat p_j]=i\hbar\delta_{ij}
$$

其中：

$$
\delta_{ij}=
\begin{cases}
1,&i=j\\
0,&i\ne j
\end{cases}
$$

这表示：

- 同一自由度：\([\hat q_i,\hat p_i]=i\hbar\)。
- 不同自由度：\([\hat q_i,\hat p_j]=0\)，当 \(i\ne j\)。

## 5. 一个直接计算

取两个坐标 \(x,y\)，令：

$$
\hat p_y=-i\hbar\frac{\partial}{\partial y}
$$

对任意 \(\psi(x,y)\)：

$$
\hat x\hat p_y\psi
=x\left(-i\hbar\frac{\partial\psi}{\partial y}\right)
$$

而：

$$
\hat p_y\hat x\psi
=-i\hbar\frac{\partial}{\partial y}(x\psi)
=-i\hbar x\frac{\partial\psi}{\partial y}
$$

因为 \(x\) 对 \(y\) 是常数，所以两者相等：

$$
[\hat x,\hat p_y]=0
$$

## 6. 物理意义

同一方向的位置和动量互相限制：

$$
\Delta q_i\Delta p_i\ge\frac{\hbar}{2}
$$

不同方向之间没有这种基本对易子下界。例如 \(x\) 和 \(p_y\) 可以同时有确定本征值结构。

## 7. 和经典力学、数学的关系

经典力学中，每个坐标 \(q_i\) 有共轭动量 \(p_i\)。

量子力学把这个正则结构变成：

$$
[\hat q_i,\hat p_j]=i\hbar\delta_{ij}
$$

这正是第 2 章泊松括号：

$$
\{q_i,p_j\}=\delta_{ij}
$$

在量子理论中的对应物。

## 8. 和后续章节的关系

三维动量算符会进入：

- 第 11 章平移对称性。
- 第 12 章角动量 \(\mathbf L=\mathbf r\times\mathbf p\)。
- 第 13 章氢原子的三维薛定谔方程。

## 9. 练习

### 练习 1

写出三维中 \(\hat p_x,\hat p_y,\hat p_z\)。

### 练习 2

计算 \([\hat y,\hat p_y]\)。

### 练习 3

计算 \([\hat z,\hat p_x]\)。

## 10. 解答

### 解答 1

$$
\hat p_x=-i\hbar\frac{\partial}{\partial x},\quad
\hat p_y=-i\hbar\frac{\partial}{\partial y},\quad
\hat p_z=-i\hbar\frac{\partial}{\partial z}
$$

### 解答 2

同一方向：

$$
[\hat y,\hat p_y]=i\hbar
$$

### 解答 3

不同方向：

$$
[\hat z,\hat p_x]=0
$$

## 11. 本讲必须记住的三句话

1. 多维动量是对应坐标的偏导数。
2. 基本对易关系是 \([\hat q_i,\hat p_j]=i\hbar\delta_{ij}\)。
3. 不同自由度的正则变量通常彼此对易。
