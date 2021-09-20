# *<u>**C语言**</u>*

- ## 程序设计基本概念

计算机不过是一种具有**内部存储能力**、由**程序自动控制**的电子设备。

**"程序"(program)：**连续执行的一条条能被计算机识别和执行的**有序指令**的集合。

**"程序设计语言"：**人与机器"对话"的一类媒介和工具，由语句(statement)组成。

**"语句"：**组成程序的**基本单位**。一个";"表示一个语句，单行一个";"叫空语句。每条语句都可以认为是一条指令

**机器语言：**(machine language)计算机直接使用的**二进制**形式的程序语言或机器代码。

**汇编语言：**(assembler language)一种面向机器的用**符号**表示的低级程序语言。相当于机器指令的助记符号，与机器语言相近。

**高级语言：**(high-level language)是易为人们所理解的**完全符号化**的程序设计语言。

**源程序：**用户用高级语言编写的程序。**C语言源程序文件名字后缀一般必须为"`.C`"**。

**目标程序：**由二进制代码组成的程序。**形式:0、1** C语言**后缀为"`.obj`"**。

**编译程序：**具有翻译功能的软件。由编译程序**转换**为**机器代码**。

**解释程序：**具有翻译功能的软件。由解释程序**转换**直接为**机器代码**。一条一条解释为二进制，必须从头到尾执行一遍。

**连接器**：用于连接相关的目标文件以生成可执行文件。

**连接(linker)：**将目标模块和其他一些必要的功能模块装配在一起，生成可执行文件，**执行文件后缀为"`.exe`"**

### 程序设计

#### 简单的程序设计一般包含以下几个部分：

- (1)**确定数据结构**。根据任务书提出的要求、指定的输人数据和输出结果，确定存放数据的数据结构。

- (2)**确定算法**。针对存放数据的数据结构来确定解决问题、完成任务的步骤。

- (3)**编码**。根据确定的数据结构和算法,使用选定的计算机语言编写程序代码,输人到计算机并保存在磁盘上,简称编程。

- (4)**在计算机上调试程序**。消除由于疏忽而引起的语法错误或逻辑错误;用各种可能的输人数据对程序进行测试，使之对各种合理的数据都能得到正确的结果,对不合理的数据能进行适当的处理。

- (5)**整理并写出文档资料。**

### 算法

算法是指为解决某个特定问题而采取的确定且有限的步骤。一个算法应当具有以下特征：

- (1)**有穷性。**一个算法包含的操作步骤应该是有限的。也就是说,在执行若干个操作步票之后,算法将结束，而且每一步都在合理的时间内完成。

- (2)**确定性**。算法中每一条指令必须有确切的含义,不能有二义性,对于相同的输人必能得出相同的执行结果。

- (3)**可行性。**算法中指定的操作,都可以通过已经验证过可以实现的基本运算执行有限次后实现。

- (4)**有零个或多个输人。**在计算机上实现的算法是用来处理数据对象的,在大多数情况下这些数据对象需要通过输人来得到。

- (5)**有一个或多个输出。**算法的目的是为了求“解”,这些“解”只有通过输出才能得到。

  算法可以用各种描述方法来进行描述,最常用的是**伪代码**和**流程图**。

#### 伪代码

​	伪代码是一种近似于高级语言但又不受语法约束的一种语言描述方式,这在英语国家中使用起来更为方便。

#### 流程图

​	流程图是算法的一种**图像化**表示方式。能直观、清晰，更有利于人们设计与理解算法。

​	<img src="img/流程图/流程图基本图形.png" style="zoom: 50%;" >

​	由这些基本图形中的框和流程线组成的流程图来表示算法形象直观,简单方便。但是,这种流程图对于流程线的走向没有任何限制,可以任意转向,在描述复杂的算法时所占篇幅较多，费时费力且不易阅读。

​	随着结构化程序设计方法的出现,**1973年**美国学者`I.Nassi`和`B.Shneiderman`提出了一种新的流程图形式,这种流程图完全去掉了流程线,算法的每一步都用一个矩形框来描述,把一个个矩形框按执行的次序连接起来就是一个完整的算法描述。这种流程图用两位学者名字的第一个英文字母命名,称为**N-S流程图**。

### 结构化程序和模块化结构

#### 结构化程序

​	结构化程序由三种基本结构组成。结构化的程序设计语言：层次清晰，便于按**模块化方式组织程序**，易于**调试和维护**。

- **顺序结构**

  如赋值语句、输入、输出语句都可构成顺序结构。当执行这些语句构成的程序时，将按照这些语句的先后顺序**逐条执行**，**没有分支**，**没有转移**。

  <img src="img/流程图/顺序结构流程图.png" style="zoom: 50%;" >

- **选择结构**

  如if语句、switch语句都可以构成选择结构。当执行到这些语句时，将根据不同的条件去执行不同分支中的语句

  <img src="img/流程图/选择结构流程图.png" style="zoom: 50%;" >

- **循环结构**

  如for循环、while循环、do-while循环。将根据各自的条件，使同一组语句重复执行多次或一次也不执行。

  - 当型循环的特点是：当指定的条件满足(成立)时，就执行循环体，否则就不执行。

  
  <img src="img/流程图/当型循环流程图.png" style="zoom: 50%;" >
  
  - 直到型循环的特点是：执行循环体直到指定的条件满足(成立)时就不再执行循环体。
  
  <img src="img/流程图/直到型循环流程图.png" style="zoom: 50%;" >

已经证明，由三种基本结构组成的算法可以解决任何复杂的问题。由三种基本结构所构成的算法称为**结构化算法**；由三种基本结构所构成的程序称作**结构化程序**。

例：先后输人若干个整数,要求打印出其中最大的数,当输人的数小于0时结束。用N-S流程图表示算法。

解题的思路是:先输人一个数,在没有其他数参加比较之前,它显然是当前最大的数，把它放到变量max中。让max始终存放当前已比较过的数中的最大值。然后输入第二个数,并与max比较,如果第二个数大于max，则用第二个数取代max中原来的值。如此先后输人和比较,每次比较后都将值大者放在max中,直到输入人的数小于0时结束。最后max中的值就是所有输入数中的最大值。

<img src="img/流程图/例题.png" style="zoom: 50%;" >

#### 模块化结构

​	当计算机在处理较复杂的任务时,所编写的程序经常由上万条语句组成,需要由许多人来共同完成。这时常常把这个复杂的任务分解为若千个子任务,每个子任务，又分成很多个小子任务，每个小子任务只完成一项简单的功能。在程序设计时,用一个个小模块来实现这些功能,每个程序设计人员分别完成一个或多个小模块。我们称这样的**程序设计方法为“模块化”的方法,由一个个功能模块构成的程序结构为模块化结构。**

​	由于把一个大程序分解成若干相对独立的子程序,每个子程序的代码一般不超过一页纸,因此对程序设计人员来说,编写程序代码变得不再困难。这时只需对程序之间的数据传递做出统一规范,同一软件可由一组人员同时进行编写,分别进行调试，这就大大提高了程序编制的效率。

​	软件编制人员在进行程序设计的时候,首先应当集中考虑主程序中的算法,写出主程序后再动手逐步完成子程序的调用。对于这些子程序也可用调试主程序的同样方法逐步完成其下一层子程序的调用。这就是**自顶向下、逐步细化、模块化**的程序设计方法。

​	C语言是一种结构化程序设计语言。它提供了**三种基本结构**的语句;**提供了定义“函数”的功能**,在c语言中没有子程序的概念，它提供的**函数**可以完成子程序的所有功能;c语言允许对函故单独进行编译,从而可以实现模块化。另外，c语言还提供了丰富的数据类型。这些都为结构化程序设计提供了有力的工具。

- ## C语言介绍

  C语言是结构化程序设计语言的代表作

  <img src="img/C语言编译程序功能.png">

  ### C语言的诞生

  - 70年代，由美国贝尔实验室的**`Thompson`** (肯·汤普森) 和**`D.M.Ritchie`** (丹尼斯·里奇)合作开发的**UNIX**操作系统和C语言诞生了，C语言**最初用于开发系统级程序**，UNIX操作系统和C语言像一对孪生姐妹，她们以自己崭新的面貌一开始就引起了人们的广泛注意。后来又经过不断改进和实践的考验，这对姐妹已迅速成长和成熟，展示出了强大的生命力，被公认为最优秀的**操作系统**和**计算机语言**之一。近30年来，C语言帮助了UNIX的成功，UNIX的发展又推动了C语言的普及和发展。C语言应用非常广泛，我们熟知的Windows操作系统基本上是用C语言编写的。
  - 1977年出现了不依赖于具体机器的C语言编译文本"可移植C语言编译程序"，使C语言移植到其他机器的工作大大简化。
  - 1983年，美国国家标准化协会(ANSI)根据C语言各种版本对C的发展和扩充，制定了新的标准ANSI C，比标准C 有了很大的发展。
  - 1988年，K&R 按照ANSI C修改了他们的《The C Programming Language》。
  - 1987年，ANSI 公布了新标准--87 ANSI C。
  - 1990年，国际标准化组织接受了87 ANSI C 为ISO C的标准(`ISO9899-1990`)。
  - 1994年，ISO又修订了C语言标准。
  - 1999年，ISO发布了最近的C语言规范，被称为`C99`。
  - 2011年12月8日，国际标准化组织(ISO)和国际电工委员会(IEC)发布的`C11`标准是C语言的第三个官方标准，也是C语言的最新标准，该语言更好的支持了汉字函数名和汉字标识符，一定程度上实现了汉字编程。

  目前流行的C语言编译系统大多是以ANSI　C为基础进行开发的从而使C发展成一种独立于UNIX、独立于具体计算机类型的计算机语言。之后，C语言先后移植到大、中、小、微型计算机上，已独立于UNIX和PDP，风靡世界，成为当今世界上最为流行的、广大程序设计者最为喜爱的计算机语言之一。

  说明：不同版本 的C编译系统所实现的语言功能和语法规则略有差别，因此要了解所用的C语言智能编译系统的特点。

  ### C语言的特点：

  1. C语言是一种**结构化语言。**层次清晰，便于按**模块化方式组织程序**，易于**调试和维护**。

  2. C语言语句**简洁、紧凑、使用方便、灵活。**

       - 只有37个关键字，分为四个大类：

           - 数据结构关键字12个。
           - 控制语句关键字12个。
           - 存储类型关键字4个。
           - 其他关键字9字。
  
       - 9种控制语句
  
       - 数据构造能力强
  
       - 运算符丰富，共有34种运算符，可以实现其他高级语言难以实现的一些运算

       - 程序书写格式自由

  3. C语言程序**易于移植。**

  ​		用C语言编写的程序可以从一种环境不加或稍加改动就能搬到另一种环境中运行。

  4. ​	C语言由**强大的处理能力。**既可以用于系统软件的开发，也适合应用软件的开发。

  5. ​	C语言是一种中级语言，**生成的目标代码质量高，运行效率高。**

  ​		它既**具有高级语言的通用性及易写易读的特点，又具有汇编语言(低级语言)的"位处理"、"地址操作"等能力。**C语言允许直接访问物理地址，能进行位操作，能实现汇编语言的大部分功能，可以直接对硬件进行操作。

  ### C语言运行过程

  ​	C源程序经过 C编译程序**编译**之后生成一个后缀`.OBJ`的二进制文件(被称为**目标文件**)，然后由称为**"连接程序"(Link)**的软件，把此`.OBJ`文件与C语言提供的各种库函数**连接**起来**生成**一个后缀为`.EXE`的**可执行文件**。在操作系统环境下，只需**点击或输入**此文件的名字(而不必输入后缀`.EXE`)，该可执行文件就可以**运行**。

  <img src="img/编译和执行过程.png" style="zoom: 50%;" >

  ### C语言构成和格式

  ​	**头文件**：含有函数的声明和预处理语句，用于帮助访问外部定义的函数。头文件的扩展名"`.h`"

  例：

  ```c
  #include <stdio.h>
  void main(){
      int a;
      printf("Hello World");
  }
  ```
  
  - 以#开始的语句称为预处理器指令
  
      #include语句不是必须的 但是 如果由该语句 就必须将它放到程序的开始处，行尾不可以加";"
  
  - C都是由**主函数**开始执行 从主函数结束执行

  - main是主函数，C程序**有且只有一个**主函数。 
    main()函数是C程序的起点 main()函数可以返回一个值 也可以不返回值 如果某个函数没有返回值，那么在它的前面有一个关键字void
  
- 在函数的起始行后面用一对花括号"{ }" 括起来的部分为函数体。在函数定义的后面有一个左大括号 即"{"它表示函数的开始，后面是函数的主体 大括号也可以将语句块括起来,在函数定义的结尾处有一个右大括号 即"}"

- 函数体内通常有定义(说明)部分和执行语句部分。

  "int a" 为程序的**定义部分**。

  "print f("Hello World");"为程序的**执行部分**。

  执行部分的语句称为可执行语句，必须放在定义部分之后，语句的数量不限，程序中有这些语句向计算机系统发出操作指令。

- 函数主体中的每个语句都以**分号**结束。C程序中的一个语句可以跨越多行，并且用分号**通知编译器该语句已结束**。

#### 注释

1. 必须成对出现
2. "/" 和 "**" 之间不能有空格*
3. 注释可以出现在程序的任何地方
4. 注释部分对程序运行不起作用
5. 在注释之间不可以再嵌套/* */

- 多行注释


  ```c
  /*
  Hello World
  */
  ```

- 单行注释


  ```c
  //
  ```

  ### 标识符、常量、变量

####  标识符

​	在C语言中，有许多符号的命名，如变量名、函数名、数组名等，都必须遵守一定的规则，按此规则命名的符号称为标识符。

​	命名规则：

1. 只能由字母、数字和_(下划线)组成

2. 必须以字母或_(下划线)开头

**注意：**

- 大写字母和小写字母是不同的两个字符

- 标识符长度：C语言编译系统是有规定的，即标识符的前若干个字符有效，超过的字符不被识别。

标识符可以分为三类：

1. ##### 关键字

   ​	C语言已经预先规定了一批标识符，它们在程序中都代表着固定的含义，不能另作他用，这些标识符称为关键字

   **C语言标识符 -->  [Here](#C语言关键字)**

   ------


2. ##### 预定义标识符

   ​	C语言中**预先定义并具有特定含义**的标识符称为预定义标识符，如C语言提供的库函数的名字(如 `printf`)和预编译处理命令(如`define`)等。C语言允许把这类标识符重新定义另作他用,但这将使这些标识符失去预先定义的原意。鉴于目前各种计算机系统的C语言都一致把这类标识符作为固定的库函数名或预编译处理中的专门命令使用,因此为了避免误解,建议用户不要把这些预定义标识符另作他用。


3. ##### 用户标识符

   ​	由用户根据**需要**定义的标识符称为用户标识符，又称自定义标识符。用户标识符一般用来给变量、函数、数组等命名。程序中使用的用户标识符除要遵守标识符命名规则外,还应注意做到"**见名知义**”,即选择具有一定含义的英文单词或汉语拼音作为标识符,如number1 , red 、yellow , green , work等,以增加程序的可读性。
   ​	如果用户标识符与关键字相同,则在对程序进行编译时系统将给出出错信息;如果用户标识符与预定义标识符相同,系统并不报错,只是该预定义标识符将失去原定含义,代之以用户确认的含义,这样有可能会引发一些运行时错误。

  #### 常量

​	在程序运行过程中，**其值不能被改变的量**叫变量。C语言中，有整型常量、实型常量、字符常量、字符串常量等类型。

​	整型常量和实型常量又称为**数值型数据**，它们有正值和负值的区分。

​	**基本整型数据**只用数字表示，不带小数点，例如12、-1等。

​	**实型常量**必须用带小数点的数表示，例如3.14159、-2等

​	**字符型常量**：＇`A`＇和＇`ｌ`＇

​	**字符串常量**：`NICE`

​	**符号常量**：在C语言程序中,可以用一个符号名来代表一个常量，称为符号常量。这个符号名必须在程序中进行特别的“指定”,并符合标识符的命名规则。如：`PI`

​	常量的命名规则：都用大写，中间用_

```c
#include <stdio.h>

#define MY_AGE 1000

void main() {
    printf("%d",MY_AGE);
}
```

​	也可以用const

```c
#include <stdio.h>

const int MY_AGE = 1000;

void main() {
    printf("%d",MY_AGE);
}
```

区别 使用define 程序在编译的时候自动把所有MY_AGE 替换为10000  不清楚类型会出现一些错误

使用 const 在运行中处理 可以明确的知道类型 推荐const	

整型常量

​	实型常量

​	字符常量

​	字符串常量
  #### 变量

​	

### 数据类型

  #### 整型数据

  	 整型数据 int long  

​	占位符是%d 

long 受限于操作系统环境 32位 4字节 64位 8字节

为了同样使用8个字节使用 长长整型 "long long"

占位符 %ld

写二进制数据

![img](D:\Data\zhan885844@163.com\e9956e82316e4c898c9565e84d62877a\截图.png)

十六进制

![img](D:\Data\zhan885844@163.com\a54a630194a5472eb3581ab9edc44f10\截图.png)

八进制

![img](D:\Data\zhan885844@163.com\000accad2e2a4c6cb2020748e7a6d098\截图.png)

无符号整型数据

![img](D:\Data\zhan885844@163.com\6eb36d4a6633436a9d412d0f4f0f8c4a\截图.png)

int32_就是常见int

八位等于一个字节 一个字节等于 -128-127

所以int8 不超过-128-127

![img](D:\Data\zhan885844@163.com\3426fff774474b44a8bd5dbdab2a6ab2\截图.png)

uint8是无符号 就是 0-255

![img](D:\Data\zhan885844@163.com\5c84d3aafa604ce0bb5b250a574f384a\截图.png)

  #### 实型数据

 float 单精度4字节 32位 占位符 %f

double 双精度 8字节 64位 

占位符 %f

long double长双精度16字节 128位

占位符 %Lf

  #### 字符型数据

char 1字节 8位

查看长度 

![img](D:\Data\zhan885844@163.com\7d633d531ba74419a85b0865958003e2\截图.png)

直接%d 输出编码 97

A 65 a97

![img](D:\Data\zhan885844@163.com\b1cc7434a367412dbd61e8e6f4450027\截图.png)

+32 A +32 = a 

![img](D:\Data\zhan885844@163.com\c4039941fc3b485b9006e261aee92ca0\截图.png)

  #### 字符串数据

  #### 自定义类型

使用typedef 自定义类型

相当于取个别名

![img](D:\Data\zhan885844@163.com\1581f8b60ed84ffd92dd24a4fc486940\截图.png)

![img](D:\Data\zhan885844@163.com\fdbe52ea8d1c44f19c4b973df3c904ba\截图.png)

![img](D:\Data\zhan885844@163.com\9557fcaa58fe431092b863b980c50d5c\截图.png)

![img](D:\Data\zhan885844@163.com\9e973974e6954e97bdfa938ef3187f76\截图.png)

  ### 算术表达式

  

  ### 赋值表达式

  

  ### 自加自减运算符和逗号


- ## 运算符

  ### 关系运算符
  ### 逻辑运算符
  
  逻辑运算符
  
  分行会清晰一点
  
  ![img](D:\Data\zhan885844@163.com\352688a4b0e147ef9713553a50bf94e7\截图.png)
  
  ![img](D:\Data\zhan885844@163.com\84a76552826d4d8fb893440829cabbdd\截图.png)
  
  关于性别
  
  ![img](D:\Data\zhan885844@163.com\0184c926e7fd42a2b2554a5c5049e783\截图.png)
  
  ![img](D:\Data\zhan885844@163.com\1a312612f9ef47ffa1fae727ff6b6036\截图.png)
  
  ### 关系运算符
  ### 关系运算符
  ### 位运算符
  
  & 位与
  
   | 位或
  
   ~ 位反
  
  ^异或
  
  \>>右移
  
  <<左移
  
  ![img](D:\Data\zhan885844@163.com\a307c53e095646278dcd9f5aa8aba308\截图.png)
  
  只要有一个是0 结果就是0 同时为1 才是1
  
  ![img](D:\Data\zhan885844@163.com\024d2eda3ed4452fb13f22737baae398\截图.png)
  
  有任何一个是1 都是1
  
  ![img](D:\Data\zhan885844@163.com\ad37068328f84e16a8aa3c3acdfe47af\截图.png)
  
  求反就是 254
  
  ![img](D:\Data\zhan885844@163.com\46a2383d24d8406da149a6e04ed61ffa\截图.png)
  
  ![img](D:\Data\zhan885844@163.com\c52fafd16d03467e8e9b95ea95fd5bfd\截图.png)
  
  无符号的 就是 最大值的差
  
  异或
  
  ![img](D:\Data\zhan885844@163.com\34bb01ea19cc4b5ab2e6a44f19c99927\截图.png)
  
  两个值 有差别 就是1  无差别就是0
  
  有符号的取反
  
  **0 -》 -1     1 => -2**
  
  ![img](D:\Data\zhan885844@163.com\a704278822514f1a9cbc46ce43facf89\截图.png)
  
  4
  
  ![img](D:\Data\zhan885844@163.com\505178f7495244f18de085a796bf89a9\截图.png)
  
  0
  
  ![img](D:\Data\zhan885844@163.com\bdec3b49262d4e4fb5eb4831665269e4\截图.png)
  
  位运算实例之提取颜色通道
  
  颜色
  
  ![img](D:\Data\zhan885844@163.com\3472b4fc51cc46088af06816cca039a7\截图.png)
  
  只取到红色的值
  
  ![img](D:\Data\zhan885844@163.com\6363dafbe6004871aeab650e4e212c54\截图.png)
  
  取红色通道值
  
  ![img](D:\Data\zhan885844@163.com\325fae9094d04608b2df43fabf7b0a67\截图.png)


- ## 顺序结构

  ### 赋值语句

  

  ### 数据输出

  

  ### 数据输入

  

  ### 复合语句和空语句

  

- ## 选择结构

  ### if语句

  

  ### 条件表达式构成的选择结构

  

  ### switch语句以及用switch语句

  如果没有break 程序会一直往下走 直到break 或程序结束

  ### 语句标号和goto语句

  label是标签 goto label 是跳到label

  ![img](D:\Data\zhan885844@163.com\a617c92136a341ed924cbe3a7ce4375a\截图.png)

  输出1-100

  ![img](D:\Data\zhan885844@163.com\6e1ebebac4124a3f8f956ef9eb3c01c5\截图.png)

  

- ## 循环结构

  ### while语句

  while 先判断后执行

  ![img](D:\Data\zhan885844@163.com\a13289fa65dc483aa851d9934018b28a\截图.png)

  只输出奇数

  ![img](D:\Data\zhan885844@163.com\4f96cecc4fc34ad38193cd59307d16c7\截图.png)

  也可以

  ![img](D:\Data\zhan885844@163.com\b565e536d7364cc494174bb21c140b67\截图.png)

  ### do-while语句

  do-while 先执行后判断

  ![img](D:\Data\zhan885844@163.com\185d8eb5368d43ee9a1d4162b149420e\截图.png)

  数学运算符

  ![img](D:\Data\zhan885844@163.com\e92da663ced74ed295c53b6e648ba80a\截图.png)

  三角函数

  ![img](D:\Data\zhan885844@163.com\c2aad8de0f7248099535c6fc5428ab7f\截图.png)

  ![img](D:\Data\zhan885844@163.com\e86fa94080824a82956b44591b9d6ac9\截图.png)

  ### for循环

  ![img](D:\Data\zhan885844@163.com\47469f3e474240fe9c0e700fc15f69ba\截图.png)

  ![img](D:\Data\zhan885844@163.com\8a40e8f5ba8b460faedc3cf58ef14bb1\截图.png)

  ### 循环结构的嵌套

  嵌套循环

  ![img](D:\Data\zhan885844@163.com\c242d67c83924bbfa8821f853545298f\截图.png)

  九九乘法表

  ![img](D:\Data\zhan885844@163.com\92d2bb30f44842e0b86df1dcb23d73cb\截图.png)

  ![img](D:\Data\zhan885844@163.com\3bed8531e6bc427bbdf23e474737e0e7\截图.png)

  ### break和continue语句

  continue

  只是跳过本次循环继续下一循环

  ![img](D:\Data\zhan885844@163.com\293a517c04e74800935720056938bb89\截图.png)

  

- ## 附录

  - ### 常用转义字符
  
    转义字符
  
    \n 换行符
  
    \r 回车符
  
    \b 退格符 backspace
  
    \t 制表符 相当于tab
  
    \f 换页符
  
    \\ 反斜杠
  
    \' 单引号
  
    \“ 双引号
  
  - ### C语言关键字
  
  - 
