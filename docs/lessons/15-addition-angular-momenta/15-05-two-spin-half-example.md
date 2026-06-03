# 第 15 章第 5 讲：两个自旋 1/2 的完整例子

本讲用最小例子把角动量加法算清楚。

## 1. 为什么看这个例子

两个自旋 \(1/2\) 是最简单、最重要的角动量加法例子。

它出现在：

- 双电子系统。
- 自旋纠缠。
- singlet/triplet 态。
- 量子信息中的两比特态。

## 2. 非耦合基底

每个自旋有两个态：

$$
|\uparrow\rangle,\quad |\downarrow\rangle
$$

两个自旋的张量积空间有四个基底：

$$
|\uparrow\uparrow\rangle
$$

$$
|\uparrow\downarrow\rangle
$$

$$
|\downarrow\uparrow\rangle
$$

$$
|\downarrow\downarrow\rangle
$$

## 3. 允许的总角动量

这里：

$$
j_1=j_2=\frac12
$$

所以：

$$
j=1,\quad 0
$$

\(j=1\) 有 3 个 \(m\) 态，叫三重态。

\(j=0\) 有 1 个 \(m\) 态，叫单重态。

## 4. 三重态

$$
|1,1\rangle=|\uparrow\uparrow\rangle
$$

$$
|1,0\rangle=
\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle+|\downarrow\uparrow\rangle\right)
$$

$$
|1,-1\rangle=|\downarrow\downarrow\rangle
$$

这三个态在交换两个自旋时是对称的。

## 5. 单重态

$$
|0,0\rangle=
\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle-|\downarrow\uparrow\rangle\right)
$$

这个态在交换两个自旋时变号，是反对称的。

它也是重要的纠缠态。

## 6. 物理意义

同样的四维空间可以组织成：

$$
2\times2=4
$$

也可以组织成：

$$
3+1=4
$$

前者是非耦合基底，后者是耦合基底。

## 7. 练习

### 练习 1

写出两个自旋 \(1/2\) 的四个非耦合基底。

### 练习 2

写出单重态。

### 练习 3

两个自旋 \(1/2\) 合成的总 \(j\) 有哪些？

## 8. 解答

### 解答 1

$$
|\uparrow\uparrow\rangle,\quad
|\uparrow\downarrow\rangle,\quad
|\downarrow\uparrow\rangle,\quad
|\downarrow\downarrow\rangle
$$

### 解答 2

$$
|0,0\rangle=
\frac{1}{\sqrt2}
\left(|\uparrow\downarrow\rangle-|\downarrow\uparrow\rangle\right)
$$

### 解答 3

$$
j=1,\quad j=0
$$

## 9. 本讲必须记住的三句话

1. 两个自旋 \(1/2\) 给出 \(1\oplus0\)。
2. 三重态是对称组合。
3. 单重态是反对称组合，也是纠缠态。
