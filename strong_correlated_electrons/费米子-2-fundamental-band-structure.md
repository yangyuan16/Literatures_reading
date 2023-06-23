# band structure
## 简介：
> tight-binding model可以描述一大类绝缘体，求解这一类系统还可以采用一些数值方法
> computer package or Mathematica which allow us to set up some simple systems
> for actually I'll look at a class of 1d system. Just diagnolize these systems look at
> the eigenvalues, look at the wave functions look at the spectral properties and so on.
> 如果考虑周期性，就可以采用Fourier transformation as a sepcific type of canonical transformation (是一类特殊的正则变换，来对角化哈密顿量)
> to diagonalize the Hamiltonian and 在布里渊区描述本征态和本征能量。
> if we have a single site per unit cell we have a single band (如果一个元胞中只有一个点，那就只有一条能带)
> if we have two-cycle unit cell already we have two bands (如果是一个two-cyle的元胞，那么就会有两条能带)
> 这就可能会出现绝缘体或者金属。

## 求解 tight-binding model
采用Fourier transformation 来对角化哈密顿矩阵：

$$ H = \sum_{i,j}t_{ij}c_i^{\dagger}c_j$$

如果 $i=j$, $t_{ij} = \epsilon_i$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_1.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_2.png)

## 考虑一些toy models, 

**（1）1d tight binding model:**

**这是一个单带模型（sing band model）, 因为一个元胞里面只有一个orbital**

**（2）SSH model (su-schrieher-Heeger model)**

**Alternating tunnelling elements so t1 t2 t1 t2 on the chain(这样的系统中，一个元胞就会包含两个orbitals)**
**所以这就是一个two band system 两能带系统**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_3.png)

对于SSH model, 这里 i label the unit cell, and a, b label the sites in unit cell. 
注意在 SSH model 中，tunneling term 中包括元胞与元胞之间的 tunneling. 

## 模型-1的数值严格解：

**需要写出以费米子产生湮灭算符为基矢量的 T 矩阵。**
通过分析能带结构会发现，模型1显然是一个金属，模型二是一个 band insulator. 

**模型-1的矩阵形式**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_4.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_5.png)

**模型-1的本征能量**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_6.png)

**模型-1的本征态**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_7.png)

**将系统扩展为100个原子**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_8.png)

会发现：the energies of the system take a particular form and the most important thing to note about this is that the 
energies are bounded so even I have a hundred sites in this system the energy only fall into this window between miuns 1 
and plus 1.  between -1 to +1, there is actually a sort of band energies and if given energy I'm might find a particular
state. In particular, if I were to go to the infinite size system in the continuum this line would instead of being discrete 
points a hundred different points for a hundred different sites, I would see a whole continum line and at any given energy
I would find a particular density of states. Outside the band, I have zero density of states. 
(系统的能量有一种特殊的形式，最重要的是要注意，能量是有界的，所以即使我在这个系统中有一百个位置，能量也只落在miun1和+1之间的这个窗口中。
在-1到+1之间，实际上有一种能带能量，如果给定能量，我可能会找到一个特定的状态。特别是，如果我去到连续体中的无限大系统，
这条线将不是离散点，而是一百个不同位置的一百个不同点，**我将看到一条完整的连续线，在任何给定的能量下，我将找到一个特定的态密度**。
**在带外，我的态密度为零**。)

**plot the wave function, 将波函数画出来**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_9.png)

（纵坐标是波函数系数的平方）
It loos a bit like particle in a box. the wave function has this sort of smooth continuous from it strongly peaked in 
the middle of the box which tells you that there's a large probability amplitude for the particle to be found and for 
the particles to be found in the middle of the box and there are sort of boundary conditions such that's the wave function
vanishes at the walls. again If go to an infinite sized system, it would be see that this wave function was totally
delocalied over the whole system subject to these boundary conditions of the vanishing wave function.
(它有点像盒子里的颗粒。波函数具有这种光滑的连续性，它在盒子的中间强烈地达到峰值，这告诉你，粒子被发现的概率振幅很大，
粒子被找到的概率振幅也很大，并且有一些边界条件，比如波函数在墙壁上消失。同样，如果去一个无限大的系统，
可以看到，在消失波函数的这些边界条件下，这个波函数在整个系统上是完全非局域的。)

**看看其他的波函数的情况:**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_10.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_11.png)

这些都是激发态的波函数。

## SSH 模型的数值严格解

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_12.png)
