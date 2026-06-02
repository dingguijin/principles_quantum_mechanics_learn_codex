# 第 6 章第 3 讲：Ehrenfest 定理，量子平均如何接近牛顿方程

Ehrenfest 定理是量子力学通向经典力学的一座桥。

## 1. 本讲要解决的问题

我们想知道：

> 量子态的平均位置和平均动量是否满足类似经典方程？

答案是：在一定形式下，是的。

## 2. Ehrenfest 定理的公式

一维粒子哈密顿量：

$$
H=\frac{p^2}{2m}+V(x)
$$

Ehrenfest 定理给出：

$$
\frac{d}{dt}\langle x\rangle=\frac{\langle p\rangle}{m}
$$

以及：

$$
\frac{d}{dt}\langle p\rangle=-\left\langle \frac{dV}{dx}\right\rangle
$$

这很像经典 Hamilton 方程：

$$
\dot x=\frac{p}{m},\quad \dot p=-\frac{dV}{dx}
$$

## 3. 公式怎么理解

第一条说：

> 平均位置的变化率等于平均动量除以质量。

第二条说：

> 平均动量的变化率等于平均力。

这里力是：

$$
F(x)=-\frac{dV}{dx}
$$

所以：

$$
\frac{d}{dt}\langle p\rangle=\langle F(x)\rangle
$$

## 4. 为什么这还不是完整经典方程

注意：

$$
\left\langle \frac{dV}{dx}\right\rangle
$$

一般不等于：

$$
\frac{dV}{dx}(\langle x\rangle)
$$

只有当波包足够窄，并且势能在波包范围内变化不剧烈时，才有近似：

$$
\left\langle \frac{dV}{dx}\right\rangle\approx \frac{dV}{dx}(\langle x\rangle)
$$

这时：

$$
\frac{d}{dt}\langle p\rangle\approx-\frac{dV}{dx}(\langle x\rangle)
$$

才接近经典牛顿方程。

## 5. 物理意义

Ehrenfest 定理不是说所有量子态都像经典粒子。

它说：

> 期望值满足一组和经典方程相似的关系；当波包集中且势能平滑时，这组关系进一步近似为经典运动。

## 6. 和数学、后续章节的关系

数学上，Ehrenfest 定理来自薛定谔方程和算符对易关系。

后续关系：

- 第 9 章不确定性会限制波包能集中到什么程度。
- 第 16 章 WKB 会用另一种方式研究经典近似。

## 7. 练习

### 练习 1

写出 Ehrenfest 定理的两条一维公式。

### 练习 2

为什么 \(\langle dV/dx\rangle\) 不一定等于 \(dV/dx(\langle x\rangle)\)？

### 练习 3

在哪些条件下 Ehrenfest 定理接近牛顿方程？

## 8. 解答

### 解答 1

$$
\frac{d}{dt}\langle x\rangle=\frac{\langle p\rangle}{m}
$$

$$
\frac{d}{dt}\langle p\rangle=-\left\langle \frac{dV}{dx}\right\rangle
$$

### 解答 2

平均一个函数的值通常不等于把平均位置代入函数。除非波包很窄，函数在波包范围内变化很小。

### 解答 3

波包足够集中、势能足够平滑、波包没有明显分裂或强干涉时，期望值运动可近似经典方程。

## 9. 本讲必须记住的三句话

1. Ehrenfest 定理说明量子期望值满足类似经典的方程。
2. 平均力 \(\langle F\rangle\) 不一定等于平均位置处的力。
3. 经典运动出现需要波包集中和势能平滑。
