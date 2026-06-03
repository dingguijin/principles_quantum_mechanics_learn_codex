# 11. Symmetries and Their Consequences

对称性是物理学中最强的组织原则之一。它说的不是“图形好看”，而是：

> 对系统做某种变换后，物理规律不变。

量子力学中，对称性通常由保持内积的变换表示，也就是幺正算符。连续对称性还会带来生成元，而生成元常常就是某个可观测量：平移的生成元是动量，时间平移的生成元是哈密顿量，转动的生成元是角动量。

本章的核心问题是：

> 为什么对称性会导致守恒量？

## 本章学习路线

建议分 5 次学习：

1. [第 1 讲：什么是对称性，为什么它能压缩物理规律](../lessons/11-symmetries/11-01-what-is-symmetry.md)
2. [第 2 讲：量子态的变换为什么要用幺正算符](../lessons/11-symmetries/11-02-unitary-transformations.md)
3. [第 3 讲：连续对称性和生成元](../lessons/11-symmetries/11-03-continuous-symmetries-generators.md)
4. [第 4 讲：平移、时间平移和动量能量](../lessons/11-symmetries/11-04-translations-momentum-energy.md)
5. [第 5 讲：守恒量、对易关系和后续角动量入口](../lessons/11-symmetries/11-05-conservation-commutators-angular-momentum-entry.md)

## 第 1 讲：什么是对称性

一个变换如果不改变系统的物理内容，就叫系统的对称变换。

例子：

- 自由粒子在空间中平移后，物理规律不变。
- 孤立系统整体延迟一段时间，物理规律不变。
- 中心势 \(V(r)\) 在空间转动后不变。

对称性重要，是因为它减少了我们需要单独分析的情况。

如果系统对空间平移对称，那么在 \(x=0\) 和 \(x=10\) 处的物理规律相同。

如果系统对转动对称，那么选哪个方向作 \(z\) 轴不应影响物理结论。

## 第 2 讲：量子对称变换和幺正算符

量子态之间的物理距离由内积决定。两个态的概率振幅是：

$$
\langle\phi|\psi\rangle
$$

概率由模平方给出：

$$
|\langle\phi|\psi\rangle|^2
$$

如果一个变换是对称变换，它不能改变可测概率。因此它应保持内积。

保持内积的线性变换由幺正算符表示：

$$
U^\dagger U=I
$$

态变换为：

$$
|\psi\rangle\to U|\psi\rangle
$$

若：

$$
\langle\phi|\psi\rangle
$$

在变换后不变，则：

$$
\langle U\phi|U\psi\rangle
=\langle\phi|U^\dagger U|\psi\rangle
=\langle\phi|\psi\rangle
$$

这就是为什么量子对称变换通常用幺正算符表示。

## 第 3 讲：连续对称性和生成元

连续对称性是一族可以用连续参数标记的变换。

例如一维空间平移：

$$
a
$$

可以取任意实数。

对应的幺正算符写成：

$$
U(a)
$$

连续变换可以由无穷小变换累积得到。一般形式是：

$$
U(\epsilon)=I-\frac{i}{\hbar}\epsilon G
$$

其中 \(G\) 叫生成元。

有限变换写成指数形式：

$$
U(a)=e^{-iaG/\hbar}
$$

为什么有这个公式？因为许多小变换连续相乘，会产生指数。

生成元 \(G\) 通常是厄米算符，因此可观测。

## 第 4 讲：平移和时间平移

空间平移由动量生成：

$$
U(a)=e^{-ia\hat p/\hbar}
$$

对位置波函数来说，平移后的函数满足：

$$
(U(a)\psi)(x)=\psi(x-a)
$$

小平移展开：

$$
\psi(x-a)=\psi(x)-a\frac{d\psi}{dx}
$$

而：

$$
U(a)\approx I-\frac{ia\hat p}{\hbar}
$$

代入：

$$
\hat p=-i\hbar\frac{d}{dx}
$$

就得到同样结果。

时间平移由哈密顿量生成：

$$
U(t)=e^{-i\hat Ht/\hbar}
$$

这正是薛定谔时间演化算符。

## 第 5 讲：对称性和守恒量

如果哈密顿量在某个变换 \(U\) 下不变，表示：

$$
U^\dagger H U=H
$$

对连续变换：

$$
U(a)=e^{-iaG/\hbar}
$$

这通常等价于：

$$
[H,G]=0
$$

而若：

$$
[H,G]=0
$$

则 \(G\) 是守恒量。理由来自 Heisenberg 形式：

$$
\frac{d\langle G\rangle}{dt}
=\frac{i}{\hbar}\langle[H,G]\rangle
+\left\langle\frac{\partial G}{\partial t}\right\rangle
$$

如果 \(G\) 不显含时间，且 \([H,G]=0\)，则：

$$
\frac{d\langle G\rangle}{dt}=0
$$

这就是量子力学中的对称性与守恒量关系。

## 本章总复习

幺正算符保持内积：

$$
U^\dagger U=I
$$

连续变换由生成元控制：

$$
U(a)=e^{-iaG/\hbar}
$$

空间平移的生成元是动量：

$$
U(a)=e^{-ia\hat p/\hbar}
$$

时间平移的生成元是哈密顿量：

$$
U(t)=e^{-i\hat Ht/\hbar}
$$

若：

$$
[H,G]=0
$$

则 \(G\) 是守恒量。

## 本章作业

### A. 幺正性

证明幺正变换保持内积。

### B. 平移生成元

用：

$$
\psi(x-a)=\psi(x)-a\frac{d\psi}{dx}
$$

说明平移生成元为什么是 \(\hat p\)。

### C. 守恒量

若 \([H,A]=0\)，且 \(A\) 不显含时间，说明 \(\langle A\rangle\) 是否随时间变化。

### D. 空间平移对称性

若一个系统的势能 \(V(x)\) 是常数，说明它为什么具有平移对称性。

### E. 转动入口

中心势 \(V(r)\) 为什么具有转动对称性？

## 参考答案

### A

若：

$$
|\psi'\rangle=U|\psi\rangle,\quad |\phi'\rangle=U|\phi\rangle
$$

则：

$$
\langle\phi'|\psi'\rangle
=\langle\phi|U^\dagger U|\psi\rangle
$$

幺正性给出：

$$
U^\dagger U=I
$$

所以：

$$
\langle\phi'|\psi'\rangle=\langle\phi|\psi\rangle
$$

### B

小平移满足：

$$
(U(a)\psi)(x)=\psi(x-a)
=\psi(x)-a\frac{d\psi}{dx}
$$

若：

$$
U(a)\approx I-\frac{iaG}{\hbar}
$$

则：

$$
-\frac{iG}{\hbar}=-\frac{d}{dx}
$$

所以：

$$
G=-i\hbar\frac{d}{dx}=\hat p
$$

### C

由：

$$
\frac{d\langle A\rangle}{dt}
=\frac{i}{\hbar}\langle[H,A]\rangle
$$

若 \([H,A]=0\)，则：

$$
\frac{d\langle A\rangle}{dt}=0
$$

\(\langle A\rangle\) 守恒。

### D

若 \(V(x)\) 是常数，平移 \(x\to x+a\) 后：

$$
V(x+a)=V(x)
$$

所以哈密顿量不因空间位置整体移动而改变，系统具有平移对称性。

### E

中心势只依赖：

$$
r=\sqrt{x^2+y^2+z^2}
$$

空间转动不改变 \(r\)，因此不改变 \(V(r)\)。所以中心势具有转动对称性。
