### [Tomato学习笔记-Vscode配置Makefile(使用task.jason和launch.jason)_vscode makefile-CSDN博客](https://blog.csdn.net/GitTomato/article/details/123170550)



值得注意的是，makefile可以简化操作，例如下表使用一些符号代替

1            $<              表示第一个匹配的依赖
2            $@            表示目标
3            $^              所有依赖
4           %.o: %.c     自动匹配

所以可以形成如下模板:

cc = g++
prog = target
obj = srouce1.o srouce2.o ...

all: $(prog) clean //这里使用了all，程序从上往下执行，看见all则相当于把all当成了主程序，会自动调用clean比较方便

target: $(obj)
    g++ -o $(prog) $(obj)

%.o: %.cpp
    g++ -c %.cpp

clean:
    rm -f $(obj)



### [编写Makefile将各个目录下的.c文件编译成各自的.o文件_makefile生成.o文件_man_ting的博客-CSDN博客](https://blog.csdn.net/FLM19990626/article/details/130983212)



CC = gcc
CFLAGS = -Wall -Wextra -Werror
SRCDIR = src
OBJDIR = obj
TARGET = myapp

SOURCES := $(wildcard $(SRCDIR)/**/*.c)
OBJECTS := $(patsubst $(SRCDIR)/%.c, $(OBJDIR)/%.o, $(SOURCES))

$(TARGET): $(OBJECTS)
	$(CC) $(CFLAGS) $^ -o $@

$(OBJDIR)/%.o: $(SRCDIR)/%.c
	$(CC) $(CFLAGS) -c $< -o $@

.PHONY: clean
clean:
	rm -rf $(OBJDIR)/*.o $(TARGET)



CC 定义了使用的编译器，这里使用 gcc。
CFLAGS 定义了编译选项，这里开启了一些警告选项。
SRCDIR 定义了源文件所在的目录。
OBJDIR 定义了中间文件和目标文件所在的目录。
TARGET 定义了最终生成的可执行文件名。
SOURCES 是所有源文件的列表，使用了通配符 ** 可以递归查找子目录中的源文件。
OBJECTS 是所有目标文件的列表，使用了 patsubst 函数将源文件路径替换成目标文件路径。
$(TARGET): $(OBJECTS) 表示目标文件依赖于所有的中间文件，可以通过在命令行输入 $ make myapp 来生成最终的可执行文件。
$(OBJDIR)/%.o: $(SRCDIR)/%.c 表示规则，将所有一个 $(SRCDIR) 目录下的 .c 文件编译成对应的 .o 文件，并存储到 $(OBJDIR) 目录下。
.PHONY: clean 表示 clean 是一个伪目标，不是真正的文件，可以通过在命令行输入 $ make clean 来删除所有的中间文件和目标文件。



#### [vs code 如何配置使用makefile? - 知乎 (zhihu.com)](https://www.zhihu.com/question/366436359)



你的目录底下不是有一个.vscode文件夹吗？

它里面是用来放配置文件的，在vscode上面那一行选项里面点击终端，配置任务，它就会自动给你生成一个task.json

你把task.json打开配置一下第一个任务属性为build，命令是make就好了，

清理目标文件的话，再创建一个任务名字叫clean，命令是make clean就好了

构建项目的时候，Ctrl+shift+B就能执行make了

清理项目的时候，alt+t+r这时候上面就会弹出来任务列表，选中clean任务，回车就好了



### [linux+vsCode+makefile -- 调试C_vscode makefile 断点-CSDN博客](https://blog.csdn.net/z896435317/article/details/77948086)



二、vsCode调试配置
tasks.json文件编写（用于生成可调试程序，如直接在终端上使用make，即不用编写）
{
    "version": "2.0.0",
    "tasks": [
        {
            "taskName": "shell", // 任务名称，与launch.json的preLaunchTask相对应
            "command": "make", // 在shell中使用命令，如需加参数，可再添加args属性
            "type":"shell"
        }
    ]
}
launch.json文件编写（用于调用调试程序）

        {
        "version": "0.2.0",
        "configurations": [
        	{
            "name": "(gdb) Launch",// 配置名称，将会在启动配置的下拉菜单中显示
            "type": "cppdbg",// 配置类型，这里只能为cppdbg
            "request": "launch",// 请求配置类型，可以为launch（启动）或attach（附加）
            "program": "${workspaceRoot}/test",// 将要进行调试的程序的路径
            "stopAtEntry": true, // 设为true时程序将暂停在程序入口处，我一般设置为true
            "cwd": "${workspaceRoot}",// 调试程序时的工作目录
            "environment": [],// （环境变量？）
            "externalConsole": true,// 调试时是否显示控制台窗口，一般设置为true显示控制台
            "MIMode": "gdb",// 指定连接的调试器，可以为gdb或lldb。
            "preLaunchTask": "shell" // 调试会话开始前执行的任务，一般为编译程序。与tasks.json的taskName相对应，可根据需求选择是否使用
        }
    ]
}
————————————————
版权声明：本文为CSDN博主「不一样的清流」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/z896435317/article/details/77948086





### [VScode调试C/C++项目调试多个C++程序makefile_vscode c/c++多工程-CSDN博客](https://blog.csdn.net/weixin_44477424/article/details/119999303?spm=1001.2101.3001.6650.16&utm_medium=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~Rate-16-119999303-blog-77948086.235^v38^pc_relevant_anti_t3&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~Rate-16-119999303-blog-77948086.235^v38^pc_relevant_anti_t3&utm_relevant_index=21)





### [linux C++ makefile文件编写方法_创建c++ lib库的makefile_令狐掌门的博客-CSDN博客](https://blog.csdn.net/yao_hou/article/details/115795099)



## [A Simple Makefile Tutorial (colby.edu)](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/) 

| hellomake.c                                                  | hellofunc.c                                                  | hellomake.h                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ | --------------------------------------------------------- |
| `#include <hellomake.h> int main() {  // call a function in another file  myPrintHelloMake();   return(0); } ` | `#include <stdio.h> #include <hellomake.h> void myPrintHelloMake(void) {   printf("Hello makefiles!\n");   return; } ` | `/* example include file */ void myPrintHelloMake(void);` |

Normally, you would compile this collection of code by executing the following command:

```
gcc -o hellomake hellomake.c hellofunc.c -I.
```

This compiles the two .c files and names the executable hellomake. The `-I.` is included so that gcc will look in the current directory (.) for the include file hellomake.h. Without a makefile, the typical approach to the test/modify/debug cycle is to use the up arrow in a terminal to go back to your last compile command so you don't have to type it each time, especially once you've added a few more .c files to the mix.

Unfortunately, this approach to compilation has two downfalls. First, if you lose the compile command or switch computers you have to retype it from scratch, which is inefficient at best. Second, if you are only making changes to one .c file, recompiling all of them every time is also time-consuming and inefficient. So, it's time to see what we can do with a makefile.

The simplest makefile you could create would look something like:

[Makefile 1](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.1)

```
hellomake: hellomake.c hellofunc.c
     gcc -o hellomake hellomake.c hellofunc.c -I.
```

If you put this rule into a file called `Makefile` or `makefile` and then type `make` on the command line it will execute the compile command as you have written it in the makefile. Note that `make` with no arguments executes the first rule in the file. Furthermore, by putting the list of files on which the command depends on the first line after the `:`, make knows that the rule `hellomake` needs to be executed if any of those files change. Immediately, you have solved problem #1 and can avoid using the up arrow repeatedly, looking for your last compile command. However, the system is still not being efficient in terms of compiling only the latest changes.

One very important thing to note is that there is a tab before the gcc command in the makefile. There must be a tab at the beginning of any command, and `make` will not be happy if it's not there.

In order to be a bit more efficient, let's try the following:

[Makefile 2](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.2)

```
CC=gcc
CFLAGS=-I.

hellomake: hellomake.o hellofunc.o
     $(CC) -o hellomake hellomake.o hellofunc.o
```

So now we've defined some constants `CC` and `CFLAGS`. It turns out these are special constants that communicate to `make` how we want to compile the files hellomake.c and hellofunc.c. In particular, the macro `CC` is the C compiler to use, and `CFLAGS` is the list of flags to pass to the compilation command. By putting the object files--hellomake.o and hellofunc.o--in the dependency list and in the rule, `make` knows it must first compile the .c versions individually, and then build the executable hellomake.

Using this form of makefile is sufficient for most small scale projects. However, there is one thing missing: dependency on the include files. If you were to make a change to hellomake.h, for example, `make` would not recompile the .c files, even though they needed to be. In order to fix this, we need to tell `make` that all .c files depend on certain .h files. We can do this by writing a simple rule and adding it to the makefile.

[Makefile 3](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.3)

```
CC=gcc
CFLAGS=-I.
DEPS = hellomake.h

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: hellomake.o hellofunc.o 
	$(CC) -o hellomake hellomake.o hellofunc.o 
```

This addition first creates the macro DEPS, which is the set of .h files on which the .c files depend. Then we define a rule that applies to all files ending in the .o suffix. The rule says that the .o file depends upon the .c version of the file and the .h files included in the DEPS macro. The rule then says that to generate the .o file, `make` needs to compile the .c file using the compiler defined in the CC macro. The -c flag says to generate the object file, the `-o $@` says to put the output of the compilation in the file named on the left side of the `:`, the `$<` is the first item in the dependencies list, and the CFLAGS macro is defined as above.

As a final simplification, let's use the special macros `$@` and `$^`, which are the left and right sides of the `:`, respectively, to make the overall compilation rule more general. In the example below, all of the include files should be listed as part of the macro DEPS, and all of the object files should be listed as part of the macro OBJ.

[Makefile 4](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.4)

```
CC=gcc
CFLAGS=-I.
DEPS = hellomake.h
OBJ = hellomake.o hellofunc.o 

%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS)
```

So what if we want to start putting our .h files in an include directory, our source code in a src directory, and some local libraries in a lib directory? Also, can we somehow hide those annoying .o files that hang around all over the place? The answer, of course, is yes. The following makefile defines paths to the include and lib directories, and places the object files in an obj subdirectory within the src directory. It also has a macro defined for any libraries you want to include, such as the math library `-lm`. This makefile should be located in the src directory. Note that it also includes a rule for cleaning up your source and object directories if you type `make clean`. The .PHONY rule keeps `make` from doing something with a file named clean.

[Makefile 5](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/makefile.5)

```
IDIR =../include
CC=gcc
CFLAGS=-I$(IDIR)

ODIR=obj
LDIR =../lib

LIBS=-lm

_DEPS = hellomake.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = hellomake.o hellofunc.o 
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))


$(ODIR)/%.o: %.c $(DEPS)
	$(CC) -c -o $@ $< $(CFLAGS)

hellomake: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~ 
```

So now you have a perfectly good makefile that you can modify to manage small and medium-sized software projects. You can add multiple rules to a makefile; you can even create rules that call other rules. For more information on makefiles and the `make` function, check out the [GNU Make Manual](http://www.gnu.org/software/make/manual/make.html), which will tell you more than you ever wanted to know (really).



### [vscode调试makefile项目_vscode makefile-CSDN博客](https://blog.csdn.net/wade1010/article/details/128808644?spm=1001.2101.3001.6650.4&utm_medium=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~Rate-4-128808644-blog-77948086.235^v38^pc_relevant_anti_t3&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~CTRLIST~Rate-4-128808644-blog-77948086.235^v38^pc_relevant_anti_t3&utm_relevant_index=9)



#### [【错误记录】Ubuntu 下 VSCode 编译报错 ( 无法生成和调试，因为活动文件不是 C 或 C++ 源文件。终端进程启动失败(退出代码: -1)。终端将被任务重用，按任意键关闭。 )_* 终端将被任务重用,按任意键关闭。_韩曙亮的博客-CSDN博客](https://blog.csdn.net/shulianghan/article/details/123965166)



核心报错是 `无法生成和调试，因为活动文件不是 C 或 C++ 源文件。`

没有找到 C/C++ 文件 ;

在 tasks.json 构建脚本中 , 指定 C/C++ 文件路径的是 `"tasks` 下的 `"args"` 路径 ,

当前配置的 g++ 参数的 args 配置如下 

			"args": [
				"-fdiagnostics-color=always",
				"-g",
				"${file}",
				"-o",
				"${fileDirname}/${fileBasenameNoExtension}"
			],



`"${file}"` 配置就是 C++ 源文件的路径 , 该路径无效 , 这里修改为 `"${workspaceFolder}/*.cpp"` 参数 ;

**修改后的 tasks.json 构建脚本 如下 :**

![image-20231010154252187](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20231010154252187.png)

使用 Ctrl + Shift + B 快捷键 , 即可完成编译操作 ;

![image-20231010154432008](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20231010154432008.png)

![image-20231010154615667](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20231010154615667.png)

生成的可执行文件在 .vscode 目录下 , 名称是 task ;

执行 cd .vscode 命令 , 进入 .vscode 目录中 ,

使用 ./task 命令 , 执行该 task 可执行文件 , 打印如下内容 ;

Hello C++ World from VS Code and the C++ extension! 

![image-20231010154716024](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20231010154716024.png)















### 在我的ubuntu 下面进行实战

在vscode 中装了 Makefile tools 插件后，事实上调试多个cpp程序不需要用 tasks.json 和 lanuch.json 这两个文件，这两个文件对于单个cpp 程序调试还行，对于多个 cpp 程序的调试就显得非常的繁琐而且容易出错

#### 实战1

* 1. vscode 进入到项目文件夹

  ​       vscode -> /home/yangyuan16/WORK/cpp_make_makefile_learn/learn-vscode-make

* 2.  vscode 打开 ~/learn-vscode-make/ 文件路径

* 3. 编写好 Makefile 文件

* 4. 直接在 vscode 的终端输入 $ make , 就可以将项目进行编译

* 5. 在终端输入 gdb 进入调试模式 （或者在编译成功后生成了二进制文件后，在 vscode 中打上断点，利用 makefile tools 进行程序调试）

* 值得注意的是：直接用 makefile tools 进行程序调试的时候，makefile tools 有时候不能识别到当前路径下的 .h 头文件，这时候还不如直接在vscode终端输入 make 命令直接进行编译。



#### 实战2

* 参考b站的教学视频，利用 vscode + make +gdb 进行程序编译
* B站教程链接：https://www.bilibili.com/video/BV1Wv4y1x7He/?spm_id_from=333.880.my_history.page.click
* 1. vscode 进入 ~/learn-vscode-make-2/ 路径
  2. 其余操作参考视频教程，需要学习的是 gdb 调试编译命令。







