# 10. Systems with N Degrees of Freedom

从第 5 章到第 9 章，我们主要研究一维单粒子问题：一个位置 \(x\)，一个动量 \(p\)，一个波函数 \(\psi(x)\)。

真实系统通常不止一个自由度。一个三维粒子需要：

$$
(x,y,z)
$$

两个一维粒子需要：

$$
(x_1,x_2)
$$

\(N\) 个自由度的系统需要：

$$
(q_1,q_2,\cdots,q_N)
$$

本章要解决的问题是：量子力学的态、算符、哈密顿量和测量规则，怎样从一个自由度推广到多个自由度。

## 本章学习路线

建议分 5 次学习：

1. [第 1 讲：为什么多自由度不是多个一维问题简单并排](../lessons/10-n-degrees-of-freedom/10-01-why-many-degrees-of-freedom.md)
2. [第 2 讲：多维位置、动量和对易关系](../lessons/10-n-degrees-of-freedom/10-02-multidimensional-position-momentum-commutators.md)
3. [第 3 讲：多自由度哈密顿量和可分变量](../lessons/10-n-degrees-of-freedom/10-03-hamiltonians-and-separation.md)
4. [第 4 讲：组合系统和张量积态空间](../lessons/10-n-degrees-of-freedom/10-04-tensor-product-composite-systems.md)
5. [第 5 讲：可分态、纠缠态和多粒子物理入口](../lessons/10-n-degrees-of-freedom/10-05-separable-entangled-states.md)

## 第 1 讲：多自由度的必要性

经典力学中，一个系统的自由度数等于描述其构型所需的独立坐标数。

量子力学中，自由度数会进入波函数的自变量。例如一维单粒子：

$$
\psi(x)
$$

三维单粒子：

$$
\psi(x,y,z)
$$

\(N\) 个自由度：

$$
\psi(q_1,q_2,\cdots,q_N)
$$

归一化条件也随之改变：

$$
\int |\psi(q_1,\cdots,q_N)|^2\,dq_1\cdots dq_N=1
$$

物理意义是：

> \(|\psi(q_1,\cdots,q_N)|^2dq_1\cdots dq_N\) 是系统同时落在这些坐标范围内的概率。

这不是 \(N\) 个互不相干的一维问题。因为波函数可以把不同自由度关联在一起。

## 第 2 讲：多维位置和动量

每个自由度 \(q_i\) 都有对应的动量：

$$
\hat p_i=-i\hbar\frac{\partial}{\partial q_i}
$$

位置算符是乘以坐标：

$$
\hat q_i\psi(q_1,\cdots,q_N)=q_i\psi(q_1,\cdots,q_N)
$$

基本对易关系推广为：

$$
[\hat q_i,\hat p_j]=i\hbar\delta_{ij}
$$

其中 \(\delta_{ij}\) 是 Kronecker delta：

$$
\delta_{ij}=
\begin{cases}
1,&i=j\\
0,&i\ne j
\end{cases}
$$

这表示同一自由度的位置和动量非对易，不同自由度之间的位置和动量对易。

因此：

$$
\Delta q_i\,\Delta p_i\ge\frac{\hbar}{2}
$$

但对 \(i\ne j\)，没有由 \([\hat q_i,\hat p_j]\) 给出的同类下界。

## 第 3 讲：多自由度哈密顿量

多个自由度的哈密顿量常写成：

$$
\hat H=\sum_{i=1}^N\frac{\hat p_i^2}{2m_i}+V(q_1,\cdots,q_N)
$$

在坐标表象中：

$$
\hat H=-\sum_{i=1}^N\frac{\hbar^2}{2m_i}\frac{\partial^2}{\partial q_i^2}+V(q_1,\cdots,q_N)
$$

定态薛定谔方程是：

$$
\hat H\psi(q_1,\cdots,q_N)=E\psi(q_1,\cdots,q_N)
$$

如果势能可以拆开：

$$
V(q_1,\cdots,q_N)=V_1(q_1)+\cdots+V_N(q_N)
$$

则解常可写成乘积形式：

$$
\psi(q_1,\cdots,q_N)=\psi_1(q_1)\cdots\psi_N(q_N)
$$

能量也相加：

$$
E=E_1+\cdots+E_N
$$

这叫变量分离。它是把复杂多维问题拆成几个一维问题的关键方法。

## 第 4 讲：组合系统和张量积

如果系统 A 的态空间是 \(\mathcal H_A\)，系统 B 的态空间是 \(\mathcal H_B\)，组合系统的态空间不是普通加法：

$$
\mathcal H_A+\mathcal H_B
$$

而是张量积：

$$
\mathcal H_A\otimes\mathcal H_B
$$

如果：

$$
|a\rangle\in\mathcal H_A,\quad |b\rangle\in\mathcal H_B
$$

组合系统的一个简单态是：

$$
|a\rangle\otimes|b\rangle
$$

通常简写成：

$$
|a\rangle|b\rangle
$$

为什么要用张量积？因为组合系统的测量结果是“同时给出 A 的结果和 B 的结果”。如果 A 有基底 \(|i\rangle\)，B 有基底 \(|j\rangle\)，组合系统基底应是：

$$
|i\rangle\otimes|j\rangle
$$

如果 A 有 \(m\) 个基矢，B 有 \(n\) 个基矢，组合系统有：

$$
mn
$$

个基矢。

## 第 5 讲：可分态和纠缠态

并不是每个组合态都能写成：

$$
|\psi\rangle=|a\rangle\otimes|b\rangle
$$

能这样写的叫可分态。

不能这样写的叫纠缠态。

最小例子是两个二能级系统：

$$
|\Psi\rangle=\frac{1}{\sqrt2}(|0\rangle|0\rangle+|1\rangle|1\rangle)
$$

这个态不是某个单独 A 态和单独 B 态的乘积。

它的物理意义是：

> 系统 A 和系统 B 不能再被看成各自拥有独立量子态；只有整体态才是基本对象。

这为后续多粒子系统、自旋、角动量耦合和量子信息中的纠缠概念打基础。

## 本章总复习

多自由度波函数：

$$
\psi(q_1,\cdots,q_N)
$$

归一化：

$$
\int |\psi(q_1,\cdots,q_N)|^2dq_1\cdots dq_N=1
$$

动量算符：

$$
\hat p_i=-i\hbar\frac{\partial}{\partial q_i}
$$

基本对易关系：

$$
[\hat q_i,\hat p_j]=i\hbar\delta_{ij}
$$

多自由度哈密顿量：

$$
\hat H=\sum_i\frac{\hat p_i^2}{2m_i}+V(q_1,\cdots,q_N)
$$

组合系统态空间：

$$
\mathcal H_A\otimes\mathcal H_B
$$

可分态：

$$
|\psi\rangle=|a\rangle\otimes|b\rangle
$$

纠缠态：不能写成单个乘积态的组合态。

## 本章作业

### A. 三维自由粒子

写出三维自由粒子的哈密顿量。

### B. 对易关系

计算 \([\hat x,\hat p_y]\) 应该等于什么？为什么？

### C. 变量分离

若：

$$
H=H_1+H_2
$$

且：

$$
H_1\psi_1=E_1\psi_1,\quad H_2\psi_2=E_2\psi_2
$$

证明 \(\psi_1(q_1)\psi_2(q_2)\) 是 \(H\) 的本征函数。

### D. 张量积维数

若系统 A 是 2 维态空间，系统 B 是 3 维态空间，组合系统维数是多少？

### E. 纠缠判断

态：

$$
\frac{1}{\sqrt2}(|0\rangle|0\rangle+|1\rangle|1\rangle)
$$

为什么不是简单乘积态？

## 参考答案

### A

三维自由粒子：

$$
\hat H=\frac{\hat p_x^2+\hat p_y^2+\hat p_z^2}{2m}
$$

坐标表象中：

$$
\hat H=-\frac{\hbar^2}{2m}\left(
\frac{\partial^2}{\partial x^2}
+\frac{\partial^2}{\partial y^2}
+\frac{\partial^2}{\partial z^2}
\right)
$$

### B

因为 \(x\) 和 \(p_y=-i\hbar\partial/\partial y\) 属于不同坐标方向：

$$
[\hat x,\hat p_y]=0
$$

对任意 \(\psi(x,y,z)\)，先乘以 \(x\) 再对 \(y\) 求导，和先对 \(y\) 求导再乘以 \(x\)，结果相同。

### C

对乘积函数作用：

$$
H(\psi_1\psi_2)=(H_1+H_2)(\psi_1\psi_2)
$$

因为 \(H_1\) 只作用在 \(q_1\)，\(H_2\) 只作用在 \(q_2\)，所以：

$$
H(\psi_1\psi_2)=E_1\psi_1\psi_2+E_2\psi_1\psi_2
$$

即：

$$
H(\psi_1\psi_2)=(E_1+E_2)\psi_1\psi_2
$$

### D

张量积维数相乘：

$$
2\times3=6
$$

### E

如果它是：

$$
(a|0\rangle+b|1\rangle)\otimes(c|0\rangle+d|1\rangle)
$$

展开会得到：

$$
ac|00\rangle+ad|01\rangle+bc|10\rangle+bd|11\rangle
$$

目标态要求 \(ad=0\)、\(bc=0\)，但又要求 \(ac\ne0\)、\(bd\ne0\)。这些条件不能同时满足，所以它不是简单乘积态。
