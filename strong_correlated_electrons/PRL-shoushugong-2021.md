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

(1) In the CDW phase, we identify stripe orders with wavelength $\lambda= 4 / (L_y\delta)$ 