# Effective bi-layer model Hamiltonian and DMRG for the high-Tc SC in La3Ni2O7 under high pressure

## 摘要

* 该模型的主要特征是3dz2电子通过两层之间的顶端氧阴离子形成层间σ键和反键带，而3dx2-y2电子在每个NiO2平面内与3dz2的电子杂化。

* 3dz2 轨道是半满， 3dx2-y2 轨道是 四分之一 填充。

* 强的Hubbard排斥作用使得 3dz2 轨道上的电子形成有效的层间反铁磁自旋超交换 J

* 加压会使得层间超交换 J 增强，并且增强3dz2 轨道上的自掺杂空穴(self-dope holes)，相应的同等程度的增强 3dx2-y2 上的电子掺杂。

* 通过 DMRG 发现 这两个杂化轨道上的电荷密度总是有着均匀的分布

* 在 J 很小的时候， 自旋密度波和自旋-轨道密度波都会出现

* 在J 很大的时候， 自旋密度波和自旋-轨道密度波都被压制，电子配对不稳定性出现，因为 3dz2电子形成层间的自旋单态

* 层内垂直于 3dx2-y2 方向上的超导对密度波给出了最强的配对相关性

 ## 背景介绍

 * [Critical Nature of the Ni Spin State in Doped NdNiO2](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.124.207004)
指出然而，氧2p轨道的电子态远低于费米能级，并且由于其on-site 能量的较大分离，其3d−2p混合大大减少，
并且与具有比铜酸盐至少小一个数量级的超级交换能量的电荷转移机制相比，它们的低能电子结构更有可能落入Mott-Hubbard机制

* 因此，母无限层镍化物可以被建模为具有两种类型电荷载流子的自掺杂莫特绝缘体，
并且电阻率的低温上升是由稀土低密度导电电子和局部Ni-3dx2−y2磁矩之间的磁自旋散射引起的

* 由于结构中NiO2双层的量子限制，经由氧的3dz2轨道通常具有大的层间耦合，

* 并且由此产生的Ni阳离子的能量分裂可以显著地改变Ni2.5+ 平均价态

* 数值结果进一步表明，在由3dz2轨道和顶端氧连接的Ni-O双层组成的费米能级下，超导性与σ-键带的金属化同时出现[17，18]。

* 这些独特的特征是Ruddlesden Popper双层钙钛矿镍化物中高Tc超导性的重要线索，它不同于无限层镍化物超导体。


## 双层模型

* 3dz2 的电子组成了层间的 $\sigma$ 键 和 anti-bonding bands via the apical oxygen anions between two layers. 

* 3dz2-y2 的电子 和 3dz2 的电子在 NiO2 平面进行了杂化

* 由于两个eg轨道的特殊空间对称性，层内3dz2轨道电子的跳跃和3dx2−y2轨道电子的层间跳跃非常小，可以忽略不计。

* 这两个轨道电子的化学势差确保了3dz2轨道接近半填充，3dx2−y2轨道接近四分之一填充。

* 强的 on-site Hubbard排斥引起 3dz2 轨道电子 J 的层间反铁磁超交换。

* 施加压力可以增加耦合强度J，并在3dz2轨道上自掺杂额外的空穴，同时在3dx2−y2轨道上掺杂相同数量的电子

* 层内垂直3dx2−y2键上的对密度波给出了最强的配对相关性，而3dz2电子的层间单线态对的配对相关性由于缺乏相干性而较弱。

> $\sigma$ 键 and anti-bonding bands 
## 哈密顿量

* 因为3dz2轨道的层内跳跃可以忽略，所以两个位点半填充的3dz2轨的基态是孤立的单线态。

* 在 3dx2-y2 的电子平均填充数为 n^c = 1/2, 因此相互作用的 3dx2-y2 的电子基态是一个顺磁金属。

* 随着有限的杂化 $t_{x^2-y^2,z^2}$, 3dz2 的电子能够跃迁到 3dx2-y2, 3dz2 电子能够通过这种方式相干，
因此在大的层间耦合作用下，可能会出现超导。这样的物理图像和文献[17][18] 中的 $\sigma$ 键金属化是相似的。

## DMRG 过程

> With a scan of $\Delta_\mu = \mu_{x^2-y^2} - \mu_{z^2}$, 设置 $\Delta_{\mu} = 0.3$ 来保证 3dz2 轨道是半满的，
> 3dx2-y2轨道是接近 1/4 满的， 这些参数是怎么选择的？背后的物理是？

> 初始的参数选择使得 3dz2 轨道的电子处于模特绝缘体的极限，3dx2-y2 轨道的电子在大的掺杂极限，类似于
> orbital selective Mott physics. 

## DMRG 结果

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-B-Arxive-Ni-SC-1/fig1.png)

* 从(b)子图中可以看出，无论 J 怎么变化，3dz2 的电子密度为半满左右， 3dx2-y2的电子密度为1/4 填充左右。

* 从(c) (d) 子图可以看出这里缺乏准长程的电荷密度波序。

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-B-Arxive-Ni-SC-1/fig2.png)

* 由于自旋-自旋管理的计算需要大的计算资源，这里采用加一个钉扎场来处理，在左边一个电子处加一个钉扎场 $h_m = 0.5$,

* 可以发现对于小的 J, 局域自旋密度衰减的非常慢，3dz2 上的电子密度大于 3dx2-y2

* 随着 J 的增大，3dz2 和 3dx2-y2 的自旋密度都会受到压制，但是 3dz2 上的自旋密度会衰减的更快，
因此，在大的J极限下，3dx2-y2上的自旋密度会远远大于 3dz2的自旋密度。

* 当 J = 0.2 的时候， 两个轨道上的电荷密度波相近，会相差一个 $\pi$ 相位。
并且 spin-orbital density wave 会消失。

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-B-Arxive-Ni-SC-1/fig3.png)

> 怎么看出 spin-orbital wave 的？

> 在大的J极限下，3dx2-y2上的自旋密度会远远大于 3dz2的自旋密度。 这个能说明什么呢？


## 疑问：

> (1) 怎么保证层间半满，层内 1/4 满 呢？

> (2) 什么是 self-dopping 呢？

## 补充知识：

### [成键轨道和反键轨道](https://www.zhihu.com/question/302039912)

* 成键：两个原子相互吸引，必须加一个拉力才能让它们维持现在的距离

* 反成键：两个原子相互排斥，必须加一个压应力才能把它们压在当前的位置

* 在同样距离下的两个原子既可以相互吸引也可以相互排斥。能让它们相互吸引的电子分布就是成键轨道，让它们始终相互排斥的就是反键轨道。

### [轨道选择莫特转变]([轨道选择Mott转变的新机理 - 中国科学院物理研究所 (cas.cn)](https://www.iop.cas.cn/xwzx/kydt/200906/t20090622_2328046.html))

在这些典型的多轨道系统中，当发生Mott转变后，只有其中一个3d轨道上的电子被局域化，而其他几个3d轨道上的电子依然保持巡游状态。这样一种特殊的Mott转变称为轨道选择的Mott转变（OSMT），对此有一种解释，即不同的3d轨道所形成的能带带宽不同，在相同的库仑排斥能下，其中较窄的能带先发生Mott转变。然而进一步的实验研究发现，在CaxSr2-xRuO4中，很可能是其中带宽较大的dxy轨道上率先发生Mott转变的，这就与此前的理论解释完全不同。





