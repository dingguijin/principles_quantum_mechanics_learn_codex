# 6. The Classical Limit

第 6 章讨论一个必要问题：

> 如果量子力学是更基本的理论，为什么我们在日常世界里看到的却像经典力学？

经典极限不是一句“令 \(\hbar=0\)”就结束。真正的问题是：在什么条件下，量子态的概率分布、期望值、相位干涉和测量精度，会共同表现得像一个经典粒子沿轨道运动？

## 本章学习路线

建议分 4 次学习：

1. [第 1 讲：为什么经典极限不是简单令 \(\hbar=0\)](../lessons/06-classical-limit/06-01-why-classical-limit-is-not-just-hbar-zero.md)
2. [第 2 讲：波包、期望值和经典轨迹](../lessons/06-classical-limit/06-02-wave-packets-expectation-values-classical-trajectories.md)
3. [第 3 讲：Ehrenfest 定理，量子平均如何接近牛顿方程](../lessons/06-classical-limit/06-03-ehrenfest-theorem.md)
4. [第 4 讲：相位快速振荡、测量精度和经典图像的出现](../lessons/06-classical-limit/06-04-rapid-phases-measurement-resolution-classical-picture.md)

本章主线是：

> 量子态不是点，而是分布；经典轨迹出现于波包足够集中、势能足够平滑、相位干涉在宏观尺度被平均、测量无法分辨微观结构的条件下。

## 第 1 讲：为什么经典极限不是简单令 \(\hbar=0\)

量子力学中很多公式含有 \(\hbar\)。例如：

$$
i\hbar\frac{\partial \psi}{\partial t}=H\psi
$$

以及：

$$
[\hat x,\hat p]=i\hbar
$$

这容易让人以为经典极限就是把 \(\hbar\) 设为 0。但这不严谨。因为如果直接把 \(\hbar=0\) 代入薛定谔方程，方程本身会退化，不能自动给出牛顿轨迹。

更好的说法是：

> 当系统的典型作用量 \(S\) 远大于 \(\hbar\) 时，量子相位快速振荡，许多非经典贡献互相抵消，经典路径附近的贡献占主导。

即：

$$
S\gg \hbar
$$

这才是经典极限的常见尺度条件。

## 第 2 讲：波包、期望值和经典轨迹

经典粒子像一个点：

$$
x(t),p(t)
$$

量子态通常是空间中的概率分布：

$$
|\psi(x,t)|^2
$$

如果这个分布非常集中，我们可以用期望值描述它的位置中心：

$$
\langle x\rangle=\int x|\psi(x)|^2dx
$$

动量期望值：

$$
\langle p\rangle=\langle\psi|\hat p|\psi\rangle
$$

当波包足够窄，并且势能在波包宽度内变化不剧烈时，\(\langle x\rangle,\langle p\rangle\) 的运动可能近似经典轨迹。

但如果波包很宽、分裂成多个部分，或者发生明显干涉，那么“一个经典位置”的说法就失效。

## 第 3 讲：Ehrenfest 定理

Ehrenfest 定理说明量子期望值与经典方程之间的联系。

一维情形中：

$$
\frac{d}{dt}\langle x\rangle=\frac{\langle p\rangle}{m}
$$

以及：

$$
\frac{d}{dt}\langle p\rangle=-\left\langle \frac{dV}{dx}\right\rangle
$$

这看起来接近 Hamilton 或 Newton 方程。但注意第二条不是：

$$
\frac{d}{dt}\langle p\rangle=-\frac{dV}{dx}(\langle x\rangle)
$$

除非势能在波包范围内足够平滑，近似有：

$$
\left\langle \frac{dV}{dx}\right\rangle\approx \frac{dV}{dx}(\langle x\rangle)
$$

这就是经典近似成立的条件之一。

## 第 4 讲：相位、测量精度和经典图像

量子干涉依赖相位。路径积分语言中，每条路径的贡献大致带有相位：

$$
e^{iS/\hbar}
$$

当 \(S/\hbar\) 很大时，相位对路径微小变化非常敏感。大量路径的贡献会快速振荡并互相抵消，经典路径附近因为 \(\delta S=0\) 保留下来。

另一个因素是测量精度。宏观测量通常无法分辨极小的量子涨落、相位差和微观干涉结构。因此实际观测会呈现更粗粒度的经典图像。

经典极限常常需要三件事一起出现：

- 尺度条件：典型作用量远大于 \(\hbar\)。
- 动力学条件：波包集中且势能平滑。
- 观测条件：测量精度不足以分辨微观干涉。

## 本章总复习

必须记住：

$$
\langle x\rangle=\int x|\psi(x)|^2dx
$$

位置期望值是概率分布的平均位置。

$$
\frac{d}{dt}\langle x\rangle=\frac{\langle p\rangle}{m}
$$

位置期望值的变化率与动量期望值相关。

$$
\frac{d}{dt}\langle p\rangle=-\left\langle \frac{dV}{dx}\right\rangle
$$

动量期望值的变化率由平均力决定。

$$
S\gg\hbar
$$

是经典极限常见的尺度条件。

## 常见误区

### 误区 1：宏观物体没有量子性

不准确。宏观物体仍由量子理论描述，只是量子效应在宏观条件下通常难以分辨。

### 误区 2：经典极限就是 \(\hbar=0\)

不准确。更重要的是 \(S/\hbar\) 很大、相位快速振荡、波包和测量条件使经典图像有效。

### 误区 3：期望值就是最可能值

不一定。分布对称或多峰时，期望值可能不等于最可能位置，也可能不代表任何实际峰的位置。

## 本章作业

### A. 期望值

如果一个粒子有一半概率在 \(x=1\)，一半概率在 \(x=3\)，求 \(\langle x\rangle\)。

### B. Ehrenfest 近似

解释为什么：

$$
\left\langle \frac{dV}{dx}\right\rangle\approx \frac{dV}{dx}(\langle x\rangle)
$$

只在波包足够窄、势能变化足够平滑时成立。

### C. 经典极限

用自己的话说明为什么 \(S\gg\hbar\) 时，经典路径更容易出现。

## 参考答案

### A

$$
\langle x\rangle=\frac12\cdot1+\frac12\cdot3=2
$$

### B

如果波包很窄，粒子主要分布在 \(\langle x\rangle\) 附近。若势能斜率在这小范围内几乎不变，平均斜率就近似等于平均位置处的斜率。

### C

路径贡献相位为 \(e^{iS/\hbar}\)。当 \(S/\hbar\) 很大时，相位随路径变化快速振荡，非经典路径贡献互相抵消；经典路径附近满足 \(\delta S=0\)，相位变化慢，因此贡献保留下来。
