# Electron interations and the Hubbard model 
## 简介:
 For truly interating problems where the electrons see each other through the 
 Coulomb interation. This is not possible and we need to resort to much more sophisticated 
 techniques to the underlying physics. What are the underlying physics, for example, it is 
 possible to have an interaction driven transition between a metal and an insulator. called 
 Mott transition. We will discuss certain models of interacting fermions on the lattice, in 
 particulat the so-called Hubbard model which treats the Coulomb interation is very short-range
 it assumes that the interaction is dominant when you have electrons of opposite spin occupying the 
 same orbital in which case you have a strong repulsion otherwise the electrons do not interact with 
 each other at longer ranges. Although simplified, we will see that this model is highly complex but
 capture a wide range of physics including the Mott transition. We also see how in this model through 
 a simple mean field approximation and we can understand the concept and the phenomenon of itinerant
 magetism which is to say a metallic system that is also very magetically ordered. This is basically the 
 stoner model a fair amout. We'll also see through a simple perturbative approach to second-order in the 
 quantum tunneling between atomic orbitals on neighboring sites. How we can derive for the Heisenberg spin 
 model from the microscopic Hubbard model. 
 (对于真正的相互作用问题，其中电子通过库仑相互作用看到彼此，我们需要对基础物理采用更复杂的技术。
 例如，潜在的物理是什么，金属和绝缘体之间有可能发生相互作用驱动的转变。称为莫特过渡。
 我们将讨论晶格上相互作用费米子的某些模型，特别是所谓的哈伯德模型，**该模型认为库仑相互作用是非常短程的**，
 **它假设当相反自旋的电子占据同一轨道时，相互作用是主导的，在这种情况下，有很强的排斥力**，电子不会在更长的范围内相互作用。
 虽然简化了，但我们会看到，这个模型非常复杂，但涵盖了包括莫特跃迁在内的广泛物理。
 我们还看到，在这个模型中，通过简单的平均场近似，我们可以理解**巡回磁的概念和现象**，
 也就是说，一个金属系统也是非常有序的。这基本上是stoner模型的。
 我们还将通过一种简单的微扰方法来了解相邻位置上原子轨道之间的二阶量子隧穿。
 我们如何从微观哈伯德模型推导出海森堡自旋模型。)
 
 ## 考虑电子自旋
 
 ![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig1.png)
 
 There are may areas of physics where we do need to include electron spin. For example, if we want to describe magnetism,
 obviously we need to include electron spin, if we have ferromagnetic ordering or antiferromagnetic ordering, this some 
 thing to with the alignments of the electron spins, we need to include spin in order to able to describe at entire
 phenomena of magnetism in materials. Also, if we have materials that involve for the heavier elements, the coupling
 between the spin and the orbital angular momentum can be signigicant. So to capture the effect of spin orbit 
 coupling which can have dramatic effects and this has been something that'been in the literature recently in the 
 context of topological quantum matter. If we want to describe spin up orbit coupling, we need to think about 
 electron spin. Also, real materials of course have some amount of disorder at finit temperature, and they 
 arise in inevitably in any system and if those impurities (for exampke transition metal atoms or some other
 kind of element with a localized moment, then we can have the phenomenon of spin flip scattering, which can change 
 the property of materials).在物理学的某些领域，我们确实需要将电子自旋包括在内。
 例如，如果我们想描述磁性，显然我们需要包括电子自旋，如果我们有铁磁有序或反铁磁有序，这与电子自旋的排列有关，
 我们需要包括自旋，以便能够描述材料中磁性的整个现象。此外，**如果我们有涉及较重元素的材料，自旋和轨道角动量之间的耦合可能是重要的**。
 因此，**捕捉自旋-轨道耦合的影响，这可能会产生巨大的影响，最近在拓扑量子物质的背景下，这已经成为文献中的一件事**。
 如果我们想描述自旋-轨道耦合，我们需要考虑电子自旋。此外，真实材料在有限温度下当然会有一定程度的无序，
 它们在任何系统中都不可避免地会出现杂质（**例如过渡金属原子或其他具有局域矩的元素，那么我们可能会出现自旋翻转散射现象，这会改变材料的性质**）
 
 If we have Cooper pair of two electrons of opposite spin, they can form a spin-zero bosonic states, and those Copper
 paires can condense into a superconductor. To describe superconductivity again, we need to think about electron spin.
 Of course, there are many many examples, where we need to think about electron spin. One example we talk
 about in this lecture is the short-range part of the Coulomb interaction between electrons in solids.
 So the Coulomb interaction of course is the electrostatic interation between two negatively charged electron in a 
 material. Due to the Pauli principle, the dominat part of the Coulomb interaction is when the electron are very very
 close to each other, and the spin up and spin down seperately. That can only happen when the electrons occupy the same
 atomic orbital and they are opposite spin. So to describe the dominant part of the Coulomb interaction in the solids,
 we need to table account of the electron spin. In particular, if you only retain the local shortest range part of 
 the Coulomb interaction which is the interaction between opposite spins in the same quantum orbitals, we can account 
 for a vast range of physical effects to do with interactions between electrons, ofthen one doesn't need to include the 
 long range Coulomb interation to capture the essential physics, partly because of the screening of the interaction 
 due to quasi particles in material itsself. 如果我们有两个自旋相反的电子的库珀对，它们可以形成自旋为零的玻色子态，
 这些库珀对可以凝聚成超导体。为了再次描述超导性，我们需要考虑电子自旋。当然，有很多例子，我们需要考虑电子自旋。
 我们在这节课上讨论的一个例子是固体中电子之间库仑相互作用的短程部分。所以库仑相互作用当然是材料中两个带负电的电子之间的静电相互作用。
 由于泡利原理，库仑相互作用的主要部分是当电子彼此非常非常接近，并且自旋向上和向下分别旋转时。
 只有当电子占据相同的原子轨道并且自旋相反时，才会发生这种情况。因此，为了描述固体中库仑相互作用的主要部分，
 我们需要考虑电子自旋。特别是，如果你只保留库仑相互作用的局部最短范围部分，即
 相同量子轨道中相反自旋之间的相互作用，我们可以解释与电子之间的相互作用力有关的大量物理效应，
 通常**不需要包括长程库仑相互作用来捕捉基本物理，部分原因是由于材料本身中的准粒子对相互作用的屏蔽**。
 
 In factor, we can regard the spin as a quantum number of label our states. we can use the label Sigma to describe either 
 up or down electron spin states. 
 
 Fermionic operator with spin,  these operator act on the local Hilbert space. 
 
 $$\hat{c}_{i\sigma}^{+}, ~~~ \hat{c}_{i\sigma}$$ 
 
 $$|0>_{i\sigma}, ~~~ |1>_{i\sigma}$$,
 
 $$\hat{c}_{i\sigma}^{+}|0>_{i\sigma}=|1>_{i\sigma}$$
 
 $$\hat{c}_{i\sigma}|1>_{i\sigma}=|0>_{i\sigma}$$
 
 $$\{c_{i\sigma}, c_{j\sigma^\prime}^{+}\} = \delta_{ij}\delta{\sigma\sigma^\prime}$$
 
 ## Tight-binding-model with spin 
 
 ![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig3.png)
 
 ![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig4.png)
 
 We could imagine for example adding here a sigma dependence to these parameters $t_{ij}$ in which case we 
 could image a tunneling of electrons from site i to site j, but depends on the spin. If we look at the diagonal
 elements $t_{ii,\sigma}$, They are correspond to the single particle energies if they are different for up and 
 down spin. that is equivalent to a magnetic field on acting on that site, which lifts the degenercy between 
 up and down spin. (例如，我们可以想象在这里添加对这些参数$t_{ij}$的西格玛依赖性，
 在这种情况下，我们可以成像电子从位置i到位置j的隧穿，但取决于自旋。
 如果我们看对角线元素$t_{ii,\sigma}$，它们对应于单粒子能量，如果单粒子能量对于上下自旋不同。
 这相当于作用在该位置上的磁场，它打开了上下自旋之间的简并性。)
 
 > 再同一个轨道上，也就是对角项上，自旋上和自旋下对应的能量可以是不一样的。
 
 This is totally generic kind of quadratic type. 
 
 **加入自旋后会出现两条能带，一条是自旋向上的能带，一条是自旋向下的能带**。
 
 我们也可以考虑比较奇怪的一部分，那就是 spin orbit coupling (自旋-轨道耦合)
 自旋 $\sigma$在轨道 i 上面，自旋 $\sigma^{\prime}$ 在轨道 j 上面：
 
 $$H_{soc} = \sum_{i,j}\sum{\sigma,\sigma^{\prime}}\epsilon_{ij\sigma\sigma^{\prime}}C_{i\sigma}^{+}C_{j\sigma^{\prime}}$$
 
 if I have orbitals with orbital angular momentum L and spin $\sigma$ and the thing is conserved is the overall 
 angular momentum, which is the orbital angular momentum plus the spin electrons. 
 
 **具有SOC项的哈密顿的结构中，整体的spin 并不是一个守恒量了，守恒量是轨道角动量加自旋**，因此，做对角化处理的时候，不能写成
 求和 $\sum_{\sigma,}$ 的形式，因此这里用一个指标 $l$ 来标记。所有的轨道和自旋混合起来形成了混合的指标 $l$
 
 ## 考虑电子相互作用的模型

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig4.png)

$$\hat{H}_{int}=\sum{i,j,k,l} \sum{\sigma_1,\sigma_2, \sigma_3, \sigma_4} U_{i,j,k,l}^{\sigma_1\sigma_2\sigma_3\sigma_4}\hat{C}_{i\sigma_1}^{+}\hat{C}_{j\sigma_2}\hat{C}_{k\sigma_3}^{+}\hat{C}_{l\sigma_4}$$

> 在 tight-binding 项中，自旋量子数守恒要求 $\sigma_1 = \sigma_2$
> 在相互作用项中，自旋量子数守恒要求 $\sigma_1 + \sigma_3 = \sigma_2 + \sigma_4$

### Dominant interactions are density-density interaction:


It turns out the dominat interactiion are so-called density density interactions. They basically depends on the 
number of electrons in a particular orbital and the number of electrons in different orbital. Also, include their spin. 

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig5.png)

**这样的库伦相互作用称为长程相互作用，这个并不是最强的相互作用**，
**最强的相互是同一个轨道上，不同自旋的两个电子之间的相互作用，这个称之为短程的相互作用**
**库伦相互作用只包含短程的相互作用，就变成了 Hubbard 模型**

**Hubbard interaction only non-zero if a site is a doubly occupied**
**(只有当一个轨道上存在两个自旋相反的电子的时候,Hubbard相互作用是非零的)**

## Hubbard model 哈伯德模型

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig6.png)

Hubbard model 可以描述重费米子系统，Lanthanide materials (镧系材料), 
a variant on the Hubbard model called the periodic Anderson model captures very
well the properties of lanthanide materials, which give rise to so-called condo inssulating
behavior. (Hubbard模型的一个变体称为周期性Anderson模型，它很好地捕捉到了镧系元素材料的特性，从而产生了所谓的Condo绝缘行为。)

These Hubbard models also probably most importantly describe high-temperature superconductors. 
In particular, these high-temperature superconductors have copper oxide planes typically in these
perovskites at least they have these copper oxide planes, which are basically perfect 2d square lattices,
and they described well by the Hubbard model on a 2d square lattice.
It is believed that this even the simple model, the Hubbard model of the 2d square lattice, 
can capture the essence of high-temperature superconductivity. There are vast amout of work on this 
and I would say that the matter is still not settled. 
(这些哈伯德模型也可能是最重要的描述高温超导体。特别是，这些高温超导体通常在这些钙钛矿中具有氧化铜平面——至少它们具有这些氧化铜平面，
它们基本上是完美的二维正方形晶格，并且它们通过二维正方形晶格上的Hubbard模型得到了很好的描述。
人们相信，即使是简单的二维正方形晶格的Hubbard模型，也能捕捉到高温超导的本质。
在这方面有大量的工作，我想说这件事仍然没有解决。)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig7.png)

Hubbard model 很难求解，if we look at a ratio u/t that very small, we can do perturbation theory in the 
interaction strength U. If we consider very very large, we can do the perturbation theory in the tunneling team.
But actually a great actually deal of interesting physics happens when U/t = 1. (如果我们看一个比值u/t很小，
我们可以在相互作用强度u中做微扰理论。如果我们考虑非常非常大，我们可以对隧道团队做微扰论。
但实际上，当u/t=1时，会发生很多有趣的物理现象。)

## The underlying physics of Hubbard model

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig8.png)

For example, metallic behavior, insulating behavior, magnetism, super conductivity, if you consider 
different lattices. 

## Half-field lattice Hubbard model 
## 在金属相中

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig9.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig10.png)

这个对应的就是粒子-空穴激发，只有当两个不同的自旋占据同一个轨道的时候，会形成一个近程的库伦相互作用。

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig11.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig12.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig13.png)

**可以看出，电子在tunneling 的过程中，就会形成铁磁或者反铁磁的涨落**

**考虑更多的tunneling effects**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig14.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig15.png)

## 在绝缘体相中

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig16.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig17.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig18.png)


**由于很强的库伦排斥作用，电子会隧穿回原来的位置，这个时候隧穿回来的时候自旋可能会发生反转**
**虽然库伦排斥很强，但是由于是量子力学系统，仍然会有很小的概率发生隧穿，再回到原来的位置上，导致自旋反转**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig19.png)

**由于很强的相互排斥，电子被局域到格点上，电子在lattice 上不能自由移动，如果电子跃迁到了近邻的位置，它又必须跃迁回来，使得**
**整个pattern能量最低**

### 这样的绝缘体有什么样的性质呢？

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig20.png)

Actually the insulator is magnetic, it has antiferromagnetic ordering. 
Due to the excitation process, here, we have two electrons paralled lines 
because I hopped the one electron over from one sites. 

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig21.png)

**当两个自旋相同的时候，两个相邻自旋之间的tunneling 不会发生，根据泡利规则，相同方向的两个自旋不能占据同一个轨道。**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig22.png)

**从这个角度出发，一定程度上解释了为什么超导中的存在的都是反铁磁涨落，因为由于Pauli不相容原理，铁磁涨落导致两个不同格点的自旋不能隧穿，也就不会存在**
**onsite 的库伦相互作用，也就不会有隧穿现象的发生，肯定不会导致超导，不会存在 spin flip 激发**

### 考虑 spin 为 反铁磁关联

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig23.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig24.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig25.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig26.png)

**这些反铁磁spin之间并不是静态的，而是会相邻格点之间互相tunnelg, 只不过形成 onsite 的2个电子的生命时间非常短，很快又会隧穿**
**回原来的位置上，这样的激发过程也可以看作是一种虚拟激发，这也是符合量子力学图景的**

## Hubbadrd 模型中的态密度和激发普

### 第一种情况，库伦相互作用趋于零

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig27.png)


 This a non-interacting binding model with electons. For example, hopping around on 
 a 2d square lattice. Because we just have a single orbital in the unit cell, we know 
 we will have a single band. Not all energies are accessible of all the eigenstates exist. 
 
 What we would expect is a single band, the width of this band we can call W, if this is a
 square lattice, this W from the calculation by tight-binding model would be 8t (4t - (-4t)). 
 (我们所期望的是一个单能带，这个能带的宽度我们可以称之为W，如果这是一个正方形晶格，通过紧束缚模型计算得到的W将是8t（4t-（-4t））。)
 
 ![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig28.png)
 
 If we want to have a half-filled system with average occupation of each sitw of 1, then we just fill 
 up the single particle states up untile the Fermi energy. If exactly half of the total number of states
 lie below the Fermi energy, then we have a half-filled system. 
 (如果我们想要一个半填充系统，每个位置的平均占有率为1，那么我们只需要填充单个粒子的状态，直到费米能量。
 如果总态数的一半正好位于费米能量以下，那么我们就有了一个半填充系统。)
 
 We can control the occupation of our system by changing the chemical potential. 
 We can actually add that into our Hamitonian. 
 (我们可以通过改变化学势来控制系统的占据数。实际上，我们可以将其添加到我们的哈密顿中。)
 
 $$-\mu\sum_{i\sigma}n_{i\sigma}$$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig29.png)

This would be a constant shify in the energy of the whole system, which basically defines the Fermi energy. 
If we want a half-filled system, which in the limits that we just pick $\mu =0$. Because exactly half of the total 
number of states lie below the Fermi energy, when we want to fill up the firm sea until the Fermi energy exactly 
half the states are filled. 

**\mu =0 的时候对应的体系处于半满的状态，这种描述方式来自于对基于tight-binding-model的单粒子模型, 也就是半满的时候**
**刚好将费米面以下填充完, 对应的费米面的能量刚好为零，因为整个能带的宽度是 -4t 到 4t，0 刚好是费米能，而费米能通过化学势**
**调节，所以化学势为零刚好对应的是半满的状态**

**如果我们将库伦相互作用增大一点，以上描述的图像基本不发生改变**

### 第二种情况，隧穿 t = 0

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig30.png)

This is the so-called atomic limit, because we imagine each atom being now totally isolated from all of 
the neighbors. What do we expect from the density of states in such a case? 
(这就是所谓的原子极限，因为我们想象每个原子现在都与所有邻居完全隔离。在这种情况下，我们对态密度的期望是什么？)

The system is going to be very highly degenerate macroscopically, beacuse we have n orbital in the system with 
n of order 10 to 23. Understandinig the entire properties of the whole system as just highly generate version of 
single atom and the properties of the single atom are just controled by the Coulomb term. We can actually just solve
that exactly for a single atom, this is extremely easy to do we have just single atom. 
(从宏观上看，这个系统将是高度退化的，因为我们在这个系统中有n个轨道，n为10的23次方。
将整个系统的整个性质理解为单个原子的高生成版本，并且单个原子的性质仅由库仑项控制。
实际上，我们可以精确地求解一个原子，这非常容易，因为我们只有一个原子。)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig31.png)

we have this chemical potential therm in there. I can imagine applying my Hamiltonian to give a basis states 

$$ H = U n_{\uparrow} n_{\downarrow} - \mu(n_{\uparrow} + n_{\downarrow})$$

将哈密顿作用于真空态：

$$H |vac\rangle = 0$$

$$H |\uparrow\rangle = -\mu$$

$$H |\downarrow\rangle = -\mu$$

$$H |\uparrow\downarrow\rangle = u - 2\mu$$

Relative to the half-filled ground state, we can have a hole excitation where we remove an electron. 
that wolud be an energy $-\mu$. 
(相对于半填充基态，我们可以有一个空穴激发，在这里我们可以去除一个电子。对应的energy变化为 -$\mu$。)

We can also have electron excitation, where we would have energy $U - 2\mu$. 
(也可以是电子激发，对应的energy 为 $U - 2\mu$)

$$0 < \mu < U$$

One excitation below the Fermi energy and one excitation above the Fermi energy. 
(一个激发在费米面的上面，一个激发在费米面的下面)

**相当于整个体系看成了单粒子的图景，总共有4个能级，0，-mu, -mu, U-2mu, 这个就是整个系统的一个激发能谱,** 
**空穴激发对应的就是 -\mu, 电子激发对应的就是 U-2\mu**

(这就是没有隧穿项，只有库伦的物理图像)

### 在U很大, t=0，的基础上 增加一点点 t, 也是就是能稍微的隧穿

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig32.png)


对应于 $-\mu$ 和 $U-2\mu$的这两条线就会有一个展宽。尽管有一个展宽，但是两个展宽区域并不交叠，存在有限大的能隙，
这样的能隙是库伦相互作用导致的。这是一个绝缘体。