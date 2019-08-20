# linux系统中ARM裸机开发环境配置
  
## Linux系统下进行ARM裸机开发，主要需要以下的工具
- **交叉编译工具链**\
    ARM裸机开发，需要在PC端编译代码，然后在arm嵌入式设备中执行，因此需要制作交叉编译工具链。
      
### 利用crosstool-ng制作交叉编译工具连
1. **下载与安装**
    1. 从网址[http://crosstool-ng.org/download/crosstool-ng/] \ 
        下载 `crosstool-ng-1.24.0.tar.xz` 
    2. 解压该文件，并进入该文件路径。\
       `cd crosstool-ng-1.24.0`
    3. 对该软件进行编译\
       `./configure --prefix=PATH`
       `make`
       `make install`
       其中PATH为crosstool的安装路径
    4. 如果configure时提示一些前置安装包不存在的话，需要安装这些包。\
       `apt-get install gperf bison flex texinfo help2man gawk automake libncurses5-dev make libtool libtool-bin`
    5. 安装完成后添加环境变量\
       `vim ~/.bashrc`
       `在文件尾部加入一行 PATH=$PATH:/home/tools/cross/bin`
       `执行source ~/.bashrc`
       `执行echo $PATH，如果看到添加的路径，则说明成功`
 2. **制作**
     1. 使用`ct-ng help`查看是否安装成功。 
     2. 使用`ct-ng list-samples`查看默认配置列表。  
     3. 使用`ct-ng arm-unknown-linux-gnueabi`配置该编译器。  
     4. 使用`ct-ng menuconfig`开始配置。。
