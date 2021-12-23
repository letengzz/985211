# 第一章:微型计算机基础

## 计算机的发展

**根据电子器件划分**：

- 1946年第一代：**电子管**计算机：**ENIAC**。

- 1958年第二代：**晶体管**计算机。

- 1964年第三代：**中小规模集成电路**计算机。

- 1971年第四代：**大规模和超大规模集成电路**计算机，出现了**微型计算机**。

**微型计算机的发展**：

1971年，Intel公司设计了世界上**第一个微处理器芯片**`Intel 4004`

 <img src="第一章/计算机的发展/微型计算机的发展.png" style="zoom:67%;" >

## 微机主要性能指标

- **字长**：CPU**一次处理加工**信息位数(二进制)。是标明微信计算机的负重和CPU的性能的参数。

- **主存容量**：能够容纳二进制位数。**最小单位**为：位(bit)，**基本单位**为：字节(Byte)  `1B = 8 bit`。

- **主频**：脉冲个数，也叫时钟速率。

  <img src="第一章/微机的主要性能指标/主频换算.png" style="zoom:67%;" >

- **时钟周期**：频率用`f`表示，主频的倒数：
  $$
  T=\frac 1f
  $$
  <img src="第一章/微机的主要性能指标/时钟周期换算.png" style="zoom:67%;" >

- **总线周期**：

<img src="第一章/微机的主要性能指标/基本总线周期.png" style="zoom:67%;" >

## 微型计算机的系统组成

### 微处理器(Micro processor)

**定义**：

​	一片/n片大规模集成电路组成**中央处理器(CPU)**叫**微处理器**。，也称为**微处理器芯片**。

**特点**：

​	集成度越来越高。

**构成**：

> CPU = ALU(运算器) + CU(控制器) + R(寄存器组)

**注意**：

​	电子部件(逻辑器件)发展到第四代才有了微处理器。**它是微型计算机的运算和控制核心**。**它能够自动按照程序的功能完成指令的运行**，所以能够**自动运行**。

### 微型计算机(Micro computer)

​	以**CPU**/(微处理器)为核心构成计算机(裸机)，只包括**硬件**。

主板主要指的是微型计算机，它是硬件集成在一块板子的集合。

**构成**：

> CPU + 内存(主存) + I/O接口(Input/Output)

### 微型计算机系统(Micro computer system)

**构成**：

> 微型计算机+软件+外围设备

**发展顺序**：

<img src="第一章/微型计算机的组成/发展过程.png" style="zoom:67%;" >

**微型计算机系统结构图**：

<img src="第一章/微型计算机的组成/微型计算机系统机构图.png" style="zoom:67%;" >

## 五大部件

<img src="第一章/五大部件/概述.png" style="zoom:67%;" >

计算机的五大部件是**控制器**、**运算器**、**存储器**、**输入设备和输出设备**。

## 总线(BUS)

​	计算机系统各部件之间**传输信息**的公共通道(BUS)。

<img src="第一章/总线/主板结构图.png" style="zoom:67%;" >

<img src="第一章/总线/PCI总线.png" style="zoom:67%;" >

### 按照连接的部件

<img src="第一章/总线/按照连接的部件.png" style="zoom:67%;" >

### 按照传送信息种类

<img src="第一章/总线/按照传送信息种类.png" style="zoom:67%;" >

### 按照数据传输方式

<img src="第一章/总线/按照数据传输方式.png" style="zoom:67%;" >

### 按照总线标准

<img src="第一章/总线/按照总线标准.png" style="zoom:67%;" >

按*功能*可分为两部分:总线接口单元BIU(Bus Interface Unit)和执行单元*EU*(Execution Unit)。

### 总线的性能指标

1. **总线带宽**：bps(bit/s) ：数据传输率。 

> USB 2.0： 480mbps
>
> USB 3.0： 4.8Gbps

2. **总线位宽**：数据通路宽度。同时传输二进制位数。

3. **总线工作频率**：MHZ 脉冲。

## 微机的软件系统

- **操作系统**	`MS-DOS`

- **编辑程序**	`EDIT.COM`

- **汇编程序**	`MASM.EXE`

- **链接程序**	`LINK.EXE`

- **调试程序**	`DEBUG.EXE`

## 冯·诺依曼计算机设计思想

1. 计算机硬件包括五大功能部件
2. 采用二进制
3. 存储程序＋程序自动控制

## 门电路


### 与门

<img src="第一章\门电路\与门.png" alt="或门图示" />


​                        														`A与Ｂ为输入端可有多个输入　Y为输出端`

**与运算**：

​	**计算机指令的＂AND＂**

​	**特点**是只有A与B都是＂`1`＂（高电平）

​	**输出端**才会输出＂1＂　**其他情况**输出端均输出＂0＂

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  1   |  1   |  1   |
|  1   |  0   |  0   |
|  0   |  1   |  0   |

**总结**：

​	**有零出零**

​	**全一出一**：只有唯一情况 保证译码唯一。

​	**输入端可以多接 最好接双数：**与门基本形式是双数。

​	**当有多个输入端为1 用与门 保证唯一性**。

------


### 或门

<img src="第一章\门电路\或门.png" />

​													                     	`A与Ｂ为输入端可有多个输入　Y为输出端`

或运算：

​	**计算机指令的＂OR＂**

​	**特点**是只有A与B都是＂0＂（高电平）

​	**输出端**才会输出＂0＂　**其他情况**输出端均输出＂1＂

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  1   |  1   |  1   |
|  1   |  0   |  1   |
|  0   |  1   |  1   |

**总结**：

​	**有一出一** 

​	**全零出零**：唯一情况

​	**碰到输入端为0 用或门**

​	**输入端可以多接 最好接双数**

------


### 非门



<img src="第一章\门电路\非门.png"  />

​											                                         	`一般输入端、输出端都只有一个`

非运算：

​	**计算机指令的＂NOT＂**

​	**特点**是将输入的内容取反后输出，即若A为＂1＂则Y输出为＂0＂；若A为＂０＂则Y输出为＂１＂

　**注意**：输出端的小圆圈　这个圆圈代表的就是取反　

|  A   |  Y   |
| :--: | :--: |
|  0   |  1   |
|  1   |  0   |

**补充**：

<img src="第一章\门电路\同相器反相器.png" />


------


### 组合型

------

#### 与非门

<img src="第一章\门电路\与非门逻辑结构.png" style="zoom:67%;" />

<img src="第一章\门电路\与非门逻辑符号.png" style="zoom:67%;" />

​										                      				`A与Ｂ为输入端可有多个输入　Y为输出端`

与非运算：

​	**特点**是只有A与B都是＂0＂（高电平）

​	**输出端**才会输出＂1＂　**其他情况**输出端均输出＂1＂

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  1   |
|  1   |  1   |  0   |
|  1   |  0   |  1   |
|  0   |  1   |  1   |

总结：

​	**有零出一**

​	**全一出零**：只有唯一情况 保证译码唯一

​	**输入端可以多接 最好接双数：**与非门基本形式是双数 

​	**当有多个输入端为1 用与非门 保证唯一性**

------


#### 或非门

<img src="第一章\门电路\或非门逻辑结构.png" style="zoom:67%;" />

<img src="第一章\门电路\或非门逻辑符号.png" style="zoom:67%;" />

​											              			`A与Ｂ为输入端可有多个输入　Y为输出端`

或非运算：

​	**特点**是只有A与B都是＂0＂（高电平）

​	**输出端**才会输出＂1＂　**其他情况**输出端均输出＂1＂

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  1   |
|  1   |  1   |  0   |
|  1   |  0   |  0   |
|  0   |  1   |  0   |

总结：

​	**有一出零** 

​	**全零出一**：只有唯一情况 保证译码唯一

​	**输入端可以多接 最好接双数**

------

#### 异或门

<img src="第一章\门电路\异或门.png" />

​														`A与Ｂ为输入端可有多个输入　Y为输出端`

​																	         **Y = A + B**

#### 异或运算

​	**计算机指令的＂XOR＂**

　异或电路的运算是A与B的**输入相同**时Y输出是＂0＂**不相同**的Y输出为＂１＂

|  A   |  B   |  Y   |
| :--: | :--: | :--: |
|  0   |  0   |  0   |
|  0   |  1   |  1   |
|  1   |  0   |  1   |
|  1   |  1   |  0   |

总结：

​	**输入相同出0**

​	**输入不同出1**


------

## 进制

**采用不同的进制的原因**是不同的领域用到的技术形式不相同　

- 在计算机底层都以**二进制**形式存在。

<img src="第一章/进制/进制总结.png" />

### 进位计数制

​	**按照进位的方法进行计数，称为进位计数制。**

​	**常见的进位计数制**：二进制、八进制、十进制、十二进制、十六进制等等。

  **R进制数的特点：**

- 具有R个不同的数符。0，1，2．．．，R－１

- 逢R进一。

  进位计数制的一般表达式(按权展开式)：

  R进制的表示方法，任一R进制数S可表示为

  > S=a<sub>n-1</sub> a<sub>n-2</sub> ... a<sub>1</sub> a<sub>0</sub> . a<sub>-1</sub>...+a<sub>-m</sub>           位置表示法
  >
  > =a<sub>n-1</sub>R<sup>n-1</sup> + ... + a<sub>1</sub>R<sup>1</sup> + a<sub>0</sub>R<sup>0</sup> + a<sub>-1</sub>R<sup>-1</sup> ... +a<sub>-m</sub>R<sup>-m</sup> (按权展开式)
  >
  > 其中:a<sub>i</sub> : R 进制中的数字符号
  >
  > ​		 R：基数
  >
  > ​         R<sup>i</sup> : 位权，简称权

###  十进制N<sub>D</sub>

​	**特点：**


  - ​	有十个数码：0~9

  - ​	逢十进一

加权展开式以10为基数，各位系数为0~9

> N<sub>D</sub> = d<sub>n-1</sub> * 10<sup>n-1</sup> + d<sub>n-2</sub> * 10<sup>n-2</sup>+...+d<sub>0</sub> * 10<sup>0</sup>+d<sub>-1</sub> * 10<sup>-1</sup>+...

例:(1234.5)<sub>10</sub> = 1 * 10<sup>3</sup> + 2 * 10<sup>2</sup> +3 * 10<sup>1</sup> +  4 * 10<sup>0</sup> +5 * 10<sup>-1</sup> 


### 二进制N<sub>B</sub>

**特点：**

- ​	有两个数码：0、1

- ​	逢二进一

加权展开式以2为基数，各位系数为0、1

> N<sub>B</sub> = b<sub>n-1</sub> * 2<sup>n-1</sup> + b<sub>n-2</sub> * 2<sup>n-2</sup>+...+b<sub>0</sub> * 2<sup>0</sup>+b<sub>-1</sub> * 2<sup>-1</sup>+...

例: `1101.101B` = 1 * 2<sup>3</sup> + 1 * 2<sup>2</sup> +0 * 2<sup>1</sup> +  1 * 2<sup>0</sup> +1 * 2<sup>-1</sup> +0 * 10<sup>-2</sup> +1 * 2<sup>-3</sup> 

**注意:**不够八位最好前面加上0 凑成八位

### 八进制N<sub>O/Q</sub>

​	**暂无**

### 十六进制N<sub>H</sub>

​	因为二进制太长 所以采用十六进制 

​	一位十六进制可以表示四位二进制

​	**特点：**


  - ​	有十六个数码：0~9、A~F

  - ​	逢十六进一

加权展开式以16为基数，各位系数为0~9，A~F

> N<sub>H</sub> = h<sub>n-1</sub> * 16<sup>n-1</sup> + h<sub>n-2</sub> * 16<sup>n-2</sup>+...+h<sub>0</sub> * 16<sup>0</sup>+h<sub>-1</sub> * 16<sup>-1</sup>+...

例:`DFC.8H` = 13 * 16<sup>2</sup> +15 * 16<sup>1</sup> +  12 * 16<sup>0</sup> +8 * 16<sup>-1</sup> 


- ### 注意

  不同进位制数以后缀区别,十进制数可不 带后缀。或加括弧，再在括弧之后注明。

  - `101`、`101D`、`101B`、`101H`、`101H`
  - (20)<sub>10</sub>、(1101)<sub>2</sub>、(345)<sub>16</sub>


### 不同进制计数制的转换

#### 			二进制、十六进制转换成十进制

​		**方法：**

​			先将二、十六进制数按权展开，然后按照十进制运算法则求和

​		**举例：** 

​			`1011.1010B`=1 * 2<sup>3</sup>+1 * 2<sup>1</sup>+1 * 2<sup>0</sup>+1 * 2<sup>-1</sup>+1*2<sup>-3</sup>

​								   =(11.625)<sub>10</sub>

​			`DFC.8H`=13 * 16<sup>2</sup> + 15 * 16<sup>1</sup> + 12 * 16<sup>0</sup> + 8 * 16<sup>-1</sup> 

​						  =(3580.5)<sub>10</sub>

#### 			十进制转换成二进制、十六进制

​		**方法：**

​			**整数部分,除基取余**

​				不断**除以**所要转换的进制基数，直至**商为0**。每除一次取一个余数，从低位排向高位。

​			**小数部分,乘基取整**
​				用转换进制的基数乘以小数部分，直至小数为0或达到转换精度要求的位数。每**乘一次取一次整数**，从最高位排到最低位。

​		**举例：**

​			**二进制最好前面加上0 凑成八位**

​			39转换成二进制数        
​			(39)<sub>10</sub>=`00100111B`

​    	    208转换成十六进制数   
​			`208D` = `D0H`

​			`0.625D`转换成十六进制数
​    	    0.625 × 16 = 10.0	 `0.625D` = `0.AH`

​            `208.625D` 转换成十六进制数 
​            `208.625D`= `D0.AH`

​			0.25十进制 转换成 二进制数
​			`0.25D`=`0.01B`

​			(15.8125)<sub>10</sub>转换成二进制数 	
​			(15.8125)<sub>10</sub>=`00001111.1101`

<img src="进制/15.8125.png" >

​        

#### 二进制转换成十六进制

​	由2<sup>4</sup>=16可知 四位二进制数对应一位十六进制数。
​	例:   `3AF.2H` 
​      		= <u>0011</u> <u>1010</u> <u>1111</u>.<u>0010</u> =`1110101111.001B` 	
​				      3      A       F        2

​           `1111101.11B` 
​			   = <u>0111</u> <u>1101</u>.<u>1100</u>  = `7D.CH`         
​					  7       D       C
​    二进制转换为16进制时，整数部分从**最低位**进行划分，**每4位二进制数为一组**，不足4位的，最高位补零；**小数部分**从**最高位**进行划分，每4位二进制数为一组，不足4位的最低为补零

#### 技巧：

​		按照`8421`方法，即对应二进制四位

##### 			十六进制转为二进制：

​				`8421`排列组合成十六进制数

​				`37FH`

​					=  	  3 	    7 	    F
​					   	`8421` `8421` `8421`

​						    **0011  0111  1111**

##### 			 二进制转换为十六进制：

​				每四位为一个 `8421`

​				`0110111100B`

​					=     <u>0001</u>  <u>1011</u>  <u>1100</u>
​					   	`8421` `8421` `8421`

​							    **1        B         C**		

##### 			八进制二进制互相转换：

​				同理，只不过将 `8421` 变为 `421`

​				`11010110`

​					=  	  11   010   110
​					    	`421`  `421`  `421`

​    						    **3       2       6**
​				
​				`765`

​					=  	  7        6       5
​					    	`421`  `421`  `421`

​    			     	    **111    110     101**

##### 		十进制转换二进制：

​				可将十进制先转换成十六进制再转成二进制

​				`39D`

​					=  	 <u>39</u> / 16		余7 

​								2	           余2
​					
​					=    `2    7  H`
​					= `8421` `8421`

​					= **0010   0111**  B
​				`0.25D`

​					=  	 <u>0.25</u> * 16		=4
​					=    `0.4H`
​					= `8421` 

​					= **0.01**  B

## 机器数的表示

### 定点表示法

所有数据的小数点位置固定不变。

## BCD码

BCD码(Binary Coded Decimal)本质就是十进制数 

**二进制编码的十进制数**

### 特点

 （1）BCD码有十个不同字符，逢十进一，是十进制数。
 （2）每一位十进制数用4 位二进制编码表示，是二进制编码的十进制数。即 0000-1001

对于1010-1111 (A~F) 属于无效编码

 （3）直观。

### 两种方式

- #### 组合BCD 也叫压缩BCD 四位表示一位十进制数

​		**举例**

​			56 ---》 (0101 0110)<sub>BCD</sub>

- #### 非组合BCD 也叫非压缩BCD 八位表示一位十进制数

  **举例**		

  ​	56 ---》 (0000 0101 0000 0110)<sub>BCD</sub>

  十进制数876的BCD码
    	876.7 = （1000 0111 0110.0111）<sub>BCD</sub>
   	 876 = `36CH` = `1101101100B`

注意：BCD码  ——>   十进制码  ——>    二进制   

- 除BCD编码外，还有其他二进制编码的十进制数。如余3码、余3循环码等。

  <img src="BCD码\十进制与BCD码.png" style="zoom:33%;" >


- ## 字符编码

  **(ASCII码 American Standard Code For Information Interchange，美国标准信息交换码)** 

  一般用来**显示** 或**传输**  用

  可表示**128种字符的7位基本ASCⅡ码**和**可表示256种字符的8位扩充ASCⅡ码**（可重新定义）。
    字符可分为：**显示字符**和**控制字符**。
      0—9：ASCII码	`30H`—`39H`
      A—Z：                 `41H`—`5AH`
      a—z：                  `61H`—`7AH`

  <img src="ASCII码\ASCII.png" style="zoom:33%;" >

- ## 带符号数的表示方法

（1）机器数与真值
机器数：计算机中数的表示形式，以二进制的形式表示，位数通常为8的倍数 。一般数的最高位作符号位，“0”表示“+”， “1”表示“-”。
真值： 机器数所代表的实际数值。可用二进制
    表示，也可用其他进制表示。
举例：一个8位机器数与它的真值对应关系如下：
    真值： X1= 84 = +1010100B       X2 = -84= -1010100B 
 机器数： [X1]<sub>机</sub>= 01010100B        [X2]<sub>机</sub>= 11010100B



# 第二章:16位微处理器

![image-20211127101638956](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127101638956.png)

![image-20211118150416207](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118150416207.png)

左侧为Eu 右侧为BIU (总线接口单元)

20位物理地址(下图) 指令队列从内存和其他组件通过系统组件存入内部的指令队列 8088是4个字节 8086是8个字节

![image-20211118150714336](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118150714336.png)

![image-20211118151007951](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118151007951.png)

ALU包括算术运算 和逻辑运算

![image-20211118151525520](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118151525520.png)

执行EU 单元的alu

两大部分形成了流水线技术 ：时间上的并行 ：同一时间同时工作。

![image-20211127102912249](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127102912249.png)



![image-20211118151738303](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118151738303.png)

*EU处理*单元是 执行单元(Execution Unit) 英文Execution Unit的缩写,是微*处理*器中的执行单元,它负责指令的执行,实际是既有控制器*的功能*,也有运算器*的功能*。 包括:ALU、标志寄存器、暂存器、寄存器组、控制单元。*EU*和BIU是组成06微*处理*器的两个基本*功能部件*,他们相互配合完成指令作。当*EU*从指令队列中去走指令后,指令队列出现空字节,BIU就立即自动地从内存中取出后续的指令放入队列;当*EU*执行指令需要作数时,BIU就根据*EU*给出的作数有效,从指定的内存单元或I/O端口取出*数据*供*EU*使用;当*EU*运算结束后,BIU将运算结果写入指定的内存单元或I/O端口。*EU*和BIU这两个*功能部件*又是相互的。

![image-20211118151951245](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118151951245.png)

Ax累加寄存器 BX细致寄存器 Cx计数寄存器 Dx数据寄存器 后面X表示通用寄存器，用于存放不同的数据，数据寄存器AX Bx CX DX 可以分为高八位低八位 

si原变址 di 目标(目的)  l指变址 用于存放特定的信息 用于存放地址的

base /stack堆栈 point指针

![image-20211118152215125](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152215125.png)

![image-20211118152307278](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152307278.png)

也叫段基地址 段首地址

cs代码段cs专门用于保存指令 代码块的指令除cs以外保存的数据信息 (DS ss es) 。

ds数据段寄存器  保存数据信息

ss堆栈段寄存器 保存数据信息

Es附加段寄存器 保存数据信息

上面是十六位的四个段寄存器

注意 功能 用法 dssses 表示对应有效的地址 对应数据的有效地址

cs 对应指令的指针 中间的冒号代表逻辑对应关系 代表逻辑地址

![image-20211118152637451](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152637451.png)

![image-20211118152652016](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152652016.png)

![image-20211127104739531](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127104739531.png)专门用于存放  通过ip指针确定指针的位置

![image-20211118152748690](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152748690.png)

![image-20211118152933439](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211118152933439.png)

![image-20211127104929318](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127104929318.png)

可以用psw 和fr表示

![image-20211127104951305](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127104951305.png)

红色的对于标志寄存器 

of溢出标志位 sf符号标志位 zf结果为0标志位 af辅助标志位 pf辅助校验标志位 cf进位或者叫借位标志位

zf=1 为0 zf=0 结果不为0

![image-20211127105304043](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127105304043.png)

df方向标志 if中断标志 tf单步标志

![image-20211127105357940](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127105357940.png)

![image-20211127105429860](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127105429860.png)

![image-20211127105517721](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127105517721.png)

8088/8086是16位为拇指大小 

![image-20211127105821481](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127105821481.png)

带a的是地址总线 带d的是数据总线 

![image-20211127110052556](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110052556.png)

*表示上面带杠  表示低电平有效

![image-20211127110150524](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110150524.png)

![image-20211127110131365](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110131365.png)

![image-20211127110324586](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110324586.png)

 ![image-20211127110334903](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110334903.png)

ad复用从a0到a15、 34号角 BHE cpu访问总存，总线高允许 、28号角高低电平不一样

![image-20211127110940347](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127110940347.png)

括号外面最小模式 括号里面是最大模式 

![image-20211127111030416](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111030416.png)

![image-20211127111211602](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111211602.png)

![image-20211127111356071](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111356071.png)

![image-20211127111634552](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111634552.png)

![image-20211127111755240](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111755240.png)

![image-20211127111822415](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127111822415.png)

![image-20211127112016188](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112016188.png)

DMA 工作时两个属于高阻态

tw等待周期

![image-20211127112237868](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112237868.png)

![image-20211127112305955](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112305955.png)

![image-20211127112352331](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112352331.png)

跟if(中断标志) if=1开中断 

![image-20211127112446393](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112446393.png)

![image-20211127112518350](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112518350.png)

![image-20211127112604389](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112604389.png)

![image-20211127112718856](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112718856.png)

![image-20211127112804023](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112804023.png)

![image-20211127112845938](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127112845938.png)

![image-20211127113007282](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127113007282.png)

![image-20211127113043152](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127113043152.png)

![image-20211127163523406](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127163523406.png)

![image-20211127163857178](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127163857178.png)

![image-20211127163905744](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127163905744.png)

![image-20211127164217937](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127164217937.png)

![image-20211127164325785](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127164325785.png)

8282地址锁存器

![image-20211127164443470](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127164443470.png)

8286缓冲器

![image-20211127165320433](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165320433.png)

![image-20211127165444742](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165444742.png)

![image-20211127165500995](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165500995.png)

![image-20211127165610263](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165610263.png)



![image-20211127165653605](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165653605.png)

![image-20211127165707983](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165707983.png)

![image-20211127165844267](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127165844267.png)



![image-20211127170036930](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170036930.png)

![image-20211127170240873](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170240873.png)

![image-20211127170251278](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170251278.png)

 ![image-20211127170442635](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170442635.png)

![image-20211127170610936](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170610936.png)

oe为0表示读 

![image-20211127170927407](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127170927407.png)

![image-20211127171219139](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127171219139.png)

![image-20211127171254241](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127171254241.png)

![image-20211127171326335](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127171326335.png)

![image-20211127171540728](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127171540728.png)

![image-20211127171600849](C:\Users\LetengZzz\AppData\Roaming\Typora\typora-user-images\image-20211127171600849.png)



# 第三章:存储器系统

# 第四章:8088/8086指令系统

# 第五章:汇编语言伪指令

# 第六章:汇编语言程序设计

# 第七章:输入输出系统

# 第八章:控制器芯片

# 第九章:转换器芯片



