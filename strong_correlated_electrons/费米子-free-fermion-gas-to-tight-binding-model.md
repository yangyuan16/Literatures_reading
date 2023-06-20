### Free electron gas
##### 简介
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
### Fermi-Dirc distribution
##### 简介
>
>
>

### tight binding models -1
##### 简介
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

##### 考虑一个简单的例子：2-site system (2 格点系统)

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

##### 求解这个两格点系统，首先考虑粒子数表象的 basis states, 测试 basis states 是否是 eigen states
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

###tight binding models -2
##### 简介
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

##### as an example, 考虑一个 2d square crystal lattice

this is something that is relevant to the description of high-temperature superconductors (一定程度上可以描述高温超导),
for example the perovskites yttrium barium copper oxide (钙钛矿钇钡铜氧化物) wich contain 2d square lattice planes of 
copper oxide let us draw a sketch of that arrangement 

consider the p orbitals (考虑每个原子的p轨道) of each atom for example the px and py orbitals and pz orbitals will be 
pointing out of the page and we will 