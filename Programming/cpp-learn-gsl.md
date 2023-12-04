[GSL的Linux安装和使用教程（小白教程）_linux安装gsl-CSDN博客](https://blog.csdn.net/weixin_42035282/article/details/131708094?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2~default~YuanLiJiHua~Position-2-131708094-blog-82113165.235^v38^pc_relevant_anti_t3&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~YuanLiJiHua~Position-2-131708094-blog-82113165.235^v38^pc_relevant_anti_t3&utm_relevant_index=5)

最新版下载链接：Index of /gnu/gsl

gsl-2.7.1.tar.gz	2021-12-01 00:33	7.2M
cd 下载目录

1. 解压压缩包：$ tar -zxvf gsl-2.7.1.tar.gz

2. 创建安装目录(自定义): 

mkdir /home/tx-deepocean/Library

cd  /home/tx-deepocean/Library

# 创建安装目录gsl_gcc

mkdir gsl_gcc

3. 进入源码目录:$ cd 下载目录/gsl-2.7.1

4. 配置configure文件：执行

$ ./configure CC="gcc" --prefix=/home/tx-deepocean/Library/gsl_gcc

# 参数含义
# ./configure -h: 可以得到配置的帮助信息
# CC:指定编译工具链
# --prefix: 指定库的安装目录
# --host: 指定安装平台,可选，交叉编译要制定安装平台如在arm上编译 --host=arm




5.使用make进行编译

$ make 

6.使用make install进行安装

$ make install
7.使用make installcheck检查安装是否成功
$ make installcheck
8. #编辑.bashrc文件
$ vi ~/.bashrc
在文件末尾添加如下代码：

export C_INCLUDE_PATH=$C_INCLUDE_PATH:/home/tx-deepocean/Library/gsl_gcc/include
export CPLUS_INCLUDE_PATH=$CPLUS_INCLUDE_PATH:/home/tx-deepocean/Library/gsl_gcc/include
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH::/home/tx-deepocean/Library/gsl_gcc/lib
export LIBRARY_PATH=$LIBRARY_PATH::/home/tx-deepocean/Library/gsl_gcc/lib
保存该文件，立刻加载修改后的设置，使之生效：source ~/.bashrc

三、GSL使用
1.新建工程文件夹

mkdir  /home/tx-deepocean/Library/gsl_test

2.新建makefile文件并编辑

#进入gsl_test文件夹并新建makefile文件
$ touch makefile
# 编辑makefile文件
$ vim makefile



三、GSL使用
1.新建工程文件夹

mkdir  /home/tx-deepocean/Library/gsl_test

2.新建makefile文件并编辑

#进入gsl_test文件夹并新建makefile文件
$ touch makefile
# 编辑makefile文件
$ vim makefile

makefile文件内容（如果出现错误注意tab的缩进，gcc前要求一个tab的缩进，最好自己手敲一遍，直接粘贴可能出问题）

IPATH=-I/home/ccchenji/Desktop/gsl_gcc/include
LPATH=-L/home/ccchenji/Desktop/gsl_gcc/lib
#这里直接链接的静态库文件
main:main.c
	gcc main.c $(IPATH)  $(LPATH) -l:libgsl.a -l:libgslcblas.a -o main

.PHONY:clean
clean:
	rm -rf main  

