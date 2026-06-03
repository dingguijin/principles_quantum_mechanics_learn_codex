# 7. The Harmonic Oscillator

谐振子是量子力学中最重要的可解模型之一。它重要不是因为“弹簧”本身多特殊，而是因为很多系统在稳定平衡点附近都可以近似为谐振子。

如果势能 $`V(x)`$ 在某个平衡点附近足够平滑，展开后最低非平凡项通常是二次项：

$$
V(x)\approx V(x_0)+\frac12 V''(x_0)(x-x_0)^2
$$

这就是谐振子形式。因此谐振子是理解振动、分子、声子、场量子和许多近似方法的基础。

## 本章学习路线

建议分 5 次学习：

1. [第 1 讲：为什么谐振子到处出现](../lessons/07-harmonic-oscillator/07-01-why-harmonic-oscillators-appear-everywhere.md)
2. [第 2 讲：谐振子哈密顿量和无量纲变量](../lessons/07-harmonic-oscillator/07-02-hamiltonian-dimensionless-variables.md)
3. [第 3 讲：升降算符和代数解法](../lessons/07-harmonic-oscillator/07-03-ladder-operators-algebraic-solution.md)
4. [第 4 讲：能级、零点能和基态波函数](../lessons/07-harmonic-oscillator/07-04-energy-levels-zero-point-ground-state.md)
5. [第 5 讲：数态、选择规则和谐振子为什么有用](../lessons/07-harmonic-oscillator/07-05-number-states-selection-rules-applications.md)

## 第 1 讲：为什么谐振子到处出现

经典谐振子的势能是：

$$
V(x)=\frac12 m\omega^2x^2
$$

力为：

$$
F=-\frac{dV}{dx}=-m\omega^2x
$$

这是线性恢复力。它的意思是：偏离平衡点越远，拉回来的力越大。

很多系统在平衡点附近都可以近似成这种形式。原因是 Taylor 展开。若 $`x_0`$ 是稳定平衡点，则：

$$
V'(x_0)=0,\quad V''(x_0)>0
$$

于是：

$$
V(x)\approx V(x_0)+\frac12 V''(x_0)(x-x_0)^2
$$

忽略常数 $`V(x_0)`$，就是谐振子势能。

## 第 2 讲：谐振子哈密顿量

量子谐振子的哈密顿量是：

$$
H=\frac{p^2}{2m}+\frac12m\omega^2x^2
$$

其中：

- 第一项是动能。
- 第二项是二次势能。

直接在位置表象求解，会得到：

$$
\left[-\frac{\hbar^2}{2m}\frac{d^2}{dx^2}+\frac12m\omega^2x^2\right]\psi(x)=E\psi(x)
$$

这当然可以解，但更有力的方法是代数法：引入升降算符。

## 第 3 讲：升降算符

定义升降算符：

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

哈密顿量可写为：

$$
H=\hbar\omega\left(a^\dagger a+\frac12\right)
$$

定义数算符：

$$
N=a^\dagger a
$$

若：

$$
N\lvert n\rangle=n\lvert n\rangle
$$

则：

$$
H\lvert n\rangle=\hbar\omega\left(n+\frac12\right)\lvert n\rangle
$$

## 第 4 讲：能级和零点能

谐振子的能级是：

$$
E_n=\hbar\omega\left(n+\frac12\right),\quad n=0,1,2,\dots
$$

能级等间隔：

$$
E_{n+1}-E_n=\hbar\omega
$$

基态能量不是 0，而是：

$$
E_0=\frac12\hbar\omega
$$

这叫零点能。

零点能不是人为加上去的常数，而是量子结构的结果。直觉上，如果粒子被限制在势阱附近，位置不可能任意确定，同时动量也不可能为零；不确定性阻止能量降到经典最低值 0。

## 第 5 讲：数态和应用

数态 $`\lvert n\rangle`$ 是谐振子的能量本征态。

升降算符作用为：

$$
a\lvert n\rangle=\sqrt{n}\lvert n-1\rangle
$$

$$
a^\dagger\lvert n\rangle=\sqrt{n+1}\lvert n+1\rangle
$$

这些公式说明：

- $`a`$ 降低一个能级。
- $`a^\dagger`$ 升高一个能级。
- 系数保证归一化正确。

谐振子广泛用于：

- 分子振动。
- 固体中的声子。
- 电磁场量子化。
- 任意平衡点附近的小振动近似。

## 本章总复习

必须记住：

$$
H=\frac{p^2}{2m}+\frac12m\omega^2x^2
$$

谐振子哈密顿量。

$$
[a,a^\dagger]=1
$$

升降算符对易关系。

$$
H=\hbar\omega\left(a^\dagger a+\frac12\right)
$$

哈密顿量的代数形式。

$$
E_n=\hbar\omega\left(n+\frac12\right)
$$

谐振子能级。

$$
a\lvert n\rangle=\sqrt{n}\lvert n-1\rangle,\quad
a^\dagger\lvert n\rangle=\sqrt{n+1}\lvert n+1\rangle
$$

升降算符作用。

## 常见误区

### 误区 1：谐振子只是弹簧模型

不对。弹簧只是最直观例子。任何稳定平衡点附近的平滑势能都可能近似为谐振子。

### 误区 2：零点能可以设为 0

不能在讨论能级结构时随便忽略。基态能量 $`\frac12\hbar\omega`$ 是量子谐振子的核心结果。

### 误区 3：升降算符只是计算技巧

升降算符揭示了能级结构和量子激发的代数本质。后面场量子化会把类似结构解释为粒子数的增减。

## 本章作业

### A. 能级

若 $`\hbar=1,\omega=2`$，求 $`E_0,E_1,E_2`$。

### B. 能级差

证明：

$$
E_{n+1}-E_n=\hbar\omega
$$

### C. 升降算符

计算：

$$
a\lvert 3\rangle,\quad a^\dagger\lvert 3\rangle
$$

## 参考答案

### A

$$
E_n=2\left(n+\frac12\right)
$$

所以：

$$
E_0=1,\quad E_1=3,\quad E_2=5
$$

### B

$$
E_{n+1}-E_n
=\hbar\omega\left(n+1+\frac12\right)-\hbar\omega\left(n+\frac12\right)
=\hbar\omega
$$

### C

$$
a\lvert3\rangle=\sqrt3\lvert2\rangle
$$

$$
a^\dagger\lvert3\rangle=2\lvert4\rangle
$$
