# MKL 编程

## [Windows 系统VS环境中MKL安装与使用(makefile)](https://zhuanlan.zhihu.com/p/169330623)

## [win10下VS2017 Intel mkl 2019版本库手动安装](https://zhuanlan.zhihu.com/p/640575484#:~:text=%E9%85%8D%E7%BD%AEVS%E5%B1%9E%E6%80%A7%E9%A1%B5%E9%9D%A2%E7%9A%84VC%2B%2B%E7%9B%AE%E5%BD%95,%E7%84%B6%E5%90%8E%E5%9C%A8%E9%93%BE%E6%8E%A5%E5%99%A8--%3E%E8%BE%93%E5%85%A5--%3E%E9%99%84%E5%8A%A0%E4%BE%9D%E8%B5%96%E9%A1%B9%E4%B8%AD%E6%B7%BB%E5%8A%A0mkl_intel_lp64.lib%3Bmkl_intel_thread.lib%3Bmkl_core.lib%3Blibiomp5md.lib%3B%20%E6%B3%A8%E6%84%8F%EF%BC%8C%E8%BF%99%E9%87%8C%E5%A6%82%E6%9E%9C%E4%BD%BF%E7%94%A8%E7%9A%84%E6%98%AF32%E4%BD%8D%E7%B3%BB%E7%BB%9F%EF%BC%8C%E5%88%99%E5%B0%86mkl_intel_lp64.lib%E6%8D%A2%E6%88%90mkl_intel_c.lib)

## [vs2022+MKL](https://blog.csdn.net/m0_63111108/article/details/124734432)

* 项目文件夹"learn-mkl-3" 右键找到项目属性

![](https://github.com/yangyuan16/Literatures_reading/blob/main/Programming/figs_MKL/fig1.png)

* 在 Intel Libraries for oneAPI 中把 Use oneMKL 设置成 Parallel
* 在 VC++目录中，设置可执行文件目录：C:\Program Files (x86)\Intel\oneAPI\mkl\2022.1.0\bin\intel64 
* 包含目录：C:\Program Files (x86)\Intel\oneAPI\mkl\2022.1.0\include
* 库目录（有两个）：C:\Program Files (x86)\Intel\oneAPI\mkl\2022.1.0\lib\intel64  ; 
* C:\Program Files (x86)\Intel\oneAPI\compiler\2022.1.0\windows\compiler\lib\intel64_win

连接器->输入->附加依赖项 加入lib文件

![](https://github.com/yangyuan16/Literatures_reading/blob/main/Programming/figs_MKL/fig4.png)


* 运行时出现的一些问题找不到 mkl_intel_thread.2.dll

![](https://github.com/yangyuan16/Literatures_reading/blob/main/Programming/figs_MKL/fig2.png)

![](https://github.com/yangyuan16/Literatures_reading/blob/main/Programming/figs_MKL/fig3.png)


* 将 mkl_intel_thread.2.dll 的路径放到里面，确定。路径放到里面，确定。