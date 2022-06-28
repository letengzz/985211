# 标志寄存器FLAGS (在EU)

​	16位寄存器，用来**存放运算结果的特征和控制标志**。

​	可以用`psw` 和`FR`表示。

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​                                                                          <img src="https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230164040154.png" alt="image-20211230164040154" style="zoom:67%;" />

<img src="https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230164103965.png" alt="image-20211230164103965" style="zoom:67%;" />

**各标志位说明**：

![image-20211230162538358](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230162538358.png)

# 状态位

## CF(Carry Flag) 进位标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​	`CF=1`，表示本次运算中**最高位**(第7位或第15位)**有进位**(加法运算时)或**有借位**(减法运算时)。

​	`CF=0`，表示本次运算中最高位没有**进位**或者**借位**。
​    进行二个无符号数加法或减法运算后，如果CF=1，表示运算的结果超出了该字长能够表示的数据范围。

**例**：执行8位数据运算后，CF=1表示加法结果超过了255，或者是减法得到的差小于零。
     进行有符号数运算时，CF对运算结果没有直接意义。

![image-20211230202120319](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230202120319.png)

## PF(Parity Flag) 奇偶标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​	`PF=1`，表示本次运算结果的低八位中有**偶数**个"`1`"

​	`PF=0`，表示本次运算结果的低八位中有**奇数**个"`1`"
​	**PF可以用来进行奇偶校验，或用来生成奇偶校验位**。

**注意**：当全为0时，`PF=1`

![image-20211230202806028](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230202806028.png)

## AF(Auxiliary Carry Flag) 辅助进位标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​	`AF=1`，表示运算结果中低4位向高4位有进位（加法运算时）或有借位（减法运算时）

​	`AF=0`，表示运算结果低4位没有向高4位**进位**或者**借位**。

![image-20211230203207394](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230203207394.png)

## ZF(Zero Flag) 零标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​	`ZF=1`，表示运算结果为0 (各位全为`0`)。

​	`ZF=0`，表示运算结果不为0。

![image-20211230204038310](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230204038310.png)

## SF(Sign Flag) 符号标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​	`SF=1`，表示运算结果的**最高位**（第7位或第15位）为`1`。

​	`SF=0`，表示运算结果的**最高位**（第7位或第15位）为`0`。

可以根据`SF`可以判断是负数和非负数。

![image-20211230213352985](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230213352985.png)

## OF(Overflow Flag) 溢出标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​    `OF=1`，表示二个用补码表示的**有符号数**的**运算结果超出了该字长所能表示的范围**，即产生溢出。

​	`OF=0`，表示二个用补码表示的**有符号数**的**运算结果没有超出该字长所能表示的范围**。

**例**：进行8位运算时，OF=1表示运算结果大于`+127` 或小于`-128`，此时不能得到正确的运算结果。
         **`OF`对无符号数的运算结果没有意义**。

![image-20211230214345085](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230214345085.png)

### 判断溢出

​     当字节运算的结果超出了范围`-128～+127`，或者当字运算的结果超出范围`-32768～+32767`时称为溢出。当计算机进行**加法运算**时，每当判断出次高位向最高位产生进位，而最高位没有进位时，便产生了溢出，`OF＝1`；或反过来，每当判断出次高位向最高位无进位，而最高位却往前有进位时，也产生溢出，`OF＝1`。在**减法运算**时，每当判断出最高位需要借位，而次高位没向最高位产生借位时产生溢出，`OF=1`；或者反过来，次高位向最高位有借位，而最高位并不需向更高位借位时产生溢出，`OF=1`。

**结论**：根据最高位的进位与次高位的进位是否相同来确定。若两者不相同则`OF=1`(表示有溢出)，否则 `OF=0`(表示无溢出)。

​	正数加正数等于负数、负数加负数等于正数、负数减正数等于正数都**属于溢出**；

​	首先**正数+负数不存在溢出**，因为正数和负数首先是在可存储范围，相加后一定不会超过显示范围，of=0。

# 控制位

## IF(Interrupt Flag) 中断允许标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​     `IF=1`，表示允许CPU响应可屏蔽中断。`IF`可通过`STI指令`置位（置1），也可通过`CLI指令`复位（清零）。从`INTR`引入。

## DF(Direction Flag) 方向标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​     在串操作指令中，若`DF=0`，表示**串操作**指令执行后**地址指针自动增量**，串操作**由低地址向高地址进行**；

​	`DF=1`，表示**地址指针自动减量**，串操作**由高地址向低地址进行**。

​	`DF`可通过`STD指令`置位，也可通过`CLD指令`复位。

![image-20211231150034574](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211231150034574.png)

## TF(Trap Flag) 单步标志位

![image-20211230161741339](https://cdn.jsdelivr.net/gh/letengzz/Two-C/img/PM/Second/image-20211230161741339.png)

​     `TF=1`，控制CPU进入单步工作方式。在这种工作方式下，CPU每执行完一条指令就会自动产生一次内部中断，这在程序调试过程中很有用。优先级最低，否则会影响程序。
