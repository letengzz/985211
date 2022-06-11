# 存储器与CPU的连接

​	存储器芯片的外部引脚按功能分为数据线、地址线和控制线。CPU对存储器的读写操作首先是向其地址线发地址信号，然后向控制线发读写信号，最后在数据线上传送数据信息。每一块存储器芯片的地址线、数据线和控制线都必须和CPU建立正确的连接，才能进行正确的操作。
​	CPU与存储器的连接就是指**地址线、数据线和控制线的连接**。重点说明的是存储器与CPU地址总线的连接方式，必须满足对这些芯片所分配的地址范围的要求。

![image-20220606154057678](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111116942.png)

## 连接方法

**片内**：系统的低位地址线与芯片地址线相连

**片外**：系统的高位地址总线

1. 进地址译码器([2:4]()或[3:8]())进行片选
2. 或者未使用
3. 或者直接片选

**数据总线**(`DB`)：CPU 8位或16位

**地址总线**(`AB`)：CPU的20位

**控制总线**(`CB`)：读/写，IO/M

当CPU选择8088时，DB为8位

- 若芯片的数据线正好8根：

  <img src="https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111116838.png" alt="image-20220606183501815" style="zoom:67%;" />

- 若芯片的数据线不足8根："[位扩充](#位扩充)"

  <img src="https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111116573.png" alt="image-20220606183629003" style="zoom:67%;" />

### 位扩充

地址线的扩充，简称为"字扩充"

**例**：1K × 4 → 1K × 8

**分析**：

①：**单片**：地址线A<sub>0</sub>~A<sub>9</sub>、数据线D<sub>0</sub>~D<sub>3</sub>

②：**总容量**：地址线A<sub>0</sub>~A<sub>9</sub>、数据线D<sub>0</sub>~D<sub>7</sub>

③需要=![image-20220606214108601](D:/Data/typora/photo/image-20220606214108601.png)

![image-20220607190802117](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111116853.png)

![image-20220607191824079](https://cdn.jsdelivr.net/gh/letengzz/Two-C@main/img/PM/Third/202206111116387.png)

## 方法及注意

- CPU系统提供的类型、字长、地址线和数据线
- 形成主存的单片芯片的类型、容量和引脚
- 形成主存的总容量
- 字扩展(组数)或位扩展(每组片数)
- 译码方式的选择
- 各组地址范围的使用或计算
