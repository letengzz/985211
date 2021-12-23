# 选择题

## 简单易错类型

1. B
2. B
3. A
4. B
5. C

## 较难类型

# 填空题

1. 6
2. result=27.00
3. t=t*n    s=s+t
4. t=sign*i;   sign=-sign;

# 编程题

1. 

   ```c
   #include <stdio.h>
   int main(){
   	int i,a[10],x,flag=0;
       for(i=0;i<10;i++)
   		scanf("%d",&a[i]);
       scanf("%d",&x);
   	for( i=0;i<10;i++)
   		if(x==a[il)
   		{	flag=i+1;break;}
           if(flag==O)
   			printf("no foundIn");
           else
   			printf(" %din",flag);
       return 0;
   }
   ```

   

2. 

   ```c
   #include<stdio.h>
   int main(){
       int strcmp(char *p1,char*p2);
       int m;
       char str1[20],str2[20],*p1,*p2;
       printf(" input two strings:\n");
       scanf("%s",str1);
   	scanf("%s",str2);
       p1=&str1[0];
       p2=&str2[0];
       m=strcmp(p1,p2);
       printf("result:%d\n" ,m);
   	return 0;
   }
   int strcmp(char *p1,char *p2){	//两个字符串比较函数
   	int i;
   	i=0;
   	while(*(p1+i)==*(p2+i))
   		if(*(p1+i++)=='\O') return(O);	//相等时返回结果0
   	return(*(p1+i)-*(p2+i));	//不等时返回结果为第一个不等字符ASCII码的差值
   }
   ```

   

