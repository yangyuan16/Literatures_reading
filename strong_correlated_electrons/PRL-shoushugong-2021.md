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

## 关联函数：

**spin correlation, 自旋关联函数**

$$S(r) = \langle S_x S_{x+r}\rangle$$

**single particle correlation, 单粒子关联**

$$G(r) = \langle\sum_{\sigma}c_{x,\sigma}^{+}c_{x+r,\sigma}\rangle$$

**自旋单态配对:**

$$P_{\alpha,\beta}(r) = \langle \hat{\Delta}_{\alpha}^{\dagger}(r_0)\hat{\Delta}_{\beta}(r_0 + r)\rangle$$

$$r_2 = r_1 + e_{\alpha}$$

$$\hat{\Delta}_{\alpha}(r_1) = (c_{r_1\uparrow}c_{r_2\downarrow} - c_{r_1\downarrow}c_{r_2\uparrow}) / \sqrt{2}$$

$e_{\alpha=x,y}$ **denote x 方向 和 y 方向的单位长度。**

**electron distribution function in the momentum space**

$$n{k}=\sum_{i,j,\sigma}\langle c_{i,\sigma}^{\dagger} c_{j,\sigma}\rangle e^{k(r_i-r_j)} / (L_xL_y)$$



## 相图

### CDW phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig1.png)

(1) In the CDW phase, we identify stripe orders with wavelength $\lambda= 4 / (L_y\delta)$ 

(2) $n_x = \sum_{y=1}^{L_y}\langle\hat{n}_{x,y}\rangle / L_y$

(3) $\lambda = 4/(L_y\delta)$ Each stripe is filled with four holes. (**每个条纹里面有4个孔**)

(4) **因为出现了两个空穴的电荷调制, 准的长程序（quasi-long-range）的超导可能出现在共存相中，**
**因为两个空穴的电荷调制可能适用于配对**

> **怎么看出CDW在y方向上的平移不变，均匀的**

> **怎么看出 CDW phase 中孔的数量的？, 一个条纹里面有4个孔**

>**波矢为8，一个条纹里面有 4 个孔**

> **为了探测准长程超导序，在原文的 fig4 对关联函数采用了两种拟合方式，一种是指数的拟合, 一种是幂律拟合**

### SC phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig2.png)
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig4.png)

(1) **关联函数中的插图显示处 D-wave 对称性**

**自旋单态配对和d-波对称性:**

$$P_{\alpha,\beta}(r) = \langle \hat{\Delta}_{\alpha}^{\dagger}(r_0)\hat{\Delta}_{\beta}(r_0 + r)\rangle$$

$$r_2 = r_1 + e_{\alpha}$$

$$\hat{\Delta}_{\alpha}(r_1) = (c_{r_1\uparrow}c_{r_2\downarrow} - c_{r_1\downarrow}c_{r_2\uparrow}) / \sqrt{2}$$

$e_{\alpha=x,y}$ **denote x 方向 和 y 方向的单位长度。**

(2) **通过检查不同配对关联性来讨论SC配对的对称性**


> **如果是 p 波配对还是这样的构型吗？**

> **为了探测准长程超导序，在原文的 fig4 对关联函数采用了两种拟合方式，一种是指数的拟合, 一种是幂律拟合**

> **SC correlations are greatly enhanced (K_{SC}) reduces from 0.96 to 0.36,**
> **density correlations are strongly suppressed with K_{CDW} increasing from 1.4 to 2.93**
### SC+CDW phase

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig3.png)

(1) **波矢 $\lambda = 4$, 每个条纹里面有2个孔**

> **Quantitatively, SC correlations still dominate all other correlations with the Luttinger exponents K_{SC} < K_{CDW} < 2**

## 费米表面演化 (Fermi surface evolution)

 **正常相和超导相有着不同的拓扑**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2021-SSGong/fig5.png)

(1) In the normal CDW phase, the size of the electron pocket near the $\Gamma=(0,0)$ point expands 
eventually convering a large portion of the Brillouin zone with a clear nematic sidtorion of 
Fermi surface from the unidirectional stripe order.

(2) In the SC and SC+CDW phases, electronic states form a closed Fermi surface with approximate $C_4$ and 
an isolated electron pocket centers around the $\Gamma$ point. 

(3) The Fermi surface topology may be related to the emergence quantum criticality between the CDW and SC phase. 

> **什么是 electron pocket centers**

## 总结：

We carefully established that the SC pairing correlation is the strongest correlation with robust
quasi-long-range order and a small power exponent. 

