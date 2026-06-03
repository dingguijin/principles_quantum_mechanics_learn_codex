# 公式索引

这份索引用于复习时快速定位核心公式。它不是公式堆叠，而是按“这个公式解决什么问题”来整理。

## 线性代数和态空间

态归一化：

$$
\langle \psi|\psi\rangle=1.
$$

基底展开：

$$
|\psi\rangle=\sum_n c_n|n\rangle,
\qquad
c_n=\langle n|\psi\rangle.
$$

完备性：

$$
\sum_n |n\rangle\langle n|=I.
$$

期望值：

$$
\langle A\rangle=\langle\psi|A|\psi\rangle.
$$

对易子：

$$
[A,B]=AB-BA.
$$

## 测量和时间演化

Born 规则：

$$
P(a_n)=|\langle a_n|\psi\rangle|^2.
$$

投影测量后态：

$$
|\psi\rangle\to
\frac{P_n|\psi\rangle}
{\sqrt{\langle\psi|P_n|\psi\rangle}}.
$$

薛定谔方程：

$$
i\hbar\frac{\partial}{\partial t}|\psi(t)\rangle=H|\psi(t)\rangle.
$$

定态演化：

$$
|n(t)\rangle=e^{-iE_nt/\hbar}|n\rangle.
$$

## 位置、动量和不确定性

动量算符：

$$
\hat p=-i\hbar\frac{d}{dx}.
$$

正则对易关系：

$$
[x,p]=i\hbar.
$$

一维定态薛定谔方程：

$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}+V(x)\psi=E\psi.
$$

一般不确定性关系：

$$
\Delta A\,\Delta B\ge
\frac12|\langle[A,B]\rangle|.
$$

位置-动量不确定性：

$$
\Delta x\,\Delta p\ge\frac{\hbar}{2}.
$$

## 谐振子

Hamiltonian：

$$
H=\frac{p^2}{2m}+\frac12m\omega^2x^2.
$$

升降算符对易关系：

$$
[a,a^\dagger]=1.
$$

能级：

$$
E_n=\hbar\omega\left(n+\frac12\right).
$$

数算符：

$$
N=a^\dagger a,
\qquad
N|n\rangle=n|n\rangle.
$$

## 经典极限和路径积分基础

Ehrenfest 定理：

$$
\frac{d}{dt}\langle x\rangle=\frac{\langle p\rangle}{m},
\qquad
\frac{d}{dt}\langle p\rangle=-\left\langle\frac{dV}{dx}\right\rangle.
$$

传播子：

$$
K(x_f,t_f;x_i,t_i)=\langle x_f|e^{-iH(t_f-t_i)/\hbar}|x_i\rangle.
$$

路径积分：

$$
K=\int\mathcal D x(t)\,e^{iS[x]/\hbar}.
$$

驻相条件：

$$
\delta S=0.
$$

## 多自由度和张量积

多维正则对易关系：

$$
[x_i,p_j]=i\hbar\delta_{ij}.
$$

组合系统态空间：

$$
\mathcal H_{AB}=\mathcal H_A\otimes\mathcal H_B.
$$

可分态：

$$
|\psi\rangle_{AB}=|\phi\rangle_A\otimes|\chi\rangle_B.
$$

## 对称性和守恒量

连续变换：

$$
U(\epsilon)=e^{-i\epsilon G/\hbar}.
$$

守恒条件：

$$
\frac{dA}{dt}=0
\quad\text{if}\quad
\frac{\partial A}{\partial t}=0,\ [A,H]=0.
$$

时间演化算符：

$$
U(t)=e^{-iHt/\hbar}.
$$

## 角动量和自旋

角动量算符：

$$
\mathbf L=\mathbf r\times\mathbf p.
$$

角动量对易关系：

$$
[L_i,L_j]=i\hbar\epsilon_{ijk}L_k.
$$

共同本征值：

$$
L^2|lm\rangle=\hbar^2l(l+1)|lm\rangle,
\qquad
L_z|lm\rangle=\hbar m|lm\rangle.
$$

升降算符：

$$
L_\pm=L_x\pm iL_y.
$$

自旋 $`1/2`$ 算符：

$$
\mathbf S=\frac{\hbar}{2}\boldsymbol{\sigma}.
$$

Pauli 矩阵对易关系：

$$
[\sigma_i,\sigma_j]=2i\epsilon_{ijk}\sigma_k.
$$

## 氢原子

约化质量：

$$
\mu=\frac{m_1m_2}{m_1+m_2}.
$$

库仑势：

$$
V(r)=-\frac{e^2}{4\pi\epsilon_0 r}.
$$

氢原子能级：

$$
E_n=-\frac{\mu e^4}{2(4\pi\epsilon_0)^2\hbar^2}\frac{1}{n^2}.
$$

量子数：

$$
n=1,2,\ldots,\qquad
l=0,\ldots,n-1,\qquad
m=-l,\ldots,l.
$$

## 近似方法

变分原理：

$$
E[\psi]=\frac{\langle\psi|H|\psi\rangle}{\langle\psi|\psi\rangle}\ge E_0.
$$

WKB 局域动量：

$$
p(x)=\sqrt{2m(E-V(x))}.
$$

WKB 波函数：

$$
\psi(x)\approx\frac{C}{\sqrt{p(x)}}
\exp\left(\pm\frac{i}{\hbar}\int^x p(x')\,dx'\right).
$$

WKB 量子化：

$$
\int_{x_1}^{x_2}p(x)\,dx=\left(n+\frac12\right)\pi\hbar.
$$

## 定态微扰

Hamiltonian 分解：

$$
H=H_0+\lambda V.
$$

能量展开：

$$
E_n=E_n^{(0)}+\lambda E_n^{(1)}+\lambda^2E_n^{(2)}+\cdots.
$$

一阶能量修正：

$$
E_n^{(1)}=\langle n^{(0)}|V|n^{(0)}\rangle.
$$

一阶态修正：

$$
|n^{(1)}\rangle=
\sum_{m\ne n}|m^{(0)}\rangle
\frac{\langle m^{(0)}|V|n^{(0)}\rangle}
{E_n^{(0)}-E_m^{(0)}}.
$$

二阶能量修正：

$$
E_n^{(2)}=
\sum_{m\ne n}
\frac{|\langle m^{(0)}|V|n^{(0)}\rangle|^2}
{E_n^{(0)}-E_m^{(0)}}.
$$

简并子空间扰动矩阵：

$$
W_{ab}=\langle a^{(0)}|V|b^{(0)}\rangle.
$$

## 含时微扰

展开态：

$$
|\psi(t)\rangle=\sum_n c_n(t)e^{-iE_nt/\hbar}|n\rangle.
$$

系数方程：

$$
i\hbar\dot c_m(t)=\sum_n V_{mn}(t)c_n(t)e^{i\omega_{mn}t}.
$$

一阶跃迁振幅：

$$
c_f^{(1)}(t)=
-\frac{i}{\hbar}\int_0^t dt'\,
V_{fi}(t')e^{i\omega_{fi}t'}.
$$

跃迁概率：

$$
P_{i\to f}=|c_f|^2.
$$

共振条件：

$$
\hbar\omega\approx E_f-E_i.
$$

Fermi 黄金规则：

$$
\Gamma=\frac{2\pi}{\hbar}|V_{fi}|^2\rho(E_f).
$$

## 散射理论

远场波函数：

$$
\psi(\mathbf r)\sim e^{ikz}+f(\theta,\phi)\frac{e^{ikr}}{r}.
$$

微分截面：

$$
\frac{d\sigma}{d\Omega}=|f(\theta,\phi)|^2.
$$

Born 近似：

$$
f_{\text{Born}}(\mathbf q)=
-\frac{m}{2\pi\hbar^2}
\int d^3r\,e^{-i\mathbf q\cdot\mathbf r}V(\mathbf r).
$$

动量转移：

$$
\mathbf q=\mathbf k'-\mathbf k,
\qquad
q=2k\sin\frac{\theta}{2}.
$$

分波振幅：

$$
f(\theta)=
\frac{1}{k}\sum_{l=0}^{\infty}
(2l+1)e^{i\delta_l}\sin\delta_l\,P_l(\cos\theta).
$$

分波总截面：

$$
\sigma=\frac{4\pi}{k^2}\sum_{l=0}^{\infty}(2l+1)\sin^2\delta_l.
$$

## Dirac 方程

相对论能量关系：

$$
E^2=p^2c^2+m^2c^4.
$$

Dirac Hamiltonian：

$$
H_D=c\boldsymbol{\alpha}\cdot\mathbf p+\beta mc^2.
$$

Dirac 方程：

$$
i\hbar\frac{\partial\psi}{\partial t}=H_D\psi.
$$

反对易关系：

$$
\{\alpha_i,\alpha_j\}=2\delta_{ij}I,
\qquad
\{\alpha_i,\beta\}=0,
\qquad
\beta^2=I.
$$

gamma 矩阵：

$$
\{\gamma^\mu,\gamma^\nu\}=2g^{\mu\nu}I.
$$

非相对论展开：

$$
E\approx mc^2+\frac{p^2}{2m}.
$$

Pauli 型 Hamiltonian：

$$
H_{\text{Pauli}}=
\frac{1}{2m}(\mathbf p-q\mathbf A)^2+q\phi
-\frac{q\hbar}{2m}\boldsymbol{\sigma}\cdot\mathbf B.
$$

## 路径积分进阶

含源生成泛函：

$$
Z[J]=
\int\mathcal D x\,
\exp\left[
\frac{i}{\hbar}
\left(S[x]+\int dt\,J(t)x(t)\right)
\right].
$$

源导数生成关联函数：

$$
\left.
\frac{\delta^2Z[J]}{\delta J(t_1)\delta J(t_2)}
\right|_{J=0}
\propto
\langle x(t_1)x(t_2)\rangle.
$$

作用量拆分：

$$
S=S_0+S_{\text{int}}.
$$

相互作用展开：

$$
e^{\frac{i}{\hbar}S_{\text{int}}}
=
1+\frac{i}{\hbar}S_{\text{int}}
+\frac{1}{2!}\left(\frac{i}{\hbar}S_{\text{int}}\right)^2+\cdots.
$$

Wick 转动：

$$
t=-i\tau,
\qquad
e^{iS/\hbar}\to e^{-S_E/\hbar}.
$$

场论路径积分入口：

$$
Z=\int\mathcal D\phi\,e^{iS[\phi]/\hbar}.
$$
