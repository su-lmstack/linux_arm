## linux系统中ARM裸机开发环境配置
# 工具
- **交叉编译工具链**
   - arm-linux-cpp: 预编译工具，处理c/c++的#开头的语句， 生成.i文件
   - cc1: 编译工具，将c/c++代码翻译为汇编代码， 生成.s文件
   - arm-linux-as: 将汇编代码翻译为机器代码
   - arm-linux-ld: 将obj文件、库文件等连接起来，最终生成可执行文件
- **安装工具包**
   - `sudo apt-get install build-essential`:安装基本的开发环境。
   - `sudo apt-get install bison flex`:安装语法、词法分析器。
   - `sudo apt-get install manpages-dev`:安装C函数库手册
- **arm-linux-gcc安装及配置**
   1. 下载arm-linux-gcc-5.4.0.tar.gz,然后解压
   2. 在/etc/profile 下，打开profile 在末尾添加以下语句：
      `export PATH=/your_path/5.4.0(文件夹版本号)/bin:$PATH`,其中your_path为arm-linux-gcc的解压路径
      或者在~/.bashrc文件中增加上述语句，修改只对当前登录的用户有效。
   3. 下载并解压ncurses。
      然后切换为root，
      ```                   
      ./configure
      make
      make install
      ```
      即可安装
