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

>作用于本征态上

$$
|n_k\rangle|1\rangle
\left[
\begin{array}{cc}
0 & 0 \\
0 & 1 \\
\end{array}
\right] 
\left[
\beign{array}{c}
0 \\
1 \\
\end{array}
\right] =
\left[
\beign{array}{c}
0 \\
1 \\
\end{array}
\right]
$$


> $$
> \hat{c_k^{\dagger}} \hat{c_k} = 
> \begin{pmatrix}
> 0 & 0 \\
> 1 & 0 \\
> \end{\pmatrix} \cdot 
> \begin{pmatrix} 
> 0 & 1 \\
> 0 & 0 \\
> \end{pmatrix} = 
> \begin{pmatrix}
> 0 & 0 \\
> 0 & 1 \\
> \end{pmatrix}$$
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
> 
#### t-J model
##### 简介
> (2) 周期边界下超对称 t-J 模型的精确解可以给出 Luttinger液体的物理图像