---
math: true  # enable math mode
title: Notes for Semiconductor Physics
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [physics,note,en,cn]     # TAG names should always be lowercase
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
![金刚石型](/assets/img/Semiconductor-Physics/金刚石型.png)
- 闪锌矿型(绝大部分III-V化合物+部分II-VI化合物)(共价键+离子键$\rightarrow$极性半导体)
![闪锌矿型](/assets/img/Semiconductor-Physics/闪锌矿型.png)
- 纤锌矿型(部分III-V化合物，典型III-N)(六方对称性)
![纤锌矿型](/assets/img/Semiconductor-Physics/纤锌矿型.png)
- 氯化钠型(IV-VI化合物)
![氯化钠型](/assets/img/Semiconductor-Physics/氯化钠型.png)

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

# 半导体中载流子的统计分布
## 状态密度
$g(E)=\frac{dZ}{dE}$
椭球型等能面(a,b,c)
$a=b=\sqrt{2m_t(E-E_c)/\hbar}$
$c=\cdots$
## 费⽶能级和载流子的统计分布
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
检查10.28录像，有要记的。
## 杂质半导体的载流子浓度

## 简并半导体
对于n型半导体：
- 一般情况：$N_D<N_c\implies E_F<E_c$费米能级在禁带
- 提高掺杂能级：$N_D\ge N_c\implies E_F\ge E_c$费米能级在导带
$$\begin{cases}E_\mathrm{c}-E_\mathrm{F}>2k_0T&\text{非简并}\\0<E_\mathrm{c}-E_\mathrm{F}\leqslant2k_0T&\text{弱简并}\\E_\mathrm{c}-E_\mathrm{F}\leqslant0&\text{简并}\end{cases}$$

# 半导体的导电性
- 迁移率
- 散射机制
- 迁移率、电阻率和温度的关系
- 强电场效应、热载流子、自由载流子

晶格振动的散射
- 声学波
- 光学波

方阻(sheet resistance)：$R_s=4.54\frac{V}{I}(\text{Ohm} / \square)$

本征半导体温度上升，电阻率迅速下降

对杂质半导体,有杂质电离和本征激发两个因素存在,
⼜有电离杂质散射和晶格散射两种散射机构的存在,因⽽电
阻率随温度的变化关系要复杂些,图砼16示意性地表示⼀
定杂质浓度的硅样品的电阻率和温度的关系,曲线⼤致分为
三段。

AB段 :温度很低,本征激发可忽略,载流⼦主要由杂质电离提供,它的浓度随温度的升⾼⽽增
⼤;散射主要由电离杂质决定,迁移率也随温度的升⾼⽽增⼤,所以,电阻率随温度的升⾼⽽减⼩。

BC段 :温度继续升⾼(包括室温),杂质已全部电离,本征激发还不⼗分显著,载流⼦基本
上不随温度变化,晶格振动散射上升为主要⽭盾,迁移率随温度的升⾼⽽减⼩,所以,电阻率随
温度的升⾼⽽增⼤。

C段 :温度继续升⾼,本征激发很快增加,⼤量本征载流⼦的产⽣远远超过迁移率减⼩对
电阻率的影响,这时,本征激发成为⽭盾的主要⽅⾯,杂质半导体的电阻率将随温度的升⾼⽽
急剧地减⼩,表现出同本征半导体相似的特征。![金刚石型](/assets/img/Semiconductor-Physics/rhoT.png)

## 强电场下的效应 、热载流⼦
电场不太强时,电流密度与电场强度关系服从欧姆定律,即$J=\sigma E$

# 非平衡载流子
## 非平衡载流子的注⼊与复合
光/电注入
## 弛豫时间
产生率-复合率动态竞争

# PN结
## PN结以及能带图
- 合金法（单边突变结 $p^+n$）
- 扩散法（线性缓变结（低浓度）/突变结（高浓度））
