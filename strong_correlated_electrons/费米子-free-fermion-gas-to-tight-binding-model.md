# Free electron gas
## 简介
> 参考youtube视频教程[Models of many-electron systems in second quantized form](https://www.youtube.com/watch?v=oxsFWuA8zns)
>
>**how many electrons are occupying each of these quantum orbitals?**
>
>In the case of fermion electron gas, we will see that these product state, basis states (in the occupation bases
>**or exactyly eigenstate of hamiltonian**),we can therefor trivially read off the energy of the full system 
> by just knowing un the energies of the individual orbitals and how many electrons either zero or one occupy 
> each of these orbitals
>
> electrons can occupy quantum states $|k\rangle$, 哈密顿量可以写为：
> 
> $$\hat{H}=\sum_{k}\epsilon_k c_k^{\dagger} c_k = \sum_k \epsilon_k n_k$$
>
> 而 $|k\rangle=|\hat{n}_k\ranlge_{k}$, $n_k = 0, 1$, 且 $\hat{n_k}|k\rangle = n_k$
> 
> 用矩阵的形式写一下：
>
>
$$
\hat{c}_k^{\dagger} \hat{c}_k = \left[ 
\begin{array}{cc}
0 & 0 \\
1 & 0 \\
\end{array}
\right] \cdot \left[
\begin{array}{cc}
0 & 1 \\
0 & 0 \\
\end{array} 
\right] = \left[
\begin{array}{cc}
0 & 0 \\
0 & 1 \\
\end{array}
\right]
$$

作用于本征态上:

$$
\hat{n}_k|1\rangle=
\left[ 
\begin{array}{cc}
0 & 0 \\
0 & 1 \\
\end{array}
\right] \cdot \left[
\begin{array}{cc}
0 \\
1 \\
\end{array} 
\right] = \left[
\begin{array}{cc}
0 \\
1 \\
\end{array}
\right] = |1\rangle
$$

$$
\hat{n}_k|0\rangle=
\left[ 
\begin{array}{cc}
0 & 0 \\
0 & 1 \\
\end{array}
\right] \cdot \left[
\begin{array}{cc}
1 \\
0 \\
\end{array} 
\right] = \left[
\begin{array}{cc}
0 \\
0 \\
\end{array}
\right] = 0
$$

>$\epsilon_k$ is the single particle energy of state, this is like the potensial energy of praticular orbital(有点像轨道上的势能),
> 系统的总能量就是所有轨道势能之和，也就是所有粒子能量的和 
>
> 这个系统的本征态是什么呢？
> $[\hat{H},\hat{n}_k] = 0$ 也就是 {$n_k$} conseved by $\hat{H}$, 是一个好量子数。
> good quantum numbers to describe the eigenstates of this quantum hamiltonian.
> 也就是我们用占据数所写的态就是这个哈密顿量的本征态。
> 假设系统有 m 个轨道：

$$\hat{H}|n_1,n_2,...n_m\rangle = E_{n_1,n_2,...,n_m}|n_1,n_2,...,n_m\rangle$$ 

where $E_{n_1,n_2,...,n_m} = \sum_i \epsilon_i n_i$, these states are eigen states of the hamiltonian precisely
because the hamiltonian is just a sum of the number operators and we know these states are eigenstates of the number 
operators 

# Fermi-Dirc distribution
## 简介
>
>
>

# tight binding models -1
## 简介
> 参考youtube视频教程[Models of many-electron systems in second quantized form](https://www.youtube.com/watch?v=oxsFWuA8zns)
> 
> tight binding models (紧束缚模型)： 这些模型中，电子之间仍然没有相互作用。相互之间的库伦势被屏蔽掉了（that's been shielded or screened away）
> but allow electrons to move from one orbital to another (允许电子从一个轨道跑到另一个轨道), of course this means the eigenstates 
> are going to be superpositions of the product state bases involving electron in specific orbitals(本征态会变得互相叠加,也就是让
> 电子会跑到特殊的轨道上)。

$$ \hat{H} = \sum_i \epsilon_i c_i^{\dagger} c_i + \sum_{i,j}t_{i,j}c_i^{\dagger}c_j$$ 

where $\epsilon_i c_i^{\dagger}c_i$ is the potential energy (势能), $t_{ij}c_i^{\dagger}c_j$ 是kinetic energy. 
which is to do with the quantum tunneling between orbitals i and j, $t_{is}$ is the so-called tunneling matrix elements
which can be considered as following: 

(1) consider single particle states (考虑单粒子态)：比如state $|j\rangle$ is obtained from the vacuum by creating 
an electron in orbital j, so $|j\rangle = c_j^{\dagger}|voc\rangle$.
what is the elements between a single particle state j and a single particle state 

$$\langle i| \hat{H} | j \rangle$$

if act the hamiltonian on single particle state $t_{ij}c_i^{\dagger}c_j$ 中的 $c_j$ will destroy that 
the particle in state $|j\rangle$ that is the $c_i^{\dagger}$ 会在state |i\rangle 产生一个电子，
因此 $\langle i | \hat{H} | j \rangle = t_{ij}$

## 考虑一个简单的例子：2-site system (2 格点系统)

we will have a single particle energy for orbital one which we call $\epsilon_1$, 
and the energy is depend whether or not that orbital is occupied. 
Let us have another energy $\epsilon_2$ associated with orbital two, they are single partile particle 
energies and this time we are going to allow **electrons to tunnel from orbital one to orbital two**,
we have 

$$\hat{H} = \epsilon_1 \hat{n}_1 + \epsilon_2 \hat{n}_2 + t(c_1^{\dagger}c_2 + c_2^{\dagger}c_1)$$

and you see that I have enforced the hermeticity of the hamiltonian by factorizing out a commom t here,
(hermrticity hamiltonian will have the real eigenstates and eigenvalues). Notice that the term $c_1^{\dagger}c_2$ corresponding
to the tunneling of an electron from one to two and is not hermitian. (单这一项并不厄密) 然而 $c_1^{\dagger}c_2$ 和 $c_2^{\dagger}c_1$
是一对 Hermitian conjugates 也就是互为厄密 $(c_1^{\dagger}c_2)^{\dagger} = c_2^{\dagger}c_1$.
**we can also regard this hermiticity property as being like a time reversal symmetry (也将这样的厄密性视作时间反演对称)**,
or we saying the tunneling rate of electrons going from one to two must be the same as the tunneling from two to one, we
are allowing for this microscopic reversibility (微观反演性质) of electrons going from 1 to 2 or 2 to 1 with same amplitude.

## 求解这个两格点系统，首先考虑粒子数表象的 basis states, 测试 basis states 是否是 eigen states
solving this model at least let us see what we get when we consider our usual basis states:

basis states for this two orbital system will be defined by the occupation numbers :

$$|n_1,n_2\rangle$$ 

with $n_1 = 0 or 1$, $n_2 = 0 or 1$.

第一种情况，total number of electron number zero, this is the vacuum state N = 0:

$$\hat{H}|0,0\rangle = 0 |0,0\rangle$$

也就是说 state $|0,0\rangle$ is the eigenstate of $\hat{H}$ with energy 0

考虑第二种情况，N = 2

$$\hat{H}|1,1\rangle = (\epsilon_1 + \epsilon_2)|1,1\rangle$$,

也就是说state $|1,1\rangle$ is also eigenstate with energy $\epsilon_1 + \epsilon_2$, is the sum of single particel energies.

考虑第三种情况，N=1, 

$$\hat{H}|0,1\rangle = \epsilon_2|0,1\rangle + t c_1^{\dagger}c_2|0,1\rangle = \epsilon_2|0,1\rangle + t c_1^{\dagger}c_2c_2^{\dagger}|vac\rangle
=\epsilon_2|0,1\rangle + t|1,0\rangle$$

so I create an electron in the vacuum then I destroy it and then I create another electron in orbital 1.
**so $|0,1\rangle$ is not the eigenstate** ($|0,1\rangle$并不是本征态)
同样的可以得到：

$$\hat{H}|1,0\rangle = \epsilon_1|1,0\rangle + t|0,1\rangle$$

同样，这样的state 也不是一个本征态。it is a linear combination of $|0,1\rangle$ and $|1,0\rangle$ that will be 
eigenstates (**如果将$|0,1\rangle$和$|1,0\rangle$线性叠加起来，将会是一个本征态**。因此也就会满足 schordinger equation)

**为什么**state $|0,1\rangle$ and states $|1,0\rangle$ **不是哈密顿的本征态呢**，**这是因为这两个 basis states 对应的粒子数** 
$n_1$ and $n_2$ are not good quantum numbers (**并不是好的量子数** )，也就是这样的量子数并不是一个守恒量（conversed）,
我是怎么知道这两个量子数不是**好量子数**，不是守恒量呢，因为

$$[\hat{H}, \hat{n}_i] \neq 0$$

一个电子并不是一个好的守恒量，因为它可以从轨道1 跑到 轨道2. So we can not label eigenstates of H according
the individual occupation numbers of the orbitals, because those things are not conseved.
However the total electron number which is the sum of the individual occupation numbers is conserved 
因此total electron number 是一个好的量子数，可以用其标记本征态。

# tight binding models -2
## 简介
> 参考youtube视频教程[Tight-binding models](https://www.youtube.com/watch?v=GFZ3Asw4dc4&list=PLotxEOxVaaoKRXdDN-7lI3Y88PaHqyOZL&index=15)

Tight-binding models 通常用来描述非相互作用费米子系统，通过能带结构可以理解很多材料的性质。例如一些分子系统，
and quantum transport through nano wires and other nano devices.

second quantized version of tight binding models also the solution of those models whcih is basically equivalent to 
solving the Schrodinger equation. I will discuss how one can construct a many particle Hamiltonian matrix and 
diagonalize that matrix to obtain the solution to type binding models but I will also describe how for tight binding models
there is a much simpler way which is involves that canonical transformation of the operators to bring the Hamiltonian 
operator into diagonal form we will see that solution of such model can be interpreted as **band structure in momentum space** 
(动量空间的能带结构) for periodic systems where such a canonical transformation is actuallly just the Fourier transform.

Most general form of Hamilton 

$$\hat{H} = \sum_{i,j} t_{ij}(c_i^{\dagger} c_j + c_j^{\dagger} c_i) + \sum_i \epsilon_i c_i^{\dagger}c_i$$ 

the sum is over orbitals or lattice sites of the system labeled i and j. $t_{ij}$ is the tunneling matrix element between
those orbitals or sites. $c_i^{\dagger}$ creates an electron in orbital site i and $c_j$ annihilates an electron in orbital j.
Also, becase of the property of hermiticity of hamiltonian , $t_{ij}$ must be equal to $t_{i,i}^*$. 

只考虑近邻的 orbital 之间的跃迁，just have the sum over of nearest neighbors. this model describes a set of quantum orbitals labeled
by i each with energy $\epsilon_i$ and a tunneling matrix elements $t_{ij}$, which describes the movements of an electron from orbital i to 
one of its neighbors j. 

这种形式的Hamiltonians are said to be quadratic (二次型的) because we just see pairs of creation and annihilation operators (因为只能看到成对的
产生和湮灭算符，这里并没有四个费米子算符项，如果是在有相互作用的模型中，就会出现四费米子算符项)

**这样的 tight-binding-model 描述的是什么样的系统呢？**
for example we can describe materials where we have atomic orbitals on particular atoms arranged into a lattice 
so that the atomic orbitals overlap (原子轨道之间会overlap), electrons can tunnel from one orbital to the other in the 
metal for example, (比如在金属中) the electrons can actually roam freely over the entire structure (电子可以很自由的在整个
结构中出现) 

>*as an example, 考虑一个 2d square crystal lattice

this is something that is relevant to the description of high-temperature superconductors (一定程度上可以描述高温超导),
for example the perovskites yttrium barium copper oxide (钙钛矿钇钡铜氧化物) wich contain 2d square lattice planes of 
copper oxide let us draw a sketch of that arrangement 

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/2d_square.png) 

consider the p orbitals (考虑每个原子的p轨道) of each atom for example the px and py orbitals and pz orbitals will be 
pointing out of the page and we will ignore those in this analysis so how does it look when we put those oritals on 
each of the lattice sites:

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/2d_square_p_orbital.png) 

electron can tunnel effectively from one atom to the next on the lattice beacuse of the overlap of the 
atomic orbitals and of course this is what a chemical bond is (这就是所谓的化学成键) the reason why the lattice adopts
this lattice structure is precisely because the electrons can form these chemical bonds (电子会形成这样的化学键) in this 
arrangement the electrons are shared between the atoms and become itinerant meaning they can move throughout the lattice so
the ovelap between the atomic orbitals means these atomic orbitals are not well-defined quantum states on their own electrons
in such atomic orbitals have a finite lifetime since they can quantum tunnel to a neighboring site on the crystal lattice and 
the amplitude for doing that is precisely the tunneling matrix elements $t_{ij}$ between nearest neighbor sites i and j. 

所以原子轨道之间的ovelap意味着这些原子轨道在它们自己的电子上不是定义明确的量子态，在这样的原子轨道中，它们的寿命是有限的，
因为它们可以量子隧穿到晶格上的相邻位置，而这样做的幅度正是最近相邻位置i和j之间的隧穿矩阵元素$t_{ij}$。

## 考虑苯分子的 tight-binding-model:

对于这个六角结构(hexagonal structure) this is so called sp2 hybridization that works for hybriding an S orbital in 
catbon with px and py orbitals to form this sp2 hybridized object and that's looks like the bonds with the angle
between these bonds being exactly 120 degrees and then there are these additonal pz orbitals which stick up above and 
below the plane of the molecule and they form the so-called $\pi$ bonding Network where we have delocalized electrons that 
can move around so they are delocalized , let's see how this looks, here:

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/benzene.png) 

in blue I have again drawn the atomic nuclei which in this case is carbon and I've tried to draw it here in perspective
actually of course this is a perfect hexagon. 将 pz orbital 也画出来：

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/benzene_2.png) 

each of pz orbital contains a single electron and the electron can actually tunnel from one orbital to another above and 
below the plane , I've illustrated that here by the green and the yellow lines:

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/benzene_3.png) 

## 这样的一个苯环系统的哈密顿是什么样的呢？ what it looks like ?

由于 sp2 杂化已经成键(形成sigma bonding)，因子只有 pz 轨道上的电子是自由电子，这样的电子称为 $\Pi$ electrons:
(just writing for the $\Pi$ bonding orbitals so these are the set of six $p_z$ orbitals that are out of the 
plane of the molecule so the sp2 hybridized carbons that are holding the molecule together are just forming 
the chemical bonds and actually they're a litte boring. Just writting for the electrons that can move around which 
are the $\Pi$ electrons):


$$\hat{H}_{\pi} = \epsilon \sum_{i=1}^{6} c_i^{\dagger}c_i + t\sum_{i=1}^{6}c_{i}^{\dagger}c_{i+1}+c_{i+1}^{\dagger}c_i$$

求解这样的模型，我们会发现，分子轨道 （molecular orbitals were there would be the eigenvectors of the Schrodinger equation to 
be basiclly the wave functions and we'd be able to find out the energies of the electrons in the system as well,）

# 考虑石墨烯系统：

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene.png) 

The graphene structure is actually held together by these Sigma bonds which are made up from sp2 hybridized carbon or orbitals 
on each atom but these orbitals overlap on the lattice each carbon atom contributes one electron per sp2 hybridized orbitall and 
there for each chemical bond has two electrons in it one contributed from each of the atoms and these chemical are therefor very stable
, the entire hexagonal 2d lattice structure of graphene is extremely stable however we're not yet considerd the $P_z$ orbitals that
stick above and below the plane and these form the $\Pi$ bonding Network that I want to discuss in more detail:
(石墨烯结构实际上是由这些sigma键连接在一起的，sigma键由sp2杂化的碳或每个原子上的轨道组成，石墨烯的整个六边形2d晶格结构是非常稳定的，
然而我们还没有考虑粘在平面上方和下方的$P_z$轨道，这些轨道形成了我想更详细讨论的$\Pi$键合网络：)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_2.png) 

可以看到 $\Pi$-bond 形成的 Network 仍然是一个六角格子。每个碳原子在 $p_z$ 轨道上有一个电子。这就是我们在凝聚态物理中
处理的六角晶格的问题。
## 写出这个六角格子的哈密顿为：

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_3.png) 

## 如何求解这样的哈密顿呢？
### 方案一：将矩阵形式写出来，然后进行对角化

对于非相互作用的费米子系统，可以方案二是最有效的，可以将哈密顿通过正则变换变为对角形式。
constrating and diagnolizing the Hamiltonian matrix in the **many-particle basis** (多粒子基矢)。
什么是多粒子基矢量呢，比如 2-particle system 中：

$|0,0\rangle$, $|0,1\rangle$, $|1,0\rangle$, $|1,1\rangle$ 

这是一组完备正交基矢。

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_4.png) 

how can we guarantee that our new basis is complete and orthonomal (如何保证我们新构成的基矢量是正交完备的呢)，
Let's just write again our basis transformation equation 

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_5.png) 

如何运用这样的基矢量变换来求解 tight-binding-models ? 
求解Schrodinger equation 就是等价于做这样的一组矢量变换，将原始的基矢量变换为哈密顿的本征基矢量。
这样哈密顿量就会变为对角哈密顿量。

如何找到这样的变换矩阵 U 呢？

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_6.png) 

**用两轨道举例：**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_7.png) 

**写成矩阵形式：**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_8.png) 

为什么这样的哈密顿会出现分块对角的形式呢？
原因是**这个哈密顿量中总的电子数是一个守恒量**，

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_9.png) 

可以看出哈密顿并不能改变粒子数的数量，也就是矩阵元素中 <N=0|H|N=1> =0, <N=0|H|N=2>=0, <N=1|H|N=2>=0.

**这样的分块对角矩阵意味着我们可以在每个量子数$N$的块里面分别进行对角化**。
比如对于 N=1 的sector, 我们可以写为：
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_10.png) 

**接下来求解薛定谔方程**
进行矩阵变换：
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_11.png) 

**考虑 N=1 sector 的对角化**
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_12.png) 

**小结**
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_13.png) 

这一方案可以处理有相互作用的系统(it can be generalized to interating systems), we can obtain eigenstates that are already
in many particle bases.
这一方案的缺点就是哈密顿系统随着格点增加变得指数增长。另一个缺点是，it's not completely physically obvious what the interpretation of the
eigenstates. it is really a numerical method we get a numerical solution. The physical content of the solution is not
completely obvious. 

**为什么没有相互作用的哈密顿，也就是只包含动能项和势能项，也就只包含两费米子算符项的哈密顿可以很好的找到幺正变换使得其很好的对角化呢？**

### 方案二：对哈密顿里面的算符进行正则变换（performing a canonical transformatiion of the operators in the Hamiltonian）

It is economical transformation of the Fermionic operators, which brings our hamiltonian operator to diagonal form.

什么是正则变换，canonical transformation is one which preserves the anticommutation relations of the original 
thermionic operators. 
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_14.png) 

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_15.png) 

将 所有格点的 $c_i$ 算符排成一个矢量，通过特定的变换，变成 $F$ 算符矢量：

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_16.png) 

F and C are vectors of operators and U here is our unitary matrix. U 可以是任意是幺正矩阵，变换完之后的F满足和C一样的反对易关系。

**The question is how can we utilize this idea this concept of canonical transformation of operators how can we**
**utilize this to actually do the work of solving our Schrodinger equation as we will see not all hamiltonians can**
**be solved in this way. In fact, it is only these quadratic Hamiltonians that only involve pairs of operators that**
**can be solved using a canonical transformation (只有不含相互作用的哈密顿量才可以用这一方法求解)**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_17.png)
 
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs/tight-binding-model/graphene_17.png)

