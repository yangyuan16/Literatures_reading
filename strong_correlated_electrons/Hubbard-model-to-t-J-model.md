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
> $$f_0^{\dagger} = \begin{pmatrix}
0&0\\
1&0\\
\end{pmatrix}$$


#### t-J model
##### 简介
> (2) 周期边界下超对称 t-J 模型的精确解可以给出 Luttinger液体的物理图像