### linux系统中ARM裸机开发环境配置
  
  Linux系统下进行ARM裸机开发，主要需要以下的工具：
  - **交叉编译工具链**
      ARM裸机开发，需要在PC端编译代码，然后在arm嵌入式设备中执行，因此需要制作交叉编译工具链。。
      
- **利用crosstool-ng制作交叉编译工具连**
   1. [http://crosstool-ng.org/download/crosstool-ng/]下载`crosstool-ng-1.24.0.tar.xz`
   2. 解压该文件，并进入该文件路径。
      - `cd crosstool-ng-1.24.0`

