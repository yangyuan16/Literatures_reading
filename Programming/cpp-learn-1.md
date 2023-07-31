### [linux+cpp+vscode配置](https://www.likecs.com/show-308176156.html)

### [linux下vscode的c++工程配置](https://www.cnblogs.com/chencarl/p/10463392.html)

### [vscode在windows和ubuntu系统下配置c/c++的详细步骤](https://blog.csdn.net/qq_57166515/article/details/130371417)

### [Linux系统下配置VScode](https://zhuanlan.zhihu.com/p/620851804) 

* ctrl + shift + p :  C/C++ g++ 生成调试活动文件
* ctrl + shift + p： C/C++ Edit configuration (UI) -> /usr/bin/g++  产生 c_cpp_properties.json
* ctrl + shift + p:  C/C++ add debug configureation -> g++ 生成调试活动文件  产生 launch.json  tasks.json
* vs code中的智能提示对于第三方库需要手动添加路径：在Command Palette (Ctrl+Shift+P)中，输入C/C++: Edit Configurations (UI) 即可进入到可视化的c/c++设置中，其中有一条“包含路径”的设置。在命令行中通过locate指令查找到所需的第三方库的路径并添加进设置中后，重新启动vs code就有对应的代码提示啦！
  ————————————————
  版权声明：本文为CSDN博主「weixin_42461385」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
  原文链接：https://blog.csdn.net/weixin_42461385/article/details/123625515

### ubuntu下Vscode C++代码补全无法使用

* VSCODE j界面 文件->首选项->设置搜索Intelli Sense Engine把Default改为Tag Parser即可



### [Ubuntu 20.04下搭建C++ & OpenCV 4.6.0 & cmake编译](https://zhuanlan.zhihu.com/p/573341843)

1. 换国内源；2. 安装依赖项；3. 下载OpenCV源文件；4. 配置、编译、安装OpenCV；5. 配置环境；6. demo测试；7. 简单项目测试；8. 其他

* sudo apt install -y g++
* sudo apt install -y cmake
* sudo apt install -y make
* sudo apt install -y wget
* sudo apt install -y unzip



### [ubuntu 20.04系统下安装VSCode（配置C/C++开发环境](https://www.cnblogs.com/icmzn/p/16244665.html)











