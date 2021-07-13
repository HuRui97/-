# -
初学练习用
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
int main()
{
	int num1 = 0;
	int num2 = 0;
	int sum = 0;
	scanf ("%d%d", &num1, &num2);
	sum = num1 + num2;
	printf("%d\n", sum);
	return 0;
}

#include <stdio.h>
int main()
{
char arr1[]="abc";
char arr2[]={'a','b','c',0};
printf("%s\n",arr1);
printf("%s\n",arr2);
return 0;
}

#include <stdio.h>
int main()
{int input=0;
printf ("开始选择\n");
printf("输入0或者1\n")；
scanf("%d",&input);
if input==1;
printf("1的结果\n")；
else
printf("0的结果\n")；
return 0;
}
#include <stdio.h>
int main()
{int arr [10]={1,2,3,4,5,6,7,8,9,10};
int i=0;
while (i<10);
{printf("%d\n",arr [i]);
i++;
}
printf("%d\n",arr[4]);//用下标访问元素，下标从0开始。
return 0;}
int main()
{int a=5%2;//%为取模，即得出余数；
printf("%d\n",a);
return 0;}

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
int main()
{
	int a, b;
	scanf("%d,%d", &a, &b);
	int c = a / b;
	int d = a % b;
	printf("%d\n",c);
	printf("余%d\n", d);
	return 0;
}
#include<string.h>
int main()
{int a=1;
int b=a<<1;//<<为左移，即将二进制数字左移一位
printf("%d\n",b);
return0;}



int main()//二进制0为假，1为真
{int a=3;//011
int b=5;//101
int c=a&b;//111
printf("%d\n",c);//&按位与（全1则1），|按位或（有1则1），^按位异或（不同则1）
return 0;}

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include<string.h>
int MAX(int x,int y)
{if x>y
return x;
else return y;}
int main()
{int num1=10;
int num2=20;
int max=0;
max=MAX(num1,num2)
printf("max=%d\n",max);
return0;
}



#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include<string.h>
int main()
{
	int arr[] = { 1,2,3,4,5,6 };
	int a = 10;
	printf("%d\n", sizeof(a));
	printf("%d\n", sizeof(int));
	printf("%d\n", sizeof a);
	printf("%d\n", sizeof(arr));
	return 0;
}

int main()//~指按（二进制）位取反，
{
	int a = 0;//000000000000000000000000
	int b = ~a;//111111111111111111111111（补码）
	//(b是有符号的整型，最高位是符号位，“1”表示负数,负数在二进制中储存的是补码)
	//111111111111111111111111（补码）
	//111111111111111111111110（反码）
	//100000000000000000000001（原码）
	printf("%d\n", b);//打印时使用的是原码，即为-1
	return 0;
}//原码符号位不变，其他位取反得到反码，反码加一得到补码

int main()
{
	int a = 10;
	int b = a++;//++自增    后置++：先使用变量值，再自增。    前置++：先自增，再使用自增后的值。
	printf("a=%d,b=%d\n", a, b);
	return 0;
}
int main()
{
	int a =(int) 3.14;//将double强制转换成int
	return 0;
}
int main()
{
	int a = 3;
	int b = 5;
	int c = a && b;
	int d = a || b;
	printf("c=%d\n", c);//&&逻辑与	左右同时为真才是真
	printf("d=%d\n", d);//||逻辑或，有1个是真即为真
	return 0;
}

int main()
{
	int a = 10;
	int b = 20;
	int max = 0;
	max = (a > b ? a : b);//exp1结果为真，执行exp2，否则执行exp3
	printf("%d\n", max);
	return 0;
}
int main()
{
	register int a = 10;//吧a定义成寄存器变量。
	return 0;
}
int main()
{
	typedef unsigned int u_int;
		unsigned int num = 20;
		u_int num2 = 20;
		return 0;
}

void test()
{
	static int a = 1;
	a++;
	printf("%d\n", a);

}
int main()
{
	int i = 0;
	while (i < 5)
	{test();
	i++;
	}
	return 0;
}
