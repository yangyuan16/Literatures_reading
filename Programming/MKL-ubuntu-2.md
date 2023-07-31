### [Linux下MKL库的安装部署与使用，并利用cmake编译器调用MKL库去提升eigen库的计算速度](https://blog.csdn.net/qjj18776858511/article/details/126127718)

Cmakelist.txt文件如下配置：

------------------------------------------------------------------------------------------------------------------

cmake_minimum_required(VERSION 3.0.2) #cmake最低要求版本
project(TestMKL)    #工程名字

#头文件的搜索路径
cmake_minimum_required(VERSION 3.0.2) #cmake最低要求版本
project(TestMKL)    #工程名字

#头文件的搜索路径
include_directories(
                     /opt/intel/mkl/include/     
                     include  #-------即/usr/local/include路径
                     )                    
#库的搜索路径
link_directories(/opt/intel/mkl/lib/intel64 
                 /opt/intel/lib/intel64)
                 
#生成可执行程序：mkl_test
add_executable(mkl_test      
               mkl_test.cpp)
               
#将库链接到可执行程序：mkl_test              
target_link_libraries(mkl_test 
                      libmkl_rt.so 
                      pthread
                      libm.so
                      libdl.so
                      )



------------------------------------------------------------------------------------------------------------------------------------------------

拿到测试代码后，进入mkl_ws,并打开终端，执行以下指令：

```c
$ cmake .
$ make
$ ./mkl_test
```





### [linux下使用cmake和vscode进行C/C++开发](https://blog.csdn.net/riversuer/article/details/130858501)



### (四) Cmake编译工具使用

#### 1 作用

CMake（cross platform make）是一个跨平台的编译工具，可以用简单的语句来描述所有平台的编译过程。能通过写简单的配置文件生成本地的Makefile，并且跨平台的特性十分友好，非常方便。

2 常用参数

    cmake_minimum_required(VERSION number)指定cmake最小版本要求
    
    project(name)定义工程名称，还可指定工程支持的语言
    
    add_executable(exename souucre1 soucre2...)生成可执行文件，可包含单个或多个cpp文件
    
    include_directories(dir)向工程添加多个指定的头文件搜索路径
    
    aux_source_directory(dir var)把指定目录下所有的源文件存储在一个变量中，常用于多文件编译
    
    调用变量时写法：${var},当使if时，直接加var
    
    set(var source1 source2..)给源文件代码定义一个变量名字，方便使用
    
    add_compile_options()添加编译参数，如-wall，-o，-std=c++11，中间用空格隔开。此命令还用于参与定义宏控制打印信息。
    
    add_subdirectory(source_dir [binary_dir] [EXCLUDE_FROM_ALL]) 这个命令用于添加源文件子目录，同时还可以指定中间二进制和目标二进制的生成路径。外层的CMakeLists.txt使用add_subdirectory来控制其它目录下的CMakeLists.txt的运行
    
    set (EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)控制make命令生成的可执行文件在主目录bin文件夹下。注意使用外部构建在build中运行cmake时，bin目录的路径位置一定要写对，../bin 或 ${PROJECT_SOURCE_DIR（意为根目录）}/bin，最好使用后者，方便别人阅读。若直接bin 会在build目录中创建一个bin文件夹。
    
    add_library(lib_name lib_type soucre) 添加一个库，参数1为库名字，参数2位库类型动态还是静态默认静态，参数3位源文件
    
    set(LIBRARY_OUTPUT_PATH${PROJECT_SOURCE_DIR}/lib)设置库文件存目录为lib，代码格式
    
    set_target_properties: 设置最终生成的库的名称，还有其它功能，如设置库的版本号等
    
    find_library(VAR_NAME LIB_NAME HINTS DIR)在指定目录下查找指定库，并把库的绝对路径存放到变量里，其第一个参数是变量名称，第二个参数是库名称，第三个参数是HINTS，第4个参数是路径，使用find能防止链接的时候才发现出错。此命令默认查动态库，若要指定查找库的类型，在第二个参数后加.so或.a
    
    target_link_libraries (main LIB) 把目标文件与库文件进行链接，第一个参数为make生成的可执行程序，第二个为库文件，可用find生成的变量名代替
> 一般会把源文件放到src目录下，把头文件放入到include文件下，生成的对象文件放入到build目录下，库文件放到lib目录下，最终输出的可执行程序文件会放到bin目录下，这样整个结构更加清晰

3 CMake编译具体步骤

    编写CMakeLists：在main.cpp文件下建立CMakeLists.txt文档–>设置minimum，project，included_dir，add_executable等必要参数–>保存
    
    外部构建：在main.cpp同级目录创建build目录–>linux终端cd进入build目录–>输入命令cmake ..运行cmake–>生成makefile以及其它文件
    
    生成可执行文件：在linux终端中输入make命令–>./name执行




### [Linux下使用VSCode和CMake搭载C/C++开发环境](https://blog.csdn.net/u010000843/article/details/114439771?spm=1001.2101.3001.6650.8&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-8-114439771-blog-130858501.235%5Ev38%5Epc_relevant_sort_base1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromBaidu%7ERate-8-114439771-blog-130858501.235%5Ev38%5Epc_relevant_sort_base1&utm_relevant_index=9)

## 2. 编写cpp和CMake文件

安装完成后按快捷键`Ctrl+Shift+e`回到文件管理列表，创建build目录，hello.cpp和CMakeLists.txt文件。

> 注意：`CMakeLists.txt`必须是这个命名，注意大小写



### [linux下vscode使用cmake创建并编译c++程序的配置方法](https://blog.csdn.net/ybyhlj/article/details/128381285?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-0-128381285-blog-127897998.235^v38^pc_relevant_sort_base1&spm=1001.2101.3001.4242.1&utm_relevant_index=3)



## 一、[VSCODE](https://so.csdn.net/so/search?q=VSCODE&spm=1001.2101.3001.7020)安装cmake

![在这里插入图片描述](https://img-blog.csdnimg.cn/61d0ef4fc7df45a7a5f3d7b033259271.png)

## 二、选择工作目录

![在这里插入图片描述](https://img-blog.csdnimg.cn/f773eab0f3bb46f2b21819e28e9b4a9d.png)

## 三、F1 → CMake:Quick Start

![在这里插入图片描述](https://img-blog.csdnimg.cn/fcc63ccb44614cfca682e64bbc49379b.png)

## 四、选择GCC编译器

![在这里插入图片描述](https://img-blog.csdnimg.cn/c6cf27c804bc46fea474da323f6de24c.png)

## 五、输入项目名称

![在这里插入图片描述](https://img-blog.csdnimg.cn/835f587e3da540649fc4426c9275449b.png)

## 六、选择生成库文件 也可以选择执行程序

![在这里插入图片描述](https://img-blog.csdnimg.cn/65e5389027004b20a637b3aeaf800f0a.png)

## 七、撰写代码

![在这里插入图片描述](https://img-blog.csdnimg.cn/79af131e029b453e98c3e93d97acfea1.png)

## 八、编译生成 F1 → Task Configure Task

![在这里插入图片描述](https://img-blog.csdnimg.cn/7ca9f39d3a0d4a299f6a6f50dcf97c67.png)

## 九、Create task json

![在这里插入图片描述](https://img-blog.csdnimg.cn/7dece4e673484bb8aad8dcab1765befe.png)



## 十、maven

![在这里插入图片描述](https://img-blog.csdnimg.cn/5dffcb315f794483be0d1b05f832ad20.png)

## 十一、补充 自动生成的task.json，例：

```cpp
"command": "cd ${workspaceFolder}/build && rm -rf CMakeFiles && cmake . && make",
1
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/9f61fd3820b64009aaf7d012308e7e41.png)



## 十二、打开CMakeLists.txt，修改如下信息

```cpp
add_library(testdll SHARED testdll.cpp)
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/d8ef0bc3c32d496280714c557a0730b4.png)



## 十三、F1→Tasks:Run Task

![在这里插入图片描述](https://img-blog.csdnimg.cn/34ea1fff792946a9af97fffc07753e1f.png)

## 十四、选test

![在这里插入图片描述](https://img-blog.csdnimg.cn/12e8def81d2442f7836d07aa28d3078f.png)

## 十五、成功

![在这里插入图片描述](https://img-blog.csdnimg.cn/58ddf0eb7d704b84a6a064c6138425c8.png)

## 十六、成果展示

![在这里插入图片描述](https://img-blog.csdnimg.cn/fa485a00317140608f658da79b1aa2b6.png)

















