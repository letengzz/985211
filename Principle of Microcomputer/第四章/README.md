# 指令

**指令**：指令是指示计算机完成特定操作的命令

**指令系统**：指令系统是计算机能够执行全部命令的集合，它取决于计算机的硬件设计。指令系统因机而异，没有通用性(可移植性)。

![1](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Fourth/202205261923253.png)

**指令格式**：

```
操作码 [操作数1],[操作数2]
```

- **操作码**：执行何种操作
- 操作数1(地址码)：**目的操作数**(指令加工之后形成的数据)
- 操作数2(地址码)：**源操作数**(指令加工之前的数据)

参加操作的数据：**目的操作数**、**源操作数**

**指令中的操作数表征方法**：

![2](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Fourth/202205261923144.png)

**地址码个数**：

- 二地址指令：

> 操作与运算指令：`AND	OP目,OP源`、逻辑或运算指令：`OR	OP目,OP源`、逻辑异或运算指令：`XOR	OP目,OP源`、测试指令：`TEST	OP目,OP源`
>
> 输入指令：`INT  累加器，端口`、输出指令：`OUT	端口,累加器`
>
> 一般数据传送指令：`MOV	OP目,OP源`、数据交换指令：`XCHG	OP1,OP2`、取有效地址EA指令：`LEA	OP目,OP源`、指针送寄存器和`DS`指令：`LDS	OP目,OP源`、指针送寄存器和`ES`指令：`LES	OP目,OP源`
>
> 不带进位的加法指令：`ADD	OP目,OP源`、进位的加法指令：`ADC	OP目,OP源`、不带借位的减法指令：`SUB	OP目,OP源`、带借位的减法指令：`SBB	OP目,OP源`、取补指令`NEG	OP`、比较指令：`CMP	OP目,OP源` 
>
> 移位指令：`SHL`、`SAL`、`SHR`、`SAR`、`ROL`、`ROR`、`RCL`、`RCR`
>
> 字符串传送指令：`MOVS  OP目，OP源`、字符串比较指令：`CMPS	OP目，OP源` 、字符串搜索指令：`SCAS	OP`
>
> 处理器交权指令：`ESC EXTOPCD，OP源`

- 一地址指令：

> 逻辑非运算指令`NOT　OP`、堆栈操作指令`PUSH	OP` `POP	OP`、加1指令：`INC	OP`、减1指令`DEC	OP`、无符号数乘法：`MUL	OP`、带符号乘法：`IMUL	OP`、无符号数除法：`DIV	OP`、带符号数除法：`IDIV	OP`
>
> 条件转移指令：`JA/JNBE	目标标号`、`JAE/JNB	目标标号`、`JB/JNAE	目标标号`、`JBE/JNA	目标标号`、`JG/JNLE	目标标号`、`JGE/JNL	目标标号`、`JL/JNGE	目标标号`、`JLE/JNG	目标标号`、`JC	目标标号`、`JNC	目标标号`、`JZ/JE	目标标号`、`JNZ/JNE	目标标号`、`JO	目标标号`、`JNO	目标标号`、`JNP/JPO	目标标号`、`JP/JPE	目标标号`、`JNS	目标标号`、`JS	目标标号`
>
> 循环控制指令：`LOOP	目标标号`、`LOOPZ/LOOPE	目标标号`、`LOOPNZ/LOOPNE	目标标号`、`JCXZ	目标标号`
>
> 软中断指令：`INT n`
>
> 条件转移指令：`JMP	OP`

- 零地址指令：

> 标志操作指令：`CLC`、`STC`、`CMC`、`CLD`、`STD`、`CLI`、`STI`
>
> 处理器暂停指令：`HLT`、处理器等待指令：`WAIT`、空操作指令：`NOP`、总线封锁前缀：`LOCK`、换码指令：`XLAT`
>
> 读取标志指令：`LAHF`、设置标志指令：`SAHF`、对标志寄存器的堆栈操作指令：`PUSHF`、`POPF`
>
> 符号扩展指令`CBW`、字扩展指令`CWD`、非组合BCD码的加法调整指令：`AAA`、组合BCD码的加法调整指令：`DAA`、非组合BCD码的减法调整指令：`AAS`、组合BCD码的减法调整指令：`DAS`、非组合BCD码的乘法调整指令：`AAM`、非组合BCD码的除法调整指令：`AAD`
>
> 溢出中断指令：`INTO`、中断返回指令：`IRET`、返回指令：`RET`
>
> 字符串搜索指令：`SCASB`、`SCASW`、取字符串指令：`LODSB`、 `LODSW`、存字符串指令：`STOSB`、`STOSW`

