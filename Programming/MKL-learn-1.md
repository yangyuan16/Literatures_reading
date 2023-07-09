# MKL 安装与使用 (makefile)

## MKL 库的主要用法：

* 使用MKL静态链接库的makefile设置
* 使用MKL动态链接库的makefile设置
* 矩阵相乘
* 矩阵SVD分解计算
* 线性方程组求解

## [在Windows系统Visual Studio中搭建MKL环境](https://zhuanlan.zhihu.com/p/169330623)

假设MKL的安装目录 d:/mkl/, MKL 的头文件数量众多，不宜为每个项目都复制一份

(1) 选择一个文件夹作为C++项目的工作文件夹，其中建立三个文件夹:\inc, \src, \tmp,
分别用于存放头文件, 源代码文件和临时文件。
