# t-t'-J model on square lattice

参考文献 [“Robust d-Wave Superconductivity in the Square-Lattice t-J model”](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.127.097003)

## 摘要

(1) **发现 stripe charge density wave phase**

(2) **没有静态电荷序的 charge order**

(3) **超导相和电荷条纹相共存区**

(4) **超导相的配对关联是幂律衰减的，衰减的速度远远小于电荷密度和自旋关联**

(5) **最佳掺杂增强的电荷和自旋涨落能够在掺杂的模特绝缘体中产生强大的d波超导电性**

## 系统哈密顿量和晶格

(1) width-6 cylinder by tuning doping level $\delta$ and hopping ratio $t_2/t_1$

> **dopping level $\delta$ 在 DMRG 中是怎么控制的**

(2) 系统出现的相：CDW (stripe charge density wave), d-wave SC phase, and SC phase coexistent with weak CDW order.

### 参数

(1) $t_1 / J_1 = 3.0$; $J_2 / J_1 = (t_2/t_1)^2$

(2) $0 < t_2/t_1 < 0.32$

(3) $1/24 < \delta < 1/6$ **空穴掺杂水平**

> **为什么参数要这样选择?**

> **PNAS-2021-White 中次近邻的自旋交换相互作用不会发生变化，这里的次近邻自旋交换相互作用是变化的**

> **这里的空穴参杂 \delta 与 PNAS-2021-White 文章中的 dopping level x 的关系是？**

## 相图

### CDW phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig1.png)

(1) In the CDW phase, we identify stripe orders with wavelength $\lambda= 4 / (L_y\delta)$ 

(2) $n_x = \sum_{y=1}^{L_y}\langle\hat{n}_{x,y}\rangle / L_y$

(3) $\lambda = 4/(L_y\delta)$ Each stripe is filled with four holes. (**每个条纹里面有4个孔**)

(4) 

> **怎么看出CDW在y方向上的平移不变，均匀的**

> **怎么看出 CDW phase 中孔的数量的？, 一个条纹里面有4个孔**
>**波矢为8，一个条纹里面有 4 个孔**

### SC phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig2.png)
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig4.png)

(1) **关联函数中的插图显示处 D-wave 对称性**

> **如果是 p 波配对还是这样的构型吗？**

### SC+CDW phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig3.png)

(1) **波矢 $\lambda = 4$, 每个条纹里面有2个孔**
