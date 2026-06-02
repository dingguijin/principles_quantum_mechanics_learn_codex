# 第 2 章第 4 讲：拉格朗日量和 Euler-Lagrange 方程

本讲进入拉格朗日形式。

## 1. 本讲要解决的问题

牛顿形式用力：

$$
F=ma
$$

拉格朗日形式不用直接写力，而用一个函数：

$$
L(q,\dot q,t)
$$

然后由 Euler-Lagrange 方程给出运动。

## 2. 为什么有拉格朗日量

拉格朗日量定义为：

$$
L=T-V
$$

它不是总能量。总能量通常是：

$$
E=T+V
$$

为什么用 \(T-V\)？因为这个组合放进作用量后，能产生正确的运动方程，而且适合广义坐标和约束系统。

## 3. 公式怎么来的

Euler-Lagrange 方程是：

$$
\frac{d}{dt}\left(\frac{\partial L}{\partial \dot q}\right)
-\frac{\partial L}{\partial q}=0
$$

它来自作用量驻值条件，第 5 讲会讲。本讲先验证它回到牛顿方程。

一维粒子：

$$
T=\frac12 m\dot{x}^2,\quad V=V(x)
$$

所以：

$$
L=\frac12 m\dot{x}^2-V(x)
$$

计算：

$$
\frac{\partial L}{\partial \dot{x}}=m\dot{x}
$$

对时间求导：

$$
\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{x}}\right)=m\ddot{x}
$$

再算：

$$
\frac{\partial L}{\partial x}=-\frac{dV}{dx}
$$

代入：

$$
m\ddot{x}-\left(-\frac{dV}{dx}\right)=0
$$

所以：

$$
m\ddot{x}=-\frac{dV}{dx}=F
$$

这就是牛顿方程。

## 4. 物理意义

拉格朗日形式把“力的局部描述”改写为“能量结构的描述”。

它的优势：

- 可以直接使用广义坐标。
- 约束系统更自然。
- 容易推广到场论和路径积分。

自由粒子例子：

$$
V=0,\quad L=\frac12 m\dot{x}^2
$$

Euler-Lagrange 方程给出：

$$
m\ddot{x}=0
$$

所以自由粒子匀速运动。

## 5. 和数学、历史、后续章节的关系

数学上，Euler-Lagrange 方程来自变分法。

历史上，拉格朗日形式把力学从“力和加速度”改写成“能量和坐标”的形式。

后续关系：

- 第 5 讲：作用量 \(S=\int Ldt\) 会解释方程来源。
- 第 6 讲：哈密顿量由 \(L\) 经过变换得到。
- 第 8 章：路径积分直接使用作用量。
- 量子场论也以拉格朗日量为核心语言。

## 6. 练习

### 练习 1

解释 \(L=T-V\) 和 \(E=T+V\) 的区别。

### 练习 2

对：

$$
L=\frac12 m\dot{x}^2
$$

用 Euler-Lagrange 方程推出运动方程。

### 练习 3

对：

$$
L=\frac12 m\dot{x}^2-\frac12 kx^2
$$

推出运动方程。

## 7. 解答

### 解答 1

\(L=T-V\) 是用来生成运动方程的函数；\(E=T+V\) 是总能量。在保守系统中，\(E\) 常守恒，但 \(L\) 不等于能量。

### 解答 2

$$
\frac{\partial L}{\partial x}=0
$$

$$
\frac{\partial L}{\partial \dot{x}}=m\dot{x}
$$

所以：

$$
\frac{d}{dt}(m\dot{x})=m\ddot{x}
$$

Euler-Lagrange 方程给出：

$$
m\ddot{x}=0
$$

### 解答 3

$$
\frac{\partial L}{\partial \dot{x}}=m\dot{x}
$$

$$
\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{x}}\right)=m\ddot{x}
$$

$$
\frac{\partial L}{\partial x}=-kx
$$

代入：

$$
m\ddot{x}+kx=0
$$

即：

$$
m\ddot{x}=-kx
$$

## 8. 本讲必须记住的三句话

1. 拉格朗日量通常是 \(L=T-V\)，不是总能量。
2. Euler-Lagrange 方程从 \(L(q,\dot q,t)\) 生成运动方程。
3. 拉格朗日形式的优势是适合广义坐标、约束和作用量思想。
