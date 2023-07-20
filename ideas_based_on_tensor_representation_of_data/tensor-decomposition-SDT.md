##### SDT
* ideas
> 将基态张量中的自旋指标看作是 R 指标 （对应于文献 “Unveil stock correlation via a new tensor-based decompositionmethod” 的标记），这样就可以分别在spin space 中得到 slice-diagnoal matrix. 
这样的diagnoal matrix 一定情况下应该反映出基态的情况，
成为判断基态相变的一个新的 information criterion. 

* plans 
> 1 把 Ran 用 Pytorch 实现张量分解的那些video看一下，并把代码写一遍
> 2 利用 Pytorch 自动微分技术把 SDT 实现出来。

* advantages of SDT
> compared with Turker decomposition, 
for SDT, restrictions on the core tensor reduce 
the possible rotation of the components,
improving uniqueness of the decompositiion.
(什么是 bilateral trade matrix? 可否通过该 matrix 将物理和金融联系起来呢？)

> A final advantage of this representation is 
achieved when we deal with skewed, asymmetric tensors, e.g. the bilateral trade matrix. 
Tucker decomposition is unable to retrieve the full asymmetry in the bilateral exposures. 
(在这种情况下，Tucker分解无法恢复双边敞口中的完全不对称性。)
This is because part of this asymmetry is incorporated on the 
core tensor off-diagonal values, while the remaining part is 
incorporated in the factor matrices.
(这是因为这种不对称性的一部分包含在核心张量的非对角线值上，而其余部分包含在因子矩阵中)
On this issue, [48] proposed the RESCAL decomposition which 
restricts the Tucker-2 model such that the factor matrices over the 
bilateral exposures are constrained to be equal so that the asymmetry is 
only reflected in the core tensor 
(关于这个问题，[48] 提出了 RESCAL 分解，该分解限制了 Tucker-2 模型，使得双边暴露上的因子矩阵被约束为相等，使得不对称性仅仅反映在核心张量中)
<font color=red> 什么是 Tucker-2 model ?</font>
Tucker-2 decomposition is a Tucker factorization with only two factor 
matrices estimated and the remaining constrained to be the identity matrix
(Tucker-2 分解就是对于三阶张量，只分解出两个非单位矩阵的 factor matrix, 另一个指标对应于一个单位矩阵。)

> In contrast to RESCAL, the SDT decomposition, haveing a core tensor which 
is slice-diagonal, has only the variance weights on the core and any asymmetry in the data is embedded in the factor matrices. 
The factor components of the SDT decomposition, as for the other ones, are 
estimated via an optimization problem which minimizes the Frobenious norn 
of the error with respect to the data tensor X.
(与 RESCAL 相反，具有切片对角线的核心张量的SDT分解在核心上只有方差权重，并且数据中的任何不对称性都嵌入到因子矩阵中。与其他分解一样，SDT分解的因子分量是通过最优化问题估计的，该优化问题使用关于数据张量 X 的误差的 Frobenius 范数最小化。)
(<font color = red> 什么是 Frobenius 范数</font>)

> 

##### related concepts

* Frobenius 范数
> The Frobenius norm, sometimes also called Euclidean norm
(a term unfortunately also used for the vector $L^2$-norm ),
is matrix norm of an m * n matrix A defined as the square root
of the sum of the absolute squares of its elements,
$$ ||A||_F = \sqrt{\sum_{i=1}^{m}\sum_{j=1}^{n}|a_{ij}|^2}$$ 

It is also equal to the square root of the matrix trace of 
$AA^H$, where $A^H$ is the conjugate transpose, i.e.,
$$||A||_F = \sqrt{Tr(AA^A)}$$

##### reference