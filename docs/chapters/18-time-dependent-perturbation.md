# 18. Time-Dependent Perturbation Theory

含时微扰论研究这样一类问题：哈密顿量中有一个随时间变化的小项，系统原本处在 \(H_0\) 的某个能级上，后来可能跃迁到另一个能级。第 17 章问“能级和本征态怎样被小修正改变”，本章问“外部随时间变化的作用怎样让系统从一个态跑到另一个态”。

这章是理解吸收、发射、共振、谱线强度、散射前奏和量子跃迁的核心工具。它把前面学过的矩阵元、相位、能级差和选择规则放到时间演化中。

## 本章逐讲

| 讲义 | 主题 |
| --- | --- |
| [第 1 讲：为什么需要含时微扰论](../lessons/18-time-dependent-perturbation/18-01-why-time-dependent-perturbation.md) | 跃迁、外场、定态微扰的边界 |
| [第 2 讲：相互作用绘景和展开系数](../lessons/18-time-dependent-perturbation/18-02-interaction-picture-coefficients.md) | 去掉 \(H_0\) 相位、系数方程 |
| [第 3 讲：一阶跃迁振幅公式怎么来](../lessons/18-time-dependent-perturbation/18-03-first-order-transition-amplitude.md) | 时间积分、相位匹配、跃迁概率 |
| [第 4 讲：周期扰动、共振和能量守恒的出现](../lessons/18-time-dependent-perturbation/18-04-periodic-driving-resonance.md) | 外场频率、共振条件、谱线宽度 |
| [第 5 讲：Fermi 黄金规则](../lessons/18-time-dependent-perturbation/18-05-fermi-golden-rule.md) | 连续末态、态密度、跃迁率 |
| [第 6 讲：选择规则、适用范围和后续入口](../lessons/18-time-dependent-perturbation/18-06-selection-rules-validity-next.md) | 矩阵元、近似失效、散射入口 |

## 18.1 为什么有这个概念

如果哈密顿量不随时间变，系统处在 \(H_0\) 的本征态中时，只会积累相位：

$$
|n(t)\rangle=e^{-iE_nt/\hbar}|n\rangle.
$$

相位会变，但测到能量 \(E_n\) 的概率不变。也就是说，定态本身不会自发变成另一个 \(H_0\) 本征态。

真实实验中，我们常用随时间变化的外场驱动系统：

- 用光照射原子，使电子吸收光子后跃迁到激发态；
- 用射频场翻转自旋；
- 用随时间变化的电场或磁场探测谱线；
- 在散射问题中，用入射波和相互作用计算从初态到末态的概率。

所以要研究：

$$
H(t)=H_0+V(t),
$$

其中 \(H_0\) 可解，\(V(t)\) 小但随时间变化。

## 18.2 展开态：让未知量变成时间系数

设

$$
H_0|n\rangle=E_n|n\rangle.
$$

如果没有扰动，每个本征态只带相位 \(e^{-iE_nt/\hbar}\)。有扰动时，态可以展开为：

$$
|\psi(t)\rangle
=
\sum_n c_n(t)e^{-iE_nt/\hbar}|n\rangle.
$$

这里 \(e^{-iE_nt/\hbar}\) 是 \(H_0\) 自己造成的已知相位；真正的未知量是 \(c_n(t)\)。如果 \(c_n(t)\) 改变，就表示不同能级的占有概率改变。

把展开式代入薛定谔方程：

$$
i\hbar \frac{d}{dt}|\psi(t)\rangle=(H_0+V(t))|\psi(t)\rangle,
$$

可得系数方程：

$$
i\hbar \dot c_m(t)
=
\sum_n V_{mn}(t)c_n(t)e^{i\omega_{mn}t},
$$

其中

$$
V_{mn}(t)=\langle m|V(t)|n\rangle,
\qquad
\omega_{mn}=\frac{E_m-E_n}{\hbar}.
$$

这条方程是含时微扰论的核心。矩阵元负责“能否耦合”，相位因子负责“是否相干累积”。

## 18.3 一阶跃迁振幅

假设系统一开始在 \(|i\rangle\)：

$$
c_i(0)=1,\qquad c_{m\neq i}(0)=0.
$$

若扰动很小，一阶近似中右边可取 \(c_i(t)\approx 1\)，其他 \(c_n\approx0\)。对 \(f\neq i\)：

$$
i\hbar \dot c_f^{(1)}(t)
=
V_{fi}(t)e^{i\omega_{fi}t}.
$$

积分得到：

$$
c_f^{(1)}(t)
=
-\frac{i}{\hbar}\int_0^t dt'\,
V_{fi}(t')e^{i\omega_{fi}t'}.
$$

跃迁概率为：

$$
P_{i\to f}(t)
=|c_f^{(1)}(t)|^2.
$$

物理意义非常直接：跃迁振幅是所有时刻的小贡献相加。若相位随时间快速转动，贡献互相抵消；若相位匹配，贡献相干累积，跃迁概率变大。

## 18.4 周期扰动和共振

设扰动有周期形式，例如：

$$
V(t)=W\cos\omega t.
$$

使用

$$
\cos\omega t=\frac12(e^{i\omega t}+e^{-i\omega t}),
$$

一阶振幅中会出现相位：

$$
e^{i(\omega_{fi}+\omega)t},
\qquad
e^{i(\omega_{fi}-\omega)t}.
$$

如果外场频率满足

$$
\omega\approx \omega_{fi}=\frac{E_f-E_i}{\hbar},
$$

其中一个相位变化很慢，时间积分会显著增大。这就是共振条件。它用量子语言表达了能量匹配：

$$
\hbar\omega \approx E_f-E_i.
$$

这不是预先硬塞进来的能量守恒，而是长时间相干累积的结果。时间越长，频率匹配越尖锐；时间越短，能量分辨率越差。

## 18.5 Fermi 黄金规则

若末态不是单个离散能级，而是一大片连续态，单个末态概率常常不是最方便的量。更自然的是单位时间总跃迁概率，也就是跃迁率。

对弱扰动、长时间、连续末态，Fermi 黄金规则给出：

$$
\Gamma_{i\to f}
=
\frac{2\pi}{\hbar}|V_{fi}|^2\rho(E_f),
$$

其中：

- \(\Gamma\)：跃迁率；
- \(V_{fi}\)：初态到末态的耦合矩阵元；
- \(\rho(E_f)\)：末态在能量 \(E_f\) 附近的态密度；
- 能量匹配由 \(E_f\approx E_i+\hbar\omega\) 或相应守恒条件给出。

黄金规则的物理意义是：

> 跃迁快不快 = 耦合强不强 × 可去的末态多不多。

它在原子辐射、粒子衰变、散射、固体中的跃迁和线性响应中都非常常见。

## 18.6 选择规则、适用范围和后续关系

含时微扰的核心对象仍是矩阵元：

$$
V_{fi}(t)=\langle f|V(t)|i\rangle.
$$

如果这个矩阵元因为对称性为零，一阶跃迁就被禁止。这就是选择规则。例如电偶极跃迁中，扰动常与位置算符相关，角动量和宇称会限制哪些跃迁可发生。

适用含时微扰论需要：

- \(V(t)\) 足够弱，跃迁概率仍小；
- 一阶近似下 \(c_i(t)\) 仍接近 1；
- 共振附近若作用时间很长或耦合很强，不能无限套一阶公式；
- 连续态问题中要正确处理态密度和归一化。

和后续章节的关系：

- 第 19 章散射理论会把“初态到末态的跃迁”用于入射粒子和散射末态。
- 第 20 章 Dirac 方程会给出相对论粒子的态和相互作用，跃迁与散射仍离不开矩阵元。
- 第 21 章路径积分进阶会从另一种语言理解传播、相位和振幅求和。

## 本章学习检查

1. 含时微扰论和定态微扰论分别问什么问题？
2. 为什么要把 \(H_0\) 的相位 \(e^{-iE_nt/\hbar}\) 先提出来？
3. 一阶跃迁振幅为什么是时间积分？
4. 共振条件为什么是 \(\hbar\omega\approx E_f-E_i\)？
5. Fermi 黄金规则中的 \(\rho(E_f)\) 有什么物理意义？
6. 选择规则为什么可以让某些跃迁概率为零？

## 练习和解答

### 练习 1：常数扰动的短时跃迁

设 \(V_{fi}(t)=V_{fi}\) 为常数，求一阶振幅。

**解答：**

$$
c_f^{(1)}(t)
=-\frac{i}{\hbar}V_{fi}\int_0^t e^{i\omega_{fi}t'}dt'
=
\frac{V_{fi}}{\hbar}
\frac{1-e^{i\omega_{fi}t}}{\omega_{fi}}.
$$

因此

$$
P_{i\to f}(t)
=
\frac{4|V_{fi}|^2}{\hbar^2\omega_{fi}^2}
\sin^2\frac{\omega_{fi}t}{2}.
$$

短时间 \(t\) 很小时，\(\sin(\omega_{fi}t/2)\approx \omega_{fi}t/2\)，所以 \(P\approx |V_{fi}|^2t^2/\hbar^2\)。

### 练习 2：共振判断

某两能级差为 \(E_f-E_i=2.0\text{ eV}\)。若用频率 \(\omega\) 的外场驱动，吸收共振条件是什么？

**解答：**

吸收时外场提供能量 \(\hbar\omega\)，所以

$$
\hbar\omega\approx 2.0\text{ eV}.
$$

也就是 \(\omega\approx (2.0\text{ eV})/\hbar\)。

### 练习 3：黄金规则中的态密度

若两个过程有相同的 \(|V_{fi}|^2\)，但过程 A 的末态密度是过程 B 的 10 倍，跃迁率如何比较？

**解答：**

由

$$
\Gamma=\frac{2\pi}{\hbar}|V_{fi}|^2\rho(E_f),
$$

跃迁率正比于态密度。因此 A 的跃迁率是 B 的 10 倍。

### 练习 4：选择规则

若某扰动满足 \(\langle f|V(t)|i\rangle=0\)，一阶跃迁概率是多少？

**解答：**

一阶振幅

$$
c_f^{(1)}(t)
=-\frac{i}{\hbar}\int_0^t dt'\,
\langle f|V(t')|i\rangle e^{i\omega_{fi}t'}
$$

为零，因此一阶跃迁概率为零。跃迁可能完全禁止，也可能只在高阶效应中出现。
