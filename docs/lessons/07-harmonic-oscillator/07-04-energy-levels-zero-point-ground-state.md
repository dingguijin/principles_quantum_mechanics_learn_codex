# 第 7 章第 4 讲：能级、零点能和基态波函数

本讲讲谐振子的最著名结果：等间隔能级和零点能。

## 1. 本讲要解决的问题

谐振子的允许能量是什么？

答案：

$$
E_n=\hbar\omega\left(n+\frac12\right),\quad n=0,1,2,\dots
$$

## 2. 公式怎么来的

上一讲得到：

$$
H=\hbar\omega\left(N+\frac12\right)
$$

若：

$$
N\lvert n\rangle=n\lvert n\rangle
$$

则：

$$
H\lvert n\rangle
=\hbar\omega\left(n+\frac12\right)\lvert n\rangle
$$

所以：

$$
E_n=\hbar\omega\left(n+\frac12\right)
$$

## 3. 等间隔能级

相邻能级差：

$$
E_{n+1}-E_n
=\hbar\omega\left(n+1+\frac12\right)-\hbar\omega\left(n+\frac12\right)
=\hbar\omega
$$

所以能级等间隔。

## 4. 零点能

基态 $`n=0`$ 的能量：

$$
E_0=\frac12\hbar\omega
$$

不是零。

这叫零点能。

经典谐振子可以静止在平衡点，能量为 0。量子谐振子不行。直觉原因是：如果位置完全固定在平衡点，动量不确定性会变得很大；系统无法同时让位置和动量贡献都为零。

## 5. 基态波函数

基态满足：

$$
a\lvert0\rangle=0
$$

在位置表象中，这会给出高斯型波函数：

$$
\psi_0(x)=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}
e^{-m\omega x^2/(2\hbar)}
$$

它集中在 $`x=0`$ 附近，但不是 delta 函数。

## 6. 物理意义

零点能说明量子系统即使在最低态，也保留不可消除的量子涨落。

这在分子振动、固体、量子场论中都很重要。

## 7. 练习

### 练习 1

若 $`\hbar=1,\omega=2`$，求 $`E_0,E_1,E_2`$。

### 练习 2

证明相邻能级差为 $`\hbar\omega`$。

### 练习 3

为什么基态能量不是零？

## 8. 解答

### 解答 1

$$
E_n=2\left(n+\frac12\right)
$$

所以：

$$
E_0=1,\quad E_1=3,\quad E_2=5
$$

### 解答 2

$$
E_{n+1}-E_n=\hbar\omega
$$

直接由公式相减得到。

### 解答 3

量子态不能同时让位置完全固定且动量为零。不确定性使最低能量仍保留 $`\frac12\hbar\omega`$。

## 9. 本讲必须记住的三句话

1. 谐振子能级为 $`E_n=\hbar\omega(n+1/2)`$。
2. 能级等间隔，间隔为 $`\hbar\omega`$。
3. 基态能量 $`\frac12\hbar\omega`$ 是零点能。
