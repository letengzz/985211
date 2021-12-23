# 选择题

## 简单易错类型

1. **一个C语言程序是由( )**

   A. `一个主程序和若干子程序组成。`

   B.`函数组成。`

   C.`若干过程组成。`

   D.`若干子程序组成。`

2. **在C语言中，整型数据在内存中以( )形式存放。**

   A.`原码`

   B.`补码`

   C.`反码`

   D.`ASCII码`

3. **若给定条件表达式(!m)?(a++):(a--)，则其中表达式!m()**

   A.`和(m==0)等价`

   B.`和(m!=0)等价`

   C.`和(m==1)等价`

   D.`和(m!=1)等价`

4. **以下程序段的输出结果是()。**

   > int i,j;
   >
   > for(j = 10;j <= 11;j++){
   >
   > ​	for(i = 9;i == j-1;i++){
   >
   > ​		printf("%d",j);
   >
   > ​	}
   >
   > }

   A.`11`

   B.`10`

   C.`9`

   D.`10 11`

6. **在C语言中，引用数组元素时，其数组下标的数据类型允许是()。**

   A.`整型常量`

   B.`整型表达式`

   C.`整型常量或整型表达式`

   D.`任何类型的表达式`

7. 

   A.

   B.

   C.

   D.

## 较难类型

# 填空题

1. __

   ```c
   #include <stdio.h>
   f(int a){
       int b = 0;
       static int c = 5;
       a=c++,b++;
       return a;
   }
   int main(){
       int a = 4,i,k;
       for(i = 0;i < 2;i++)  k=f(a++);
       printf("%d\n",k);
       return 0;
   }
   ```

2. __

   ```c
   #include <stdio.h>
   double xpn(float x,int n){
       if(a == 0) return(1);
       else return(x*xpn(x,n-1));
   }
   int main(){
       int n = 3;
       float x = 3;
       double y;
       printf("\n");
       if(n<0)printf("Input n<0!\n");
       else{
           y=xpn(x,n);
           printf("result =%.2f",y);
       }
       return 0;
   }
   ```

3. **下面程序的功能是：求 1!+2!+....+20!的值，请填空：**

   > #include <stdio.h>
   >
   > 
   >
   > int main(){
   >
   > ​	double s = 0,t = 1;
   >
   > ​	int n;
   >
   > ​	for(n = 1;n <= 20;n++){
   >
   > ​		__ ① __
   >
   > ​		__ ② __
   >
   > ​	}
   >
   > ​	printf("1!+2!...+20! = %22.15e\n",s);
   >
   > ​	return 0;
   >
   > }

4. **下面程序的功能是：计算1-3+5-7+...-99+101的值，请填空：**

   > #include <stdio.h>
   >
   > void main(){
   >
   > ​	int i,t,s = 0,sign = 1; 
   >
   > ​	for(i = 1;i <= 10;i+=2){
   > ​		__ ① __
   >
   > ​		s += t;
   >
   > ​		__ ② __
   >
   > ​	}
   >
   > ​	printf("s=%d",s);
   >
   > }

# 编程题

1. **编写程序，输入10个整数存入数组a，在输入一个整数x，在数组a中查找x，找到输出x在10个数中的序号，找不到则输出"no found"**
2. **编写一 函数`int strcmp(char *p1,char *p2)`，实现两个字符串的比较。当字符串1 = 字符串2时，返回0，当字符串1 ≠ 字符串2时，返回它们两者第一个不同字符的`ASCII码`的差值。**
