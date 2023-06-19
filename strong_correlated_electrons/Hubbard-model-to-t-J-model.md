#### Hubbard model 
##### 简介
> (1) 周期边界下Hubbard模型的精确解可以解释 Mott 绝缘体的物理本质
>
> (2) Lieb 和 Wu 早在 1968年就通过坐标 Bethe ansatz 方法求得了周期性边界条件下
> 一维 Hubbard 模型的精确解，**证明了在半满带的情况下，金属绝缘体相变的相变点在相互作用系数 U=0处**
>  
##### 模型
> $$H = -t \sum_{\alpha,j=1}^{N}[c_{j,\alpha}^{\dagger}c_{j+1, \alpha} + c_{j+1,\alpha}^{\dagger}c_{j,\alpha} ] + 
> U\sum_{j=1}^{N} n_{j,\uparrow} n_{j,\downarrow}$$
> 
> N 是系统的格点数；t 是近邻电子跳动常数；U 是位于同一格点的两电子之间的相互作用强度，U>0 为库伦排斥势，U<0为库伦吸引势。
> $c_{j,\alpha}^{\dagger}$ 和 $c_{j,\alpha}$ 分别是第 $j$ 个格点上自旋为 $\alpha(=\uparrow , \downarrow)$ 的电子产生和
> 湮灭算符，并且，根据周期性边界条件，我们假定 $c_{N+1,\alpha} = c_{1,\alpha}$ 以及 $c_{N+1,\alpha}^{\dagger} = c_{1,\alpha}^{\dagger}$

##### fermionic creation and annihilation operators
> $$f_0 = \begin{pmatrix}
0&1\\
0&0\\
\end{pmatrix}$$ 
>
> $$f_0^{\dagger} = \begin{pmatrix}
0&0\\
1&0\\
\end{pmatrix}$$
>
> $$f_0|1\rangle = |0\rangle = \begin{pmatrix}
1\\
0\\
\end{pmatrix}$$
>
> $$f_0|0\rangle = 0$$
>  
> $$ f_0^{\dagger}|1\rangle = 0$$
>
> $$ f_0^{\dagger}|0\rangle = |1\rangle = \begin{pmatrix}
0\\
1\\
\end{pmatrix}$$
>
>参考youyube 上的视频教程[fermionic creation and annihilation operators](https://www.youtube.com/watch?v=HZ43XE89n8s)
>费米子满足的运算规则如下：
> $$
>
#### Free electron gas
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
#### Fermi-Dirc distribution
##### 简介
>
>
>

#### tight binding models
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
#### t-J model
##### 简介
> (2) 周期边界下超对称 t-J 模型的精确解可以给出 Luttinger液体的物理图像