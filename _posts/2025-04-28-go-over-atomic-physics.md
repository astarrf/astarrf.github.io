---
math: true  # enable math mode
title: Go over Atomic Physics(Chris. Foot)
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [physics,note,en]     # TAG names should always be lowercase
---
# Introduction
To better understand what happens in an ion trap, how we manipulate the ions and what **can** we manipulate in the ions, we need to dive deeper into the atomic physics. Though the book is for undergrad level, taking another look at it help us learn how everything works here, as well as some new insights in using those ions to implement real quantum computation.

Here I am going to write down the note I think valuable during the reading. I try to use an easy language so that I hope even undergrads in not only physics but also other STEM majors can learn from it easily.

# Early atomic physics
In this stage, people had no idea of the internal structure of an atom. However, with increasing experiments, hypnosis were proposed, checked and moved on.
## Experiment 1: Spectrum of Hydrogen
We can use prism to get the spectrum of a beam of light. As the rainbow extends, the wavelength can be measured. Thus, Rydberg found the spectral lines in Hydrogen follows:
$$\frac{1}{\lambda}=R(\frac{1}{n^2}-\frac{1}{m^2}),\ m\ge n, 
 \ m,n \text{ are integers}$$
The wavenumber, denoted as $\tilde{\nu}=\frac{1}{\lambda}$, is useful in atomic physics, with the unit cm$^{-1}$ or m$^{-1}$.

Here are some good results with the expression of wavenumber:
$$E=hc\tilde{\nu},\ \tilde{\nu}_n^m=\tilde{\nu}_n^k+\tilde{\nu}_k^m$$
where the $\tilde{\nu}_i^j$ means the wavenumber from $n=i$ to $m=j$.
![energy level of H atom](/assets/img/go-over-atomic-physics/energy_level_of_H.png)
## Hypnosis 1: Bohr's theory
It's obvious if you guess according to the form of the wavelength formula that, the $n$ and $m$ are related to some level of energy inside the atom. Plus, due to some unknown reason (we will mention it later), the energy is not continuous, but level by level with some specific energy. So here we just move on to the classic model and see what kind of 'quantized' condition can be added to solve the problem.

With the Coulomb attraction of the nucleus, we can get
$$\frac{m_ev^2}{r}=\frac{e^2}{4\pi\epsilon_0r^2}$$
therefore the angular velocity is 
$$\omega^2=\left(\frac{v}{r}\right)^2=\frac{e^2/4\pi\epsilon_0}{m_er^3}$$
and the energy of the electron
$$E_e=\frac{1}{2}m_ev^2-\frac{e^2/4\pi\epsilon_0}{r}=-\frac{e^2/4\pi\epsilon_0}{2r}$$
which is negative because the nucleu is attracting the electron, so it needs extra energy to get to the free space.

### Assumption: quantisation of angular momentum
$$m_evr=n\hbar$$

