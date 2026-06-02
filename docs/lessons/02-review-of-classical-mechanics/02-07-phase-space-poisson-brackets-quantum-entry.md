# 第 2 章第 7 讲：相空间、泊松括号和量子力学的入口

本讲收束第 2 章，把经典力学和量子力学的入口连接起来。

## 1. 本讲要解决的问题

哈密顿形式使用 \(q,p\)。那么：

- 由所有 \(q,p\) 组成的空间是什么？
- 经典力学怎样表达 \(q,p\) 的基本关系？
- 这个关系怎样预告量子力学的对易子？

答案是：相空间和泊松括号。

## 2. 相空间是什么

哈密顿形式中，系统状态由：

$$
(q,p)
$$

给出。所有可能的 \((q,p)\) 组成相空间。

一维系统有一个 \(q\) 和一个 \(p\)，相空间是二维的。

\(N\) 个自由度时：

$$
(q_1,\dots,q_N,p_1,\dots,p_N)
$$

相空间维数是：

$$
2N
$$

## 3. 相空间中的演化

给定：

$$
H(q,p)
$$

Hamilton 方程：

$$
\dot q=\frac{\partial H}{\partial p}
$$

$$
\dot p=-\frac{\partial H}{\partial q}
$$

告诉我们相空间中的点怎样随时间移动：

$$
(q(t),p(t))
$$

这是经典系统的状态轨道。

## 4. 泊松括号

一维情形下，两个相空间函数 \(f(q,p)\)、\(g(q,p)\) 的泊松括号定义为：

$$
\{f,g\}
=\frac{\partial f}{\partial q}\frac{\partial g}{\partial p}
-\frac{\partial f}{\partial p}\frac{\partial g}{\partial q}
$$

最重要例子：

$$
\{q,p\}=1
$$

验证：

$$
\frac{\partial q}{\partial q}=1,\quad
\frac{\partial p}{\partial p}=1
$$

$$
\frac{\partial q}{\partial p}=0,\quad
\frac{\partial p}{\partial q}=0
$$

所以：

$$
\{q,p\}=1\cdot1-0\cdot0=1
$$

反过来：

$$
\{p,q\}=0\cdot0-1\cdot1=-1
$$

## 5. 为什么泊松括号重要

Hamilton 方程可以用泊松括号写成：

$$
\frac{df}{dt}=\{f,H\}
$$

如果 \(f=q\)：

$$
\dot q=\{q,H\}=\frac{\partial H}{\partial p}
$$

如果 \(f=p\)：

$$
\dot p=\{p,H\}=-\frac{\partial H}{\partial q}
$$

这说明泊松括号编码了经典相空间的演化结构。

## 6. 从泊松括号到对易子

量子力学中：

$$
q\to \hat q,\quad p\to \hat p
$$

经典泊松括号结构对应量子对易子结构。

核心联系是：

$$
\{q,p\}=1
$$

对应：

$$
[\hat q,\hat p]=i\hbar
$$

这里：

$$
[\hat q,\hat p]=\hat q\hat p-\hat p\hat q
$$

这说明位置和动量算符不对易。第 9 章的不确定性关系会从这种不对易结构中出现。

## 7. 三种经典语言的关系

| 形式 | 基本变量 | 核心对象 | 运动方程 |
| --- | --- | --- | --- |
| 牛顿 | \(x,v\) | 力 \(F\) | \(F=ma\) |
| 拉格朗日 | \(q,\dot q\) | \(L=T-V\) | Euler-Lagrange 方程 |
| 哈密顿 | \(q,p\) | \(H\) | Hamilton 方程 |

量子力学最接近哈密顿语言：

$$
q,p,H \to \hat q,\hat p,\hat H
$$

## 8. 物理意义

相空间中的一个点表示经典系统的完整状态。量子力学中，系统状态不再是相空间点，而是 Hilbert 空间中的态矢量。

但经典 \(q,p,H\) 的结构没有消失，而是被提升为算符结构。

## 9. 和数学、历史、后续章节的关系

数学上，泊松括号是相空间上的代数结构。

历史上，从泊松括号到对易子，是量子力学形式体系建立的关键线索之一。

后续关系：

- 第 3 章：会讨论经典力学为什么不足。
- 第 4 章：\(q,p,H\) 会进入量子公设。
- 第 5 章：位置和动量算符进入薛定谔方程。
- 第 9 章：\([\hat q,\hat p]=i\hbar\) 导向不确定性关系。

## 10. 练习

### 练习 1

\(N\) 个自由度的系统，相空间维数是多少？

### 练习 2

用定义验证：

$$
\{q,p\}=1,\quad \{p,q\}=-1
$$

### 练习 3

解释为什么量子力学更接近 Hamilton 语言。

## 11. 解答

### 解答 1

每个自由度有一个 \(q_i\) 和一个 \(p_i\)，所以相空间维数是：

$$
2N
$$

### 解答 2

$$
\{q,p\}
=\frac{\partial q}{\partial q}\frac{\partial p}{\partial p}
-\frac{\partial q}{\partial p}\frac{\partial p}{\partial q}
=1\cdot1-0\cdot0=1
$$

$$
\{p,q\}
=\frac{\partial p}{\partial q}\frac{\partial q}{\partial p}
-\frac{\partial p}{\partial p}\frac{\partial q}{\partial q}
=0\cdot0-1\cdot1=-1
$$

### 解答 3

因为量子力学中位置、动量、哈密顿量分别变成算符 \(\hat q,\hat p,\hat H\)，而态的时间演化由哈密顿算符决定。这直接继承了 Hamilton 形式中 \(q,p,H\) 的结构。

## 12. 第 2 章总复习

你现在应该能说清楚：

- 牛顿形式：力决定加速度。
- 拉格朗日形式：真实路径满足 \(\delta S=0\)。
- 哈密顿形式：\(H\) 决定 \(q,p\) 在相空间中的演化。
- 量子入口：\(q,p,H\) 变成算符，\(\{q,p\}=1\) 对应 \([\hat q,\hat p]=i\hbar\)。

## 13. 本讲必须记住的三句话

1. 相空间由所有 \(q,p\) 组成，\(N\) 个自由度对应 \(2N\) 维相空间。
2. 泊松括号编码经典 Hamilton 演化结构。
3. 经典 \(\{q,p\}=1\) 预告量子 \([\hat q,\hat p]=i\hbar\)。
