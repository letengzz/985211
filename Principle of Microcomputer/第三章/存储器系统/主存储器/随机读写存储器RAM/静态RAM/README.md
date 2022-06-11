# 静态RAM(`SRAM`)

## 工作原理

   MOS型静态RAM的基本存储单元，可由六个MOS场效应晶体管构成，其基本存储单元电路：

![image-20220602181831304](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111504295.png)

- VF1,VF2：组成双稳态触发器
- VF3,VF4：负载管
- VF5,VF6：控制管

设VF1截止，VF2导通，为1；

​    VF2截止，VF1导通，为0；（A点状态）

## 组成

将多个存储单元按一定方式排列起来，就组成了一个静态RAM存储器

![image-20220602183738153](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111504729.png)

**例**：[Intel 2114]()  1K × 4位 4094字节  64 × 64矩阵

![image-20220602183801906](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111504178.png)

## 特点

- 只要不断电，就不会丢失信息;相对[DRAM]()，存取速度更快。

- 由**触发器**构成，集成度较低，功耗大，造价成本高。
- 一般用作高速缓冲存储器 (`cache`)。