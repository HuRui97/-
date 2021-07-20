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


#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include<string.h>
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

int main()
{
	extern int g_val;//声明外部符号
	printf("g_val=%d\n", g_val);
	return 0;
}
extern int Add(int, int);
int main()
{
	int a = 10;
	int b = 20;
	int sum = Add(a,b);
	printf("sum=%d\n", sum);
	return 0;
}
 int Add(int x, int y)//定义函数
{
	int z = x + y;
	return z;
}
 
#define MAX 100//定义标识符常量。
int main()
{
	int a = MAX;
	return 0;
}
#define MAX(X,Y) (X>Y?X:Y)//定义宏
int main()
{
	int a = 10;
	int b = 20;
	int max = MAX(a, b);
	printf("max=%d\n", max);
	return 0;
}


int main()
{
	int a = 10;//申请4个byte
	int* p = &a;//用指针变量存放地址
	//printf("%p\n", &a);//&a 取地址，显示十六进制
	//printf("%p\n", p);
	*p = 20;//*解引用操作符
	printf("a=%d\n", a);
	return 0;
}

#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include<string.h>
int main()
{
	char ch = 'w';
	char* pc = &ch;
	printf("%d\n", sizeof(pc));//指针大小在32位平台是4个字节，64位平台是8个字节
	return 0;
}

#include <stdio.h>
#include <string.h>
struct Boook
{char name[20];
short price;
};
int main()
{struct Book b1={"C语言程序设计"，55}；
printf("书名：%s\n",b1.name);
printf("价格：%d元\n",b1.price);
b1.price=20;
printf（"修改后%d\n",b1.price）;
struct Book*pb=&b1;
printf("%s\n",(*pb).name);
printf("%d\n",(*pb).price);
printf("%s\n",pb->name);
printf("%d\n",pb->price);
strcpy(b1.name,"C++")；
printf("书名：%s\n",b1.name);
}


#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
//int main()
//{
//	int age = 60;
//	if (age < 18)
//		printf("未成年\n");
//	else if (age >= 18 && age < 28)
//		printf("青年\n");
//	else if (age >= 28 && age < 58)
//		printf("中年\n");
//	else
//		printf("老年\n");
//	return 0;
//}

int main()
{
	int num = 0;
	scanf("%d", &num);
	int a = num % 2;
	if (1 == a)
		printf("奇数\n");
	else
		printf("偶数\n");
	return 0;
}


int main()
{
int day = 0;
scanf("%d",&day);
switch (day)
{case 1:
	printf("星期一\n");
	break;
case 2:
	printf("星期二\n");
	break;
case 3:
	printf("星期三\n");
	break;
}
	return 0;
}

int main()
{int day = 0;
	scanf("%d", &day);
	switch (day)
	{
	case 1:
	case 2:
	case 3:
	case 4:
	case 5:
		printf("工作日\n");
		break;
	case 6:
	case 7:
		printf("休息日\n");
		break;
	default:
		printf("输入错误\n");
	}
	return 0;}
	

	
int main()
{
	int n = 1;
	int m = 2;
	switch (n) 
	{
	case 1:
		m++;
	case 2:
		n++;
	case 3:
		switch (n)
		{
		case 1:
			n++;
		case 2:
			m++;
			break;
		}
	case 4:
		m++;
		break;
	default:
		break;
	}
	printf("m=%d,n=%d", m, n);
	return 0;
}
	
#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>

int main()
{
	int ch = 0;
	while ((ch = getchar()) != EOF)//EOF--end of file文件结束标志
	{
		if (ch < '0' || ch>'9')
			continue;
		putchar(ch);
	}
	return 0;
}

int main()
{
	int i = 0;
	//初始化；判断；调整
	for (i = 1; i <= 10; i++)
	{
		if (5 == i)
			continue;
		printf("%d ", i);
	}
	return 0;
}
