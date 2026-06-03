# 第 12 章第 2 讲：轨道角动量算符从 r x p 来

本讲把经典轨道角动量转成量子算符。

## 1. 为什么有这个概念

在三维运动中，粒子不只会平移，还可能绕某点运动。

描述这种“绕转趋势”的量就是角动量。

量子力学需要把角动量写成算符，才能讨论测量、本征值和守恒。

## 2. 它解决了什么问题

它解决“如何在波函数上计算角动量”的问题。

有了 $`L_x,L_y,L_z`$，我们才能：

- 判断角动量分量。
- 建立角动量代数。
- 写出 $`L^2`$。
- 求球谐函数。

## 3. 公式怎么来的

经典轨道角动量：

$$
\mathbf L=\mathbf r\times\mathbf p
$$

其中：

$$
\mathbf r=(x,y,z),\quad \mathbf p=(p_x,p_y,p_z)
$$

叉乘分量为：

$$
L_x=yp_z-zp_y
$$

$$
L_y=zp_x-xp_z
$$

$$
L_z=xp_y-yp_x
$$

量子化时：

$$
p_x=-i\hbar\frac{\partial}{\partial x},\quad
p_y=-i\hbar\frac{\partial}{\partial y},\quad
p_z=-i\hbar\frac{\partial}{\partial z}
$$

所以：

$$
L_z=-i\hbar\left(x\frac{\partial}{\partial y}-y\frac{\partial}{\partial x}\right)
$$

## 4. 球坐标中的 $`L_z`$

球坐标中，绕 $`z`$ 轴转动只改变方位角 $`\phi`$。

因此：

$$
L_z=-i\hbar\frac{\partial}{\partial\phi}
$$

这是最常用的角动量公式之一。

若：

$$
\psi(\phi)=e^{im\phi}
$$

则：

$$
L_z\psi=\hbar m\psi
$$

所以 $`m`$ 是 $`L_z`$ 的量子数。

## 5. 物理意义

$`L_z`$ 测量角动量在 $`z`$ 轴方向的分量。

但它不是说角动量真的只在 $`z`$ 轴上；它只是选定一个方向后测量投影。

不同方向的投影之间会有非对易关系。

## 6. 和经典力学的关系

经典中，$`\mathbf L=\mathbf r\times\mathbf p`$ 是轨道运动的几何量。

量子中，同一个公式保留，但 $`\mathbf p`$ 变成微分算符，因此角动量变成作用在波函数上的微分算符。

## 7. 和后续章节的关系

第 13 章氢原子会把三维波函数写成径向部分和角向部分：

$$
\psi(r,\theta,\phi)=R(r)Y_l^m(\theta,\phi)
$$

其中 $`Y_l^m`$ 就是 $`L^2,L_z`$ 的共同本征函数。

## 8. 练习

### 练习 1

从 $`\mathbf r\times\mathbf p`$ 写出 $`L_x,L_y,L_z`$。

### 练习 2

写出坐标表象中的 $`L_z`$。

### 练习 3

若 $`\psi(\phi)=e^{i3\phi}`$，求 $`L_z\psi`$。

## 9. 解答

### 解答 1

$$
L_x=yp_z-zp_y,\quad
L_y=zp_x-xp_z,\quad
L_z=xp_y-yp_x
$$

### 解答 2

$$
L_z=-i\hbar\left(x\frac{\partial}{\partial y}-y\frac{\partial}{\partial x}\right)
$$

球坐标中：

$$
L_z=-i\hbar\frac{\partial}{\partial\phi}
$$

### 解答 3

$$
L_z e^{i3\phi}
=-i\hbar\frac{\partial}{\partial\phi}e^{i3\phi}
=3\hbar e^{i3\phi}
$$

## 10. 本讲必须记住的三句话

1. 轨道角动量来自 $`\mathbf L=\mathbf r\times\mathbf p`$。
2. 量子角动量是微分算符。
3. $`L_z=-i\hbar\partial/\partial\phi`$ 是理解 $`m`$ 的关键。
