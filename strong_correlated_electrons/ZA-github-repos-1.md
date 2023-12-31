# Useful github repos

# Tensors

## iPEPS

(1) [iPEPS.jl](https://github.com/yitan1/iPEPS.jl) by yitan1, related to this paper by Corboz
[Automatic differentiation applied to excitations with projected entangled pair states](https://scipost.org/SciPostPhys.12.1.006).
**This is a julia package about basic implementation of iPEPS, including optimization of the ground-state and excitedstate.**
**We use CTMRG contraction algorithm, and use autodiff to solve the gradient**

(2) [ad-peps](https://github.com/b1592/ad-peps) Basic implementation of iPEPS ground-state and excited-state optimization
using automatic differentiation. More extensive documentation can be found at [https://b1592.github.io/ad-peps]( https://b1592.github.io/ad-peps).

(3) [ipeps](https://github.com/rezah/ipeps) 2D ipeps code, including simple, full and variational update.
Use different branches for symmetry. 

(4) [iPEPS](https://github.com/xichuang/iPEPS) Symmetric iPEPS algrithm based on itensor for spin and **fermionic system**. 
Including simple, full and fast full update in the current stage.

## learning for tensor network

(1) [tense_example](https://github.com/ryuikaneko/tenes_example), 
examples of iTPS/iPEPS calculation by TeNeS(Tensor Network Solver)

(2) [学习tensor基础算法中的一些基础缩并写法和缩并规则以及基础的算法](https://www.tensors.net/code)

# DMRG

## using itensor to realize DMRG

(1) [DMRG with sine square deformation by ITensor](https://github.com/ryuikaneko/ssd_dmrg_by_itensor)

Gtand canonical finite-size numerical approach by sine square deformatiion of a given Hamiltonian,
related works, [Grand canonical finite-size numerical approaches: A route to measuring bulk properties in an applied field](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.86.041108),
[Grand canonical finite size numerical approaches in one and two dimensions: Real space energy renormalization and edge state generation](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.87.115128).

(2) [RPMPS-T](https://github.com/ShimpeiGoto/RPMPS-T)

This is the ITensor based implementation of random phase matrix product states with Trotter gates (RPMPS + T)
approach proposed in [Matrix product state approach for a quantum system at finite temperatures using random phases and Trotter gates](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.104.045133) 
to simulate quasi one-dimensional quantum many-body system at finite temperatures.

**可以用来模拟有限温度的情况**

The purpose of this implmentation is to explain the approches to reader by working example.
So we dropped some optimizations especially on the composition of Trotter gates on purpose.


# Exact Diagonalization

(1) [exact diagonalization](https://github.com/ryuikaneko/exact_diagonalization)

* Python and Julia codes of exact diagonalization
* Use sparse matrices
* Sz conseved/ Sz nonconseved
* Sz conserved case: algorithm based on titpack2 and HPhi
  
(2) [C++代码实现严格对角化](https://github.com/awietek/hydra) by [Alexander Wietek](https://github.com/awietek)

A C++ library to perform efficient Exact Diagonalizations of quantum many body systems.

**Features**
* Basic algebra of operators in quantum many-body systems
* Iterative linear algebra for computing eigendecompositions and time-evolutions (e.g. Lanczos algorithm)
* Local spin, t-J, or fermionic models
* Full support of generic space group syymmetries
* parallelization both with OpenMP and MPI
* modern C++17 impementation simplifying usage.

# Codes of ryuikaneko

(1) [The publications of ryuikaneko and related codes](https://github.com/ryuikaneko/codes_for_my_publications)

[Rényi entanglement entropy after a quantum quench starting from insulating states in a free boson system](https://arxiv.org/abs/2207.08353)

[Magnetic field induced competing phases in spin-orbital entangled Kitaev magnets](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.2.013014)

[Gapless Kitaev Spin Liquid to Classical String Gas through Tensor Networks](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.123.087203)

[Thermal algebraic-decay charge liquid driven by competing short-range Coulomb repulsion](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.97.205125)

[Suppression of topological Mott-Hubbard phases by multiple charge orders in the honeycomb extended Hubbard model](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.97.125142)

[Emergent lattices with geometrical frustration in doped extended Hubbard models](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.94.195111)

[Spontaneous symmetry breaking in correlated wave functions](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.93.125127)

# Usefule repos' authors:

(1) [ryuikaneko](https://github.com/ryuikaneko?tab=repositories) repos 信息非常丰富

(2) [Alexander Wietek](https://github.com/awietek) 严格对角化的c++代码和python 代码

(3) [Hasik](https://github.com/jurajHasik?tab=repositories) 有很多的关于 ipeps 模拟复杂两维量子多体系统的代码
    
* [j1j2_ipeps_states](https://github.com/jurajHasik/j1j2_ipeps_states) Infinite PEPS states for J1-J2 model on a square lattice.
* [peps-torch](https://github.com/jurajHasik/peps-torch) A tensor network library for two-dimensional lattice models.
peps-torch performs optimization of iPEPS. The energy is evaluated using enviroments obtained by the corner-transfer matrix (CTM)
algorithm. Afterwards, the gradients are computed by reverse-mode automatic differentiation (AD). 
* [pi-peps](https://github.com/jurajHasik/pi-peps) C++ library on top of ITensor for running iPEPS simulation 
of two dimensional spin systems. Wavefunctions are optimized through Simple Update or Full Update. Expectation values
and environments are computed by directional CTMRG algorithm. 
* [tensorgrad](https://github.com/jurajHasik/tensorgrad) Differentiable Programming Tensor Networks

(4) [yitan1](https://github.com/yitan1)

* [iPEPS.jl](https://github.com/yitan1/iPEPS.jl) This is a julia package about basic implementation of iPEPS,
including optimization of the ground-state and excited state. We use CTMRG contraction algorithm, and use autodiff to 
solve the gradient. 
* [uMPS.jl](https://github.com/yitan1/uMPS.jl) uniform Matrix product state
* [PhyOperators.jl](https://github.com/yitan1/PhyOperators.jl) PhyOperators
* [ad-peps](https://github.com/yitan1/ad-peps) Basic implementation of iPEPS ground-state and excited-state optimization automatic differentiation

(5) [niusen](https://github.com/niusen)

* [Symmetric_IPEPS](https://github.com/niusen/Symmetric_IPEPS)
* [Gaussian-fermion-peps](https://github.com/niusen/Gaussian-fermion-peps)
* [GfPEPS_parton](https://github.com/niusen/GfPEPS_parton)
 
(6) [rezah](https://github.com/rezah) 他的代码都是用Python写的 

* [ipeps](https://github.com/rezah/ipeps)
* [QMERA](https://github.com/rezah/QMERA)
* [fPEPS](https://github.com/rezah/fPEPS)
* [cpeps](https://github.com/rezah/cpeps)
* [qMPS](https://github.com/rezah/qMPS)
* [unitary-tensor-network-operator](https://github.com/rezah/unitary-tensor-network-operator)


# Useful softwares related to tensor network

(1) [TeNeS](https://github.com/issp-center-dev/TeNeS)
 
 * TeNeS (Tensor Network Solver) is a solver for 2D quantum lattice system based on a PEPS wave function and 
 * the CTM method. TeNeS can make use of many CPU/nodes through an OpenMP/MPI hybirid parallel tensor operation
 * library mptensor.