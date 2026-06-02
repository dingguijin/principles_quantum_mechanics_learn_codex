# 2. Review of Classical Mechanics

这一章的任务不是让你成为经典力学专家，而是让你明白：量子力学中的 `H`、`p`、`q`、对易关系、薛定谔方程，不是凭空出现的。它们继承了经典力学里“状态如何描述、系统如何演化”的语言。

如果第 1 章建立的是数学语言，那么第 2 章建立的是物理语言。

## 本章学习路线

建议分 7 次学习：

1. 第 1 课：位置、速度、动量、力、能量。
2. 第 2 课：牛顿形式，已知力如何求运动。
3. 第 3 课：从坐标 `x` 到广义坐标 `q`。
4. 第 4 课：拉格朗日量 `L = T - V` 和 Euler-Lagrange 方程。
5. 第 5 课：作用量 `S` 和最小作用量思想。
6. 第 6 课：哈密顿量 `H`、正则动量和 Hamilton 方程。
7. 第 7 课：相空间、泊松括号和量子力学的入口。

你现在要抓住一条主线：

```text
牛顿:       位置 x 和速度 v
拉格朗日:   坐标 q 和速度 qdot
哈密顿:     坐标 q 和动量 p
量子力学:   q、p 变成算符，H 决定态的演化
```

## 第 1 课：最基础的物理量

### 1.1 位置

一维运动中，位置用 `x` 表示。它告诉你物体在哪里。

如果位置随时间变化，就写成：

```text
x(t)
```

这表示：输入时间 `t`，输出位置 `x`。

例子：

```text
x(t) = 3t
```

意思是每过 1 秒，位置增加 3 个单位。

### 1.2 速度

速度是位置的变化率：

```text
v(t) = dx/dt
```

如果：

```text
x(t) = 3t
```

那么：

```text
v(t) = 3
```

如果：

```text
x(t) = t^2
```

那么：

```text
v(t) = 2t
```

这表示速度本身也随时间变化。

### 1.3 加速度

加速度是速度的变化率，也是位置的二阶导数：

```text
a(t) = dv/dt = d^2x/dt^2
```

如果：

```text
x(t) = t^2
```

那么：

```text
v(t) = 2t
a(t) = 2
```

普通语言：位置越来越快地增加，所以有加速度。

### 1.4 动量

非相对论中，动量是：

```text
p = mv
```

其中 `m` 是质量，`v` 是速度。

动量不只是“速度换个名字”。质量大的物体，即使速度不大，也可能有很大动量。

例子：

```text
m = 2
v = 3
p = mv = 6
```

后面量子力学中，动量 `p` 会成为一个非常核心的算符。

### 1.5 力

牛顿第二定律是：

```text
F = ma
```

也可以写成：

```text
F = dp/dt
```

当质量不变时：

```text
dp/dt = m dv/dt = ma
```

这两个说法等价。

普通语言：力改变动量。

### 1.6 动能、势能和总能量

动能：

```text
T = (1/2)mv^2
```

用动量写：

```text
T = p^2/(2m)
```

势能：

```text
V(x)
```

总能量常写为：

```text
E = T + V
```

在很多保守系统中，总能量守恒。

### 第 1 课检查题

1. `x(t)`、`v(t)`、`a(t)` 分别表示什么？
2. 为什么 `F = dp/dt` 比 `F = ma` 更接近“力改变运动状态”的说法？
3. 动量和速度有什么区别？
4. 如果 `m = 4`、`v = 2`，动量和动能分别是多少？

## 第 2 课：牛顿形式

### 2.1 牛顿力学问什么问题

牛顿力学的典型问题是：

```text
已知初始位置 x(0)
已知初始速度 v(0)
已知力 F(x,t)
求未来的位置 x(t)
```

比如自由粒子没有受力：

```text
F = 0
```

于是：

```text
ma = 0
a = 0
```

速度不变，位置匀速变化。

### 2.2 常力例子

假设质量：

```text
m = 2
```

受恒定力：

```text
F = 6
```

则：

```text
a = F/m = 3
```

如果初始条件：

```text
x(0) = 0
v(0) = 0
```

那么：

```text
v(t) = 3t
x(t) = (1/2)3t^2 = 1.5t^2
```

你看，牛顿形式很直接：力给出加速度，加速度积分得到速度，速度积分得到位置。

### 2.3 势能和力的关系

在一维保守力中，力和势能关系为：

```text
F(x) = -dV/dx
```

负号的意思是：系统倾向于朝势能降低的方向运动。

例子：

```text
V(x) = (1/2)kx^2
```

则：

```text
F(x) = -kx
```

这就是弹簧力。离平衡点越远，恢复力越大，而且方向指向平衡点。

### 2.4 牛顿形式的局限

牛顿形式很直观，但在复杂坐标、约束系统和通向量子力学时不够方便。

比如一个粒子被限制在圆环上运动。你可以用二维坐标 `(x,y)` 加约束：

```text
x^2 + y^2 = R^2
```

但更自然的是只用角度：

```text
theta
```

这就引出广义坐标和拉格朗日力学。

### 第 2 课检查题

1. 牛顿形式中，初始位置和初始速度为什么重要？
2. `F = 0` 时，为什么速度保持不变？
3. 若 `V(x)` 随 `x` 增大而增大，力的方向通常朝哪里？
4. 为什么带约束的问题中，直接用牛顿形式可能不方便？

## 第 3 课：广义坐标

### 3.1 坐标不是只能用 x、y、z

坐标只是描述系统构型的变量。最熟悉的是：

```text
x, y, z
```

但如果系统受到约束，别的变量可能更自然。

例子：圆环上的粒子。

如果半径固定为 `R`，粒子位置可以由角度 `theta` 完全决定：

```text
x = R cos theta
y = R sin theta
```

这时 `theta` 就是一个广义坐标。

### 3.2 用 q 表示广义坐标

拉格朗日和哈密顿力学通常用：

```text
q
```

表示广义坐标。

如果系统有多个自由度，就写：

```text
q1, q2, q3, ...
```

它们不一定是长度，也可以是角度或其他描述构型的变量。

### 3.3 自由度

自由度就是描述系统构型所需的独立变量个数。

例子：

- 一维直线上的粒子：1 个自由度，`x`。
- 平面上的自由粒子：2 个自由度，`x, y`。
- 圆环上的粒子：1 个自由度，`theta`。
- 空间中的自由粒子：3 个自由度，`x, y, z`。

Shankar 后面讲 “N degrees of freedom” 时，就是在推广这件事。

### 3.4 广义速度

如果广义坐标是：

```text
q(t)
```

广义速度就是：

```text
qdot = dq/dt
```

如果 `q = theta`，那么：

```text
thetadot = dtheta/dt
```

就是角速度。

### 第 3 课检查题

1. 为什么圆环上的粒子只需要一个自由度？
2. 广义坐标 `q` 一定是长度吗？
3. `qdot` 表示什么？
4. 为什么选择合适坐标能简化问题？

## 第 4 课：拉格朗日量和运动方程

### 4.1 拉格朗日量是什么

拉格朗日量定义为：

```text
L = T - V
```

其中：

```text
T = 动能
V = 势能
```

它通常是 `q`、`qdot` 和 `t` 的函数：

```text
L(q, qdot, t)
```

注意：拉格朗日量不是总能量。总能量通常是 `T + V`，而拉格朗日量是 `T - V`。

### 4.2 Euler-Lagrange 方程

拉格朗日力学的运动方程是：

```text
d/dt (partial L / partial qdot) - partial L / partial q = 0
```

初看很抽象。我们用一维粒子验证它会回到牛顿方程。

一维粒子：

```text
T = (1/2)m xdot^2
V = V(x)
L = (1/2)m xdot^2 - V(x)
```

先算：

```text
partial L / partial xdot = m xdot
```

再对时间求导：

```text
d/dt(partial L / partial xdot) = m xddot
```

再算：

```text
partial L / partial x = -dV/dx
```

代入 Euler-Lagrange 方程：

```text
m xddot - (-dV/dx) = 0
```

所以：

```text
m xddot = -dV/dx
```

这正是：

```text
ma = F
```

因为：

```text
F = -dV/dx
```

### 4.3 为什么要绕一圈

你可能会问：既然最后还是牛顿方程，为什么要学拉格朗日形式？

原因有三点：

1. 它适合广义坐标，不要求坐标一定是直角坐标。
2. 它处理约束系统更自然。
3. 它通向作用量和路径积分，而路径积分是 Shankar 后面重要主题。

拉格朗日形式不是为了复杂而复杂，而是为了让物理规律不依赖某个具体坐标选择。

### 4.4 最小例子：自由粒子

自由粒子没有势能：

```text
V = 0
```

所以：

```text
L = (1/2)m xdot^2
```

Euler-Lagrange 方程：

```text
partial L / partial x = 0
partial L / partial xdot = m xdot
d/dt(m xdot) = m xddot
```

于是：

```text
m xddot = 0
xddot = 0
```

自由粒子匀速运动。

### 第 4 课检查题

1. `L = T - V` 和总能量有什么不同？
2. `partial L / partial qdot` 是对哪个变量求偏导？
3. 一维粒子的 Euler-Lagrange 方程如何回到 `F = ma`？
4. 为什么拉格朗日形式适合广义坐标？

## 第 5 课：作用量和最小作用量思想

### 5.1 作用量是什么

作用量定义为：

```text
S = integral_{t1}^{t2} L(q, qdot, t) dt
```

普通语言：

```text
沿着一条路径，把拉格朗日量随时间累积起来。
```

一条路径不是一个点，而是一整个函数：

```text
q(t)
```

所以作用量是“给整条路径打分”的量。

### 5.2 真实路径的原则

经典力学中的真实路径满足：

```text
delta S = 0
```

这常被口头说成“最小作用量原理”，但更准确说是“驻作用量原理”。因为真实路径不一定让 `S` 最小，也可能让它取驻值。

“驻值”意思是：对路径做很小改变时，作用量的一阶变化为零。

### 5.3 为什么这对量子力学重要

路径积分会说：从初态到末态，所有路径都贡献振幅，贡献大致带有相位：

```text
exp(iS/hbar)
```

当路径偏离经典路径时，相位快速变化，很多贡献会互相抵消。经典路径附近因为 `delta S = 0`，相位变化慢，贡献更容易相干叠加。

所以作用量不是经典力学的小技巧，而是连接经典极限和路径积分的核心对象。

### 第 5 课检查题

1. 作用量是给一个点打分，还是给一条路径打分？
2. `delta S = 0` 为什么不一定等于“最小”？
3. 为什么路径积分中会重新出现作用量？
4. 如果你只知道某一时刻的位置，能不能算整条路径的作用量？

## 第 6 课：哈密顿量和 Hamilton 方程

### 6.1 从 qdot 换到 p

拉格朗日形式使用：

```text
q, qdot
```

哈密顿形式使用：

```text
q, p
```

其中正则动量定义为：

```text
p = partial L / partial qdot
```

对普通一维粒子：

```text
L = (1/2)m xdot^2 - V(x)
```

所以：

```text
p = partial L / partial xdot = m xdot
```

这时正则动量等于我们熟悉的 `mv`。

但要注意：在更复杂系统中，正则动量不一定简单等于 `mv`。量子力学中用的通常是正则动量。

### 6.2 哈密顿量怎么定义

哈密顿量定义为：

```text
H = p qdot - L
```

如果有多个自由度：

```text
H = sum_i p_i qdot_i - L
```

对普通一维粒子，我们来算一遍。

已知：

```text
p = m xdot
xdot = p/m
L = (1/2)m xdot^2 - V(x)
```

代入：

```text
H = p xdot - L
  = p(p/m) - [(1/2)m(p/m)^2 - V(x)]
  = p^2/m - p^2/(2m) + V(x)
  = p^2/(2m) + V(x)
```

这就是总能量：

```text
H = T + V
```

### 6.3 Hamilton 方程

哈密顿形式的运动方程是：

```text
dq/dt = partial H / partial p
dp/dt = - partial H / partial q
```

对：

```text
H = p^2/(2m) + V(q)
```

第一条：

```text
dq/dt = partial H / partial p = p/m
```

这就是：

```text
qdot = v
```

第二条：

```text
dp/dt = -partial H / partial q = -dV/dq
```

这就是力：

```text
dp/dt = F
```

所以 Hamilton 方程也回到了牛顿力学，但它使用的是 `q,p` 两个变量。

### 6.4 为什么哈密顿量对量子力学特别重要

薛定谔方程写作：

```text
i hbar d|psi>/dt = H|psi>
```

这里 `H` 的角色是：

```text
决定态如何随时间变化
```

这个角色来自经典 Hamilton 形式。在经典力学中，给定 `H(q,p)`，就能通过 Hamilton 方程得到系统演化。在量子力学中，给定哈密顿算符 `H`，就能通过薛定谔方程得到态演化。

### 第 6 课检查题

1. 正则动量如何定义？
2. 普通一维粒子中，为什么 `p = m xdot`？
3. 哈密顿量 `H = p qdot - L` 对普通粒子为什么变成 `T + V`？
4. Hamilton 方程中的两个变量是什么？
5. 为什么量子力学特别重视 `H`？

## 第 7 课：相空间、泊松括号和量子入口

### 7.1 相空间是什么

牛顿形式中，我们常说系统状态由位置和速度决定：

```text
x, v
```

哈密顿形式中，系统状态由位置和动量决定：

```text
q, p
```

由所有 `q,p` 组成的空间叫相空间。

一维粒子的相空间是二维的：

```text
(q, p)
```

如果系统有 `N` 个自由度：

```text
(q1,...,qN,p1,...,pN)
```

相空间维数是 `2N`。

### 7.2 相空间中的演化

给定哈密顿量：

```text
H(q,p)
```

Hamilton 方程告诉你相空间中的点如何运动：

```text
(q(t), p(t))
```

这就是经典系统的状态随时间变化。

量子力学中情况会改变：系统状态不是相空间中的一个点，而是 Hilbert 空间中的态向量。但 `q,p,H` 的结构会留下来。

### 7.3 泊松括号

经典力学中有一个结构叫泊松括号。对两个函数 `f(q,p)` 和 `g(q,p)`，一维情形定义为：

```text
{f,g} = (partial f/partial q)(partial g/partial p)
      - (partial f/partial p)(partial g/partial q)
```

最重要的例子：

```text
{q,p} = 1
```

我们验证：

```text
partial q/partial q = 1
partial p/partial p = 1
partial q/partial p = 0
partial p/partial q = 0
```

所以：

```text
{q,p} = 1 x 1 - 0 x 0 = 1
```

### 7.4 从泊松括号到对易子

量子力学中，`q` 和 `p` 会变成算符：

```text
q -> q_hat
p -> p_hat
```

经典的泊松括号结构会对应到量子中的对易子结构。最核心关系是：

```text
[q_hat, p_hat] = i hbar
```

这不是本章要证明的事，但你要先看见连接：

```text
经典: {q,p} = 1
量子: [q_hat,p_hat] = i hbar
```

这就是为什么第 1 章的对易子不是纯数学兴趣，而会直接影响物理。

### 7.5 三种经典语言的关系

你现在可以把三套形式整理成表：

| 形式 | 基本变量 | 核心对象 | 运动方程 |
| --- | --- | --- | --- |
| 牛顿 | `x, v` | 力 `F` | `F = ma` |
| 拉格朗日 | `q, qdot` | `L = T - V` | Euler-Lagrange 方程 |
| 哈密顿 | `q, p` | `H` | Hamilton 方程 |

它们通常描述同一物理内容，只是语言不同。Shankar 需要你熟悉这些语言，是因为量子力学最自然地从 Hamilton 形式进入。

### 第 7 课检查题

1. 相空间中的一个点代表什么？
2. `N` 个自由度的经典系统相空间维数是多少？
3. 为什么 `{q,p} = 1` 是最重要的泊松括号例子？
4. 经典泊松括号和量子对易子有什么关系？
5. 为什么说量子力学更接近 Hamilton 语言？

## 本章总复习

### 你必须掌握的公式

```text
v = dx/dt
a = dv/dt
p = mv
F = dp/dt
T = (1/2)mv^2 = p^2/(2m)
F = -dV/dx
```

```text
L(q,qdot,t) = T - V
d/dt(partial L/partial qdot) - partial L/partial q = 0
S = integral L dt
```

```text
p = partial L/partial qdot
H = p qdot - L
dq/dt = partial H/partial p
dp/dt = -partial H/partial q
```

```text
{q,p} = 1
[q_hat,p_hat] = i hbar
```

### 你必须掌握的普通语言

- 牛顿形式：力决定加速度。
- 拉格朗日形式：真实路径让作用量取驻值。
- 哈密顿形式：哈密顿量决定 `q,p` 在相空间中的演化。
- 量子形式：哈密顿算符决定态向量随时间的演化。

### 和量子力学的连接

第 4 章会出现量子公设。提前看一眼连接：

```text
经典位置 q        -> 位置算符 q_hat
经典动量 p        -> 动量算符 p_hat
经典哈密顿量 H(q,p) -> 哈密顿算符 H
经典演化方程      -> 薛定谔方程
经典泊松括号      -> 量子对易子
```

## 本章作业

### A. 基础运动量

若：

```text
x(t) = 2t^2 + 3t
```

求：

```text
v(t)
a(t)
```

### B. 势能和力

若：

```text
V(x) = 3x^2
```

求：

```text
F(x) = -dV/dx
```

### C. Euler-Lagrange 方程

对一维自由粒子：

```text
L = (1/2)m xdot^2
```

用 Euler-Lagrange 方程推出运动方程。

### D. 正则动量和哈密顿量

对：

```text
L = (1/2)m xdot^2 - V(x)
```

求：

```text
p = partial L/partial xdot
H = p xdot - L
```

并把 `H` 写成 `p` 和 `x` 的函数。

### E. Hamilton 方程

对：

```text
H = p^2/(2m) + V(q)
```

写出：

```text
dq/dt
dp/dt
```

### F. 泊松括号

用定义验证：

```text
{q,p} = 1
{p,q} = -1
```

## 参考答案

### A

```text
v(t) = dx/dt = 4t + 3
a(t) = dv/dt = 4
```

### B

```text
dV/dx = 6x
F(x) = -6x
```

### C

```text
partial L/partial x = 0
partial L/partial xdot = m xdot
d/dt(partial L/partial xdot) = m xddot
```

Euler-Lagrange 方程给出：

```text
m xddot = 0
```

所以自由粒子匀速运动。

### D

```text
p = partial L/partial xdot = m xdot
xdot = p/m
```

```text
H = p xdot - L
  = p(p/m) - [(1/2)m(p/m)^2 - V(x)]
  = p^2/(2m) + V(x)
```

### E

```text
dq/dt = partial H/partial p = p/m
dp/dt = -partial H/partial q = -dV/dq
```

### F

```text
{q,p} = (partial q/partial q)(partial p/partial p)
      - (partial q/partial p)(partial p/partial q)
      = 1 x 1 - 0 x 0
      = 1
```

```text
{p,q} = (partial p/partial q)(partial q/partial p)
      - (partial p/partial p)(partial q/partial q)
      = 0 x 0 - 1 x 1
      = -1
```

## 进入第 3 章前请确认

你应该能独立说清楚：

1. 牛顿、拉格朗日、哈密顿三种形式分别用什么变量描述系统。
2. 为什么 `L = T - V` 不是总能量。
3. 为什么 `H = p^2/(2m) + V(x)` 对普通一维粒子是总能量。
4. 为什么 Hamilton 形式自然使用 `q,p`。
5. 为什么经典的 `{q,p}=1` 会让我们期待量子中 `q,p` 有特殊对易关系。

第 3 章会讨论经典力学为什么不够。你只有先知道经典力学到底在说什么，才会明白它在哪里失效。
