## ARM开发相关的基础知识
# ARM开发所需工具
- USB转串口连接线
   - 用于PC端与ARM板信息交互，显示调试信息，控制ARM板内的程序等。
- JLINK 调试工具
   - 用于刷写FLASH,在线调试等。
- USB 线
   - 用于通过USB的方式下载程序到开发板
# 软件刷写方式
- JTAG/JLINK刷写
   - JTAG和JLINK可以将软件刷写至NAND FLASH 和 NOR FLASH中。刷写NOR FLASH时，可直接写入到FLASH，无需事先刷新程序到内存。
   刷写NAND FLASH时，需要事先刷写引导程序到内存，并把要刷写的程序写入内存，然后让CPU将内存中的程序移到NAND FLASH中。
   - 软件工具：J FLASH ARM/ J LINK COMMANDER
   - 硬件工具：JLINK调试器。
- USB刷写
   - USB刷写前，需要用JTAG将boot刷写到NOR FLASH中
   - 板子通过NOR FLASH 启动后，连接USB，进入USB模式，通过NOR 中的程序将数据写入NAND FLASH。
