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

**1d 的情况**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_28.png)

**2d 的情况**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_29.png)


$a_{cc}$ is the constant distance, which is the nearest neighbor between the carbon atoms of this graphene lattice 
and the vector itself is 

$$
\vec{a_1} = \sqrt{3}a_{cc} 
\left [
\begin{array}{c}
\sqrt{3}/2 \\
1/2\\
0\\
\end{array}
\right]
$$

$$
\vec{a_2} = \sqrt{3}a_{cc} 
\left [
\begin{array}{c}
\sqrt{3}/2 \\
-1/2\\
0\\
\end{array}
\right]
$$

**2d super unit cell (超胞)**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_30.png)

The question is what is the Hamiltonian for such system? (这样的系统的哈密顿量该如何写呢?)

For a unit cell located at position $\vec{r} = (x,y)$, 

$$H_{x,y} = \vec{C}_{xy}^{+} M \vec{C}_{xy}$$

There will be some matrix M which tell us about what's going on inside the unit cell
so we have L. if we have L degree of freedom, this will be a L by L matrix. Notice that this 
matrix M does not have X&Y labels, why is that? That is beacuse the unit cell is a repeating unit and it's 
the same Hamiltonian describing this unit as any other unit cell on the lattice. It's always the same because that's 
the whole point we copy the unit cell and shifted. So it doesn't have any XY dependence itself. So let's just write 
down what these various things in the Hamiltonian.(会有一些矩阵M告诉我们晶胞内部发生了什么，所以我们有L。
如果我们有L的自由度，这将是一个L乘L的矩阵。请注意，这个矩阵M没有X和Y标签，为什么是这样？
这是因为晶胞是一个重复单元，它与晶格上的任何其他晶胞都是相同的哈密顿量。它总是一样的，
因为这就是我们复制单元并移动的全部点。所以它本身没有任何XY依赖性。所以我们就写吧把哈密顿量中的各种各样的东西都记下来。) 

**先构建超包内的哈密顿量**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_31.png)

Let's see that, 我们可以构建 C 算符的矢量，that is 

$$
\vec{C}_{xy} =  
\left [
\begin{array}{c}
\vec{C}_{xy, 1} \\
\vec{C}_{xy, 2}\\
\vec{C}_{xy, 3}\\
\vdots\\
\end{array}
\right]
$$

**再构建整个系统的哈密顿量**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_32.png)


**采用傅里叶变换来求解这样的具有超包的 2d lattice model**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_33.png)

带有M矩阵的第一项描述在超包内的interations, 带有 P 矩阵的第二项和第三项描述在X轴方向的胞间tunneling,
带有 Q 矩阵的第四第五项描述 Y 轴方向的胞间 tunneling.
注意上面在做傅里叶变换的时候，先在X轴的方向做了傅里叶变换。Y 轴上没有做傅里叶变换，因此是一个混合基底。

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_34.png)

**值得注意的是，我们可以看到，当通过变换到K空间的时候:**

$$C_{x,y}^{\dagger}C_{x+1,y} \rightarrow C_{k_{x},y}^{\dagger}C_{k_{x},y}e^{-ik_{x}}$$

原本在晶格空间中的**非对角项 变换到了k空间的对角项**, **同时多出了一个相位** $e^{-ik_{x}}$. 

合并对角项，注意此时，哈密顿中带有Q矩阵的项仍然存在非对角项目：

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_35.png)

在 Y 轴方向上进行傅里叶变换，采用 delta 函数的性质 得到整个系统的对角形式：

到目前为止我们还没有真正的得到Hamitonian矩阵，因为E矩阵不是对角的。我们需要对E矩阵进行对角化处理。
E 矩阵的大小为 L by L, L 是超包内的轨道自由度，也就是超胞内的不同轨道的数目，超包内格点的数目。

对 E 矩阵分别进行对角化处理，when I do that, it will tell me about all the different energy bands in the 
system and I'll L different energy bands for L different eigen values, and those bands will depends on 
Kx and Ky, so when I diagnolize E I will L different eigen values, which depends on Kx and Ky, and they are the 
bands of our system and each of then has their own dispersion relation, each band will have a different 
dispersion relation, which tells me how the energy of that bands corresponds to the momentum of Kx and Ky, 
and for different bands that relation will be different. (当我这样做的时候，它会告诉我系统中所有不同的能带，
**对于L个不同的本征值，我会得到L个不同能带，这些能带取决于Kx和Ky**，
**所以当我诊断E时，我会得出L个不同本征值。这取决于Kx和Ky**。
**它们是我们系统的能带。每个能带都有自己的色散关系**，
**每个带都有不同的色散关系**，
**这告诉了我这些带的能量是如何对应于Kx和Ky的动量的，对于不同的带，这种关系是不同的**。)

### 如何对角化 E 呢？

$$H = \sum_{k_x, k_y} C_{k_x,k_y}^{+} E C_{k_x, k_y}$$

$$ E(k_x,k_y) = M + P e^{-ik_x} + P^{+} e^{ik_x} + Q e^{-ik_y} + Q^{+}e^{ik_y} $$

diagonalize E really depends on what these matrix M, P, and Q. that in the end is telling us about the geometry of 
our actual underlying quantum system. I can image even a simple square lattice of individual atoms but each atom in reality
has more than one electrom we're not talking about a lattice of hydrogen atoms so in a real system even a square lattice 
would involve many atomic orbitals on each atom and each of those atomic orbitals has some energy in some its coupling
neighboring atoms and so on. 
(对角化E实际上取决于这些矩阵M、P和Q，它们最终告诉我们实际底层量子系统的几何结构。我甚至可以想象一个简单的单个原子的正方形晶格，
但实际上每个原子都有不止一个电子，我们不是在谈论氢原子的晶格，所以在真实的系统中，
即使是正方形晶格也会涉及每个原子上的许多原子轨道，这些原子轨道中的每一个在其耦合的相邻原子中都有一些能量，等等。)

So in real system you do have many electrons per unit cell and you do there for have many bands. The relation between 
the energy of each band and momentum is exactly the information contained in the band structure 
(所以在真实的系统中，每个晶胞中确实有很多电子，而且有很多能带。每个能带的能量和动量之间的关系正是包含在能带结构中的信息)

To understand the band structure of our solid material from the fundamental model we need to do one final step 
we need to another canonical transformation of our C operators:

$$ \vec{C}_{k_x, k_y} = U(k_x,k_y)\vec{F}_{k_x,k_y}$$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_36.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_37.png)

What is the energy bands means? it is the eigenstates of the system as a function of momentum. There is the 
L bands in total. L is the number of degrees of freedom in the unit cell, so there are the same number of bands
in the solid as there are degrees of freedom in the repeating unit cell of the lattice.
$\epsilon_p{k_x,k_y}$ here is the dispersion of each band. So, for each P labeling the band, I can now work out or 
I now know what the energy momentum relation is.
 
 
## 用每个超包中有5个轨道来举例说明

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_38.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_39.png)

This is basically a metallic system because if I look at any particular energy, for example, set the Fermi level here
then as I go across in momentum space, I see that several bands across this Fermi energy maybe even the same 
band several times and this gives me an overall density of states at the fermi energy and that means the system is a metal. 
(这基本上是一个金属系统，因为如果我观察任何特定的能量，例如，在这里设置费米能级，当我在动量空间中穿过时，
我看到穿过这个费米能量的几个能带，
甚至可能是同一个能带好几次，这给了我在费米能量下的整体态密度，这意味着这个系统是一种金属。)

**再画一个绝缘体**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/band-structure/hamitonian_40.png)

I could image a certain band structure that has a gap in the bands. There are no
bands cross the Fermi energy at any momentum and therefor when I sum over all the momentum there 
are no density of states at Fermi energy and therefor this system would be an insulator.
I would cost a finite amount of energy to promote an electron across the gap and indeed we can identify 
what the minimum gap is. we can see this particular momentum there is a particular energy gap $\Delta E$
over here. 

