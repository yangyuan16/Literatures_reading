# [OpenACC: 更多科学研究更少编程](https://developer.nvidia.cn/zh-cn/openacc)

(1) 如今，加速计算推动着某些最为激动人心的科学发现。对于寻求高速应用性能的科学家和研究人员而言，OpenACC 为他们带去了福音：
这是一款基于指令的编程模型，**无需费时费力的编程，便可为加速器提供简单而强大的加速方式**。
借助 OpenACC，单一源代码版本将实现平台间的性能可移植性。

(2) [加速GPU应用程序的主要方法有三种](https://developer.nvidia.com/zh-cn/blog/accelerating-gpu-applications-with-nvidia-math-libraries/)
编译器指令、编程语言和预编程库。编译器指令，例如OpenACC a 允许您顺利地将代码移植到GPU以使用基于指令的编程模型进行加速。
虽然它易于使用，但是在某些情况下可能无法提供最佳性能。

编程语言，例如CUDA C 和 C++ 在加速应用程序时，为您提供更大的灵活性，但是用户也有责任编写代码，利用新的硬件功能在最新的硬件
上实现最佳性能。

NVIDIA 数学库，作为 CUDA 工具包和高新能计算(HPC)软件开发工具包(SDK),提供各种计算密集型应用程序中遇到的函数的高质量实现。
这些应用包括机器学习、深度学习、分子动力学、计算流体力学(CFD)、计算化学、医学成像和地质勘测等领域。

这些库旨在取代常见的CPU库，如 OpenBLAS, LAPACK 和 Intel MKL, 并加速上的应用程序 NVIDIA GPU 代码更改最少。
为了展示这个过程，我们创建了一个双精度通用矩阵乘法(DGEMM)功能的示例，以比较 cuBLAS 与 OpenBLAS 的性能。

(3) 加速张量应用

这个 cuTENSOR 库是一个张量线性代数库实现。张量是机器学习应用的核心，是推到应用问题控制方程的重要数学工具。
cuTENSOR 提供了直接张量收缩、张量约化和元素级别张量运算例程。cuTENSOR 用于提高深度学习训练和推理、计算机视觉、
量子化学和计算物理应用中的性能。

(4) [TensorLy](https://developer.nvidia.com/zh-cn/blog/nvidia-research-tensors-are-the-future-of-deep-learning/) 
是 Python 中张量方法和深度张量化神经网络的高级API,旨在使得张量学习变得简单易懂。
基于张量的深度神经网络的正确实现可能很棘手，主要的神经网络库，例如 PyTorch 或 TensorFlow 
不提供基于张量代数方法层，并且对稀疏张量的支持有限。在 NVIDIA 中，通过对 TensorLy 项目和 Minkowski 引擎，
领导开发了一系列工具，以使得张量方法在深度学习中无缝使用。