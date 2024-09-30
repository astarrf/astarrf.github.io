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
