# 第 1 章第 2 讲：基底、坐标和展开

本讲继续 Shankar 第 1 章的数学语言。上一讲说量子态要看成向量，本讲解决下一个问题：

> 如果态是向量，那么我们怎样用数字描述它？

答案是：先选一组基底，再写出态在这组基底下的坐标。

## 1. 本讲要解决的问题

上一讲我们写过：

$$
\lvert \psi \rangle = c_1 \lvert 1 \rangle + c_2 \lvert 2 \rangle
$$

这个式子里有两个层次：

- \(\lvert \psi\rangle\)：态本身。
- \(c_1,c_2\)：态在某组基底下的坐标。

初学量子力学时，最容易把这两件事混在一起。比如看到：

$$
\lvert \psi \rangle =
\begin{pmatrix}
c_1\\
c_2
\end{pmatrix}
$$

就误以为“量子态就是这两个数”。这不准确。更准确地说：

> 这两个数是态在某组基底下的表示。

本讲要建立一个核心习惯：先问“选了什么基底”，再谈“坐标是多少”。

## 2. 为什么需要基底这个概念

### 2.1 没有基底，向量不能变成数字

向量本身是一个几何或抽象对象。要把它写成一串数字，必须先选参照方向。

在二维平面中，常用基底是：

$$
e_1 =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\quad
e_2 =
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

如果：

$$
v =
\begin{pmatrix}
3\\
4
\end{pmatrix}
$$

真正意思是：

$$
v = 3e_1 + 4e_2
$$

坐标 \((3,4)\) 不是凭空来的，而是相对于 \(e_1,e_2\) 这组基底来的。

### 2.2 量子力学必须允许换问题

量子力学中，不同测量对应不同的问题。比如一个自旋系统，你可以问：

- 沿 \(z\) 方向测量，自旋向上还是向下？
- 沿 \(x\) 方向测量，自旋向上还是向下？

这两个问题对应不同基底。

所以同一个量子态，在不同测量问题下会有不同展开：

$$
\lvert \psi \rangle = c_1 \lvert 1\rangle + c_2 \lvert 2\rangle
$$

也可能写成：

$$
\lvert \psi \rangle = d_+ \lvert +\rangle + d_- \lvert -\rangle
$$

态没有变，基底变了，坐标变了。

## 3. 公式怎么来的

### 3.1 从二维向量开始

二维平面中的标准基底为：

$$
e_1 =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\quad
e_2 =
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

任意二维向量都可以写成：

$$
v = v_1 e_1 + v_2 e_2
$$

因为：

$$
v_1
\begin{pmatrix}
1\\
0
\end{pmatrix}
{}+ v_2
\begin{pmatrix}
0\\
1
\end{pmatrix}
=
\begin{pmatrix}
v_1\\
v_2
\end{pmatrix}
$$

所以坐标列向量：

$$
\begin{pmatrix}
v_1\\
v_2
\end{pmatrix}
$$

其实是展开式：

$$
v = v_1 e_1 + v_2 e_2
$$

的压缩写法。

### 3.2 推广到量子态

如果量子态空间中有一组基底：

$$
\lvert 1\rangle,\lvert 2\rangle,\dots,\lvert n\rangle
$$

那么一般态可以展开为：

$$
\begin{gathered}
\lvert \psi\rangle = \\
c_1\lvert 1\rangle + c_2\lvert 2\rangle + \cdots + c_n\lvert n\rangle
\end{gathered}
$$

这可以简写成求和：

$$
\lvert \psi\rangle = \sum_{i=1}^{n} c_i \lvert i\rangle
$$

这里：

- \(\lvert i\rangle\) 是第 \(i\) 个基底态。
- \(c_i\) 是 \(\lvert \psi\rangle\) 在第 \(i\) 个基底方向上的坐标。
- 如果这组基底对应某个测量，那么 \(|c_i|^2\) 会给出对应结果的概率。

最后一句在第 4 章会作为测量公设正式出现。本章先把数学语言准备好。

## 4. 坐标怎么变：一个最小换基底例子

定义旧基底：

$$
\lvert 1\rangle =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\quad
\lvert 2\rangle =
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

定义新基底：

$$
\begin{gathered}
\lvert +\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle + \lvert 2\rangle)
\end{gathered}
$$

$$
\begin{gathered}
\lvert -\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle - \lvert 2\rangle)
\end{gathered}
$$

现在问：旧基底态 \(\lvert 1\rangle\) 在新基底下怎么写？

把上面两式相加：

$$
\begin{gathered}
\lvert +\rangle + \lvert -\rangle \\
= \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle + \lvert 2\rangle) \\
{}+ \frac{1}{\sqrt{2}}(\lvert 1\rangle - \lvert 2\rangle)
\end{gathered}
$$

右边的 \(\lvert 2\rangle\) 抵消：

$$
\begin{gathered}
\lvert +\rangle + \lvert -\rangle \\
= \\
\frac{2}{\sqrt{2}}\lvert 1\rangle \\
= \\
\sqrt{2}\lvert 1\rangle
\end{gathered}
$$

所以：

$$
\begin{gathered}
\lvert 1\rangle = \\
\frac{1}{\sqrt{2}}\lvert +\rangle \\
{}+ \frac{1}{\sqrt{2}}\lvert -\rangle
\end{gathered}
$$

同一个态 \(\lvert 1\rangle\)，在旧基底下坐标是：

$$
(1,0)
$$

在新基底下坐标是：

$$
\left(\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}}\right)
$$

态没变，描述方式变了。

## 5. 物理意义

基底不只是数学上的坐标轴。在量子力学中，一组特殊基底常常对应一类测量的可能结果。

如果态为：

$$
\lvert \psi\rangle = \lvert 1\rangle
$$

那么在 \(\lvert 1\rangle,\lvert 2\rangle\) 这组基底对应的测量中：

$$
P_1 = 1,\quad P_2 = 0
$$

但同一个态也可以写成：

$$
\begin{gathered}
\lvert \psi\rangle = \\
\frac{1}{\sqrt{2}}\lvert +\rangle \\
{}+ \frac{1}{\sqrt{2}}\lvert -\rangle
\end{gathered}
$$

所以在 \(\lvert +\rangle,\lvert -\rangle\) 这组基底对应的测量中：

$$
P_+ = \frac12,\quad P_- = \frac12
$$

这句话非常重要：

> 同一个态，对不同测量问题，会给出不同概率分布。

这不是矛盾。因为“测量什么”本身就是物理问题的一部分。

## 6. 它和经典力学的关系

经典力学也有坐标变换。例如平面上的点可以用直角坐标表示：

$$
(x,y)
$$

也可以用极坐标表示：

$$
(r,\theta)
$$

同一个点没有变，只是描述方式变了。

量子力学中的换基底和这个思想相似：同一个态可以有不同表示。

但二者有一个关键差异：

| 经典力学坐标变换 | 量子力学换基底 |
| --- | --- |
| 多数时候只是换描述方式 | 常常对应换一类测量问题 |
| 坐标值通常描述已有物理量 | 展开系数给出概率振幅 |
| 坐标变换不一定涉及概率 | 换基底会改变概率分布的呈现 |

所以量子力学中的基底选择，不只是计算方便问题，也直接连接“你用什么实验问系统”。

## 7. 它和数学的关系

本讲用到三个线性代数概念。

### 7.1 线性组合

形式：

$$
c_1 v_1 + c_2 v_2 + \cdots + c_n v_n
$$

意思是把一些基本向量按系数组合起来。

### 7.2 基底

一组向量若能表示空间中所有向量，并且没有多余重复，就叫基底。

“能表示所有向量”叫张成空间。“没有多余重复”叫线性无关。后面我们不急着形式化证明，先会用。

### 7.3 坐标

选定基底后，一个向量前面的展开系数就是坐标。

在量子力学中：

$$
\lvert \psi\rangle = \sum_i c_i \lvert i\rangle
$$

中的 \(c_i\) 就是坐标，也叫展开系数，物理上常常叫概率振幅。

## 8. 历史关系

量子力学早期有两种看起来不同的表达：

- Schrodinger 的波函数 \(\psi(x)\)。
- Heisenberg 的矩阵。

后来人们理解到，它们不是两套不同物理理论，而是同一个态和同一批算符在不同表示下的写法。

例如：

- \(\psi(x)\) 是态在位置基底下的表示。
- \(\phi(p)\) 是态在动量基底下的表示。

Dirac 的 bra-ket 记号把这个事实写得非常清楚：

$$
\lvert \psi\rangle
$$

是态本身；

$$
\psi(x)
$$

是它在位置基底下的坐标函数。

这个思想是现代量子力学语言统一的关键。

## 9. 和后续章节的关系

本讲会在后面反复出现：

- 第 3 讲：内积会告诉我们怎样从态中取出某个基底方向的系数。
- 第 4 讲：算符的矩阵表示依赖于所选基底。
- 第 4 章：测量公设会说明观测量的本征态构成测量基底。
- 第 5 章：一维问题中，波函数 \(\psi(x)\) 是位置基底展开系数。
- 第 7 章：谐振子态可展开为能量本征态的叠加。
- 第 12 章和第 14 章：角动量、自旋会大量使用不同基底之间的转换。

后面看到“位置表象”“动量表象”“能量表象”，先不要害怕。它们本质上都是：同一个态，换不同基底来写。

## 10. 最小计算例子

设旧基底为：

$$
\lvert 1\rangle =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\quad
\lvert 2\rangle =
\begin{pmatrix}
0\\
1
\end{pmatrix}
$$

态：

$$
\begin{gathered}
\lvert \psi\rangle = \\
2\lvert 1\rangle - \lvert 2\rangle
\end{gathered}
$$

在旧基底下坐标是：

$$
(2,-1)
$$

它还没有归一化，因为：

$$
|2|^2 + |-1|^2 = 5
$$

归一化后：

$$
\begin{gathered}
\lvert \psi_{\text{norm}}\rangle = \\
\frac{2}{\sqrt{5}}\lvert 1\rangle \\
- \frac{1}{\sqrt{5}}\lvert 2\rangle
\end{gathered}
$$

如果用旧基底对应的测量，两个结果的概率是：

$$
P_1 = \frac45,\quad P_2 = \frac15
$$

## 11. 常见误解

### 误解 1：换基底就是换了物理状态

不是。换基底通常只是换描述方式。物理态 \(\lvert \psi\rangle\) 没变，坐标变了。

### 误解 2：坐标一定就是概率

不是。坐标是概率振幅，概率来自模平方。并且只有当基底对应某个测量结果时，才可以直接把 \(|c_i|^2\) 解释为该测量结果的概率。

### 误解 3：所有基底都一样方便

数学上都可以用，但物理和计算上不一样。研究能量时，能量本征态基底通常方便；研究位置分布时，位置基底方便；研究动量分布时，动量基底方便。

## 12. 练习

### 练习 1

设：

$$
\lvert \psi\rangle = 3\lvert 1\rangle + 4\lvert 2\rangle
$$

它在 \(\lvert 1\rangle,\lvert 2\rangle\) 基底下的坐标是什么？是否归一化？如果没有，归一化后的态是什么？

### 练习 2

定义：

$$
\begin{gathered}
\lvert +\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle+\lvert 2\rangle), \\
\quad \\
\lvert -\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle-\lvert 2\rangle)
\end{gathered}
$$

把 \(\lvert 2\rangle\) 写成 \(\lvert +\rangle,\lvert -\rangle\) 的线性组合。

### 练习 3

同一个态在旧基底下是：

$$
\lvert \psi\rangle = \lvert 1\rangle
$$

在新基底 \(\lvert +\rangle,\lvert -\rangle\) 下，它的两个测量结果概率是多少？

### 练习 4

解释下面这句话：

> \(\psi(x)\) 不是态本身，而是态在位置基底下的表示。

## 13. 解答

### 解答 1

坐标是：

$$
(3,4)
$$

总概率因子为：

$$
|3|^2 + |4|^2 = 25
$$

所以没有归一化。长度是：

$$
5
$$

归一化后的态为：

$$
\begin{gathered}
\lvert \psi_{\text{norm}}\rangle = \\
\frac35\lvert 1\rangle + \frac45\lvert 2\rangle
\end{gathered}
$$

### 解答 2

由定义：

$$
\begin{gathered}
\lvert +\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle+\lvert 2\rangle)
\end{gathered}
$$

$$
\begin{gathered}
\lvert -\rangle = \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle-\lvert 2\rangle)
\end{gathered}
$$

两式相减：

$$
\begin{gathered}
\lvert +\rangle - \lvert -\rangle \\
= \\
\frac{1}{\sqrt{2}}(\lvert 1\rangle+\lvert 2\rangle) \\
- \frac{1}{\sqrt{2}}(\lvert 1\rangle-\lvert 2\rangle)
\end{gathered}
$$

\(\lvert 1\rangle\) 抵消，得到：

$$
\begin{gathered}
\lvert +\rangle - \lvert -\rangle \\
= \\
\sqrt{2}\lvert 2\rangle
\end{gathered}
$$

所以：

$$
\begin{gathered}
\lvert 2\rangle = \\
\frac{1}{\sqrt{2}}\lvert +\rangle \\
- \frac{1}{\sqrt{2}}\lvert -\rangle
\end{gathered}
$$

### 解答 3

上一节已经得到：

$$
\begin{gathered}
\lvert 1\rangle = \\
\frac{1}{\sqrt{2}}\lvert +\rangle \\
{}+ \frac{1}{\sqrt{2}}\lvert -\rangle
\end{gathered}
$$

所以：

$$
\begin{gathered}
P_+ = \\
\left|\frac{1}{\sqrt{2}}\right|^2 \\
= \frac12
\end{gathered}
$$

$$
\begin{gathered}
P_- = \\
\left|\frac{1}{\sqrt{2}}\right|^2 \\
= \frac12
\end{gathered}
$$

### 解答 4

\(\lvert \psi\rangle\) 是抽象态矢量。要把它写成函数，需要先选择位置基底。选了位置基底后，每个位置 \(x\) 上的展开系数就是：

$$
\psi(x)
$$

所以 \(\psi(x)\) 是态在位置表示下的坐标函数，不是态本身。以后同一个态也可以写成动量表示 \(\phi(p)\)，这说明表示变了，态本身没有变。

## 14. 本讲必须记住的三句话

1. 基底是一组用来展开态的基本方向。
2. 坐标是选定基底以后才有的，态本身不等于某一组坐标。
3. 量子力学中的换基底常常对应换测量问题，因此会改变概率分布的呈现方式。
