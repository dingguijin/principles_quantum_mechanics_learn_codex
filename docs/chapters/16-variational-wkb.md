# 16. The Variational and WKB Methods

前面许多章节都在研究可以精确求解的问题：无限深势阱、谐振子、氢原子。真实量子系统通常没有这么友好。

本章进入近似方法。

近似不是“算不准所以随便估计”。好的近似方法必须说明：

- 为什么这样近似。
- 误差方向或适用条件是什么。
- 哪些物理信息被保留。
- 哪些区域可能失效。

本章介绍两种重要近似：

1. 变分法：用试探态估计基态能量。
2. WKB 方法：在势能缓慢变化时，用经典动量近似量子相位。

## 本章学习路线

建议分 6 次学习：

1. [第 1 讲：为什么量子力学需要近似方法](../lessons/16-variational-wkb/16-01-why-approximation-methods.md)
2. [第 2 讲：变分原理，为什么试探能量给出基态上界](../lessons/16-variational-wkb/16-02-variational-principle-upper-bound.md)
3. [第 3 讲：试探波函数、参数优化和物理判断](../lessons/16-variational-wkb/16-03-trial-wavefunctions-optimization.md)
4. [第 4 讲：WKB 基本思想，从局域波长到相位积分](../lessons/16-variational-wkb/16-04-wkb-basic-idea.md)
5. [第 5 讲：WKB 量子化、转折点和隧穿](../lessons/16-variational-wkb/16-05-wkb-quantization-turning-points-tunneling.md)
6. [第 6 讲：近似方法的适用范围和后续章节入口](../lessons/16-variational-wkb/16-06-validity-and-next-methods.md)

## 第 1 讲：为什么需要近似

定态薛定谔方程：

$$
H\psi=E\psi
$$

是一个本征值问题。

但多数势能 $`V(x)`$ 或 $`V(\mathbf r)`$ 都不能给出封闭解析解。

近似方法的目标是：在不能精确求解时，仍然提取可靠物理信息。

变分法偏向回答：

> 基态能量大概是多少？波函数大概长什么样？

WKB 偏向回答：

> 半经典区域中，波函数相位如何积累？束缚态和隧穿概率如何估计？

## 第 2 讲：变分原理

设哈密顿量 $`H`$ 的真实基态能量为 $`E_0`$。

取任意归一化试探态 $`|\psi\rangle`$，定义试探能量：

$$
E[\psi]=\langle\psi|H|\psi\rangle
$$

变分原理说：

$$
E[\psi]\ge E_0
$$

为什么？

把试探态展开在能量本征态中：

$$
|\psi\rangle=\sum_n c_n|n\rangle
$$

其中：

$$
H|n\rangle=E_n|n\rangle
$$

且：

$$
E_0\le E_1\le E_2\le\cdots
$$

于是：

$$
\langle H\rangle=\sum_n |c_n|^2E_n
$$

因为每个 $`E_n\ge E_0`$，所以：

$$
\langle H\rangle\ge E_0\sum_n|c_n|^2=E_0
$$

这就是上界性质。

## 第 3 讲：试探波函数和参数优化

变分法的实际步骤：

1. 选择带参数的试探态 $`\psi_\alpha`$。
2. 计算：

$$
E(\alpha)=\frac{\langle\psi_\alpha|H|\psi_\alpha\rangle}
{\langle\psi_\alpha|\psi_\alpha\rangle}
$$

3. 对参数最小化：

$$
\frac{dE(\alpha)}{d\alpha}=0
$$

4. 得到最佳估计：

$$
E_{\text{var}}=\min_\alpha E(\alpha)
$$

试探函数必须尊重问题的基本物理：

- 对称性。
- 边界条件。
- 归一化。
- 大小尺度。
- 节点结构。

试探态选得越接近真实基态，估计越好。

## 第 4 讲：WKB 基本思想

一维定态方程：

$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V(x)\psi=E\psi
$$

如果 $`V(x)`$ 变化很慢，可以定义局域经典动量：

$$
p(x)=\sqrt{2m(E-V(x))}
$$

在经典允许区 $`E>V(x)`$，WKB 波函数近似为：

$$
\psi(x)\approx \frac{C}{\sqrt{p(x)}}
\exp\left(\pm\frac{i}{\hbar}\int^x p(x')dx'\right)
$$

物理意义：

- 相位由经典作用量积分给出。
- 局域波长为：

$$
\lambda(x)=\frac{h}{p(x)}
$$

- 振幅因子 $`1/\sqrt{p(x)}`$ 反映概率流守恒。

## 第 5 讲：转折点、量子化和隧穿

转折点满足：

$$
E=V(x)
$$

这里 $`p(x)=0`$，普通 WKB 公式会失效。

在两个转折点 $`x_1,x_2`$ 之间的束缚态，WKB 给出量子化条件：

$$
\int_{x_1}^{x_2}p(x)\,dx
=\left(n+\frac12\right)\pi\hbar
$$

这可以看成相位绕一圈后必须自洽。

在经典禁区 $`E<V(x)`$，令：

$$
\kappa(x)=\sqrt{2m(V(x)-E)}
$$

波函数近似指数衰减：

$$
\psi(x)\sim
\exp\left(-\frac{1}{\hbar}\int^x\kappa(x')dx'\right)
$$

势垒穿透概率的主要指数估计为：

$$
T\sim
\exp\left(-\frac{2}{\hbar}\int_{x_1}^{x_2}\kappa(x)\,dx\right)
$$

## 第 6 讲：适用范围

变分法可靠之处：

- 总能给基态能量上界。
- 好的试探函数可给出好估计。
- 对基态尤其有用。

变分法风险：

- 试探函数空间太差会给出很粗的上界。
- 上界接近不代表波函数处处准确。

WKB 可靠之处：

- 势能缓慢变化。
- 作用量尺度远大于 $`\hbar`$。
- 高量子数、半经典区域。

WKB 风险：

- 转折点附近普通形式失效。
- 势能突变处失效。
- 低能级、强量子效应区域可能很差。

近似方法的核心不是公式本身，而是知道公式何时可以相信。

## 本章总复习

变分能量：

$$
E[\psi]=\frac{\langle\psi|H|\psi\rangle}{\langle\psi|\psi\rangle}
$$

变分上界：

$$
E[\psi]\ge E_0
$$

WKB 经典动量：

$$
p(x)=\sqrt{2m(E-V(x))}
$$

允许区 WKB：

$$
\psi(x)\approx \frac{C}{\sqrt{p(x)}}
\exp\left(\pm\frac{i}{\hbar}\int^x p(x')dx'\right)
$$

束缚态量子化：

$$
\int_{x_1}^{x_2}p(x)\,dx
=\left(n+\frac12\right)\pi\hbar
$$

隧穿指数：

$$
T\sim
\exp\left(-\frac{2}{\hbar}\int_{x_1}^{x_2}\kappa(x)\,dx\right)
$$

## 本章作业

### A. 变分上界

为什么任意归一化试探态的能量期望值不低于基态能量？

### B. 参数优化

若试探能量 $`E(a)=a+1/a`$，其中 $`a>0`$，求最佳 $`a`$ 和最小能量。

### C. WKB 动量

写出经典允许区的局域动量 $`p(x)`$。

### D. 转折点

什么是 WKB 转折点？

### E. 隧穿

势垒越宽、越高，对 WKB 隧穿概率有什么影响？

## 参考答案

### A

把试探态展开在能量本征态中：

$$
|\psi\rangle=\sum_n c_n|n\rangle
$$

则：

$$
\langle H\rangle=\sum_n |c_n|^2E_n
$$

由于每个 $`E_n\ge E_0`$，所以：

$$
\langle H\rangle\ge E_0
$$

### B

求导：

$$
\frac{dE}{da}=1-\frac{1}{a^2}
$$

令其为 0，得：

$$
a=1
$$

最小能量：

$$
E_{\min}=1+1=2
$$

### C

$$
p(x)=\sqrt{2m(E-V(x))}
$$

适用于 $`E>V(x)`$ 的经典允许区。

### D

转折点满足：

$$
E=V(x)
$$

在这里经典动量为 0，普通 WKB 近似失效。

### E

势垒越宽或越高，积分：

$$
\int \kappa(x)dx
$$

越大，因此：

$$
T\sim e^{-2\int\kappa dx/\hbar}
$$

越小。
