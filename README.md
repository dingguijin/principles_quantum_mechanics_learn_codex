# Principles of Quantum Mechanics 学习笔记

这是一套配合 R. Shankar, *Principles of Quantum Mechanics*, 2nd ed. 学习的中文一对一导学笔记。目标不是压缩原书，而是像老师带学生一样，从零基础开始逐步补齐数学、经典力学和量子力学形式体系。

当前仓库采用“先搭全书提纲，再逐章扩写”的方式维护。第 0-10 章已经完成细讲或逐讲扩写，后续章节会按同样标准继续扩展。

## 使用方式

1. 先读 [00-foundations.md](docs/00-foundations.md)，不要跳过检查题。它不是附录，而是零基础入口。
2. 再读 [第 1 章细讲版](docs/chapters/01-mathematical-introduction.md)，按“第 1 课、第 2 课...”分次学习。
3. 新增的逐讲版会放在 [docs/lessons](docs/lessons)。每一讲单独一个 Markdown 文件，固定包含：为什么有这个概念、解决什么问题、公式怎么来、物理意义、与经典力学/数学/历史/后续章节的关系、练习和解答。
4. 每节课都按这个顺序学习：普通语言解释 -> 最小计算例子 -> 检查题 -> 作业。
5. 按章节顺序学习 [docs/chapters](docs/chapters)。目前第 11 章之后仍是导学提纲，会继续逐章扩写为细讲版。
6. 纸质书用于阅读原书推导和习题；本仓库只提供原创讲解、学习路线、补充例题和自测。

## 逐讲版目录

| 讲义 | 主题 |
| --- | --- |
| [第 1 章第 1 讲：为什么量子态要看成向量](docs/lessons/01-mathematical-introduction/01-01-why-quantum-states-are-vectors.md) | 叠加、概率振幅、归一化、态矢量 |
| [第 1 章第 2 讲：基底、坐标和展开](docs/lessons/01-mathematical-introduction/01-02-basis-coordinates-expansion.md) | 基底、坐标、换基底、表象 |
| [第 1 章第 3 讲：内积、长度、正交和归一化](docs/lessons/01-mathematical-introduction/01-03-inner-product-norm-orthogonality-normalization.md) | 内积、概率振幅、正交归一、归一化 |
| [第 1 章第 4 讲：线性算符和矩阵](docs/lessons/01-mathematical-introduction/01-04-linear-operators-and-matrices.md) | 线性算符、矩阵元、对易子 |
| [第 1 章第 5 讲：本征值、本征向量和测量预告](docs/lessons/01-mathematical-introduction/01-05-eigenvalues-eigenvectors-measurement-preview.md) | 本征值、本征向量、本征基底、测量结果 |
| [第 1 章第 6 讲：厄米、幺正、投影和无限维推广](docs/lessons/01-mathematical-introduction/01-06-hermitian-unitary-projection-infinite-dimensional.md) | 厄米算符、幺正算符、投影、波函数 |
| [第 2 章第 1 讲：位置、速度、动量、力和能量](docs/lessons/02-review-of-classical-mechanics/02-01-basic-physical-quantities.md) | 基础运动量、动量、力、能量 |
| [第 2 章第 2 讲：牛顿形式，已知力如何求运动](docs/lessons/02-review-of-classical-mechanics/02-02-newtonian-form.md) | 牛顿方程、初始条件、势能和力 |
| [第 2 章第 3 讲：从坐标 x 到广义坐标 q](docs/lessons/02-review-of-classical-mechanics/02-03-generalized-coordinates.md) | 广义坐标、自由度、约束 |
| [第 2 章第 4 讲：拉格朗日量和 Euler-Lagrange 方程](docs/lessons/02-review-of-classical-mechanics/02-04-lagrangian-and-euler-lagrange-equation.md) | 拉格朗日量、Euler-Lagrange 方程 |
| [第 2 章第 5 讲：作用量和驻作用量思想](docs/lessons/02-review-of-classical-mechanics/02-05-action-and-stationary-action.md) | 作用量、驻值、路径积分入口 |
| [第 2 章第 6 讲：哈密顿量、正则动量和 Hamilton 方程](docs/lessons/02-review-of-classical-mechanics/02-06-hamiltonian-and-hamilton-equations.md) | 正则动量、哈密顿量、Hamilton 方程 |
| [第 2 章第 7 讲：相空间、泊松括号和量子力学的入口](docs/lessons/02-review-of-classical-mechanics/02-07-phase-space-poisson-brackets-quantum-entry.md) | 相空间、泊松括号、对易子入口 |
| [第 3 章第 1 讲：经典图像到底假设了什么](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-01-classical-picture-assumptions.md) | 经典粒子、经典波、经典假设 |
| [第 3 章第 2 讲：黑体辐射和能量量子化](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-02-blackbody-radiation-energy-quantization.md) | 黑体辐射、紫外灾难、能量量子 |
| [第 3 章第 3 讲：光电效应和光量子](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-03-photoelectric-effect-light-quanta.md) | 光电效应、光量子、阈频 |
| [第 3 章第 4 讲：原子光谱和离散能级](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-04-atomic-spectra-discrete-energy-levels.md) | 线状光谱、能级、跃迁 |
| [第 3 章第 5 讲：双缝干涉和电子的波动性](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-05-double-slit-electron-wave-nature.md) | 双缝、振幅叠加、相位 |
| [第 3 章第 6 讲：德布罗意关系和波粒统一](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-06-de-broglie-relation-wave-particle-unity.md) | 德布罗意波长、物质波、波函数 |
| [第 3 章第 7 讲：这些事实如何逼出量子公设](docs/lessons/03-all-is-not-well-with-classical-mechanics/03-07-how-experiments-force-quantum-postulates.md) | 量子态、算符、本征值、概率规则 |
| [第 4 章第 1 讲：态公设，系统状态为什么是 Hilbert 空间向量](docs/lessons/04-postulates-general-discussion/04-01-state-postulate-hilbert-space.md) | 态向量、归一化、Hilbert 空间 |
| [第 4 章第 2 讲：观测量公设，为什么可观测量由厄米算符表示](docs/lessons/04-postulates-general-discussion/04-02-observables-hermitian-operators.md) | 厄米算符、本征值、观测量 |
| [第 4 章第 3 讲：测量概率和 Born 规则](docs/lessons/04-postulates-general-discussion/04-03-measurement-probabilities-born-rule.md) | Born 规则、投影概率、模平方 |
| [第 4 章第 4 讲：测量后的态，投影和塌缩](docs/lessons/04-postulates-general-discussion/04-04-state-after-measurement-collapse.md) | 测量后态、投影算符、塌缩 |
| [第 4 章第 5 讲：时间演化和薛定谔方程](docs/lessons/04-postulates-general-discussion/04-05-time-evolution-schrodinger-equation.md) | 薛定谔方程、哈密顿算符、幺正演化 |
| [第 5 章第 1 讲：位置表象和一维定态薛定谔方程](docs/lessons/05-simple-problems-one-dimension/05-01-position-representation-stationary-schrodinger-equation.md) | 位置表象、波函数、定态方程 |
| [第 5 章第 2 讲：自由粒子和平面波](docs/lessons/05-simple-problems-one-dimension/05-02-free-particle-plane-waves.md) | 自由粒子、平面波、动量本征态 |
| [第 5 章第 3 讲：阶跃势、势垒和隧穿](docs/lessons/05-simple-problems-one-dimension/05-03-step-potentials-barriers-tunneling.md) | 势垒、指数衰减、隧穿 |
| [第 5 章第 4 讲：无限深势阱和能级量子化](docs/lessons/05-simple-problems-one-dimension/05-04-infinite-square-well-quantized-energy.md) | 无限深势阱、边界条件、离散能级 |
| [第 5 章第 5 讲：有限势阱和束缚态](docs/lessons/05-simple-problems-one-dimension/05-05-finite-wells-bound-states.md) | 有限势阱、束缚态、散射态 |
| [第 5 章第 6 讲：边界条件、归一化和一维问题总复习](docs/lessons/05-simple-problems-one-dimension/05-06-boundary-conditions-summary.md) | 边界条件、归一化、一维问题方法 |
| [第 6 章第 1 讲：为什么经典极限不是简单令 hbar=0](docs/lessons/06-classical-limit/06-01-why-classical-limit-is-not-just-hbar-zero.md) | 经典极限、作用量尺度、相位抵消 |
| [第 6 章第 2 讲：波包、期望值和经典轨迹](docs/lessons/06-classical-limit/06-02-wave-packets-expectation-values-classical-trajectories.md) | 波包、期望值、经典轨迹 |
| [第 6 章第 3 讲：Ehrenfest 定理，量子平均如何接近牛顿方程](docs/lessons/06-classical-limit/06-03-ehrenfest-theorem.md) | Ehrenfest 定理、平均力、经典近似 |
| [第 6 章第 4 讲：相位快速振荡、测量精度和经典图像的出现](docs/lessons/06-classical-limit/06-04-rapid-phases-measurement-resolution-classical-picture.md) | 快速相位、测量分辨率、经典图像 |
| [第 7 章第 1 讲：为什么谐振子到处出现](docs/lessons/07-harmonic-oscillator/07-01-why-harmonic-oscillators-appear-everywhere.md) | 二次近似、平衡点、小振动 |
| [第 7 章第 2 讲：谐振子哈密顿量和无量纲变量](docs/lessons/07-harmonic-oscillator/07-02-hamiltonian-dimensionless-variables.md) | 谐振子哈密顿量、自然长度、位置表象 |
| [第 7 章第 3 讲：升降算符和代数解法](docs/lessons/07-harmonic-oscillator/07-03-ladder-operators-algebraic-solution.md) | 升降算符、数算符、代数解法 |
| [第 7 章第 4 讲：能级、零点能和基态波函数](docs/lessons/07-harmonic-oscillator/07-04-energy-levels-zero-point-ground-state.md) | 等间隔能级、零点能、基态 |
| [第 7 章第 5 讲：数态、选择规则和谐振子为什么有用](docs/lessons/07-harmonic-oscillator/07-05-number-states-selection-rules-applications.md) | 数态、选择规则、应用 |
| [第 8 章第 1 讲：为什么需要路径积分表述](docs/lessons/08-path-integral-formulation/08-01-why-path-integrals.md) | 路径积分动机、振幅求和、作用量 |
| [第 8 章第 2 讲：传播子，量子演化的核函数](docs/lessons/08-path-integral-formulation/08-02-propagator-kernel.md) | 传播子、演化核、位置表象 |
| [第 8 章第 3 讲：路径积分公式和作用量相位](docs/lessons/08-path-integral-formulation/08-03-path-integral-action-phase.md) | 路径积分公式、作用量、相位 |
| [第 8 章第 4 讲：经典路径如何从相位相干中出现](docs/lessons/08-path-integral-formulation/08-04-classical-path-stationary-phase.md) | 驻相、经典路径、相位抵消 |
| [第 8 章第 5 讲：自由粒子例子和与薛定谔表述的关系](docs/lessons/08-path-integral-formulation/08-05-free-particle-and-schrodinger-equivalence.md) | 自由粒子传播子、等价表述 |
| [第 9 章第 1 讲：平均值、方差和不确定度](docs/lessons/09-heisenberg-uncertainty/09-01-expectation-variance-uncertainty.md) | 平均值、方差、不确定度 |
| [第 9 章第 2 讲：波包直觉，为什么越局域动量越分散](docs/lessons/09-heisenberg-uncertainty/09-02-wave-packet-localization-momentum-spread.md) | 波包、Fourier 直觉、动量分散 |
| [第 9 章第 3 讲：一般不确定性关系和对易子](docs/lessons/09-heisenberg-uncertainty/09-03-general-uncertainty-commutator.md) | 一般不确定性、对易子 |
| [第 9 章第 4 讲：位置动量不确定性关系](docs/lessons/09-heisenberg-uncertainty/09-04-position-momentum-uncertainty.md) | 位置动量、基本对易关系 |
| [第 9 章第 5 讲：常见误解、物理意义和应用](docs/lessons/09-heisenberg-uncertainty/09-05-misconceptions-meaning-applications.md) | 误解澄清、零点能、量子态结构 |
| [第 10 章第 1 讲：为什么多自由度不是多个一维问题简单并排](docs/lessons/10-n-degrees-of-freedom/10-01-why-many-degrees-of-freedom.md) | 多自由度、构型空间、联合概率 |
| [第 10 章第 2 讲：多维位置、动量和对易关系](docs/lessons/10-n-degrees-of-freedom/10-02-multidimensional-position-momentum-commutators.md) | 多维动量、偏导数、正则对易关系 |
| [第 10 章第 3 讲：多自由度哈密顿量和可分变量](docs/lessons/10-n-degrees-of-freedom/10-03-hamiltonians-and-separation.md) | 多自由度哈密顿量、变量分离 |
| [第 10 章第 4 讲：组合系统和张量积态空间](docs/lessons/10-n-degrees-of-freedom/10-04-tensor-product-composite-systems.md) | 张量积、组合系统、联合基底 |
| [第 10 章第 5 讲：可分态、纠缠态和多粒子物理入口](docs/lessons/10-n-degrees-of-freedom/10-05-separable-entangled-states.md) | 可分态、纠缠态、多粒子入口 |

## 教学原则

- 不假设你已经熟练掌握线性代数、微积分或经典力学。
- 每个新符号先解释“它是什么”，再解释“它怎么计算”，最后解释“它有什么物理意义”。
- 尽量用最小例子训练概念，例如二维向量、`2 x 2` 矩阵、两个结果的量子系统。
- 不把原书改写成摘要；重点是补足原书对零基础读者省略的中间步骤。
- 不复制原书正文，也不搬运原书习题。可以讲同类题、补充题和解题方法。

## 章节目录

| 章 | 笔记 | 主题 |
| --- | --- | --- |
| 0 | [零基础准备](docs/00-foundations.md) | 数学、物理量、学习方法 |
| 1 | [Mathematical Introduction](docs/chapters/01-mathematical-introduction.md) | 向量空间、内积、算符、基底 |
| 2 | [Review of Classical Mechanics](docs/chapters/02-review-of-classical-mechanics.md) | 牛顿、拉格朗日、哈密顿形式 |
| 3 | [All Is Not Well with Classical Mechanics](docs/chapters/03-all-is-not-well-with-classical-mechanics.md) | 经典理论的失效 |
| 4 | [The Postulates: A General Discussion](docs/chapters/04-postulates-general-discussion.md) | 态、观测量、测量、演化 |
| 5 | [Simple Problems in One Dimension](docs/chapters/05-simple-problems-one-dimension.md) | 一维薛定谔方程 |
| 6 | [The Classical Limit](docs/chapters/06-classical-limit.md) | 经典极限与对应关系 |
| 7 | [The Harmonic Oscillator](docs/chapters/07-harmonic-oscillator.md) | 谐振子、升降算符 |
| 8 | [Path Integral Formulation](docs/chapters/08-path-integral-formulation.md) | 传播子、作用量、路径积分 |
| 9 | [Heisenberg Uncertainty Relations](docs/chapters/09-heisenberg-uncertainty.md) | 不确定性关系 |
| 10 | [Systems with N Degrees of Freedom](docs/chapters/10-n-degrees-of-freedom.md) | 多自由度与多粒子 |
| 11 | [Symmetries and Their Consequences](docs/chapters/11-symmetries.md) | 对称性与守恒量 |
| 12 | [Rotational Invariance and Angular Momentum](docs/chapters/12-rotational-invariance-angular-momentum.md) | 转动与角动量 |
| 13 | [The Hydrogen Atom](docs/chapters/13-hydrogen-atom.md) | 氢原子 |
| 14 | [Spin](docs/chapters/14-spin.md) | 自旋 |
| 15 | [Addition of Angular Momenta](docs/chapters/15-addition-angular-momenta.md) | 角动量耦合 |
| 16 | [Variational and WKB Methods](docs/chapters/16-variational-wkb.md) | 变分法与 WKB |
| 17 | [Time-Independent Perturbation Theory](docs/chapters/17-time-independent-perturbation.md) | 定态微扰 |
| 18 | [Time-Dependent Perturbation Theory](docs/chapters/18-time-dependent-perturbation.md) | 含时微扰 |
| 19 | [Scattering Theory](docs/chapters/19-scattering-theory.md) | 散射理论 |
| 20 | [The Dirac Equation](docs/chapters/20-dirac-equation.md) | 相对论量子力学入门 |
| 21 | [Path Integrals: Part II](docs/chapters/21-path-integrals-part-ii.md) | 路径积分进阶 |

## 学习节奏

零基础学习不建议直接追求速度。一个稳妥节奏是：

- 第 0 章：3-7 天，重点是复数、函数、向量、矩阵、微积分和概率。
- 第 1 章：2-4 周，重点是线性代数语言和 Dirac 记号。
- 第 2-4 章：2-3 周，建立从经典到量子的形式转换。
- 第 5-9 章：4-6 周，掌握一维问题、谐振子和不确定性。
- 第 10-15 章：4-6 周，进入多粒子、对称性和角动量。
- 第 16-21 章：4-8 周，学习近似方法、散射、Dirac 方程和路径积分。

## 当前扩写状态

| 文件 | 状态 |
| --- | --- |
| [00-foundations.md](docs/00-foundations.md) | 细讲版 |
| [01-mathematical-introduction.md](docs/chapters/01-mathematical-introduction.md) | 细讲版；逐讲版 6/6 完成 |
| [02-review-of-classical-mechanics.md](docs/chapters/02-review-of-classical-mechanics.md) | 细讲版；逐讲版 7/7 完成 |
| [03-all-is-not-well-with-classical-mechanics.md](docs/chapters/03-all-is-not-well-with-classical-mechanics.md) | 细讲版；逐讲版 7/7 完成 |
| [04-postulates-general-discussion.md](docs/chapters/04-postulates-general-discussion.md) | 导学提纲；逐讲版 5/5 完成 |
| [05-simple-problems-one-dimension.md](docs/chapters/05-simple-problems-one-dimension.md) | 导学提纲；逐讲版 6/6 完成 |
| [06-classical-limit.md](docs/chapters/06-classical-limit.md) | 细讲版；逐讲版 4/4 完成 |
| [07-harmonic-oscillator.md](docs/chapters/07-harmonic-oscillator.md) | 细讲版；逐讲版 5/5 完成 |
| [08-path-integral-formulation.md](docs/chapters/08-path-integral-formulation.md) | 细讲版；逐讲版 5/5 完成 |
| [09-heisenberg-uncertainty.md](docs/chapters/09-heisenberg-uncertainty.md) | 细讲版；逐讲版 5/5 完成 |
| [10-n-degrees-of-freedom.md](docs/chapters/10-n-degrees-of-freedom.md) | 细讲版；逐讲版 5/5 完成 |
| 第 11-21 章 | 导学提纲，待逐章扩写 |

## 版权边界

这些笔记不复制原书正文，也不系统搬运原书习题。遇到原书习题时，建议你自己先做，再把题号和你的解法发给我，我可以帮你检查、提示或讲解同类题。

## 参考目录来源

- Springer 页面：<https://link.springer.com/book/10.1007/978-1-4757-0576-8>
- Google Books 页面：<https://books.google.com/books/about/Principles_of_Quantum_Mechanics.html?id=sDvrBwAAQBAJ>
