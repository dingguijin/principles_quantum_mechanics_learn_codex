# 9. The Heisenberg Uncertainty Relations

不确定性关系是量子力学最容易被误解的主题之一。它不是说“仪器不够好”，也不是说“实验者干扰了系统所以测不准”。更根本地说，它是量子态、内积、方差和非对易算符共同决定的结构限制。

最著名的形式是：

$$
\Delta x\,\Delta p\ge \frac{\hbar}{2}
$$

这句话的意思不是“不能精确测量位置”，而是：

> 对同一个量子态来说，位置分布和动量分布不能同时任意窄。

## 本章学习路线

建议分 5 次学习：

1. [第 1 讲：平均值、方差和不确定度](../lessons/09-heisenberg-uncertainty/09-01-expectation-variance-uncertainty.md)
2. [第 2 讲：波包直觉，为什么越局域动量越分散](../lessons/09-heisenberg-uncertainty/09-02-wave-packet-localization-momentum-spread.md)
3. [第 3 讲：一般不确定性关系和对易子](../lessons/09-heisenberg-uncertainty/09-03-general-uncertainty-commutator.md)
4. [第 4 讲：位置动量不确定性关系](../lessons/09-heisenberg-uncertainty/09-04-position-momentum-uncertainty.md)
5. [第 5 讲：常见误解、物理意义和应用](../lessons/09-heisenberg-uncertainty/09-05-misconceptions-meaning-applications.md)

## 第 1 讲：平均值、方差和不确定度

对观测量 $`A`$，量子态 $`\lvert\psi\rangle`$ 中的平均值是：

$$
\langle A\rangle=\langle\psi|A|\psi\rangle
$$

不确定度描述测量结果围绕平均值的分散程度。定义：

$$
(\Delta A)^2=\langle A^2\rangle-\langle A\rangle^2
$$

其中：

$$
\Delta A=\sqrt{\langle A^2\rangle-\langle A\rangle^2}
$$

这和概率论中的标准差是同一个思想。

如果 $`\Delta A=0`$，说明态是 $`A`$ 的某个本征态，测量 $`A`$ 得到确定结果。

## 第 2 讲：波包直觉

位置波函数 $`\psi(x)`$ 越集中，表示粒子位置越确定。

但一个非常窄的波包需要很多不同波长的平面波叠加。不同波长对应不同动量：

$$
p=\hbar k
$$

所以位置越局域，动量成分越分散。

这就是 $`\Delta x\Delta p`$ 关系的直观来源。

普通语言：

> 要把波包压得很窄，就必须混合许多 $`k`$；而 $`k`$ 的分散就是动量分散。

## 第 3 讲：一般不确定性关系

对两个观测量 $`A,B`$，一般有：

$$
\Delta A\,\Delta B\ge \frac12\left|\langle [A,B]\rangle\right|
$$

其中：

$$
[A,B]=AB-BA
$$

是对易子。

如果：

$$
[A,B]\ne0
$$

则两个观测量通常不能在同一个态中同时拥有任意小的不确定度。

如果：

$$
[A,B]=0
$$

则它们可能有共同本征态，在合适态中可以同时确定。

## 第 4 讲：位置和动量

位置和动量满足：

$$
[\hat x,\hat p]=i\hbar
$$

代入一般不确定性关系：

$$
\Delta x\,\Delta p\ge \frac12|\langle i\hbar\rangle|
$$

因为 $`\hbar`$ 是常数：

$$
\Delta x\,\Delta p\ge \frac{\hbar}{2}
$$

这就是 Heisenberg 位置动量不确定性关系。

## 第 5 讲：物理意义和常见误解

不确定性关系不是禁止你精确测量单个量。你可以制备一个位置很集中的态，使 $`\Delta x`$ 很小。

但代价是：

$$
\Delta p
$$

会变大。

它限制的是同一个态中两个非对易观测量分布宽度的乘积。

常见误解：

- 误解：只是仪器不够精密。
- 更正：这是态本身的结构限制。

- 误解：测量位置会让动量“被撞乱”，所以不确定。
- 更正：测量扰动是另一个问题；这里的不确定性是测量前态的分布宽度关系。

- 误解：不确定性说明量子力学不精确。
- 更正：量子力学精确给出概率分布及其限制。

## 本章总复习

必须记住：

$$
(\Delta A)^2=\langle A^2\rangle-\langle A\rangle^2
$$

不确定度是标准差。

$$
\Delta A\,\Delta B\ge \frac12|\langle[A,B]\rangle|
$$

一般不确定性关系。

$$
[\hat x,\hat p]=i\hbar
$$

位置和动量的基本对易关系。

$$
\Delta x\,\Delta p\ge \frac{\hbar}{2}
$$

位置动量不确定性关系。

## 本章作业

### A. 方差

某观测量只有两个可能结果 $`+1,-1`$，概率各为 $`1/2`$。求平均值和方差。

### B. 对易子

如果 $`[A,B]=0`$，这对同时确定 $`A,B`$ 有什么意义？

### C. 位置动量

如果某态中 $`\Delta x`$ 变得很小，$`\Delta p`$ 必须怎样变化？

## 参考答案

### A

平均值：

$$
\langle A\rangle=\frac12(1)+\frac12(-1)=0
$$

二次平均：

$$
\langle A^2\rangle=\frac12(1)^2+\frac12(-1)^2=1
$$

方差：

$$
(\Delta A)^2=1-0=1
$$

所以：

$$
\Delta A=1
$$

### B

对易为零表示两个算符可能有共同本征态。在共同本征态中，两个观测量都可以有确定值。

### C

由于：

$$
\Delta x\,\Delta p\ge \frac{\hbar}{2}
$$

$`\Delta x`$ 变小会迫使 $`\Delta p`$ 不能任意小，通常需要变大。
