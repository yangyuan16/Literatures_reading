##### MDA
* ideas
> 采用经典的机器学习方法来研究量子多体系统的基态问题首先面临的一个问题就是输入数据的矢量化。基于张量网络计算的量子系统的基态从数据结构（sample structure）角度来看是一系列的多指标张量，而从经典问题中（如图像识别，自然语言处理）发展而来的神经网络等机器学习方法处理的输入数据是特征矢量数据。Yang, Sun, Ran and Su (2021) 年的文章中已经揭示直接将基态张量结构拉成一个特征矢量输入到t-SNE 方法中，不同量子相对应的基态并不能聚类，这是因为破坏掉了基态物理空间和几何空间直接的关联 （比如，对于自旋系统，就是MPS中的物理指标和虚拟指标之间的关联）。
针对这一问题，人们采用神经网络研究量子多体系统的基态问题的时候，一般有如下的方案：Ran 的一篇文章中将量子态表示为图片的形式，图片内部为分形结构。
这一方案把张量网络态的虚拟指标全部缩并，只留下了物理指标，这一方案的
缺点是物理希尔伯特空间是指数大的，因此生成的图片表示也是有限大的，这样导致事实上神经网络处理的量子系统的尺寸较小。
在另外一篇有名的nature文章中，作者是用张量网络基态的纠缠普来代表输入数据的
特征矢量处理量子基态问题。

> 针对这一问题，我们提出了MDA方法来处理具有张量结构的输入数据，能够同时考虑到物理空间和辅助虚拟空间之间的关联，使得使用机器学习方法处理量子基态相变问题上变得更为自然，不需要在关键的输入数据这一步丢失掉重要的信息。 

> 我们的方法是 LDA（线性判别分析）方法在具有张量结构的输入数据上的拓展。

>我们采用了MDA 方法，能够考虑到 我们在横场Ising model 上做了验证，
不同于LDA处理的是数据特征矢量，MDA 可以直接处理张量形式的样本数据。

##### similar concepts

##### similar methods
* Multilinear principal component analysis (MPCA) with github address <https://github.com/pykale/pykale/tree/7ba8e4fd06b2b5d7c8a04ebcb58b0d2abbfa2b08/examples/cmri_mpca>

* 这里可以引生出很多其他想法，除了 MPCA ，还有量子版本的PCA, 也就是量子PCA [Lloyd, 2013](https://www.nature.com/articles/nphys3029), 可以得到这样一个题目 “PCA-based methods to study quantum many-body systems”, 可以总结出很多基于PCA的方法把量子基态研究一下。

* [Kelly et al. (2019)](https://cireqmontreal.com/wp-content/uploads/2019/12/pruitt.pdf) suggest a new modeling approach known as instrumented principal components
analysis (or IPCA). IPCA inherits Barra's versatility and tractability, yet avoids its statistical
inefficiency via a built-in dimension reduction:

* idea tips
> 1, can this methods used to analysis PEPS, the two dimensional quantum many-body system


##### reference
* Tensor Representation in High-Frequency Financial Data for Price Change Prediction, arXiv:1709.01268v4 





