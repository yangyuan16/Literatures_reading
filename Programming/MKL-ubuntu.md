### [ubuntu配置机器学习环境（四） 安装intel MKL](https://www.yii666.com/article/744742.html) 

### [Ubuntu下MKL（Intel Math Kernel Library）安装教程](https://dgrt.cn/a/1508014.html?action=onClick)



环境：linux 我用的是 ubuntu 16.04

**具体步骤：**

1 . 下载ubuntu下的MKL包

```javascript
// download the latest MKL
https://software.intel.com/content/www/us/en/develop/tools/math-kernel-library.html
tar -zxvf l_mkl_2019.0.117.tgz  //解压文件
```

2 . 安装MKL包

```javascript
cd l_mkl_2019.0.117
./install.sh
```

3 . 编译

```javascript
source ~/intel/bin/compilervars.sh intel64
```



### [Intel oneAPI Base Toolkit 安装教程（Linux）](https://blog.csdn.net/qq_42951560/article/details/121438924?ydreferer=aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyOTUxNTYwL2FydGljbGUvZGV0YWlscy8xMjE0NDExMjk%3D)

……
……
……
source /opt/intel/oneapi/setvars.sh intel64
:wq

温馨提示：/etc/profile 里面配置的是系统环境变量，开机自启动，所有用户均可使用。但每次用户登录后都会弹出 oneapi 环境变量加载页，会造成一定的卡顿，影响用户体验，因此，不建议配置。替换方法是：管理员告诉普通用户 oneapi 的安装路径，默认是 /opt/intel/oneapi，然后让用户将其配置在自己的用户变量 .bashrc 文件中，这样用户可以自己选择是否使用（不想用就注释掉）。



### [Intel® oneAPI Base Toolkit+Intel® oneAPI HPC Toolkit安装教程+环境变量设置](https://blog.csdn.net/weixin_44466025/article/details/119543854?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-119543854-blog-121438924.235%5Ev38%5Epc_relevant_sort_base1&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-119543854-blog-121438924.235%5Ev38%5Epc_relevant_sort_base1&utm_relevant_index=1)



3.环境变量设置

 在/home/username/intel/oneapi/下面会有setvars.sh的文件，这个文件包含了你所安装的所有oneAPI工具包的环境变量。

临时使用Intel oneAPI，则只需要在每次使用之前执行命令source ~/intel/oneapi/setvars.sh intel64即可；

```cobol
source ~/intel/oneapi/setvars.sh intel64
```

长期使用需要在/etc/profile或者~/.bashrc里面source它即可。

```cobol
source /home/username/intel/oneapi/setvars.sh intel64
```

启动/.bashrc文件

```bash
source /.bashrc
```





### [Ubuntu20.4.5+Clion+Falshlight+ArrayFire+Intel-MKL 人工智能深度机器学习C++开发环境搭建](https://yusupjan.blog.csdn.net/article/details/126588737?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-126588737-blog-108899379.235%5Ev38%5Epc_relevant_sort_base1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-3-126588737-blog-108899379.235%5Ev38%5Epc_relevant_sort_base1&utm_relevant_index=6)



