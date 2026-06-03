# 第 19 章第 4 讲：Born 近似，弱势散射的 Fourier 图像

## 这一讲要解决的问题

一般势场的散射波函数很难精确求。Born 近似给出弱势散射的一阶公式，把散射振幅写成势能的 Fourier 变换。

## 为什么有这个概念

如果势很弱，粒子在相互作用区内的波函数应该和入射平面波差不多。于是可先忽略散射波对势区波函数的反作用，用入射波估计散射振幅。

这和第 17、18 章的微扰思想一致：用未扰动解代替完整解，计算一阶修正。

## 公式怎么来

入射动量为 \(\mathbf k\)，出射动量为 \(\mathbf k'\)。弹性散射中：

$$
|\mathbf k|=|\mathbf k'|=k.
$$

定义动量转移：

$$
\mathbf q=\mathbf k'-\mathbf k.
$$

一阶 Born 近似给出：

$$
f_{\text{Born}}(\mathbf k'\leftarrow \mathbf k)
=
-\frac{m}{2\pi\hbar^2}
\int d^3r\,
e^{-i(\mathbf k'-\mathbf k)\cdot\mathbf r}V(\mathbf r).
$$

也就是：

$$
f_{\text{Born}}(\mathbf q)
=
-\frac{m}{2\pi\hbar^2}
\int d^3r\,e^{-i\mathbf q\cdot\mathbf r}V(\mathbf r).
$$

## 物理意义

Born 近似说明：弱势散射看到的是势 \(V(\mathbf r)\) 的动量空间结构。

小角度散射对应小 \(q\)，看的是势的长距离、整体结构。大角度散射对应大 \(q\)，看的是势的短距离、快速变化结构。

这也是为什么散射可以当作显微镜：改变入射能量和测量角度，就能选择不同的空间尺度。

## 适用条件

Born 近似通常要求：

- 势不强；
- 势区内完整波函数和入射波差别不大；
- 散射相位积累不大；
- 没有强共振或束缚态附近的增强。

如果势很强或低能下相互作用时间长，Born 近似可能失败。

## 和前后章节的关系

第 18 章的黄金规则中，跃迁率由矩阵元平方决定。Born 近似中的积分也可理解为平面波初态和末态之间的势矩阵元：

$$
\langle \mathbf k'|V|\mathbf k\rangle.
$$

第 19 章第 5 讲会介绍另一种适合中心势的办法：分波法。

## 练习

1. Born 近似为什么会出现 \(e^{-i\mathbf q\cdot\mathbf r}\)？
2. 大角度散射对应大 \(q\) 还是小 \(q\)？
3. Born 近似和第 18 章的矩阵元思想有什么关系？

## 解答

1. 初态和末态平面波相乘给出相位差，正是动量转移 \(\mathbf q=\mathbf k'-\mathbf k\) 对应的 Fourier 因子。
2. 大角度散射对应大 \(q\)。弹性散射中 \(q=2k\sin(\theta/2)\)。
3. Born 振幅本质上是 \(\langle \mathbf k'|V|\mathbf k\rangle\)，即势把入射动量态耦合到出射动量态的矩阵元。
