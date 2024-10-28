---
math: true  # enable math mode
title: Notes for Semiconducting Physics
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [physics,note,en]     # TAG names should always be lowercase
---
# Introduction
- semiconductor lumination
- semiconductor power generation
- diode/triode
- Conductivity: conductor, semiconductor, insulator
- C, Si, Ge
- Al, Ga, In
- N, P, As, Sb
- O, S, Se, Te
- Si, GaAs, GaN

## history
### birthday of semiconductor
Jan. 1946, Schokely, Bardeen and Brattain build the very first triode.
### invention of integrated circuit
Sept. 1958, research group leaded by Kilby in TI invented the first IC.

## terms
doping (掺杂)

# State of Electrons in Semiconductor
固体分类：晶体；非晶体
晶体：单晶体；多晶体($10^{-4}\sim10^{-6}$m范围内是周期性排列的)

求解：单电子近似$\rightarrow$能带论

晶体结构基本构型：简立方；体心立方；面心立方。

常见晶体结构：
- 金刚石型(IV)
![金刚石型](/assets/img/Semiconducting-Physics/金刚石型.png)
- 闪锌矿型(绝大部分III-V化合物+部分II-VI化合物)(共价键+离子键$\rightarrow$极性半导体)
![闪锌矿型](/assets/img/Semiconducting-Physics/闪锌矿型.png)
- 纤锌矿型(部分III-V化合物，典型III-N)(六方对称性)
![纤锌矿型](/assets/img/Semiconducting-Physics/纤锌矿型.png)
- 氯化钠型(IV-VI化合物)
![氯化钠型](/assets/img/Semiconducting-Physics/氯化钠型.png)

## 半导体中的电子状态和能带
- 自由电子运动
- Bloch势中的薛定谔方程
  $$-\frac{\hbar^2}{2m}\frac{d^2\psi(x)}{dx^2}+V(x)\psi(x)=E\psi(x)$$
  $$\psi_k(x)=u_k(x)e^{ikx}, \ u_k(x)=u_k(x+na)$$
- 氢原子模型采用Bohr模型
$$\frac{q^2}{4\pi\varepsilon_0}\frac{1}{r^2} = m_e\frac{v^2}{r}$$
轨道量子化:
$$m_e vr=\frac{nh}{2\pi}, n=1,2, \cdots$$
解得波尔能级：
$$E_n=\frac{E_1}{n^2}, E_1=-\frac{me^4}{8\varepsilon_0^2h^2}$$

### 禁带、导带
- 导体: 导带没有被电子填满
- 绝缘体： 导带被电子填满，且禁带>3eV
- 半导体： 导带被电子填满，且禁带1-3eV


## 掺杂
### IV族
III族 $\to$ P型
V族  $\to$ N型

浅能级杂质=杂质离子+束缚电子/空穴

用类氢原子模型分析：
$$\Delta E_\mathrm{D}=\frac{m_\mathrm{n}^*q^4}{2(4\pi\varepsilon_0\varepsilon_\mathrm{r})^2\hbar^2}=\frac{m_\mathrm{n}^*}{m_0}\frac{E_0}{\varepsilon_\mathrm{r}^2}$$
$$\Delta E_\mathrm{A}=\frac{m_\mathrm{p}^*q^4}{2(4\pi\varepsilon_0\varepsilon_\mathrm{r})^2\hbar^2}=\frac{m_\mathrm{p}^*}{m_0}\frac{E_0}{\varepsilon_\mathrm{r}^2}$$

> 这个公式没有反应不同杂质的区别
{: .prompt-warning}

补偿效应：可以通过高浓度的N型补偿低浓度的P型，使他从P变成N，反之亦然。
> 注意两者恰好补偿时会导致半导体性能变差，所以一般不会使用。
{: .prompt-warning}

深能级杂质
非常复杂，不好控制，一般不使用。


### III-V族化合物的杂质能级
II族通常是替位式，引入浅受主能级，VI族通常引入施主能级（可能深可能浅）
IV族都可以替代。

4纤锌矿结构
GaN：硅、氮空位起浅施主杂质作用（N）
     Mg，Zn起深受主杂质作用（P）难掺杂

AlN: C、N深施主
     Zn、Mg深受主
     非常难掺杂

### 缺陷、位错能级
金属-半导体接触；功函数
欧姆接触
肖特基接触

掺杂方法：高温扩散、离子注入

# 半导体中载流⼦的统计分布
## 状态密度
$g(E)=\frac{dZ}{dE}$
椭球型等能面(a,b,c)
$a=b=\sqrt{2m_t(E-E_c)/\hbar}$
$c=\cdots$
## 费⽶能级和载流⼦的统计分布
$f(E)=\frac{1}{1+exp(\frac{E-E_F}{k_0T})}$
$$
n_{0}= 2\left(\frac{m_\mathrm{n}^* k_0 T}{2\pi\hbar^2}\right)^{3/2}\exp\left(-\frac{E_\mathrm{c} - E_\mathrm{F}}{k_0 T}\right) $$
$$N_{\mathrm{c}}= 2\left(\frac{m_\mathrm{n}^*k_0T}{2\pi\hbar^2}\right)^{3/2}=2\frac{(2\pi m_\mathrm{n}^*k_0T)^{3/2}}{h^3}$$
$$n_0=N_\mathrm{c}\exp\left(-\frac{E_\mathrm{c}-E_\mathrm{F}}{k_0T}\right) $$
$$p_0=2\left(\frac{m_\mathrm{p}^*k_0T}{2\pi\hbar^2}\right)^{3/2}\exp\left(\frac{E_\mathrm{v}-E_\mathrm{F}}{k_0T}\right)$$
$$N_\mathrm{v}=2\left(\frac{m_\mathrm{p}^*k_0T}{2\pi\hbar^2}\right)^{3/2}=2\frac{(2\pi m_\mathrm{p}^*k_0T)^{3/2}}{h^3}$$
$$p_0=N_\mathrm{v}\exp\left(\frac{E_\mathrm{v}-E_\mathrm{F}}{k_0T}\right)$$
## 本征半导体的载流⼦浓度
$$E_\mathrm{i}=E_\mathrm{F}=\frac{E_\mathrm{c}+E_\mathrm{v}}2+\frac{3k_0T}4\mathrm{ln}\frac{m_\mathrm{p}^*}{m_\mathrm{n}^*}$$
| 材料 | $m_p^*/m_n^*$ |
| ---- | ------------- |
| Si   | 0.55          |
| Ge   | 0.52          |
| AsGa | 7             |
| InTe | 32            |
> P79-tab3.2
{: .prompt-tip}
## 杂质半导体的载流⼦浓度
