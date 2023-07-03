# read paper "Quantum Phase Diagram and Spontaneously Emergent ..." [PRL 130,136003(2023)](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.130.136003)
## 摘要信息
(1) 拓扑超导态是一种备受追捧的量子态，具有拓扑序和 Majorana 激发。

(2) d+id-wave chiral TSC with spontaneous TRS breaking, 可以通过Chern number C=2 和 quasi-long-range 超导序来刻画。

(3) TSC出现在中间耦合区，该区过渡到具有较大NNN耦合的d波超导相。
 TSC的出现是由几何挫折和空穴动力学驱动的，它们抑制了自旋关联和电荷顺序，

(4) 导致了拓扑量子相变。

## intro 信息
(1) 在外磁场[1，2]下的二维（2D）电子系统中发现的分数量子霍尔态是物质的显著状态，表现出拓扑序和分数激发[3-5]。
 
(2) 在2D莫特绝缘体中，几何挫折和量子涨落可以抑制磁序，并导致拓扑有序的量子自旋液体（QSL）[6-8]。

(3) 通过掺杂对莫特绝缘体进行调谐，出现了更奇异的相，包括非常规超导（SC）和非费米液体，这是凝聚态物理学的中心主题。

(4) 有趣的是，有一类时间反转对称性（TRS）破缺QSL被命名为手性自旋液体（CSL），
它是Kalmeyer和Laughlin（KL）首次提出的分数量子霍尔态的类似物[18]。

(5)值得注意的是，掺杂CSL可能通过成对分数准粒子的凝聚导致d + id波拓扑超导（TSC）[19-21]。

(6)最近，理论上在具有竞争相互作用的kagome自旋系统[22-25]中发现了KL-CSL，
并在三角形Hubbard模型[26-28]中的金属-绝缘体跃迁附近通过自发TRS断裂发现了KL-CSL。

(7) 对 CSL 掺杂的数值研究表明[25,26]发现了 Wigner 晶体固体或非超导电手性金属[29-31].这挑战了实现 TSC 的
原始方案[19-21]并证明了掺杂阻挫系统的丰富性质[32-48]

(8) 一个突破来自密度矩阵重整化群（DMRG）的研究，该研究通过在三角晶格 t-J模型中掺杂 CSL[49,50]或弱Mott绝缘体[50]来确定d+id波TSC,
其中三个自旋手性耦合 Jx 很明确的破坏了 TRS.

(9) 尽管取得了令人兴奋的进展，但是在 TRS系统中实现TSC(拓扑超导)的机制依然是一个悬而未决的问题，
需要在平均场和变分处理之外进行无偏的数值研究。

(10)专注于 TRS 三角系统，先前对参杂的J1-J2 QSL 的DMRG研究确定了 d波 SC,<font color='red'>而在
此类系统中，传统序，空穴动力学，自旋涨落之间丰富的相互作用仍然没有得到探索</font>, 这可能为通过自发 TRS 破缺实现
TSC提供了一种新的机制。

(11)实验上，三角晶格化合物是最有前途的拓扑态的主要候选者之一，也是实现包括 weak Mott 绝缘体的的QSL的
 主要候选者。d+id 波超导的候选者 $Na_xCoO_2$ 和 $Sn/Si(111)$ systems,并且扭曲过渡金属（twisted transition）
 二硫族（dichalcogenides,TMD）moire 系统可以模拟Hubbard 和相关的t-J模型。关联绝缘体和可能从超导体可以在这些
 系统中被发现，从理论上理解实验可调参数之间的丰富相互作用，如电子hopping 或相互作用。
  
## summary of the intro:
> （1）分数量子霍尔效应会导致出现拓扑序和分数激发。
> 而破缺了时间反演的手征量子自旋液体态属于一种分数量子霍尔态。
> 这种量子自旋液体态称为 KL-CLS. 一般来说对 CSL 进行掺杂
> 可以导致 d + id 波的拓扑超导。
> 最近在理论上发现了 KL-CLS 态。一方面理论上是在Kagome自旋系统中发现的
> 另一方面，理论上在三角形Hubbard模型中的金属绝缘体跃迁附件发现了KL-CSL。
>
> （2） 从Mott绝缘体到量子自旋液体再到非常规超导和非费米液体。
> 几何阻挫和量子涨落会导致模特绝缘体上产生出量子自旋液体。通过掺杂，
> 会出现非常规的超导和非费米液体。

### 哈密顿和参数设置

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig1.png)

(1) $J_1 = 1$

(2) $t_1 / J_1 = 3$

(3) $t_1 / J_1 = 3$ to mimic a strong Hubbard interaction U/t = 12

(4) The electron number $N_e$ is related to hole doping level $\delta$ as $N_e/N=1-\delta$

> **为什么 t_1/J_1 = 3 可以模拟哈伯德中的 U/t = 12**
>  
> **电子数与掺杂浓度的关系**
> $$N_e/N = 1 - \delta$$

## 文章所用关联函数

(1) **自旋关联函数, spin correlations**

$$S(\textbf{r}) = \langle\hat{S}_{\textbf{r}_0}\hat{S}_{\textbf{r}_0+\textbf{r}}\rangle$$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/corr_spin.png)



(2) **单粒子关联函数, single-particle correlation**

$$G(\textbf{r}) = \sum_{\sigma}\langle\hat{c}_{\textbf{r}_0,\sigma}^{+}\hat{c}_{\textbf{r}_0+\textbf{r},\sigma}\rangle$$
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/corr_number.png)


(3) **密度关联函数, density correlation**

$$D(\textbf{r}) = \langle\hat{n}_{\textbf{r}_0}\hat{n}_{\textbf{r}_0+\textbf{r}}\rangle-\langle\hat{n}_{\textbf{r}_0}\rangle\langle\hat{n}_{\textbf{r}_0+\textbf{r}}\rangle$$
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/corr_density.png)


(4) **自旋单态配对关联函数, spin-singlet pairing correlations**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/corr_pair.png)
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/corr_pair_2.png)

$$ P_{\alpha\beta}(r) = \langle\hat{\Delta}_{\alpha}^{\dagger}(r_0)\hat{\Delta}_{\beta}(r_0 + r)\rangle$$

$$\hat{\Delta}_{\alpha}(r) = (\hat{c}_{r\uparrow}\hat{c}_{r+e_\alpha\downarrow} - \hat{c}_{r\downarrow}\hat{c}_{r+e_\alpha\uparrow})/sqrt{2}$$

## 序参量

(1) **手征序，chiral prder**

$$\langle\chi\rangle=\langle\hat{S}_{i}\cdot(\hat{S}_j\times\hat{S}_k)\rangle$$

(2) **自旋结构因子, spin structure factor**

$$S(\textbf{k}) = (1/N_m)\sum_{i,j}\hat{S}_i\cdot\hat{S}_je^{i\textbf{k}(\textbf{r}_i-\textbf{r}_j)}$$

(3) **k 空间的电子占据数**

$$n(\textbf{k}) = (1/N_m)\sum_{i,j,\sigma}\langle\hat{c}_{i,\sigma}^{+} \hat{c}_{j,\sigma}\rangle$$
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/n_k.png)


## 相图和陈数

 $$\delta = 1/12$$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig2.png)

(1) **在小的 $J_2$ 和 $t_2$ 区域, 出现一个赝能隙相, 这个相里面主要是 CDW order 和 短程的 d-wave SC 涨落**

(2) **TSC (拓扑超导) 会在次近邻强度中等的区域出现, d-wave 超导出现在较大的的次近邻耦合区域**

(3) **To identify the topological nature of the phases, we perform the inserting flux simulation flux adiabatically**
**with $\theta_F \rightarrow \theta_F + \Delta \theta_F$, and $\Delta\theta_F = 2\pi/16$**

(4) We measure the accumulated spin 

$$Q_s = n_{\uparrow} - n_{\downarrow}$$

$n_{\sigma}$ is the total charge with spin $\sigma$ near the edge. 

(6) **在次近邻强度中等的区域，可以获得非零的 $\Delta Q_s$, 随着 $\theta_F$ 线性增加，如 Fig2(a)**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig3.png)

(7) **当 $\theta_F$ 从 0 变到 2$\pi$ 的时候，陈数变化为：**

$$C = \Delta Q_s = 2.0$$

**这刻画了一个非常稳定的时间反演对称性的拓扑态**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig4.png)

> **这里的拓扑性质是怎么刻画的？** 

> **用无限大DMRG算法来计算 flux 的绝热过程**

> **在左边缘测量每一个累计自旋 $Q_s = n_{\uparrow} - n_{\downarrow}$, $n_{\sigma} 是在边缘**
> **自旋 $\sigma$ 对应的总的电荷, 当 $\theta_F$ 从 0 变化到 $2\pi$ 的时候, 陈数就等于 $\Delta Q_s$**

> **这里的 $\theta_F$ 是什么了？**

> **平均格点能量 E_0 随着 $\theta_F$ 平缓的变化, 表示 gapped spectrum flow and robust topological quantization**

> **在DMRG中设置复数的波函数？ Because the time-reversal symmetry is breaking spotaneously, we can iidentify**
> **nonzero Chern number C = 2/-2 with equal probability in our DMRG simulation with random initial complex wavefunction**

> **C = 2 identifies the number of chiral Majorana edge modes (马约拉纳边缘模式)**

> **获取陈数沿着 $t_2/t_1$^2 = J_2/J_1, 为什么选择这样的参数路径？**

> **The chiral orders after bond-dimension scaling to M$\rightarrow \inf$ limit remain finite, supporting**
> **the spontaneous TRS breaking in the TSC, 手征序的出现意味着在TSC中发生了时间反演对称破缺**

> **在 t_2 = J_2 =0  的情况下，自旋单态配对关联为 0, 在 CDW+SDW 相中，配对关联会稍微增强，在TSC 和 SC 中会显著增强** 
> 
## 自旋结构因子和电荷占据数

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig5.png)


## 不同相中关联函数和序参量的表现

### CDW + SDWF 相

**CDW + SDEF 相，是一个类赝能隙相（pseudogaplike phase）, 在小的次近邻耦合下，会同时存在**
**强的自旋密度波涨落(strong density wave fluctuation,SDWF),涨落超导(fluctuating superconductivity,FSC)**
**这种共存会是出现超导的一种趋势**

(1) **$t_2 = J_2 = 0$的时候，自旋关联指数衰减，关联长度为 $\xi_S \approx 9.2$**,
**说明没有磁序，而且短程的自旋密度波函数(SDWF)**
![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig6_1.png)

(2) **$t_2 = J_2 = 0$的时候，对比自旋关联函数，单粒子关联函数，密度关联函数，配对关联函数，**
**尽管自旋关联函数相对来说还是最强的，单粒子关联函数的指数衰减关联长度为 $\xi_G\approx 3.7$**
**尽管配对关联函数也衰减的非常快，但是比两个单粒子关联函数要强的多，**
**这意味着单粒子通道会被压制**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig6_2.png)

(3) $(t_2/t_1)^2 = J_2/J_1 = 0.02$, **配对关联增强，代数衰减, 代数衰减指数为 $K'_{SC}\approx 1.05$,**
**配对关联是短程的，也就是存在强的局域配对，这是一种涨落超导（fluctuating superconductivity, FSC）**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig6_3.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig6_4.png)

**配对关联和单粒子关联的平方都会显著增强，在大距离下，配对关联比单粒子关联的平方大4个量级**
**这是一种赝能隙的行为。**

**进一步探索涨落超导的行为，我们在巨正则系统中调节化学势，哈密顿变为 $H\rightarrow H - \sum_i\mu_i n_i$,**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig6_4.png)

**可以看到有限的d-wave超导配对序**

> **(e)子图的计算是怎么做出来的** 

> **(e) 当 n > 20% 的时候，配对序全部变为0，意味着什么了？**

### TSC 相, 拓扑超导相

**陈数 C=2, 出现时间反演对称性，超导配对关联呈现代数衰减，指数为 $K_{sc}\approx 1.0$, 强于自旋关联和电荷关联**
**是二维拓扑超导体的准一维态.**

(1) **通过截断尺寸外推，可以看到代数衰减的配对关联函数**
**当 $(t_1/t_2)^2=J_1/J_2=0.05$, $|P_{bb}(r)|\sim r^{-K_{SC}}$**, **K_{SC}\approx 1.03**
**这表明在零温极限下，会有发射的超导磁化率**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig7_1.png)

(2) **为了验证配对对称性, 我们配对序重新写为:**

$$\Delta_{\alpha}(\textbf{r}) = |\Delta_{\alpha}(\textbf{r})|e^{i\theta_{\alpha}(\textbf{r})}$$

$$P_{\alpha\beta}(\textbf{r})=|P_{\alpha\beta}(\textbf{r})|e^{i\phi_{\alpha\beta}(\textbf{r})}$$

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig7_2.png)

>**这个计算是这么做的，虚数部分是怎么处理的呢**

> **d+id-wave 配对对称性**

**在TSC中观察到的是 $\theta_{ba}=\theta_{ac}=\theta{cb}\approx 2\pi/3$, 是一种 d+id wave 配对对称性**

**在 SC 中观察到的是 $\theta_{ba} = \theta_{cb} = \pi$**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig7_3.png)


**在TSC中，自旋关联函数和单粒子关联函数都是指数衰减的，密度关联函数是代数衰减的，但是衰减指数比较大 $K_{CDW}\approx 2.4$**
**在所有的关联函数中，配对关联函数是主要的关联函数。**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-t'-J-model-2023-SSGong/fig7_4.png)


## nematic d-wave SC, 向列D波超导

**在大的次近邻相互作用下，向列D波超导相会出现，打破旋转对称性的各向异性配对关联(anisotropic pairing correlations breaking rotational symmetry)**
**这和 $J_1-J_2$ 自旋液体中发现的超导是一样的。[55]**

> **参考文献[55]似乎不太正确**

