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

   > `int i,j;`
   >
   > `for(j = 10;j <= 11;j++){`
   >
   > ​	`for(i = 9;i == j-1;i++){`
   >
   > ​		`printf("%d",j);`
   >
   > ​	`}`
   >
   > `}`

   A.`11`

   B.`10`

   C.`9`

   D.`10 11`

6. **在C语言中，引用数组元素时，其数组下标的数据类型允许是()。**

   A.`整型常量`

   B.`整型表达式`

   C.`整型常量或整型表达式`

   D.`任何类型的表达式`

7. 若i和k都是int类型变量，有以下for语句

   `for(i=0,k=-1;k=1;k++)printf("*****\n");`
   下面关于语句执行情况的叙述中正确的是（D)
   
   A.`循环体执行两次`
   
   B.`循环体执行一次`
   
   C.`循环体一次也不执行`
   
   D.`构成无限循环`
   
7. 有以下程序(说明:字母A的 ASCII 码值是65)

   > `#include`
   > `void fun(char *s)
   > `
   >
   > `{`
   >
   > ​	`while(*s)`
   > ​	`{if(*s%2) printf("%c",*s);`
   >
   > ​		`s++;`
   >
   > ​	`}`
   > `}`
   > `main()`
   > `{ char a[]="BYTE";`
   >
   > ​	`fun(a); printf("\n");`
   >
   > `}`
   
   程序运行后的输出结果是（D)
   A.`BY`
   B.`BT`
   C.`YT`
   D.`YE`
   
7. 

   A.

   B.

   C.

   D.

## 较难类型

1. 已知各变量的类型说明如下:

   > int k,a,b;
   > unsigned long w=5;
   >
   > double x=1.42
   >

   则以下不符合C语言语法的表达式是(A )。

   A.`x%(-3)`

   B.`w+=-2`

   C.`k=(a=2,b=3,a+b)`

   D.`a+=a-=(b=4)*(a=3)`

2. 有以下程序

   > #include
   >
   > main()
   >
   > {int x=011;
   > printf(" %d\n",++x);
   >
   > }

   程序运行后的输出结果是(C )
   A.`12`
   B.`11`
   C.`10`
   D.`9`

3. 有以下程序段

   > int i,n;
   > for(i=0;i<8;i++)
   >
   > {
   > 	n=rand()%5;
   >
   > ​	switch (n)
   >
   > ​	{
   >
   > ​		case 1:
   > ​		case 3: printf("%d\n",n); break;
   >
   > ​		case 2:
   > ​		case 4: printf("%d\n",n); continue;
   >
   > ​		case 0: exit(0);
   > ​	}
   > ​	printf("%d\n",n);
   >
   > }

   以下关于程序段执行情况的叙述，正确的是( )

   A. for循环语句固定执行8次

   B. 当产生的随机数n为4时结束循环操作

   C. 当产生的随机数n为1和2时不做任何操作

   D. 当产生的随机数n为0时结束程序运行

4. 有以下程序

   > #include
   >
   > main()
   > {
   >
   > ​	char s[]="012xy\08s34f4w2";
   >
   > ​	int i,n=0;
   >
   > ​	for(i=0;s[i]!=0;i++)
   > ​	if(s[i]>='0'&&s[i]<='9')n++;
   >
   > ​	printf("%d\n",n);
   >
   > }

   程序运行后的输出结果是(B )
   A.`0`
   B.`3`
   C.`7`
   D.`8`

5. 有以下程序

   > `#include`
   > `main()`
   > `{	int x=1,y=0;`
   >
   > ​	`if(!x) y++;`
   >
   > ​	`else if(x==0)`
   >
   > ​	`if (x) y+=2;`
   >
   > ​	`else y+=3;`
   > ​	`printf("%d\n",y);`
   >
   > `}`

   程序运行后的输出结果是D

   A.`3`
   B.`2`
   C.`1`
   D.`0`

6. 若有定义语句:`char s[3][10],(*k)[3],*p;`，则以下赋值语句正确的是（ )
   A.`p=s;`
   B.`p=k;` 

   C.`p=s[0];`
   D.`k=s;`

7. 有以下程序

   > `#include`
   >
   > `main()`
   >
   > `{`
   >
   > ​	`int s;`
   > ​	`scanf("%d",&s);`
   >
   > ​	`while(s>0)`
   >
   > ​	`{`
   >
   > ​		`switch(s)`
   >
   > ​	`{case1:printf("%d",s+5);`
   >
   > ​	`case2:printf("%d",s+4); break;`
   >
   > ​	`case3:printf("%d",s+3);`
   > ​	`default:printf("%d",s+1 );break;`
   >
   > ​	`}`	
   >
   > ​		`scanf("%d" ,&s);`
   > ​	`}`
   > `}`

   运行时,若输入`1 2 3 4 5 0<回车>`,则输出结果是（ )

   A.`6566456`
   B.`66656`
   C.`66666`
   D.`6666656`

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
