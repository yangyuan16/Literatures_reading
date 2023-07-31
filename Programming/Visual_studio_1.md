# 配置

## [静态库的创建](https://www.bilibili.com/video/BV1vQ4y1r7uF/?spm_id_from=333.788&vd_source=cf9aaab1f09e7e5b19cf23e0b4d3c771)

注意 MT 和 MD:

## [属性与环境变量](https://www.bilibili.com/video/BV1y54y197GM/?spm_id_from=pageDriver&vd_source=cf9aaab1f09e7e5b19cf23e0b4d3c771)

在visual studio 中使用更为便捷的方法来配置第三方数据库
[视图]==>[其他窗口]==>[属性管理器]==>

## [动态库的使用](https://www.bilibili.com/video/BV1hE411Y7vd/?spm_id_from=pageDriver&vd_source=cf9aaab1f09e7e5b19cf23e0b4d3c771)

如果库是用 c++ 写的，但是调用的程序是 c, 调用的方式会不一样。
在Windows下，生成dll时，都会生成一个同名的.lib文件，该.lib文件记录包含dll中的函数名和位置，dll包含实际的函数和数据，.exe(执行程序)使用lib文件链接到dll文件。
在应用程序的可执行文件中，存放的不是被调用的函数代码，而是dll中相应函数代码的地址，从而节省了内存资源。dll和lib文件必须随应用程序一起发行，否则应用程序会产生错误。
Windows在查找dll时，会按照如下路径来查找
1． 包含EXE文件的目录，
2． 进程的当前工作目录，
3． Windows系统目录，
4． Windows目录，
5． 列在Path环境变量中的一系列目录。
问题原因,
因为在使用编译好的gtestdll时，上述dll并没有存放在上述五个目录之一，从而导致应用程序无法根据lib文件查找到对应的dll
解决办法,
最简单的解决办法就是将对应的dll文件VS工程的输出目录下，首先找到VS工程的输出目录，将对应的dll拷贝过去即可

## lib 和 dll 文件的作用是什么？



# [pragma 用法详解](https://blog.csdn.net/qq_62199813/article/details/130703715?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EYuanLiJiHua%7EPosition-2-130703715-blog-58586014.235%5Ev38%5Epc_relevant_anti_vip&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EYuanLiJiHua%7EPosition-2-130703715-blog-58586014.235%5Ev38%5Epc_relevant_anti_vip&utm_relevant_index=3)

pragma 指令对每个编译器给出了一个方法，在保持与 c 和 c++ 语言完全兼容的情况下，给出主机或操作系统专有特征。
依据定义，编译指令是机器或操作系统专有的，且对于每个编译器都是不同的

其格式一般为: #pragma Para 其中 Para 为参数，下面来看看一些常用的参数

* (1) #Pragma message 参数能够在编译信息输出窗口中输出相应的信息。

Pragma message ("消息文本") 当我们在程序中定义了许多宏来控制源代码版本的时候，我们自己有可能会忘记
有没有正确设置这些宏，此时我们可以用这条指令在编译的时候进行检查。

* (2) # pragma code_seg 能够设置程序中函数代码存放的代码段

开发驱动程序的时候会使用到它

*（3） pragma one (比较常用) 若用在头文件的最开始处就能够保证头文件被编译一次。

* (4) #pragma hdrstop 表示预编译头文件到此为止

* (5) #pragma resource "*.dfm", 表示把 *.dfm 文件中的资源加入工程。 *.dfm 包括窗体外观定义。

* (6) #pragma warning 允许有选择性的修改编译器的警告消息的行为

* (7) #pragma comment 将一个注释记录放入一个对象文件或可执行文件中

* (8) #pragma data_seg 建立一个新的数据段并定义共享数据

ta_seg 建立一个新的数据段并定义共享数据

