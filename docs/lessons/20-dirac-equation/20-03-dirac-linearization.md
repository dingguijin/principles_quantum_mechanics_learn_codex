# 第 20 章第 3 讲：Dirac 的线性化思路

## 这一讲要解决的问题

Dirac 想要一个对时间一阶、对空间也一阶的相对论量子方程。本讲推导为什么这会迫使我们引入矩阵。

## 为什么有这个概念

薛定谔方程有清楚的一阶时间演化：

$$
i\hbar\frac{\partial\psi}{\partial t}=H\psi.
$$

Dirac 希望保留这种形式，同时让 Hamiltonian 的平方给出相对论能量：

$$
E^2=p^2c^2+m^2c^4.
$$

## 公式怎么来

设

$$
H_D=c\boldsymbol{\alpha}\cdot\mathbf p+\beta mc^2.
$$

Dirac 方程写成：

$$
i\hbar\frac{\partial\psi}{\partial t}=H_D\psi.
$$

为了符合相对论关系，要求：

$$
H_D^2=p^2c^2+m^2c^4.
$$

展开：

$$
H_D^2
=
c^2\sum_{i,j}\alpha_i\alpha_jp_ip_j
+mc^3\sum_i(\alpha_i\beta+\beta\alpha_i)p_i
+\beta^2m^2c^4.
$$

要让它等于 $`p^2c^2+m^2c^4`$，需要：

$$
\{\alpha_i,\alpha_j\}=2\delta_{ij}I,
\qquad
\{\alpha_i,\beta\}=0,
\qquad
\beta^2=I.
$$

## 为什么必须是矩阵

普通数彼此交换，无法让非零的 $`\alpha_i`$ 和 $`\beta`$ 反对易。只有矩阵可以满足这种代数关系。

因此 $`\psi`$ 必须是多分量对象，矩阵才能作用在它上面。

## 物理意义

Dirac 不是凭空添加复杂性，而是从三个要求推出矩阵结构：

- 时间一阶；
- 空间一阶；
- 平方后回到相对论能量关系。

矩阵和旋量是这些要求的代价，也是自旋和反粒子出现的入口。

## 和前后章节的关系

第 1 章的矩阵和本征值语言在这里升级为物理必需品。第 14 章自旋中的 Pauli 矩阵则是 Dirac 矩阵结构的低能影子。

## 练习

1. Dirac 为什么不直接使用 $`E^2=p^2c^2+m^2c^4`$ 的二阶方程？
2. $`\{\alpha_i,\beta\}=0`$ 消掉了什么项？
3. 为什么普通数不能完成 Dirac 线性化？

## 解答

1. 他想保留一阶时间演化和更好的概率解释。
2. 消掉 $`H_D^2`$ 中与 $`p_i`$ 一次成正比的交叉项。
3. 普通数彼此交换，非零普通数不能反对易；矩阵才可以满足 $`\alpha_i\beta+\beta\alpha_i=0`$。
