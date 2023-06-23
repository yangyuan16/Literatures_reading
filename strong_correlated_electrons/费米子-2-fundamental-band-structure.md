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

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_13.png)

这里画出来的是 two different scenarios we imageine a chain that stats with $t_1$ on the left hand side and stats 
with $t_2$ on the right hand side. So we image a chain a 1d chain that goes "t_1, t_2, t_1, t_2 ..." and so on. 
(左边这幅图的结果是t相互作用排序为"t_1, t_2, t_1, t_2 ...", 也就是从 t_1 开始)， 右边这幅图的刚好相反，t 相互作用的排序是
“t_2, t_1, t_2, t_1,...”, 也就是从 t_2 开始。**t_1 是元胞内的tunneling项, t_2是元胞之间的 tunneling项**

**这两个子图都是考虑 t_2 等于 0 的情况**，
t_2 = 0, it dimerize the whole system. (t_2 = 0 的时候，整个系统 dimerized). 考虑100个格点，分成50个元胞,
由于 t_2 等于 0， I just have 25 sort of dimerized paries which decoupled from each other and each dimer has an 
energy one of the site, one of the eigenstates as energy of -1, the other one has an eigen state energy of +1.
So I just have 25 values -1 and 25 values of +1. 

对于右边子图的情况，几乎和左边子图的情况是一致的，except for the situation at the end of chain. At the end of the chain, 
because I start with a t_2 bond and t_2 = 0, that I just have an isolated orbitals that not coupled to anything at 
the end of the chain and therefor that just has zero energy because the $\epsilon = 0$, so I have 24 pairs of dimers with 
two sites left over one each at end of the chain and therefor you see that in the middle of the spectrum here I have
just these two sites sitting exactly a zero energy and they site in an eigen energy gap, on the left hand side and on 
the right hand side, you see that there a big gap where there's basically no density of any states between -1 and +1.
(因为我从t_2键开始，t_2=0，我有一个孤立的轨道，它没有耦合到链末端的任何东西，**因此它的能量为零，因为**$\epsilon=0$，
我有24对二聚体，链的末端各有一个位点，剩下两个位点，所以你可以看到，**在能谱的中间，这两个位点正好处于零能量**，
它们位于本征能隙中，你可以看到有一个很大的能隙，在-1和+1之间，基本上没有任何态的密度。)

**将 t_2 从零调整到非零**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_14.png)

**观察能隙：随着 t_2 的增加，能隙在减小**, in both the system here the gap has now been reduced to -0.5 to 0.5, 
but one of the interesting things is that's the on the right hand side, I still see two states sitting exactly to 
zero energy and this is rather interesting because they're actually now coupled into rest of the system with a finite
t_2, but yet still they appear to have zero energy. On the left-hand side even though all the sites coupled in together
to each other we see there are no such states sitting at zero energy and there's still a pristine gap in the spectrum. 
(在这两个系统中，间隙现在都减少到了-0.5-0.5，但有趣的是，在右边，**我仍然看到两个状态正好处于零能量**，
**这很有趣，因为它们实际上以有限的 t2 耦合到系统的其他部分，但它们看起来仍然是零能量**。
在左手边，尽管所有的位置都耦合在一起，但我们看到没有这样的状态处于零能量，光谱中仍然存在原始的差距。)

**不断的增加t_2来关闭能隙**，

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_15.png)

As I increase the T to further, I can close the gap, now I have a homogeneous system when t_1 is equal to t_2,
this is the metallic system we looked at before. We don't have a unit cell of two sites now, everything just looks exactly
the same as I go down the chain and I have a cosine type of behavior of the eigen energies. 

**继续增大 t_2, 能隙又会打开**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_16.png)

**观察最低能量对应的本征态**

**\Dealt t >0 的情况**

$\Delta t = t_1 - t_2$, 当 $\Delta t > 0$ 时, 
lowest energy states and surely the ones around the Fermi energy expanded in the basis of physical real space sites on the chain.
(最低能态就是费米能级附近的态。)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_17.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_18.png)

这里画的是最低能量的两个态，我们可以看到在有能隙的相中，这里有两个不同的非局域的波函数， the electrons are 
propagating on the chain, they are delocalized and they look like regular kind of particle in a box type states
(电子在链上传播，它们是非局域的，看起来像盒子状态下的规则粒子). These are the lowest energy states living sort of at the
gap edge. 

**\Dealt t < 0 的情况**

$\Delta t = t_1 - t_2$, 当 $\Delta t < 0$ 时,

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_19.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_20.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_21.png)

However if I make the $\Delta t$ negative, as I make the $\Delta t$ smaller and smaller and smaller, these 
states become exponetially localized at the edge of the system. So these zero energy states in one of the phases 
are not delocalized throughout the system, these ones sitting right in the middle of the spectrum there. They are
actually exponetially well localized at the edge of the system and of course in the dimerize limit when $t_2$ is equal to 
zero (t_2 = 0), we expect indeed that there are these pristine zero energy states perfectly localized. The energy thing is 
here even when t_2 is finite and those states are coupled into the rest of the system, they are exponentially low in the 
energy and they are exponentially well localized

(然而，如果我使$\Delta t$为负，就像我使$\Delta t$越小越小一样，
**这些状态会在系统的边缘明显地局部化**。
因此，其中一个相中的这些零能态在整个系统中都都是局域的，零能态位于能谱中间，
它们实际上在系统的边缘被很好地局部化。
当然在二聚极限中，当$t_2$等于零（t_2=0）时，
我们确实期望存在这些完全局部化的原始零能态。
问题是这里，即使t2是有限的，并且这些状态耦合到系统的其余部分，
它们的能量也是指数低的，并且它们是指数良好的局部化)

> 推论: 如果能谱上有零能，对应的基态波函数会出现局域。

## Diagonalize the periodic systems by a Fourier transform  傅里叶变换求解系统

it is important for these systems have a translational symmetry of periodicity to the lattice. 

**考虑最简单的情况，1d wire again**

$$H = \sum_{x=-\inf}^{\inf} t(c_x^{+}c_{x+1} + c_{x+1}^{+}c_{k})$$

**对算符进行Fourier transformation**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_22.png)

$$c_x = \frac{1}{\sqrt{N}} \sum_{k} e^{i k a_{0}} c_k$$

N is the number of the unit cells, k is the momentum , $a_0$ is the lattice constant. 

**同样也可以做 inverse Fourier transformation**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_23.png)

**验证 Fourier transformation is canonical transformation**

canonical transformation means that the 费米子的反对易关系不会发生变化

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_24.png)

**将上面的Fourier 变换带入到hamitonian 中**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_25.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_26.png)

可以推出来 哈密顿为： 

$$H = \sum_{k} \epsilon_{k} c_k^{\dagger} c_k$$

$$\epsilon_k = t (e^{ika_0} + e^{-ika_0}) = 2tcos(ka_0)$$ 

称为 “色散关系” diperision relation. 

如果哈密顿是平移对称不变的，那么动量 K 就是一个守恒量 （**从哈密顿最终可以写成动量的对角形式就可以看出来**）

### 考虑单粒子态

在实空间的单粒子态并不是哈密顿的本征态，

**对比单粒子态和单粒子本征态**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_27.png)

you see that therefore there are these sort of oscillating patterns of these
real space basis orbitals X and if I want to know the probability to find an 
electron with immense K at a given real space position X then I just have to 
take the square of this coefficient. 你会发现所有的概率都是 $\frac{1}{N}$, 也就是
there are equal probability of finding the electron at any given sites in their 
system, the electron are totally delocalized over the whold system.
So, the electrons are really spread out over the whole system in the eigenstates. 
and therefor this is certainly a metal, because the electron are totally delocalized.
Also noted that all different momenta are basically equivalent in terms of where you can 
find the electrons what the probability density is and if we look at the structure of these states,
there is a phase information. It is really this phase information is a complex number, so, there 
are some phase information that depends on both the position and the momentum is basically capturing 
all of the quantum mechanical information. This would give rise to possibilities for example quantum 
interference and all the other good stuff. But in terms of probability density, the electrons are totally 
delocalized and equivalent and this is basically related to Bloch's theorem. 
(你看，这些实空间基轨道X有这些振荡模式，如果我想知道在给定的实空间位置X上有巨大K的电子，
那么我只需要取这个系数的平方。你会发现所有的概率都是 $\frac{1}{N}$，也就是 
在**它们的系统中的任何给定位置找到电子的概率都是相等的，电子在整个系统中都是完全离域的**。
**所以，电子在本征态中真的分布在整个系统上。因此，这肯定是一种金属，因为电子是完全非局域的**。
还注意到，所有不同的动量基本上是相等的，在哪里可以找到电子，概率密度是多少，如果我们看看这些态的结构，
存在相位信息。实际上，这个相位信息是一个复数，
所以，有一些相位信息取决于位置和动量，基本上捕获了所有的量子力学信息。
这将产生各种可能性，例如量子干涉和所有其他好东西。
但就概率密度而言，电子是完全离域和等价的，这基本上与布洛赫定理有关。)


## 傅里叶变换求解元胞中包含多个轨道的系统

