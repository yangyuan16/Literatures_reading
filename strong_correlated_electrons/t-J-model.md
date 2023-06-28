# t-J-model 

# t-t'-J model on Square lattice 
参考文献 [Ground-state phase diagram of the t-t'-J model](https://www.pnas.org/doi/10.1073/pnas.2109978118)

## 系统的哈密顿量

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-J-model/fig1.png)

(1) t' < 0 属于空穴掺杂；t'>0 属于电子掺杂

(2) $n_i^{tot} = n_{i\uparrow} + n_{i\downarrow}$ 是格点 i 上面的总粒子密度 (total particle density on site i)

(3) Doubly occupied states are specifically excluded in the Hilbert space (在希尔伯特空间中，双占据态被明确地排除在外。)

(4) set t=1, J=0.4 (J=0.4t 处于实际高温超导材料的参数区间)

(5) A chemical potential $\mu$ is used to control the doping level in some of calculation 

(6) For t'/t < 0, it describes a hole-doped system with electron filling $n_e = 1-x$

(7) For t'/t > 0, based on a particle-hole transformation, it describes an electron-doped 
system with $n_e = 1+x$


## 序参量选择

Focus on local measurements of the density, the magnetization, and pairing. 

(1) magnetization:  $S_z = \frac{1}{2}(n_{i\uparrow} - n_{i\downarrow})$

(2) hole density: $n_{hold} = 1 - n_{i\uparrow} - n_{i\downarrow}$

(3) singlet (s) and triplet (t) link pairing operators:

$$\Delta_{s,t}^{+}(l) = \frac{1}{\sqrt{2}}(C_{l_1,\uparrow}^{+}C_{l_2,\downarrow}^{+} \pm C_{l_2,\uparrow}^{+}C_{l_1,\downarrow}^{+})$$

**"+" for singlet, "-" for triplet** 

> **为什么 '+' 代表单态, '-' 代表三重态?**

(4) $\langle\Delta^{+} + \Delta\rangle$ gives the local pairing strength. For d-wave superconductor, 
$\Delta_s^{+} + \Delta_s\rangle$ switches sign between bonds in the x and y directions. 

## DMRG 计算过程

(1) 为了防止计算到 metastate states 上, we perfrom a variety of simulations with different starting states 
and temporary pinning fields, comparing energies and convergence of different states. 
(**我们用不同的起始态和临时钉扎场进行了各种模拟，比较了不同态的能量和收敛性**)

(2) 在态的选择上，在许多情况下，例如传统的条纹状态(striped state)，
从直积状态开始，**在直积态的末端应该是一个空穴**，这是所有必要的，**人们应该尝试不同的填充和条纹间距**

(3) 例如，**条纹状态下的八个空穴可能会形成两个四空穴条纹或四个两空穴条纹**。在这种情况下，我们会尝试两种可能性并比较能量。

(4) **Doping x ($n_e = 1-x$ or $n_e = 1 + x$) varies shlowly along the length of the cylinder.** 

(5) **x is fixed, t' slowly varing along the length of the cylinder**

(6) **Spontaneously broken symmetry in DMRG**

> 这样的设定在代码中怎么实现的？

> **第(4)点和 第（5）点怎么理解呢？, x 和 t' 沿着 cylinder 是变化的**

> **DMRG中的自发对称破缺应该怎么做呢？**

## t-t'-J 模型的背景和设定

(1) The t-J model cannot be doped above half-filling, so it does not appear that one can simulate electron-doped cuprates.
**t-J 模型不能在半填充以上掺杂，因此似乎不能模拟电子掺杂的铜酸盐。**

(2) However, a particle-hole transformation of the single-band Hubbard model maps electron doping to hole doping,
but with a change in the sign of t' (**单带Hubbard模型中的粒子空穴变换可以将电子掺杂映射为空穴掺杂，相应的 t' 的符合会发生变化**)

(3) t-J 模型可以被视作 particle-hole-transformed Hubbard model 的低能描述。

(4) **我们可以将 t' = -0.2 可以视作空穴掺杂的铜酸盐**
**将 t' = 0.2 为电子掺杂的铜酸盐**

## 相图

(1) 在 t'- x 的参数空间中做出相图

> **x is the doping, x 和哈密顿里面的化学势 $\mu$ 是什么关系**

(2) Much of the phase diagram is taken up by a phase with conventional stripes 
(**相图的大部分区域被传统的条纹相占据**)

(3) These stripes are lines of increased hole density two or three sites wide, which act as domain
walls to $\pi$-phase shifted AFM (or at least significant local AFM correlations) 
(**这些条纹是两个或三个位点宽的空穴密度相，这些条纹相当于移动了一个 \pi 相位的反铁磁畴壁，至少在局域的反铁磁关联很显著**)

(4) Although the holes in these stripes correlate into pairs, the pairs tend to lack phase coherence, and 
pairing correlations are weak. 
(**尽管这些条纹相中的空穴相互关联成对，但成对往往缺乏相位相干性，并且配对关联较弱**)

(5) Signigicantly, negative t' is found to decrease the pairing correlations, this phase makes up 
most of the t'<0 side of the diagram. (**空穴掺杂会导致配对关联减弱**)

(6) 

### t' < 0 空穴掺杂的情况

(1) 在 t' < 0 的空穴掺杂区域，发现了一个非常规的条纹相 W3 striped phase, 
在 W3 striped phase 中，**条纹宽度为一个位点宽，它们之间正好有两排大部分未掺杂的位点**
**作为自旋梯子(spin ladder)**。

(2) The holes within stripes are unpaired with a spacing of about 4 between holes 
(**条纹内的孔是不成对的，孔之间的间距为 4**)

(3) The Heisenberg two-leg ladder is spin gapped, with very short-range spin correlations, and the 
"ladders" in the W3 phase behave similarly. 
(**海森堡两腿梯子自旋模型是一个有自旋能隙的模型，自旋关联非常短程，W3 条纹相中的自旋梯子也是类似的**)

(4) **W3 条纹相中不存在 \pi-phase shift to the spins on either side, 这大概率是由于条纹相中低掺杂的孔穴和短程自旋关联的结合**
**W3 条纹相中的空穴并没有形成筹壁，相反它将自旋梯子进行了解耦合**

(5) **W3 相似乎在未掺杂的自旋梯子（spin ladder）和掺杂了空穴的链之间有实质上的解耦，并且横向周期为三个格点宽度**

(6) **W3 中并不存在配对关联，条纹相很快会将 AFM order 破坏掉**

### t'> 0 电子 弱掺杂区域

(1) t' = 0.2, x = 0.12, with simultaneous pairing and AFM order. 
The higest-probability configuration of a pair of holes is diagonal next-nearest neighbor. 
(**一对空穴的最高概率配对构型是对角次近邻**。)

> 配对是的时候，电子或者空穴的自旋必须是自旋指向一致的吗？

(2) t' 只是刚刚大于零的时候，系统会同时出现三个相。分别是占据主要部分的两个相，AFM 相 和 d-wave 超导。
[这两个相在最近研究Hubbard模型的文章中也被发现](https://arxiv.org/pdf/1907.01909.pdf). 
加一点点掺杂，在这个区域看不到条纹相，而且磁序为 Q = ($\pi,\pi$). 
**在这一区域可以看到很明显的 d-wave 超导** 

(3) t' 只是刚刚大于零的时候，系统会同时出现三个相。**除了反铁磁和 d-wave 超导，还会出现p-wave 超导**，
**p-wave 超导序在这一区域相对而言有点弱。** **弱的p-wave超导是由AFM 和d-wave超导结合形成的**
**弱的p-wave超导的出现是由于 AFM 的出现破坏了 SU(2)对称性，因此单态和三重态的配对不再显著**
**在p-channel 中并没有看到单独的具有吸引力的常规相互作用，因此这一区域 p-wave 超导的出现来源于 AFM 和 d-wave超导**

### t' > 0 的电子 高掺杂区域

(1) **会出现超导条纹相**

(2) **超导条纹相，从局域的角度来看，像一个低浓度掺杂的相，但是会有条纹出现**

(3) **这些条纹相看上去和传统的条纹相非常像，但是这里的条纹相呈现出明显的 d-wave 配对，这和空穴掺杂区域的条纹相完全不一样**

(4) **这些条纹相是反铁磁序的筹壁，而且局域的可以看到由条纹相调制的 \pi-p-triplet order**

(5) **在高浓度参杂的区域，triplet 配对变得很弱，很大程度上是由于条纹相导致的**

(6) **尽管超导和条纹相在一定程度上属于竞争关系，单最主要的导致配对不能成型的原因是负的t'(也就是空穴掺杂)**

(7) **正的t'会增加电子配对的流动性，使得它们很容易形成相位相干（phase cohere）, 从而避免被锁定到某些条纹中（locked into stripes）**

## 构型图

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-J-model/fig3.png)

### A 子图和 B子图

(1) **A子图和B子图都是 d-wave 超导态，可以看到 空穴都形成了配对，形成对角次近邻配对**

(2) **B图中能看到明显的对角条纹(diagonal stripe)**

> **为什么 A 子图和 B 子图都是 d-wave 超导态呢，这是怎么看出来的呢**

### C 子图和 D子图

(1) pairs of holes appear as the most probable state, but the state has only short-ranged pairing correlation 
and the small hole probability between the stripes suggests that the binding of the pairs to the stripes is 
suppressing superconductivity
(**成对的空穴似乎是最有可能的状态，但这种状态只有很短的配对相关性，条纹之间的小孔概率表明成对与条纹的结合抑制了超导性**)

> **超导被抑制是怎么看出来的？**

### E 子图 和 F 子图

(1) **是 W 条纹态**

(2) **在条纹中，最可能态对应着空穴有着最大的分开距离 (maximum separation), 畴壁在垂直于空穴的方向上清晰可见，并不是竖直方向**

(3) **这种构型和一维的 t-J 模型的条纹是一致的，人们可以将这些空穴视作生活在压缩的海森堡自旋链中的全息子**

### 寻找 A,B,C,D,E,F图中的态

(1) An alternate view is given by the high-probablility product state plots in B, D, F.
These product states are determined from the ground state by a limited search for the most probable product states. 

(2) One way to search for a probable spin configuration is to sequentially go through the site of the lattice and,
at each site, pick the most probable spin state

(3) After each spin is picked, the wavefunction is projected to reflet this, just as a physical measurement of 
spin i (say finging the up state) would leave the wavefunction projected into the associated up-i space

(4) However, this approach fails in the presence of holes, sice at low doping there are far fewer holes than spins,
and the holes end up appearing at the end of the search path 
(**然而，这种方法在存在空穴的情况下失败了，因为在低掺杂时，空穴比自旋少得多，并且空穴最终出现在搜索路径的末端.**)

(5) Here we search for the hole position separately, finding the most probable position for a hole over all sites at each
step, using the hole density of the projected wavefunction. 
(**在这里，我们分别搜索空穴位置，使用投影波函数的空穴密度，在每个步骤的所有位置上找到空穴最可能的位置**)

(6) After the holes are found, then we perform a determination of the spin configuration with a fixed 
path through the reset of the sites, optimizing each spin and projecting. 
(**在发现空穴后，我们通过重置位置，以固定路径确定自旋配置，优化每个自旋和投影**)

> **这个最大概率的直积态是不是通过计算保真度得到的？**

> **这个选择态的过程是怎么实现的？**

> **空穴出现在搜索路径的末端是什么意思？**

> **自旋构型中domain wall 是怎么画出来的？**

> **(A)子图为什么超导配对是非对角的，这个是怎么看出来的？**

> **(B)子图的对角条纹态(diagonal stripe)是怎么看出来的？**

> **(C)子图是怎么看的？怎么能够看出来条纹？(pairing is visible within the stripes, but lacking phase coherence)**

> **(E) 和 (F) 子图是怎么看出来空穴没有配对的？(holes unpaired within the stripes), 怎么看出条纹的？**


## 参数空间扫描相图

(1) **扫描相图最最需要注意的地方就是确定态是否是亚稳态(metastable state)**

(2) In nonscan calculations where one is looking for a particular order, it is common to 'pin the edges' with a 
corresponding field applied to the edge sites. 
(**在寻找特定顺序的非扫描计算中，通常将相应的场应用于边缘位置来“固定边缘”**)

(3) The gist is that DMRG tends to break a continuous symmetry and develop an order parameter just as a 
real experimental sample does 
(**要点是，DMRG倾向于打破连续对称性，产生出一个序参量，就是真实的实验样本一样**)

(4) **在大的保留截断的极限下，对称性的破坏会消失，对于中等的截断，系统产生了一个序参量，序参量的量级与2D**
 **热力学极限下的量级相似**

(5) **消除对称破缺所需要的截断维数随着系统尺寸会迅速增加，试图收敛到不发生对称破缺可能会适得其反，因为在满足对称性的相中**，
**序参量只能通过关联函数来观察，并且可能错过一些意味的序参量, 另外关联函数本质上远不如局域测量准确**

(6) **当系统中存在很强的 d-wave 超导相的时候，我们不采用外加 pin field, 而是让系统 self-pin**

(7) **当系统中 d-wave 超导， 我们加载一个弱的全局的配对场，通过这一方式，如果 SC 不存在的话，那么这就是一个**
**清晰的信号，超导态并不是最低能态**

(8) **在一些情况下，我们会在系统的边缘加一个pin场来减少edge effect, 这样的pin field并不会影响bulk 的磁序**


> 这个过程是怎么做的？

> 第(4)点是怎么理解呢？

> 第(5)点怎么理解呢？

### 固定 t' 沿着 x 方向扫描

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-J-model/fig4.png)

(1) **随着掺杂的增加，远离半填充，配对迅速增加**

> **这个图 x 方向对应的是晶格的 x 方向吗？**

> **d-wave 单态配对关联为什么有正有负呢？**

### 固定 x 沿着 t' 方向扫描

(1) **在 t' 变化的情况下，还需要调整化学势 $\mu$, 以保持整个系统的掺杂大致恒定**

$$\mu{(l_x)}=\mu_0 + a\sqrt{1+(b|2l_x-L_x|/L_x)^2}$$

(2) 

> **扫描这一块儿的时候为什么会加一个 pin field**

## 低电子浓度掺杂相，AFM, d-wave Singlet, ($\pi, \pi$) p-wave Trilet Pairing 共存

(1) **这一区域中，主要存在两种序参量，Uniform AFM order 和 强的 d-wave singlet 配对。**

(2) **同时还存在弱的 p-wave triplet 配对，P 波的配对是由于 AFM 和 d-wave 的共同存在导致的**

![](https://github.com/yangyuan16/Literatures_reading/blob/main/strong_correlated_electrons/figs-t-J-model/fig5.png)

(3) **(c)子图是 Triplet pairing 的示意图**

(4) **不管加多强的 pin 场，Singlet pairing 都是稳定的，Triplet pairing 会随着 pin 场的减小而减小**

(5) **这里不会出现其他竞争的态, 从非配对的直积态开始, 系统自发破缺了粒子数守恒的对称性，形成了配对序**

(6) $(\pi,\pi)$ p_x - p_y form:

$$\langle\Delta_t(l_x,l_y)\rangle = e^{i\pi(l_x+l_y)}[\langle\Delta_t(l_x,l_y,x)\rangle - \langle\Delta_t(l_x,l_y,y)\rangle]$$

$\Delta_t{(l_x,l_y,x/y)}$ being a triplet pairing on a horizontal/vertical link with left/lower site $(l_x,l_y)$

(7) **This triplet order is a consequence of the other two order, not a competing order**
(**三重态配对是来源与另外两个主要的序，也就是 AFM 和 Singlet pairing, 三重态配对并不是一个竞争序**)

(8) As mentioned before, the existence of AFM order breaks SU(2) spin symmetry, so that singlet and triplet 
pairings are no longer distinct, making the d-wave pairing have a triplet component. 
(**AFM有序的存在打破了SU(2)的自旋对称性，使得自旋单态和自旋三重态配对不再明显，使得d-wave配对具有三重态分量**)

(9) The magnitude of the triplet pairing is roughly proportional to that fo the singlet pairing, 
$\langle\Delta_t \rangle / \langle\Delta_s\rangle = 0.4$, if no magnetic field is applied, and this 
ratio is mostly t' independent. 

(10) It is interesting that there is no competition betwee strong AFM order and d-wave pairing;
they happily coexist, but as a consequence of increased AFM order, the triplet order gets larger. 
(**加了global 交错磁场之后, 由于 AFM 的增强, triplet pairing order 也增强了**)

(11) **三种序之间的关系很稳定**：

$$\langle\Delta_t\rangle = A(x)\langle\Delta_s\rangle\langle S_z\rangle$$

这一关系在文章[Coexistence of superconductivity and antiferromagnetism in the Hubbard model for cuprates](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.99.184510)也被发现

> 第（7） 点，**为什么三重态配对序是来自于其他两个序呢？**

> 第（8）点怎么理解呢？

## 高浓度电子掺杂相：Stripes with d-Wave Singlet and Striped p-Wave Pairing




## Questions: 


## 相关文献