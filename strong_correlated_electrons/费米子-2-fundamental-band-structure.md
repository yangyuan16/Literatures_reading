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

