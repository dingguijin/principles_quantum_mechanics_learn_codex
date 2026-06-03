# 第 2 章第 6 讲：哈密顿量、正则动量和 Hamilton 方程

本讲从拉格朗日形式转到哈密顿形式。

## 1. 本讲要解决的问题

拉格朗日形式使用：

$$
q,\dot q
$$

哈密顿形式使用：

$$
q,p
$$

量子力学最自然继承的是哈密顿形式，因为位置和动量会变成算符，哈密顿量会决定态的时间演化。

## 2. 为什么要从 $`\dot q`$ 换到 $`p`$

速度 $`\dot q`$ 很直观，但动量 $`p`$ 更适合表达状态和演化。

正则动量定义为：

$$
p=\frac{\partial L}{\partial \dot q}
$$

普通一维粒子：

$$
L=\frac12 m\dot{x}^2-V(x)
$$

所以：

$$
p=\frac{\partial L}{\partial \dot{x}}=m\dot{x}
$$

这时正则动量等于熟悉的 $`mv`$。但复杂系统中，正则动量不一定简单等于 $`mv`$。

## 3. 哈密顿量怎么定义

哈密顿量定义为：

$$
H=p\dot q-L
$$

多自由度时：

$$
H=\sum_i p_i\dot q_i-L
$$

对一维普通粒子：

$$
p=m\dot{x},\quad \dot{x}=\frac{p}{m}
$$

$$
L=\frac12 m\dot{x}^2-V(x)
$$

代入：

$$
H=p\dot{x}-L
$$

$$
=p\frac{p}{m}-\left[\frac12 m\left(\frac{p}{m}\right)^2-V(x)\right]
$$

$$
=\frac{p^2}{m}-\frac{p^2}{2m}+V(x)
=\frac{p^2}{2m}+V(x)
$$

这就是总能量形式：

$$
H=T+V
$$

## 4. Hamilton 方程

哈密顿形式的运动方程是：

$$
\frac{dq}{dt}=\frac{\partial H}{\partial p}
$$

$$
\frac{dp}{dt}=-\frac{\partial H}{\partial q}
$$

对：

$$
H=\frac{p^2}{2m}+V(q)
$$

第一条：

$$
\frac{dq}{dt}=\frac{p}{m}
$$

第二条：

$$
\frac{dp}{dt}=-\frac{dV}{dq}
$$

所以 Hamilton 方程仍然回到牛顿力学：

$$
\dot q=v,\quad \dot p=F
$$

## 5. 物理意义

哈密顿量在经典力学中生成 $`q,p`$ 的演化。

在量子力学中，哈密顿算符 $`H`$ 生成态矢量的演化：

$$
i\hbar\frac{d}{dt}\lvert\psi\rangle=H\lvert\psi\rangle
$$

这就是为什么量子力学特别重视 $`H`$。

## 6. 和经典力学、数学、历史、后续章节的关系

数学上，从 $`L(q,\dot q)`$ 到 $`H(q,p)`$ 是 Legendre 变换。

历史上，Hamilton 形式把力学写成相空间中的一阶方程系统。

后续关系：

- 第 7 讲：相空间由 $`q,p`$ 构成。
- 第 4 章：哈密顿算符控制量子态时间演化。
- 第 5 章：一维薛定谔方程使用 $`H=p^2/(2m)+V(x)`$。
- 第 7 章：谐振子的哈密顿量是核心对象。

## 7. 练习

### 练习 1

对：

$$
L=\frac12 m\dot{x}^2-V(x)
$$

求正则动量。

### 练习 2

把上题的哈密顿量写成 $`x,p`$ 的函数。

### 练习 3

对：

$$
H=\frac{p^2}{2m}+V(q)
$$

写出 Hamilton 方程。

## 8. 解答

### 解答 1

$$
p=\frac{\partial L}{\partial \dot{x}}=m\dot{x}
$$

### 解答 2

由 $`\dot{x}=p/m`$：

$$
H=p\dot{x}-L
=\frac{p^2}{2m}+V(x)
$$

### 解答 3

$$
\frac{dq}{dt}=\frac{\partial H}{\partial p}=\frac{p}{m}
$$

$$
\frac{dp}{dt}=-\frac{\partial H}{\partial q}=-\frac{dV}{dq}
$$

## 9. 本讲必须记住的三句话

1. 正则动量定义为 $`p=\partial L/\partial\dot q`$。
2. 哈密顿量定义为 $`H=p\dot q-L`$，普通粒子中等于 $`p^2/(2m)+V`$。
3. 量子力学中的哈密顿算符继承了经典 $`H`$ 生成演化的角色。
