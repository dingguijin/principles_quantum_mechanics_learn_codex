# 第 9 章第 4 讲：位置动量不确定性关系

本讲推出最著名的不确定性关系：

$$
\Delta x\,\Delta p\ge\frac{\hbar}{2}
$$

## 1. 本讲要解决的问题

位置和动量为什么不能同时任意精确？

答案来自基本对易关系：

$$
[\hat x,\hat p]=i\hbar
$$

## 2. 从一般关系推出

一般不确定性关系：

$$
\Delta A\,\Delta B\ge \frac12|\langle[A,B]\rangle|
$$

令：

$$
A=\hat x,\quad B=\hat p
$$

则：

$$
\Delta x\,\Delta p\ge \frac12|\langle[\hat x,\hat p]\rangle|
$$

使用：

$$
[\hat x,\hat p]=i\hbar
$$

得到：

$$
\Delta x\,\Delta p\ge \frac12|\langle i\hbar\rangle|
$$

因为 $`\hbar`$ 是常数：

$$
\Delta x\,\Delta p\ge\frac{\hbar}{2}
$$

## 3. 物理意义

同一个量子态中，位置分布和动量分布不能同时任意窄。

如果：

$$
\Delta x\to0
$$

则：

$$
\Delta p
$$

必须变大。

反过来，如果动量非常确定，位置就会非常分散。

## 4. 它禁止什么，不禁止什么

它不禁止精确测量一次位置。

它限制的是：

> 一个态在位置和动量两种测量中的分布宽度乘积。

也就是说，你可以制备位置很窄的态，但这个态的动量分布会很宽。

## 5. 和一维问题的关系

无限深势阱中，粒子被限制在长度 $`L`$ 内，所以位置不确定度有限。

因此动量不可能精确为 0。这帮助理解为什么基态能量不为 0。

谐振子零点能也可用同样直觉理解。

## 6. 练习

### 练习 1

用一般不确定性关系推出 $`\Delta x\Delta p\ge\hbar/2`$。

### 练习 2

如果 $`\Delta x`$ 很小，$`\Delta p`$ 可以也很小吗？

### 练习 3

不确定性关系是否禁止测量位置？

## 7. 解答

### 解答 1

代入 $`[\hat x,\hat p]=i\hbar`$：

$$
\Delta x\Delta p\ge \frac12|\langle i\hbar\rangle|=\frac{\hbar}{2}
$$

### 解答 2

不可以。乘积必须至少为 $`\hbar/2`$。

### 解答 3

不禁止。它限制的是同一个态的位置分布宽度和动量分布宽度的乘积。

## 8. 本讲必须记住的三句话

1. 位置动量关系来自 $`[\hat x,\hat p]=i\hbar`$。
2. $`\Delta x\Delta p\ge\hbar/2`$ 是态分布宽度的限制。
3. 它不禁止精确测量单个物理量。
