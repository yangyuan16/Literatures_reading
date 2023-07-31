### [Linux 版的 Intel MKL 的安装使用](https://codeleading.com/article/91414391954/)

### MKL 程序在linux下的编译，c 和 c++

3.使用以编译官方文档上的 dgemm_example.c 为例

```cpp
#define min(x,y) (((x) < (y)) ? (x) : (y))
#include <stdio.h>
#include <stdlib.h>
#include "mkl.h"
int main()
{
    double *A, *B, *C;
    int m, n, p, i, j;
    double alpha, beta;
    printf ("\n This example computes real matrix C=alpha*A*B+beta*C using \n
            " Intel(R) MKL function dgemm, where A, B, and  C are matrices and \n"
            " alpha and beta are double precision scalars\n\n");
    m = 2000, p = 200, n = 1000;
    printf (" Initializing data for matrix multiplication C=A*B for matrix \n"
            " A(%ix%i) and matrix B(%ix%i)\n\n", m, p, p, n);
    alpha = 1.0; beta = 0.0;
    printf (" Allocating memory for matrices aligned on 64-byte boundary for better \n"
            " performance \n\n");
    A = (double *)mkl_malloc( m*p*sizeof( double ), 64 );
    B = (double *)mkl_malloc( p*n*sizeof( double ), 64 );
    C = (double *)mkl_malloc( m*n*sizeof( double ), 64 );
    if (A == NULL || B == NULL || C == NULL) {
        printf( "\n ERROR: Can't allocate memory for matrices. Aborting... \n\n");
        mkl_free(A);
        mkl_free(B);
        mkl_free(C);
        return 1;
    }
    printf (" Intializing matrix data \n\n");
    for (i = 0; i < (m*p); i++) {
        A[i] = (double)(i+1);
    }
    for (i = 0; i < (p*n); i++) {
        B[i] = (double)(-i-1);
    }
    for (i = 0; i < (m*n); i++) {
        C[i] = 0.0;
    }
    printf (" Computing matrix product using Intel(R) MKL dgemm function via CBLAS interface \n\n");
    cblas_dgemm(CblasRowMajor, CblasNoTrans, CblasNoTrans, 
                m, n, p, alpha, A, p, B, n, beta, C, n);
    printf ("\n Computations completed.\n\n");
    printf (" Top left corner of matrix A: \n");
    for (i=0; i<min(m,6); i++) {
        for (j=0; j<min(p,6); j++) {
            printf ("%12.0f", A[j+i*p]);
        }
        printf ("\n");
    }
    printf ("\n Top left corner of matrix B: \n");
    for (i=0; i<min(p,6); i++) {
        for (j=0; j<min(n,6); j++) {
            printf ("%12.0f", B[j+i*n]);
        }
        printf ("\n");
    }
    printf ("\n Top left corner of matrix C: \n");
    for (i=0; i<min(m,6); i++) {
        for (j=0; j<min(n,6); j++) {
            printf ("%12.5G", C[j+i*n]);
        }
        printf ("\n");
    }
    printf ("\n Deallocating memory \n\n");
    mkl_free(A);
    mkl_free(B);
    mkl_free(C);
    printf (" Example completed. \n\n");
    return 0;
}
```

（代码下载地址：https://software.intel.com/en-us/product-code-samples）

编译命令为：

$ gcc -I/opt/intel/mkl/include dgemm_example.c -lmkl_core -lmkl_intel_lp64  -lmkl_intel_thread -liomp5 -lpthread -lm -L/opt/intel/mkl/lib/intel64  -L/opt/intel/lib/intel64

或者

$ gcc -I/opt/intel/mkl/include dgemm_example.c -lmkl_rt -L/opt/intel/mkl/lib/intel64 -L/opt/intel/lib/intel64

再或者

$ . /opt/intel/bin/compilervars.sh intel64

$ gcc dgemm_example.c -lmkl_rt

（此方法可行是因为前一个命令设置了环境变量 CPATH，LD_LIBRARY_PATH，LIBRARY_PATH，致使编译器可以找到所需的头文件和库文件。编译C时头文件查找 C_INCLUDE_PATH 中包含目录，C++ 查找 CPLUS_INCLUDE_PATH，C和C++都查找 CPATH）

链接MKL的库的方法见：https://software.intel.com/en-us/mkl-linux-developer-guide-linking-your-application-with-the-intel-math-kernel-library

(学习文档：https://software.intel.com/en-us/get-started-with-mkl-for-linux ,https://software.intel.com/en-us/mkl-linux-developer-guide)

-------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------

### 实战

#### 在我的ubuntu下编译mkl程序

**(1) 在我的ubuntu下设置MKL的环境变量, 并在终端采用 gcc 和 g++编译**

* $ cd /opt/intel/oneapi
* $ source setvars.sh

测试编译mkl的c程序是否成功：

* $ cd /home/yangyuan16/WORK/c_mkl_example/example
* $ source /opt/intel/oneapi/setvars.sh intel64    # 编译前运行这一行命令
* $ gcc dgemm.c -lmkl_rt        # 编译 .c 程序
* $ g++ dgemm.cpp -o dgemm -lmkl_rt  # 编译 .cpp 程序

**(2) 尝试采用 vscode + cmake 进行编译**

* $ cd /home/yangyuan16/WORK/c_mkl_example/example3

* $ source /opt/intel/oneapi/setvars.sh intel64    # 编译前运行这一行命令

*  code .

* vscode = > ctrl + shift +p ==> Cmake Quick

* enter a name for a project:  example3

* chose:   c++ project

* chose:  excutable file

* vscode 自动生成 build folder 和 CMakeLists.txt

* 修改 CMakeLists.txt  ==>  add_executable(example3 dgemm.cpp)  

  将 CMakeLists.txt整体修改为如下的格式：

> cmake_minimum_required(VERSION 3.0.0) #cmake最低要求版本
>
> project(example3 VERSION 0.1.0 LANGUAGES C CXX) #工程名字
>
> include(CTest)
>
> enable_testing()
>
> \#头文件的搜索路径
>
> include_directories(
>
> ​                     /opt/intel/mkl/include/     
>
> ​                     include  #-------即/usr/local/include路径
>
> ​                     )  
>
> \#库的搜索路径
>
> link_directories(/opt/intel/mkl/lib/intel64 
>
> ​                 /opt/intel/lib/intel64)
>
> \#生成可执行程序：example3
>
> add_executable(example3 dgemm.cpp)
>
> \#将库链接到可执行程序：example3              
>
> target_link_libraries(example3 
>
> ​                      libmkl_rt.so 
>
> ​                      pthread
>
> ​                      libm.so
>
> ​                      libdl.so
>
> ​                      )
>
> set(CPACK_PROJECT_NAME ${PROJECT_NAME})
>
> set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
>
> include(CPack)

* $ cd ./build   (在linux终端执行)
* $ cmake ..
* $ make 
* $ ./example3 

> 编写 CMakeLists.txt文件参考：https://blog.csdn.net/qjj18776858511/article/details/126127718  ;   https://zhuanlan.zhihu.com/p/628678249   



**(3) 尝试采用 vscode + cmake + gdb 进行debug**

* 在 （2） 的基础上先写好 CMakeLists.txt        
* $ cd /home/yangyuan16/WORK/c_mkl_example/example4
* $ cp ../example3/dgemm.cpp .    
* $ cp ../example3/CMakeLists.txt .
* $ code . 
* 在cmakelist.txt中可以加入使用不同的CMAKE_BUILD_TYPE，取值是 Debug Release RelWithDebInfo和 MinSizeRel。
  当这个变量值为 Debug 的时候,CMake 会使用变量 CMAKE_CXX_FLAGS_DEBUG 和 CMAKE_C_FLAGS_DEBUG 中的字符串作为编译选项生成 Makefile
  当这个变量为RELESE时候，cmake会使用变量CMAKE_CXX_FLAGS_RELEASE 和 CMAKE_C_FLAGS_RELEASE 中的字符串作为编译选项生成 Makefile。所以如果需要通过cmake+make生成可以使用用于调试程序，要在cmakelist.txt

* > 在CMakeLists.txt 加入以下三句语法
  >
  > SET(CMAKE_BUILD_TYPE "Debug")  # 定义编译类型
  > SET(CMAKE_CXX_FLAGS_DEBUG "$ENV{CXXFLAGS} -O0 -Wall -g2 -ggdb") # 定义Debug编译参数
  > SET(CMAKE_CXX_FLAGS_RELEASE "$ENV{CXXFLAGS} -O3 -Wall") # 定义Release编译参数
  > 参考链接：https://blog.csdn.net/wei242425445/article/details/103752836

* $ ctrl + shift + p ==> CMake Configure  ==> 自动生成 build folder  + Makefile

* $ cd  ./buid

* $  gdb example  (gdb linux  Termial  debug)

* $ (gdb)  ==> Enter

* $ (gdb) l   # 查看主文件的代码

* $ (gdb) b 26 #  在 26 行处设置断点

* $ (gdb) info b # 查看断点信息

* $ (gdb) delete 1 # 删除第一个断点

* $ (gdb) info b # 查看断点信息

* $ (gdb) r # 运行

* $ (gdb) start # 打出一个屏幕输出

* $ (gdb) b 66 #  在 66 行处设置断点

* $ (gdb) c # 运行到 66 这个断点

* $ (gdb) n # 执行下一行 （不进入函数）

* $ (gdb) s # 执行下一行 （会进去函数）

* $ (gdb) k # 终止正在调试的任务 

* $ (gdb) q # 退出调试环境

* > 参考链接：https://blog.csdn.net/wei242425445/article/details/103752836
  >
  > 参考链接 https://blog.csdn.net/get_you_1/article/details/100066184 
  >
  > 参考链接 [gdb与Cmake的使用](https://blog.csdn.net/wei242425445/article/details/103752836?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-103752836-blog-90769079.235%5Ev38%5Epc_relevant_sort_base1&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-103752836-blog-90769079.235%5Ev38%5Epc_relevant_sort_base1&utm_relevant_index=2) 

**(4) 尝试采用 vscode + cmake + vscode设置 lanuch.json 进行编译**

* > 参考链接 [Linux环境下使用VScode调试CMake工程](https://blog.csdn.net/hypc9709/article/details/129430861) 

* $ cd /home/yangyuan16/WORK/c_mkl_example/example5

* $ cp ../example4/dgemm.cpp .    

* $ cp ../example4/CMakeLists.txt .

* $ code . 

* $ mkdir build  # 建立一个build 路径, 这一步是关键

* 在VSCode的主菜单中，选择 **Terminal>Configure Default Build Task**，

* 选择 **“CMake: build”**

* 将生成一个 `tasks.json`文件，将其中的内容替换为以下内容即可：

* > {
  > 	"version": "2.0.0",
  > 	"tasks": [
  >         {
  >             "label": "cmake",
  >             "type": "shell",
  >             "command": "cmake",
  >             "args": [
  >                 "../"
  >             ],
  >             "options": {
  >                 "cwd": "${fileDirname}/build"
  >             },            
  >         },
  >         {
  >             "label": "make",
  >             "type": "shell",
  >             "command": "make",
  >             "args": [],
  >             "options": {
  >                 "cwd": "${fileDirname}/build"
  >             }, 
  >         },
  >         {
  >             "label": "build",
  >             "dependsOn":["cmake", "make"]
  >         },
  >     ],
  > }

* 在VSCode的主菜单中，选择 **Terminal>Run Task…**，然后选择 **build** ，再选择 **“continue without scanning the task output”**，可以在编辑器下方的终端显示界面中看到，VSCode执行完成了cmake和make两个任务：

* 将会在 build 目录下生成一个可执行文件 example3，下面将介绍如何在VSCode中对其进行调试：

* 在VSCode的上方菜单中，选择 Run -> Add Configuration，会生成一个空白的`launch.json`文件：

* 我们要做的就是在该文件中告诉VSCode：用gdb调试前面生成的可执行文件，在`launch.json`文件中添加如下内容：

* > {
  >     "version": "0.2.0",
  >     "configurations": [
  >         {
  >             "name": "g++ - Build and debug active file",
  >             "type": "cppdbg",
  >             "request": "launch",
  >             "program": "${fileDirname}/build/${fileBasenameNoExtension}",
  >             "args": ["para1", "para2"],
  >             "stopAtEntry": false,
  >             "cwd": "${fileDirname}",
  >             "environment": [],
  >             "externalConsole": false,
  >             "MIMode": "gdb",
  >             "setupCommands": [
  >                 {
  >                     "description": "Enable pretty-printing for gdb",
  >                     "text": "-enable-pretty-printing",
  >                     "ignoreFailures": true
  >                 }
  >             ],
  >             "preLaunchTask": "build",
  >             "miDebuggerPath": "/usr/bin/gdb"
  >         }
  >     ]
  > }

* > 其中，
  >
  >     "program"：用于指定要调试的可执行文件，这里用变量名指代，其值就是 example3
  >     "args"：执行代码时，需要添加的命令行参数
  >     prelaunchTask：在执行gdb调试前，预先需要执行的任务，这里设置为"build"，就是指定第3节中配置完成的build任务，即在gdb调试前，先执行cmake和make

* > 参考链接 [Linux环境下使用VScode调试CMake工程](https://blog.csdn.net/hypc9709/article/details/129430861) 



**(5) 对方法 (4) 进行修正**

* 由于 在 CMakeLists.txt 中的这句话：add_executable(example3 dgemm.cpp)

* 导致 build 中生成的是 exmaple3 二进制可执行文件  而不是 dgemm

* 在 CMakeLists.txt 中对应修改的地方有：

* >add_executable(example3 dgemm.cpp) ==> add_excutable(dgemm  degmm.cpp)
  >
  >target_link_libraries(dgemm # 这里相应修改为 dgemm
  >                      libmkl_rt.so
  >                      pthread
  >                      libm.so
  >                      libdl.so
  >                      )

* $ mkdir build
* 重复 方法（4）即可在 vscode 中对代码进行debug调试！



**(6) **

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------------



