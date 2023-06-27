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

(6) 

## 序参量选择

Focus on local measurements of the density, the magnetization, and pairing. 

(1) magnetization:  $S_z = \frac{1}{2}(n_{i\uparrow} - n_{i\downarrow})$

(2) hole density: $n_{hold} = 1 - n_{i\uparrow} - n_{i\downarrow}$

(3) singlet (s) and triplet (t) link pairing operators:

$$\Delta_{s,t}^{+}(l) = \frac{1}{\sqrt{2}}(C_{l_1,\uparrow}^{+}C_{l_2,\downarrow}^{+} \pm C_{l_2,\uparrow}^{+}C_{l_1,\downarrow}^{+})$$

**"+" for singlet, "-" for triplet** 

> **为什么 '+' 代表单态, '-' 代表三重态**

(4) $\langle\Delta^{+} + \Delta\rangle$ gives the local pairing strength. For d-wave superconductor, 
$\Delta_s^{+} + \Delta_s\rangle$ switches sign between bonds in the x and y directions. 

## DMRG 计算过程

(1) 为了防止计算到 metastate states 上, we perfrom a variety of simulations with different starting states 
and temporary pinning fields, comparing energies and convergence of different states. 
(**我们用不同的起始态和临时钉扎场进行了各种模拟，比较了不同态的能量和收敛性**)

(2) 在态的选择上，在许多情况下，例如传统的条纹状态(striped state)，
从直积状态开始，**在直积态的末端应该是一个空穴**，这是所有必要的，**人们应该尝试不同的填充和条纹间距**

(3) 例如，**条纹状态下的八个空穴可能会形成两个四空穴条纹或四个两空穴条纹**。在这种情况下，我们会尝试两种可能性并比较能量。

## 相图