# 第 7 章第 5 讲：数态、选择规则和谐振子为什么有用

本讲收束第 7 章：谐振子不只是一个可解例子，它提供了后来许多量子结构的模板。

## 1. 本讲要解决的问题

数态 $`\lvert n\rangle`$ 有什么物理意义？

为什么升降算符会在后面反复出现？

## 2. 数态是什么

数态是数算符：

$$
N=a^\dagger a
$$

的本征态：

$$
N\lvert n\rangle=n\lvert n\rangle
$$

也是哈密顿量的本征态：

$$
H\lvert n\rangle=\hbar\omega\left(n+\frac12\right)\lvert n\rangle
$$

这里 $`n`$ 可以理解为激发数。

## 3. 升降关系

$$
a\lvert n\rangle=\sqrt n\lvert n-1\rangle
$$

$$
a^\dagger\lvert n\rangle=\sqrt{n+1}\lvert n+1\rangle
$$

这说明：

- $`a`$：减少一个激发。
- $`a^\dagger`$：增加一个激发。

系数 $`\sqrt n`$、$`\sqrt{n+1}`$ 来自归一化要求。

## 4. 选择规则的预告

位置算符可以写成：

$$
x=\sqrt{\frac{\hbar}{2m\omega}}(a+a^\dagger)
$$

因此 $`x`$ 作用在 $`\lvert n\rangle`$ 上，只连接：

$$
\lvert n-1\rangle,\quad \lvert n+1\rangle
$$

这预告了谐振子跃迁常有：

$$
\Delta n=\pm1
$$

这类选择规则。

## 5. 为什么谐振子有用

谐振子结构出现在很多地方：

- 分子振动：振动能级近似等间隔。
- 晶格振动：声子可看作振动模式量子。
- 电磁场：每个模式可量子化成谐振子。
- 小振动近似：复杂势能最低点附近。

## 6. 和后续章节的关系

升降算符思想会在角动量中再次出现：

$$
J_+,\quad J_-
$$

场量子化中，$`a^\dagger`$ 和 $`a`$ 会变成创造和湮灭粒子的算符。

第 16 章的近似方法也会不断把复杂系统近似为谐振子。

## 7. 练习

### 练习 1

计算：

$$
a\lvert3\rangle,\quad a^\dagger\lvert3\rangle
$$

### 练习 2

为什么 $`x\propto a+a^\dagger`$ 会导致只连接相邻能级？

### 练习 3

列出两个谐振子模型的应用。

## 8. 解答

### 解答 1

$$
a\lvert3\rangle=\sqrt3\lvert2\rangle
$$

$$
a^\dagger\lvert3\rangle=\sqrt4\lvert4\rangle=2\lvert4\rangle
$$

### 解答 2

因为 $`a`$ 把 $`\lvert n\rangle`$ 变成 $`\lvert n-1\rangle`$，$`a^\dagger`$ 把它变成 $`\lvert n+1\rangle`$。二者相加只产生相邻能级。

### 解答 3

例如分子振动、晶格声子、电磁场模式、小振动近似。

## 9. 本讲必须记住的三句话

1. $`\lvert n\rangle`$ 是谐振子的能量本征态，也可理解为激发数态。
2. 升降算符改变激发数，且系数由归一化决定。
3. 谐振子是分子、固体、场量子和小振动近似的基础模型。
