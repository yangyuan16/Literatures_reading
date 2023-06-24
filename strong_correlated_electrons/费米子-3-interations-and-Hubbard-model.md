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

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/electronics-interactions-Hubbard/fig2.png)

$$\hat{H}_{int}=\sum{i,j,k,l} \sum{\sigma_1,\sigma_2, \sigma_3, \sigma_4} U_{i,j,k,l}^{\sigma_1\sigma_2\sigma_3\sigma_4}\hat{C}_{i\sigma_1}^{+}\hat{C}_{j\sigma_2}\hat{C}_{k\sigma_3}^{+}\hat{C}_{l\sigma_4}$$

> 在 tight-binding 项中，自旋量子数守恒要求 $\sigma_1 = \sigma_2$
> 在相互作用项中，自旋量子数守恒要求 $\sigma_1 + \sigma_3 = \sigma_2 + \sigma_4$