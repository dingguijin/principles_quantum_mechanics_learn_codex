# 8. The Path Integral Formulation of Quantum Theory

路径积分是量子力学的另一种表述。第 4 章以后我们主要用薛定谔方程：

$$
i\hbar\frac{d}{dt}\lvert\psi(t)\rangle=H\lvert\psi(t)\rangle
$$

来描述态如何演化。路径积分换一个问题：

> 从 \(x_i,t_i\) 到 \(x_f,t_f\) 的量子振幅是多少？

答案不是只取一条路径，而是把所有连接初末点的路径的振幅贡献相加。

## 本章学习路线

建议分 5 次学习：

1. [第 1 讲：为什么需要路径积分表述](../lessons/08-path-integral-formulation/08-01-why-path-integrals.md)
2. [第 2 讲：传播子，量子演化的核函数](../lessons/08-path-integral-formulation/08-02-propagator-kernel.md)
3. [第 3 讲：路径积分公式和作用量相位](../lessons/08-path-integral-formulation/08-03-path-integral-action-phase.md)
4. [第 4 讲：经典路径如何从相位相干中出现](../lessons/08-path-integral-formulation/08-04-classical-path-stationary-phase.md)
5. [第 5 讲：自由粒子例子和与薛定谔表述的关系](../lessons/08-path-integral-formulation/08-05-free-particle-and-schrodinger-equivalence.md)

## 第 1 讲：为什么需要路径积分表述

薛定谔表述强调态随时间演化：

$$
\lvert\psi(t_f)\rangle=U(t_f,t_i)\lvert\psi(t_i)\rangle
$$

路径积分强调从一个位置到另一个位置的振幅：

$$
K(x_f,t_f;x_i,t_i)
$$

它特别适合理解：

- 为什么作用量 \(S\) 在量子力学中重新出现。
- 为什么经典路径在经典极限中突出。
- 多路径干涉如何系统化。
- 后续场论和统计物理中的量子表述。

## 第 2 讲：传播子

传播子定义为：

$$
K(x_f,t_f;x_i,t_i)=\langle x_f|U(t_f,t_i)|x_i\rangle
$$

它的普通语言含义是：

> 系统从 \(t_i\) 时刻位于 \(x_i\)，到 \(t_f\) 时刻位于 \(x_f\) 的概率振幅。

如果知道初始波函数 \(\psi(x_i,t_i)\)，末态波函数可由：

$$
\psi(x_f,t_f)=\int dx_i\,K(x_f,t_f;x_i,t_i)\psi(x_i,t_i)
$$

得到。

所以传播子像一个“演化核函数”。

## 第 3 讲：路径积分公式

路径积分形式上写作：

$$
K(x_f,t_f;x_i,t_i)=\int \mathcal D x(t)\,
\exp\left(\frac{iS[x(t)]}{\hbar}\right)
$$

其中积分覆盖所有满足：

$$
x(t_i)=x_i,\quad x(t_f)=x_f
$$

的路径。

作用量是：

$$
S[x(t)]=\int_{t_i}^{t_f}L(x,\dot x,t)\,dt
$$

每条路径贡献一个相位：

$$
e^{iS/\hbar}
$$

注意：这不是说粒子像经典小球一样真的同时走所有路径。更谨慎地说，路径积分是一种计算总振幅的规则：所有路径的振幅贡献都要相加。

## 第 4 讲：经典路径如何出现

第 6 章已经讲过，经典极限常常对应：

$$
S\gg\hbar
$$

路径积分中，非经典路径的相位：

$$
e^{iS/\hbar}
$$

随路径变化很快。相近路径贡献相位差异大，容易互相抵消。

经典路径满足驻作用量条件：

$$
\delta S=0
$$

因此经典路径附近的相位变化慢，贡献更容易相干叠加。

这解释了为什么经典轨迹不是被量子理论外加进去的，而是在经典极限中从量子振幅求和里浮现出来。

## 第 5 讲：自由粒子例子和等价性

自由粒子的拉格朗日量：

$$
L=\frac12m\dot x^2
$$

传播子有标准形式：

$$
K(x_f,t_f;x_i,t_i)
=\sqrt{\frac{m}{2\pi i\hbar T}}
\exp\left[\frac{im(x_f-x_i)^2}{2\hbar T}\right]
$$

其中：

$$
T=t_f-t_i
$$

指数中的量正是经典直线路径的作用量：

$$
S_{\text{cl}}=\frac{m(x_f-x_i)^2}{2T}
$$

路径积分表述和薛定谔表述不是两套不同理论，而是等价表述。一个强调微分方程，一个强调路径振幅求和。

## 本章总复习

必须记住：

$$
K(x_f,t_f;x_i,t_i)=\langle x_f|U(t_f,t_i)|x_i\rangle
$$

传播子是从初位置到末位置的演化振幅。

$$
\psi(x_f,t_f)=\int dx_i\,K(x_f,t_f;x_i,t_i)\psi(x_i,t_i)
$$

传播子推进波函数。

$$
K=\int\mathcal D x(t)\,e^{iS[x]/\hbar}
$$

路径积分的核心结构。

$$
\delta S=0
$$

经典路径是作用量驻值路径。

## 常见误区

### 误区 1：路径积分说粒子真的走所有经典路径

不要这样理解。路径积分是振幅计算规则。它把所有路径的相位贡献相加，而不是把每条路径都当作可同时观测的经典轨迹。

### 误区 2：路径积分和薛定谔方程是两种不同物理

不是。它们是同一量子力学的等价表述。

### 误区 3：经典路径是路径积分里唯一路径

不是。所有路径都贡献。只是经典极限中，非经典路径相位抵消，经典路径附近贡献占主导。

## 本章作业

### A. 传播子含义

用普通语言解释：

$$
K(x_f,t_f;x_i,t_i)
$$

### B. 作用量相位

为什么路径积分中会出现：

$$
e^{iS/\hbar}
$$

这种形式时，\(S\gg\hbar\) 会导致快速振荡？

### C. 经典路径

解释为什么 \(\delta S=0\) 会让经典路径附近贡献更容易保留下来。

## 参考答案

### A

它是系统从 \(t_i\) 时刻位置 \(x_i\) 演化到 \(t_f\) 时刻位置 \(x_f\) 的概率振幅。

### B

指数相位是 \(S/\hbar\)。当 \(S\) 远大于 \(\hbar\) 时，路径稍微变化就会让相位变化很多，导致不同路径贡献快速振荡。

### C

\(\delta S=0\) 表示作用量在经典路径附近一阶变化为零，因此附近路径相位变化慢，振幅更容易同相叠加；非经典路径相位变化快，容易抵消。
