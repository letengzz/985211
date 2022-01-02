## 指令指针寄存器IP (在BIU)16位


功能：用来存放将要执行的下一条指令在代码段中的偏移地址。在程序运行过程中，BIU自动修改IP中的内容，使它始终指向将要执行的下一条指令。
注意：程序不能直接访问IP，但是可通过某些指令修改IP的内容。例如, 执行转移指令时，会将转移的目标地址送入IP中，以实现程序的转移。






总是指向下一条指令的偏移地址

![image-20211127104739531](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127104739531.png)专门用于存放  通过ip指针确定指针的位置

![image-20211118152748690](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152748690.png)

![image-20211118152933439](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152933439.png)
