# 1. Mathematical Introduction

这一章不是普通的数学复习，而是在建立量子力学的语言。你以后看到的态、波函数、测量、能量、自旋、角动量，本质上都在使用本章的几个工具：向量空间、内积、算符、本征值、基底变换。

如果你是零基础，请不要试图“一遍读懂”。这章建议分 6 次学习，每次只掌握一组概念。

## 本章学习路线

1. 第 1 课：为什么量子态要当作向量。
2. 第 2 课：基底、坐标和展开。
3. 第 3 课：内积、长度、正交和归一化。
4. 第 4 课：线性算符和矩阵。
5. 第 5 课：本征值、本征向量和测量预告。
6. 第 6 课：厄米、幺正、投影以及无限维推广。

学习目标不是背定义，而是能把符号翻译成普通语言。比如：

$$
A\lvert \psi \rangle = \lvert \phi \rangle
$$

你应该能读成：

> 算符 $`A`$ 作用在状态 $`\lvert\psi\rangle`$ 上，得到新状态 $`\lvert\phi\rangle`$。

## 第 1 课：为什么量子态要当作向量

### 1.1 从一个最小实验想起

先想一个只有两个可能结果的系统。比如某个量子系统测量后只可能得到：

> 结果 1
> 结果 2

我们暂时不关心它是什么具体系统。只问：怎样描述它的状态？

最简单的办法是给两个结果各配一个“权重”：

> 状态 = $`(c_{1},c_{2})`$

这里 $`c_{1}`$ 和 $`c_{2}`$ 不是概率，而是概率振幅。真正概率是：

$$
\begin{gathered}
P_{1} = \lvert c_{1}\rvert^2 \\
P_{2} = \lvert c_{2}\rvert^2
\end{gathered}
$$

如果系统只可能出现这两个结果，那么：

$$
\lvert c_{1}\rvert^2 + \lvert c_{2}\rvert^2 = 1
$$

你已经看到向量语言自然出现了：一个状态可以用一组分量表示。

### 1.2 什么是向量空间

一个向量空间是一类对象的集合，里面的对象可以相加，也可以乘以数。

例如：

$$
\begin{gathered}
v = (1, 2) \\
w = (3, -1)
\end{gathered}
$$

相加：

$$
v + w = (4, 1)
$$

数乘：

$$
2v = (2, 4)
$$

量子态也要允许相加和数乘，因为量子力学有叠加原理。如果 $`\lvert 1 \rangle`$ 和 $`\lvert 2 \rangle`$ 是两个可能状态，那么：

$$
\lvert \psi \rangle = c_{1}\lvert 1 \rangle + c_{2}\lvert 2 \rangle
$$

也是一个可能状态。

这句话就是量子力学形式体系的入口。它不是说系统“一半在状态 1，一半在状态 2”，而是说系统处在两个基态的叠加态，测量概率由系数决定。

### 1.3 Dirac 记号先怎么读

书里会大量使用：

$$
\lvert \psi \rangle
$$

这叫 ket，读作“ket psi”。你现在不用管名字来源，只要知道它表示一个向量，也就是一个量子态。

对应还有：

$$
\langle \psi \rvert
$$

这叫 bra。bra 和 ket 合起来：

$$
\langle \phi \mid \psi \rangle
$$

表示两个态的内积。它会告诉我们两个态有多“重合”。

先记一个翻译表：

| 符号 | 普通语言 |
| --- | --- |
| $`\lvert \psi \rangle`$ | 一个态向量 |
| $`\langle \psi \rvert`$ | 与 $`\lvert \psi \rangle`$ 对应的 bra |
| $`\langle \phi \mid \psi \rangle`$ | $`\lvert \phi \rangle`$ 与 $`\lvert \psi \rangle`$ 的内积 |
| $`A\lvert \psi \rangle`$ | 算符 $`A`$ 作用在态上 |
| $`\lvert \psi \rangle = c_1\lvert 1 \rangle + c_2\lvert 2 \rangle`$ | 态在一组基底上的展开 |

### 1.4 最小计算例子

设：

$$
\begin{gathered}
\lvert 1 \rangle = (1, 0) \\
\lvert 2 \rangle = (0, 1)
\end{gathered}
$$

如果：

$$
\lvert \psi \rangle = (3/5)\lvert 1 \rangle + (4/5)\lvert 2 \rangle
$$

那么在这组基底下：

$$
\lvert \psi \rangle = (3/5, 4/5)
$$

概率是：

$$
\begin{gathered}
P_{1} = \lvert 3/5\rvert^2 = 9/25 \\
P_{2} = \lvert 4/5\rvert^2 = 16/25 \\
P_{1} + P_{2} = 1
\end{gathered}
$$

所以这是归一化态。

### 第 1 课检查题

1. 为什么 $`(c_{1},c_{2})`$ 可以用来描述一个两结果系统的状态？
2. $`c_{1}`$ 是概率吗？如果不是，概率怎么得到？
3. $`\lvert \psi \rangle = c_1\lvert 1 \rangle + c_2\lvert 2 \rangle`$ 用普通语言怎么说？
4. 为什么要求 $`|c_{1}|^2 + |c_{2}|^2 = 1`$？

## 第 2 课：基底、坐标和展开

### 2.1 基底是什么

基底是一组“基本方向”。有了基底，就可以用坐标描述向量。

二维平面最常用基底是：

$$
\begin{gathered}
e_{1} = (1, 0) \\
e_{2} = (0, 1)
\end{gathered}
$$

任何二维向量都能写成：

$$
v = v_{1} e_{1} + v_{2} e_{2}
$$

比如：

$$
(3, 4) = 3(1, 0) + 4(0, 1)
$$

这里 $`(3,4)`$ 是坐标表示，$`e_{1}`$ 和 $`e_{2}`$ 是基底向量。

### 2.2 向量本身和坐标不是一回事

这是初学者最容易混淆的地方。

一个向量是一个对象。坐标是你选定某组基底后，用数字描述它的方式。

换一组基底，同一个向量的坐标会变。向量没有变，描述方式变了。

类比：同一个地点可以用中文地址表示，也可以用经纬度表示。地点没变，坐标系统变了。

量子力学中也一样。同一个态可以用位置表示：

$$
\psi(x)
$$

也可以用动量表示：

$$
\phi(p)
$$

它们不是两个不同物理系统，而是同一个态在不同基底下的表示。

### 2.3 展开系数是什么意思

如果：

$$
\lvert \psi \rangle = c_{1}\lvert 1 \rangle + c_{2}\lvert 2 \rangle + c_{3}\lvert 3 \rangle
$$

那么 $`c_{1},c_{2},c_{3}`$ 是 $`\lvert\psi\rangle`$ 在这三个基底方向上的分量。

若这组基底是正交归一的，那么：

$$
\lvert c_{1}\rvert^2, \lvert c_{2}\rvert^2, \lvert c_{3}\rvert^2
$$

常常可以直接解释为对应测量结果的概率。

但注意：这句话依赖于你选的基底对应某个观测量的本征态。第四章会正式讲。

### 2.4 最小计算例子

设：

$$
\begin{gathered}
\lvert a \rangle = (1, 0) \\
\lvert b \rangle = (0, 1) \\
\lvert \psi \rangle = (2, -1)
\end{gathered}
$$

那么：

$$
\lvert \psi \rangle = 2\lvert a \rangle - 1\lvert b \rangle
$$

如果要归一化它，先算长度：

$$
\lVert \psi\rVert = \sqrt{2^2 + (-1)^2} = \sqrt{5}
$$

归一化态是：

$$
\begin{gathered}
\lvert \psi_{norm} \rangle = (1/\sqrt{5})(2, -1) \\
= (2/\sqrt{5}, -1/\sqrt{5})
\end{gathered}
$$

此时两个方向上的概率是：

$$
\begin{gathered}
P_{a} = \lvert 2/\sqrt{5}\rvert^2 = 4/5 \\
P_{b} = \lvert -1/\sqrt{5}\rvert^2 = 1/5
\end{gathered}
$$

### 第 2 课检查题

1. 基底和坐标有什么区别？
2. 为什么同一个量子态可以有不同表示？
3. 如果 $`\lvert\psi\rangle = 2\lvert a\rangle - \lvert b\rangle`$，这个态是否已经归一化？
4. 为什么归一化时要除以长度？

## 第 3 课：内积、长度、正交和归一化

### 3.1 内积先理解成“重合程度”

两个向量的内积告诉你它们有多对齐。

实向量例子：

$$
\begin{gathered}
v = (1, 0) \\
w = (0, 1)
\end{gathered}
$$

内积：

$$
v · w = 1 \cdot 0 + 0 \cdot 1 = 0
$$

它们互相垂直，所以内积为 0。

再看：

$$
\begin{gathered}
u = (1, 0) \\
v = (3, 0)
\end{gathered}
$$

内积：

$$
u · v = 3
$$

它们方向完全一致，所以内积非零。

### 3.2 复向量内积为什么要复共轭

量子态通常有复数分量。复向量内积定义为：

$$
\langle v \mid w \rangle = v_{1}^\ast w1 + v_{2}^\ast w2 + \dots
$$

为什么第一个向量要取复共轭？因为我们希望长度平方：

$$
\langle v \mid v \rangle
$$

一定是非负实数。

例子：

$$
v = (1, i)
$$

如果不用复共轭，得到：

$$
1 \cdot 1 + i \cdot i = 1 - 1 = 0
$$

这会荒谬地说非零向量长度为 0。

用复共轭：

$$
\langle v \mid v \rangle = 1^\ast \cdot 1 + i^\ast \cdot i = 1 + (-i)i = 2
$$

这才是合理的长度平方。

### 3.3 长度和归一化

长度定义为：

$$
|\lvert v\rvert| = \sqrt{\langle v \mid v \rangle}
$$

量子态要求：

$$
\langle \psi \mid \psi \rangle = 1
$$

这叫归一化。物理意义是总概率为 1。

如果一个态还没有归一化，比如：

$$
v = (1, i)
$$

长度平方：

$$
\langle v \mid v \rangle = 2
$$

长度：

$$
|\lvert v\rvert| = \sqrt{2}
$$

归一化：

$$
\lvert \psi \rangle = (1/\sqrt{2})(1, i)
$$

检查：

$$
\langle \psi \mid \psi \rangle = 1/2 + 1/2 = 1
$$

### 3.4 正交

如果：

$$
\langle v \mid w \rangle = 0
$$

则 $`v`$ 和 $`w`$ 正交。

在量子力学中，正交常常表示两个状态可以被清楚区分。比如某个测量的两个不同结果对应两个正交本征态。

### 3.5 正交归一基底

一组基底若满足：

$$
\begin{gathered}
\langle i\mid j\rangle = 0 \quad (i\ne j) \\
\langle i\mid i\rangle = 1
\end{gathered}
$$

可合写成：

$$
\langle i \mid j \rangle = \delta_{ij}
$$

这里 $`\delta_{ij}`$ 是 Kronecker delta：

$$
\delta_{ij} =
\begin{cases}
1, & i=j,\\
0, & i\ne j.
\end{cases}
$$

正交归一基底最大的好处是：展开系数可以用内积直接取出来。

如果：

$$
\lvert \psi \rangle = c_{1}\lvert 1 \rangle + c_{2}\lvert 2 \rangle
$$

那么：

$$
\begin{gathered}
\langle 1 \rvert \psi \rangle = c_{1} \\
\langle 2 \rvert \psi \rangle = c_{2}
\end{gathered}
$$

### 第 3 课检查题

1. 为什么复向量内积要取复共轭？
2. 归一化的物理意义是什么？
3. 正交是否只是“几何垂直”？在量子力学中还意味着什么？
4. 若 $`\lvert\psi\rangle = (1/2,\sqrt{3}/2)`$，它是否归一化？
5. 若 $`v = (1, i)`$，归一化后的向量是什么？

## 第 4 课：线性算符和矩阵

### 4.1 算符是什么

算符是作用在向量上的规则。

写作：

$$
A\lvert \psi \rangle = \lvert \phi \rangle
$$

普通语言：

> $`A`$ 把状态 $`\lvert\psi\rangle`$ 变成状态 $`\lvert\phi\rangle`$。

在有限维空间里，算符可以用矩阵表示。

### 4.2 线性是什么意思

线性算符满足：

$$
A(a\lvert v \rangle + b\lvert w \rangle) = aA\lvert v \rangle + bA\lvert w \rangle
$$

这句话很重要。它说：如果一个态是叠加态，那么算符对它的作用可以分别作用到每个部分上，再加起来。

例子：

$$
A =
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

对：

$$
v = (1, 1)
$$

作用：

$$
Av = (2, 3)
$$

如果：

$$
v = e_{1} + e_{2}
$$

那么：

$$
A(e_{1} + e_{2}) = Ae_1 + Ae_2 = (2,0) + (0,3) = (2,3)
$$

这就是线性。

### 4.3 矩阵乘法怎么读

设矩阵 $`A`$ 和向量 $`v`$：

$$
v = (5, 6)
$$

$$
A =
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
$$

则：

$$
\begin{gathered}
Av = (1x5 + 2x6, 3x5 + 4x6) \\
= (17, 39)
\end{gathered}
$$

不要把矩阵乘法看成神秘规则。它是在计算新向量每个分量由旧分量如何组合得到。

### 4.4 算符的矩阵表示依赖基底

同一个算符，在不同基底下矩阵可以不同。

这和同一个向量在不同基底下坐标不同是同一件事。

物理上重要的是算符本身做了什么，而不是某个矩阵长什么样。矩阵是选了基底之后的坐标表达。

### 4.5 对易子

两个算符的先后顺序可能影响结果。定义：

$$
[A,B] = AB - BA
$$

如果：

$$
[A,B] = 0
$$

则说它们对易。

如果不对易，先做 $`A`$ 再做 $`B`$ 和先做 $`B`$ 再做 $`A`$ 不一样。

量子力学中，不对易是非常核心的现象。位置和动量算符不对易，这会导向不确定性关系。

### 最小计算例子

设：

$$
A =
\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$

计算：

$$
AB =
\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

所以：

$$
[A,B] = AB - BA =
\begin{pmatrix}
0 & 2 \\
-2 & 0
\end{pmatrix}
$$

它们不对易。

### 第 4 课检查题

1. $`A\lvert \psi \rangle`$ 用普通语言怎么读？
2. 什么叫线性算符？
3. 为什么矩阵表示依赖基底？
4. $`[A,B] = 0`$ 说明什么？
5. 如果两个操作先后顺序会改变结果，你觉得这在测量中可能意味着什么？

## 第 5 课：本征值和本征向量

### 5.1 先从普通矩阵看

如果：

$$
A\lvert v \rangle = \lambda \lvert v \rangle
$$

那么 $`\lvert v\rangle`$ 是 $`A`$ 的本征向量，$`\lambda`$ 是本征值。

普通语言：

> $`A`$ 作用在 $`\lvert v\rangle`$ 上以后，没有改变 $`\lvert v\rangle`$ 的方向，只把它乘了一个数 $`\lambda`$。

例子：

$$
A =
\begin{pmatrix}
2 & 0 \\
0 & 5
\end{pmatrix}
$$

对：

$$
e_{1} = (1, 0)
$$

作用：

$$
Ae_1 = (2, 0) = 2e_1
$$

所以 $`e_{1}`$ 是本征向量，本征值是 $`2`$。

对：

$$
e_{2} = (0, 1)
$$

作用：

$$
Ae_2 = (0, 5) = 5e_2
$$

所以 $`e_{2}`$ 是本征向量，本征值是 $`5`$。

### 5.2 为什么量子力学特别重视本征值

量子力学中，可观测量用算符表示。某个可观测量的可能测量结果，对应这个算符的本征值。

这句话先作为预告，第四章会正式讲。

现在你只要记住：

> 算符 -> 问的问题
> 本征值 -> 可能答案
> 本征向量 -> 得到该答案时对应的特殊状态

例如，如果能量算符 $`H`$ 满足：

$$
H\lvert E_{n} \rangle = E_{n}\lvert E_{n} \rangle
$$

那么 $`E_n`$ 是一个允许的能量值，$`\lvert E_n\rangle`$ 是对应的能量本征态。

### 5.3 怎样手算 2x2 本征值

对矩阵：

$$
B =
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$

找满足：

$$
B(x, y) = \lambda(x, y)
$$

左边是：

$$
B(x, y) = (y, x)
$$

所以：

$$
\begin{gathered}
y = \lambda x \\
x = \lambda y
\end{gathered}
$$

把第一式代入第二式：

$$
x = \lambda(\lambda x) = \lambda^2 x
$$

若 $`x`$ 不为 0，则：

> $`\lambda^2=1`$
> $`\lambda=1`$ 或 $`\lambda=-1`$

当 $`\lambda=1`$：

$$
y = x
$$

本征向量可取：

$$
(1, 1)
$$

归一化后：

$$
(1/\sqrt{2})(1, 1)
$$

当 $`\lambda=-1`$：

$$
y = -x
$$

本征向量可取：

$$
(1, -1)
$$

归一化后：

$$
(1/\sqrt{2})(1, -1)
$$

### 5.4 本征基底就是“最适合某个问题的基底”

如果你要讨论算符 $`A`$ 对应的测量，那么 $`A`$ 的本征向量基底通常是最自然的基底。

因为在本征态上，算符作用最简单：

$$
A\lvert a_{n} \rangle = a_{n}\lvert a_{n} \rangle
$$

一般态可以展开成：

$$
\lvert \psi \rangle = \sum_{n} c_{n} \lvert a_{n} \rangle
$$

测量结果和概率就会围绕这些展开系数组织起来。

### 第 5 课检查题

1. $`A\lvert v\rangle = \lambda\lvert v\rangle`$ 用普通语言怎么说？
2. 为什么本征向量不是随便一个向量？
3. 对角矩阵的本征向量为什么容易看出来？
4. 对 $`B = [[0,1],[1,0]]`$，本征值为什么是 $`1`$ 和 $`-1`$？
5. 在量子力学中，本征值预告了什么物理意义？

## 第 6 课：厄米、幺正、投影和无限维

### 6.1 厄米算符：适合表示可观测量

复矩阵的 dagger 操作表示：

> 先转置，再复共轭

如果：

$$
A^\dagger = A
$$

则 $`A`$ 是厄米算符。

例子：

$$
A =
\begin{pmatrix}
2 & 0 \\
0 & 5
\end{pmatrix}
$$

它是厄米的。

再看：

$$
C =
\begin{pmatrix}
0 & -i \\
i & 0
\end{pmatrix}
$$

它也是厄米的，因为转置并复共轭后仍回到自己。

厄米算符重要是因为：

1. 本征值是实数。
2. 不同本征值对应的本征向量正交。

物理测量结果必须是实数，所以可观测量要由厄米算符表示。

### 6.2 幺正算符：适合表示保持概率的变换

如果：

$$
U^\dagger U = I
$$

则 $`U`$ 是幺正算符。

它保持长度：

$$
\langle Upsi \mid Upsi \rangle = \langle \psi \mid \psi \rangle
$$

物理意义是：如果一个态总概率原来是 1，经过幺正变换后仍然是 1。

量子态随时间自然演化时，总概率不能丢失，所以时间演化由幺正变换描述。

### 6.3 投影算符：取出某个方向的分量

假设 $`\lvert n\rangle`$ 是归一化向量。投影到 $`\lvert n\rangle`$ 方向的算符是：

$$
P_{n} = \lvert n \rangle\langle n \rvert
$$

对任意态：

$$
P_{n}\lvert \psi \rangle = \lvert n \rangle\langle n \mid \psi \rangle
$$

这里：

$$
\langle n \mid \psi \rangle
$$

就是 $`\lvert \psi \rangle`$ 在 $`\lvert n\rangle`$ 方向上的分量。

例子：

$$
\begin{gathered}
\lvert n \rangle = (1,0) \\
\lvert \psi \rangle = (a,b)
\end{gathered}
$$

则投影结果是：

$$
P_{n}\lvert \psi \rangle = (a,0)
$$

也就是只保留第一个方向的分量。

### 6.4 完备性：所有基底方向加起来覆盖整个空间

如果一组正交归一基底覆盖了整个空间，那么：

$$
\sum_{n} \lvert n \rangle\langle n \rvert = I
$$

这叫完备性。

普通语言：

> 把所有基底方向的投影加起来，就等于什么都不丢地保留原向量。

对二维空间：

$$
\lvert 1 \rangle\langle 1 \rvert + \lvert 2 \rangle\langle 2 \rvert = I
$$

所以：

$$
\begin{aligned}
\lvert\psi\rangle
&= I\lvert\psi\rangle \\
&= \lvert 1\rangle\langle 1\mid\psi\rangle
 + \lvert 2\rangle\langle 2\mid\psi\rangle
\end{aligned}
$$

这就是展开公式的算符写法。

### 6.5 从有限维到无限维

前面我们用二维、三维向量讲概念。量子力学中的位置空间通常是连续的，所以会出现无限维。

有限维展开：

$$
\lvert \psi \rangle = \sum_{n} c_{n} \lvert n \rangle
$$

连续位置基底展开：

$$
\lvert \psi \rangle = \int dx \psi(x)\lvert x \rangle
$$

有限维归一化：

$$
\sum_{n} \lvert c_{n}\rvert^2 = 1
$$

连续位置归一化：

$$
\int dx \lvert \psi(x)\rvert^2 = 1
$$

有限维内积：

$$
\langle \phi \mid \psi \rangle = \sum_{n} \phi_n^\ast \psi_n
$$

连续位置内积：

$$
\langle \phi \mid \psi \rangle = \int dx \phi^\ast(x) \psi(x)
$$

你不需要害怕积分形式。它只是把“对所有分量求和”换成“对连续位置积分”。

### 第 6 课检查题

1. 为什么厄米算符适合表示可观测量？
2. 为什么幺正算符适合表示时间演化？
3. 投影算符 $`\lvert n\rangle\langle n\rvert`$ 做了什么？
4. $`\sum_n \lvert n\rangle\langle n\rvert = I`$ 用普通语言怎么解释？
5. 为什么连续情形中求和会变成积分？

## 本章总复习

### 你现在应该能读懂的句子

$$
\lvert \psi \rangle = \sum_{n} c_{n} \lvert n \rangle
$$

意思：

> 态 $`\lvert\psi\rangle`$ 在基底 $`\lvert n\rangle`$ 上展开，$`c_n`$ 是展开系数。

$$
\langle \psi \mid \psi \rangle = 1
$$

意思：

> 态已经归一化，总概率为 1。

$$
A\lvert a_{n} \rangle = a_{n}\lvert a_{n} \rangle
$$

意思：

> $`\lvert a_n\rangle`$ 是算符 $`A`$ 的本征态，$`a_n`$ 是对应本征值。

$$
P_{n} = \lvert n \rangle\langle n \rvert
$$

意思：

> $`P_n`$ 是投影到 $`\lvert n\rangle`$ 方向的算符。

$$
U^\dagger U = I
$$

意思：

> U 是幺正算符，会保持内积和归一化。

### 最重要的概念关系

> 态 -> 向量
> 表示方式 -> 基底下的坐标
> 概率 -> 振幅模平方
> 观测量 -> 厄米算符
> 可能结果 -> 本征值
> 特殊确定态 -> 本征向量
> 时间演化 -> 幺正变换

## 本章作业

### A. 归一化

给定：

$$
v = (2, 2)
$$

求归一化后的向量。

### B. 复内积

给定：

$$
\begin{gathered}
v = (1, i) \\
w = (1, -i)
\end{gathered}
$$

计算：

$$
\begin{gathered}
\langle v \mid w \rangle \\
\langle v \mid v \rangle
\end{gathered}
$$

### C. 本征值

给定：

$$
A =
\begin{pmatrix}
3 & 0 \\
0 & -2
\end{pmatrix}
$$

求本征值和对应本征向量。

### D. 非对角矩阵

给定：

$$
B =
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$

验证：

$$
\begin{gathered}
(1/\sqrt{2})(1,1) \\
(1/\sqrt{2})(1,-1)
\end{gathered}
$$

是它的归一化本征向量。

### E. 投影

设：

$$
\begin{gathered}
\lvert n \rangle = (1,0) \\
\lvert \psi \rangle = (3/5, 4/5)
\end{gathered}
$$

求：

$$
P_{n}\lvert \psi \rangle
$$

并解释结果。

## 参考答案

### A

长度：

$$
|\lvert v\rvert| = \sqrt{2^2 + 2^2} = \sqrt{8} = 2sqrt(2)
$$

归一化：

$$
v_{norm} = (1/\sqrt{2}, 1/\sqrt{2})
$$

### B

先取第一个向量的复共轭：

$$
v^\ast = (1, -i)
$$

所以：

$$
\begin{gathered}
\langle v \mid w \rangle = 1 \cdot 1 + (-i)(-i) = 1 - 1 = 0 \\
\langle v \mid v \rangle = 1 \cdot 1 + (-i)i = 2
\end{gathered}
$$

### C

$$
\begin{gathered}
A(1,0) = 3(1,0) \\
A(0,1) = -2(0,1)
\end{gathered}
$$

本征值为 $`3`$ 和 $`-2`$，对应本征向量可取 $`(1,0)`$ 和 $`(0,1)`$。

### D

对：

$$
u_+ = (1/\sqrt{2})(1,1)
$$

有：

$$
Bu_+ = u_+
$$

本征值为 $`1`$。

对：

$$
u_- = (1/\sqrt{2})(1,-1)
$$

有：

$$
Bu_- = -u_-
$$

本征值为 $`-1`$。

### E

投影到 $`(1,0)`$ 方向，只保留第一个分量：

$$
P_{n}\lvert \psi \rangle = (3/5, 0)
$$

这表示态在 $`\lvert n\rangle`$ 方向上的部分。对应概率是：

$$
\lvert 3/5\rvert^2 = 9/25
$$

## 进入第 2 章前请确认

你应该能独立解释：

1. 为什么量子态可以看作向量。
2. 为什么态的坐标依赖基底。
3. 为什么内积要能给出长度和重合程度。
4. 为什么复数振幅的模平方才给概率。
5. 为什么本征值和本征向量会在测量理论中变得重要。

如果这些还不稳，不要急着进入经典力学复习。量子力学后面的困难，很多其实是第 1 章语言没练熟。
