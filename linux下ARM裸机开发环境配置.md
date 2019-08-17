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
