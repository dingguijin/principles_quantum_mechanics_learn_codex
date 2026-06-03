# 第 7 章第 3 讲：升降算符和代数解法

本讲讲谐振子的核心技巧：不用先解微分方程，而用算符代数求能级。

## 1. 本讲要解决的问题

谐振子哈密顿量：

$$
H=\frac{p^2}{2m}+\frac12m\omega^2x^2
$$

看起来像 $`p^2+x^2`$。能不能把它写成某种“平方”的形式？

答案是引入升降算符。

## 2. 升降算符定义

定义：

$$
a=\sqrt{\frac{m\omega}{2\hbar}}x+\frac{i}{\sqrt{2m\hbar\omega}}p
$$

$$
a^\dagger=\sqrt{\frac{m\omega}{2\hbar}}x-\frac{i}{\sqrt{2m\hbar\omega}}p
$$

它们满足：

$$
[a,a^\dagger]=1
$$

这个对易关系是整个代数解法的核心。

## 3. 哈密顿量怎么改写

利用定义可得：

$$
H=\hbar\omega\left(a^\dagger a+\frac12\right)
$$

定义数算符：

$$
N=a^\dagger a
$$

于是：

$$
H=\hbar\omega\left(N+\frac12\right)
$$

如果：

$$
N\lvert n\rangle=n\lvert n\rangle
$$

那么：

$$
H\lvert n\rangle=\hbar\omega\left(n+\frac12\right)\lvert n\rangle
$$

## 4. 为什么叫升降算符

它们对数态作用为：

$$
a\lvert n\rangle=\sqrt n\lvert n-1\rangle
$$

$$
a^\dagger\lvert n\rangle=\sqrt{n+1}\lvert n+1\rangle
$$

所以：

- $`a`$ 把能级降一级。
- $`a^\dagger`$ 把能级升一级。

## 5. 物理意义

升降算符揭示谐振子能级像一层层楼梯。

每作用一次 $`a^\dagger`$，能量增加：

$$
\hbar\omega
$$

每作用一次 $`a`$，能量减少：

$$
\hbar\omega
$$

不能无限下降，因为能量不能低于基态。

## 6. 和后续章节的关系

升降算符不是只适用于谐振子。

它会在：

- 角动量升降算符。
- 自旋。
- 场量子化中的产生和湮灭算符。

中反复出现。

## 7. 练习

### 练习 1

写出 $`H`$ 的升降算符形式。

### 练习 2

如果 $`a^\dagger`$ 作用在 $`\lvert n\rangle`$ 上，会得到什么？

### 练习 3

为什么 $`a`$ 不能无限作用下去？

## 8. 解答

### 解答 1

$$
H=\hbar\omega\left(a^\dagger a+\frac12\right)
$$

### 解答 2

$$
a^\dagger\lvert n\rangle=\sqrt{n+1}\lvert n+1\rangle
$$

### 解答 3

因为能级不能降到负数编号。最低态 $`\lvert0\rangle`$ 满足 $`a\lvert0\rangle=0`$。

## 9. 本讲必须记住的三句话

1. 升降算符满足 $`[a,a^\dagger]=1`$。
2. $`H=\hbar\omega(a^\dagger a+1/2)`$。
3. $`a`$ 降低能级，$`a^\dagger`$ 升高能级。
