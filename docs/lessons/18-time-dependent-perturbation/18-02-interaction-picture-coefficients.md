# 第 18 章第 2 讲：相互作用绘景和展开系数

## 这一讲要解决的问题

含时微扰论要计算跃迁概率。第一步不是直接解完整薛定谔方程，而是把 \(H_0\) 的已知演化先拿掉，只留下扰动造成的系数变化。

## 为什么有这个概念

如果直接写 \(|\psi(t)\rangle\)，其中既包含 \(H_0\) 自己造成的相位，也包含 \(V(t)\) 造成的真实跃迁。我们希望把两者分开：

- \(H_0\) 的演化已知；
- \(V(t)\) 的作用才需要近似计算。

这就是相互作用绘景的思想。

## 公式怎么来

设

$$
H_0|n\rangle=E_n|n\rangle.
$$

把态展开为：

$$
|\psi(t)\rangle
=
\sum_n c_n(t)e^{-iE_nt/\hbar}|n\rangle.
$$

如果没有扰动，\(c_n(t)\) 是常数；如果 \(c_n(t)\) 改变，就说明发生了跃迁。

代入薛定谔方程：

$$
i\hbar\frac{d}{dt}|\psi(t)\rangle=(H_0+V(t))|\psi(t)\rangle.
$$

左边求导时有两类项：

$$
i\hbar\sum_n \dot c_n e^{-iE_nt/\hbar}|n\rangle
+
\sum_n c_n E_n e^{-iE_nt/\hbar}|n\rangle.
$$

右边的 \(H_0\) 项为：

$$
\sum_n c_n E_n e^{-iE_nt/\hbar}|n\rangle.
$$

两边的 \(H_0\) 项抵消，剩下：

$$
i\hbar\sum_n \dot c_n e^{-iE_nt/\hbar}|n\rangle
=
\sum_n c_n V(t)e^{-iE_nt/\hbar}|n\rangle.
$$

左乘 \(\langle m|\)，再乘以 \(e^{iE_mt/\hbar}\)，得到：

$$
i\hbar \dot c_m(t)
=
\sum_n \langle m|V(t)|n\rangle c_n(t)
e^{i(E_m-E_n)t/\hbar}.
$$

定义

$$
V_{mn}(t)=\langle m|V(t)|n\rangle,
\qquad
\omega_{mn}=\frac{E_m-E_n}{\hbar},
$$

于是：

$$
i\hbar \dot c_m(t)
=
\sum_n V_{mn}(t)c_n(t)e^{i\omega_{mn}t}.
$$

## 物理意义

这条系数方程说明：

- \(V_{mn}(t)\) 决定 \(n\) 态能否流向 \(m\) 态；
- \(e^{i\omega_{mn}t}\) 来自能级差导致的相位；
- 所有其他态的系数 \(c_n(t)\) 会耦合到 \(c_m(t)\)。

如果矩阵元为零，扰动不能在一阶连接这两个态。如果相位快速转动，贡献可能相互抵消。

## 和前后章节的关系

第 4 章的薛定谔方程给出时间演化，第 11 章的时间平移告诉我们能量对应时间相位。本讲把这些内容用于实际近似计算。

第 18 章后面的所有公式，都是从这个系数方程出发。

## 练习

1. 为什么展开式中要写 \(e^{-iE_nt/\hbar}\)？
2. 若没有 \(V(t)\)，\(c_n(t)\) 如何变化？
3. 系数方程中的 \(V_{mn}(t)\) 表示什么？

## 解答

1. 这是 \(H_0\) 的已知时间演化。先把它提出来，可以让未知量只剩扰动造成的系数变化。
2. \(c_n(t)\) 都是常数，所以各能级占有概率不变。
3. 它是扰动在 \(m,n\) 两个未扰动态之间的矩阵元，表示扰动把 \(n\) 态耦合到 \(m\) 态的能力。
