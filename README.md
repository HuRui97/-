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

int main()
{
	for (;;)//for循环的初始化，判断，调整部分都可以省略，但是，判断部分省略会导致判断条件恒为真
	{
		printf("hehe\n");
	}
	return 0;
}

int main()
{
	int i = 0;
	for (i = 0; i < 10; i++)
	{
		int j = 0;
		for (j = 0; j < 10; j++)//循环次数为内外层代码循环次数相乘
		{
			printf("hehe\n");
		}
	}
	return 0;
}

int main()
{
	int i = 0;
	int k = 0;
	for (i = 0, k = 0; k = 0; i++, k++)//“=”为赋值，赋值为0表示假，不循环
		k++;
	return 0;
}

int main()
{
	int i = 1;
	do 
	{
		printf("%d ", i);
		i++;
	}
	while (i <= 10);
	return 0;
}

int main()
{
	int a = 0;
	int n = 0;
	int ret = 1;
	scanf("%d", &n);
	for (a = 1; a <= n; a++)
	{
		ret = ret * a;
	}
	printf("%d\n", ret);
	return 0;
}


int main()
{
	int a = 0;
	int n = 0;
	int ret = 1;
	int sum = 0;
	for (n = 1; n <= 4; n++)
	{
		for (a = 1,ret=1; a <= n; a++)
		{
			ret = ret * a;
		}
		sum = sum + ret;
	}
	
	printf("%d\n", sum);
	return 0;
}


int main()
{
	int a = 0;
	int n = 0;
	int ret = 1;
	int sum = 0;
	for (n = 1; n <= 4; n++)
	{
		ret = ret * n;
		sum = sum + ret;
	}
	printf("%d\n", sum);
	return 0;
}


int main()
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int k = 10;
	int i = 0;
	int sz = sizeof(arr) / sizeof(arr[0]);
	for (i = 0; i < sz; i++)
	{
		if (k == arr[i])
		{
			printf("找到下标为%d ", i);
			break;
		}
	}
	if (i == sz)
	{
		printf("找不到");
	}
	return 0;
}


#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>
int main()//二分法
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int k = 7;
	int sz = sizeof(arr) / sizeof(arr[0]);
	int left = 0;
	int right = sz - 1;
	while (left <= right)
	{
		int mid = (left + right) / 2;
		if (k < arr[mid])
		{
			right = mid - 1;
		}
		else if (k > arr[mid])
		{
			left = mid + 1;
		}
		else
		{
			printf("找到下标为%d\n", mid);
			break;
		}
	}
	if (left > right)
	{
		printf("找不到\n");
	}
	return 0;
}


#include<stdio.h>
#include<windows.h>
#include<stdlib.h>
int main()
{
char arr1[]="123456789";
char arr2[]="#########";
int left=0;
int right=strlen(arr1)-1;
while(left<=right)
{
arr2[left]=arr1[left];
arr2[right]=arr1[right];
printf("%s\n",arr2);
Sieep(1000);
system("cls");
left++;
right--;
}
printf("%s\n",arr2);
return 0;
}

int main()
{
int i=0;
char arr[20]={0};
for(i=0;i<3;i++)
{
printf("请输入密码\n");
scanf("%s",arr);
if(strcmp(arr,"123456")==0);
{
printf("密码正确\n");
break;
}
else
{
printf("密码错误\n");
}
}
if(i==3)
{
printf("三次均错，退出程序\n")；
}
return 0;
}


int main()
{
	int a = 0;
	int b = 0;
	int c = 0;
	scanf("%d,%d,%d", &a, &b, &c);
	if (a < b)
	{
		int tmp = a;
		a = b;
		b = tmp;
	}
	if (a < c)
	{
		int tmp = a;
		a = c;
		c = tmp;
	}
	if (b < c)
	{
		int tmp = b;
		b = c;
		c = tmp;
	}
	printf("%d,%d,%d", a, b, c);
	return 0;
}

int main()
{
	int i = 1;
	for (i = 1; i <= 100; i++)
	{
		if (i % 3 == 0)
		{
			printf("%d ", i);
		}
	}
	return 0;
}
int main()
{
	int m = 24;
	int n = 18;
	int r = 0;
	scanf("%d,%d", &m,&n);
	while (m % n != 0)
	{
		int r = m % n;
		m = n;
		n = r;
	}//辗转相除法求最小公约数
	printf("%d\n", n);
	return 0;
}

int main()
{
	int year = 0;
	for (year = 1000; year <= 2000; year++)
	{
		if (year % 4 == 0 && year % 100 != 0)
		{
			printf("%d  ", year);
		}
		else if (year % 400 == 0)
		{
			printf("%d  ", year);
		}
	}
	return 0;
}


int main()
{
	int i = 0;
	for (i = 100; i <= 200; i++)
	{
		int j = 0;
		for (j = 2; j < i; j++)
		{
			if (i % j == 0)
			{
				break;
			}
		}
		if (j == i)
		{
			printf("%d,",i);
		}
	}
	return 0;
}


int main()
{
	int i = 0;
	for (i = 101; i <= 200; i+=2)
	{
		int j = 0;
		for (j = 2; j <=sqrt(i); j++)
		{
			if (i % j == 0)
			{
				break;
			}
		}
		if (j >sqrt(i) )
		{
			printf("%d,",i);
		}
	}
	return 0;
}


int main()
{
	int i = 0;
	int j = 0;
	for (i = 1; i <= 100; i++)
	{
		if (i % 10 == 9)
		{
			j++;
		}
		if (i / 10 == 9)
		{
			j++;
		}
	}
	printf("%d\n", j);
	return 0;
}



int main()
{
	int i = 0;
	double sum = 0.0;
	int flag = 1;
	for (i = 1; i <= 100; i++)
	{
		sum += flag*1.0 / i;
		flag = -flag;
	}
	printf("%lf\n", sum);
	return 0;
}

int main()
{
	char arr[] = { -1,-2,-3,-4,-5,-6,-7,-8,-9,-10 };
	int i = 0;
	int max = arr[0];
	int sz = sizeof(arr) / sizeof(arr[0]);
	for (i = 0; i < sz; i++)
	{
		if (max < arr[i])
		{
			max = arr[i];
		}
	}
	printf("%d\n", max);
	return 0;
}

int main()//99乘法表
{
	int i = 0;
	for (i = 1; i <= 9; i++)//打印9行
	{
		int j = 1;
		for (j = 1; j <= i; j++)//打印9列
		{
			printf("%d*%d=%-2d ", j, i, i * j);//打印两位，位数不够打印空格（2为右对齐，-2为左对齐）
		}
		printf("\n");
	}
	return 0;
}



#include<stdio.h>
#include<string.h>
#include<stdlib.h>
#include<time.h>
void menu()
{
printf("1.play	0.exit");
}
void game()
{
int ret=0;
int guess=0;
ret=rand()%100+1;1
while(1)
{
printf("请输入猜测数字：");
scanf("%d",&guess);
if(guess>ret)
{
printf("猜大了\n");
}
else if(guess<ret)
{
printf("猜小了\n")；
}
else
{
printf("猜对了\n");
break;
}
}
}
int main()
{
int input=0;
srand((unsigned int)time (NULL));
do
{
menu();
scanf("%d",&input);
switch(input)
{
case 1:
game();
break;
case 0;
printf("退出游戏\n");
break;
default:
printf("输入错误\n");
break;
}
}
while(input);
return 0;
}



#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
int main()
{
	printf("hello\n");
	goto again;
	printf("你好\n");
again:
	printf("再见\n");
	return 0;
}


#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
	char input[10] = { 0 };
	system("shutdown -s -t 60");//
again:
	printf("电脑将在一分钟后关机，如果输入“我是猪”，就取消关机！\n请输入：");
	scanf("%s", input);
	if (0 == strcmp(input, "我是猪"))
	{
		system("shutdown -a");
	}
	else
	{
		goto again;
	}
	return 0;
}


#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include<string.h>
int ADD(int x, int y)
{
	int z = 0;
	z = x + y;
	return z;
}



int main()
{
	int a = 10;
	int b = 20;
	int sum=ADD(a, b);
	printf("%d\n", sum);
	return 0;
}


int main()
{
	char arr1[] = "bit";
	char arr2[20] = "##########";
	strcpy(arr2, arr1);
	printf("%s\n", arr2);
	return 0;
}



void swap1(int x, int y)//void表示这个自定义函数没有返回值,x,y改变不了a,b
{
	int tmp = 0;
	tmp = x;
	x = y;
	y = tmp;
}

void swap2(int* pa, int* pb)
{
	int tmp = 0;
	tmp = *pa;
	*pa = *pb;
	*pb = tmp;
}
int main()
{
	int a = 10;
	//int* pa = &a;
	int b = 20;
	/*int* pb = &b;*/
	printf("a=%d  b=%d\n", a, b);
	swap2(&a, &b);
	printf("a=%d  b=%d\n", a, b);
	return 0;
}


int is_prime(int n)
{
	int j = 0;
	for(j=2;j<=sqrt(n);j++)
	{
		if (n % j == 0)
			return 0;
	}
	return 1;
}
int main()
{
	int i = 0;
	for (i = 101; i <= 200; i += 2)
	{
		/*int j = 0;
		for (j = 2; j <= sqrt(i); j++)
		{
			if(i%j==0)
			{
				break;
			}
		}
		if(j>sqrt(i))
		{
			printf("%d  ", i);
		}*/
		if(is_prime(i)==1)
		{
			printf("%d  ", i);
		}
	}
	return 0;
}




int is_leap_year(int n)
{
	if (n % 4 == 0 && n % 100 != 0|| n % 400 == 0)
		return 1;
	else
		return 0;
}



int main()
{
	int year = 0;
	for (year = 1000; year <= 2000; year++)
	{
		if (is_leap_year(year) == 1)
			printf("%d  ", year);
	}
	return 0;
}


int binary_search(int arr[], int k,int sz)//int arr[]实质上是一个指针，只是把数组arr的第一个元素的地址传了过来，不能用以计算数组大小
{
	
	int left = 0;
	int right = sz-1;
	while (left <= right)
	{
		int mid = (left + right) / 2;
		if (k < arr[mid])
		{
			right = mid - 1;
		}
		else if (k > arr[mid])
		{
			left = mid + 1;
		}
		else
		{
			return mid;
		}
	}
	return -1;
}

int main()
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int sz = sizeof(arr) / sizeof(arr[0]);
	int k = 6;
	int ret = binary_search(arr, k,sz);
	if (ret == -1)
		printf("找不到\n");
	else
		printf("找到下标为%d", ret);
	return 0;
}


void Add(int* p)
{
	(*p)++;//++的优先级高，不加括号会加到p上
}
int main()
{
	int num = 0;
	Add(&num);//改变num的值，所以使用传址变量
	printf("%d\n", num);
	return 0;
}



void new_line()
{
	printf("hehe\n");
}
void three_line()
{
	int i = 0;
	for (i = 0; i < 3; i++)
	{
		new_line();//函数的嵌套调用
	}
}
int main()
{
	three_line();
	return 0;
}

int main()
{
	printf("%d", printf("%d", printf("%d", 43)));
	//printf的返回值是所打印字符的个数，先打印“43”，返回值是2，于是再打印“2”，返回值为1，最后打印1；
	return 0;
}


void print(int n)
{
	if (n > 9)
	{
		print(n / 10);
	}
	printf("%d\n", n%10);
}

int main()
{
	unsigned int num = 0;
	scanf("%d", &num);
	print(num);
	return 0;
}


int my_strlen(char* str)
{
	int count = 0;
	while (*str != '\0')
	{
		count++;
		str++;
	}
	return count;
}

int my_strlen(char* str)
{
	if (*str != '\0')
		return   1 + my_strlen(str + 1);
	else
		return 0;
}
int main()
{
	char arr[] = "bit";
	int len = my_strlen(arr);
	printf("%d\n", len);
	return 0;
}


int Fac1(int n)
{
	int i = 0;
	int ret = 1;
	for (i = 1; i <=n; i++)
	{
		ret *= i;
	}
	return ret;
}

int Fac2(int n)
{
	if (n > 1)
		return n * Fac2(n - 1);
	else
		return 1;
}

int fib1(int n)
{
	if (n > 2)
		return fib1(n - 1)+fib1(n-2);
	else
		return 1;
}

int fib2(int n)
{
	int a = 1;
	int b = 1;
	int c = 0;
	while (n > 2)
	{
		c = a + b;
		a = b;
		b = c;
		n--;
	}
	return c;
}
int main()
{
	int n = 0;
	int ret = 0;
	scanf("%d", &n);
	ret = fib2(n);
	printf("%d\n", ret);
	return 0;
}



int main()
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int sz = sizeof(arr) / sizeof(arr[0]);
	int i = 0;
	for (i = 0; i < sz; i++)
	{
		printf("&arr[%d]=%p\n", i, arr[i]);
	}
	return 0;
}

int main()
{
	int arr[3][4] = { {1,2,3,4},{5,6,7,8},{9,10,11,12} };
	int i = 0;
	for (i = 0; i < 3; i++)
	{
		int j = 0;
		for (j = 0; j < 4; j++)
		{
			printf("%d ", arr[i][j]);
		}
		printf("\n");
	}
	return 0;
}



void bubble_sort(int arr[],int sz)
{
	int i = 0;
	for (i = 0; i < sz - 1; i++)//确定冒泡排序趟数
	{
		int j = 0;
		int flag = 1;//假设有序
		for (j = 0; j < sz - 1 - i; j++)//每趟排序次数
		{
			if (arr[j] > arr[j + 1])
			{
				int tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;
				flag = 0;//确定无序
			}
		}
		if (flag == 1)
		{
			break;//有序则退出循环
		}
	}
}
int main()
{
	int arr[] = { 9,8,7,6,5,4,3,2,1,0 };
	int i = 0;
	int sz = sizeof(arr) / sizeof(arr[0]);
	bubble_sort(arr,sz);
	for (i = 0; i < sz; i++)
	{
		printf("%d ", arr[i]);
	}
	return 0;
}



int main()
{
	int arr[] = { 1,2,3,4,5,6,7 };//arr即为数组arr的首元素地址，但有两个例外
	printf("%p\n", arr);
	printf("%p\n", &arr[0]);
	printf("%d\n", *arr);
	int sz = sizeof(arr) / sizeof(arr[0]);//第一个例外，在函数sizeof(数组名)内表示整个数组，单位是字节
	printf("%p\n", &arr);//&数组名时，数组名代表整个数组，地址与首元素地址相同，表示数组地址从此地址开始
	return 0;
}





#define _CRT_SECURE_NO_WARNINGS 1
#pragma once
#define ROW 3
#define COL 3
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
void InitBoard(char board[ROW][COL], int row, int col);//初始化函数声明，形参应跟实参不同
void DisplayBoard(char board[ROW][COL], int row, int col);//声明打印函数
void PlayerMove(char board[ROW][COL], int row,int col);//玩家下棋函数
void ComputerMove(char board[ROW][COL], int row, int col);//电脑下棋函数
char IsWin(char board[ROW][COL], int row, int col);//判断函数


#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include"game1.h"
void InitBoard(char board[ROW][COL], int row, int col)//初始化棋盘元素
{
	int i = 0;
	int j = 0;
	for (i = 0; i < row; i++)
	{
		for (j = 0; j < col; j++)
		{
			board[i][j] = ' ';
		}
	}
}

void DisplayBoard(char board[ROW][COL], int row, int col)
{
	int i = 0;
	int j = 0;
	for (i = 0; i < row; i++)
	{
		//printf(" %c | %c | %c \n", board[i][0], board[i][1], board[i][2]);
		for (j = 0; j < col; j++)
		{
			printf(" %c ", board[i][j]);
			if (j < col - 1)
				printf("|");
		}
		printf("\n");
		if (i < row - 1)
			//printf("___|___|___\n");
		{
			for (j = 0; j < col; j++)
			{
				printf("___");
				if (j < col - 1)
					printf("|");
			}
			printf("\n");
		}
	}
}


void PlayerMove(char board[ROW][COL], int row, int col)
{
	int x = 0;
	int y = 0;
	printf("玩家落子\n");
	while (1)
	{
		printf("请输入落子行列\n");
		scanf("%d,%d", &x, &y);
		if (x >= 1 && x <= row && y >= 1 && y <= col)
		{
			if (board[x - 1][y - 1] == ' ')
			{
				board[x - 1][y - 1] = '*';
				break;
			}
			else
			{
				printf("所输位置已被占用\n");
			}

		}
		else
		{
			printf("输入行列非法，重新输入\n");
		}
	}
	

}

void ComputerMove(char board[ROW][COL], int row, int col)
{
	int x = 0;
	int y = 0;
	printf("电脑落子\n");
	while (1)
	{
		x = rand() % row;
		y = rand() % col;
		if (board[x][y] == ' ')
		{
			board[x][y] = '#';
			break;
		}
	}
}

int IsFull(char board[ROW][COL], int row, int col)
{
	int i = 0; 
	int j = 0;
	for (i = 0; i < row; i++)
	{
		for (j == 0; j < col; j++)
		{
			if (board[i][j] == ' ')
			{
				return 0;
			}
		}
	}
	return 1;
}

char IsWin(char board[ROW][COL], int row, int col)
{
	int i = 0;
	for (i = 0; i < row; i++)
	{
		if (board[i][0] == board[i][1] && board[i][1] == board[i][2] && board[i][0] != ' ')
		{
			return board[i][0];
		}
	}
	for (i = 0; i < col; i++)
	{
		if (board[0][i] == board[1][i] && board[1][i] == board[2][i] && board[0][i] != ' ')
		{
			return board[0][i];
		}
	}
	if (board[0][0] == board[1][1] && board[1][1] == board[2][2] && board[0][0] != ' ')
	{
		return board[0][0];
	}
	if (board[2][0] == board[1][1] && board[1][1] == board[0][2] && board[1][1] != ' ')
	{
		return board[1][1];
	}
	if (1 == IsFull(board,ROW,COL))
	{
		return 'Q';
	}
	return 'C';
}


#define _CRT_SECURE_NO_WARNINGS 1
#include<stdio.h>
#include"game1.h"
void menu()
{
	printf("******************************\n");
	printf("***** 1.play     0.exit  *****\n");
	printf("******************************\n");
}
void game()
{
	char ret = 0;
	char board[ROW][COL] = { 0 };//创建游戏数组，存放棋盘信息
	InitBoard(board,ROW, COL);//初始化棋盘
	DisplayBoard(board,ROW,COL);//打印棋盘
	while (1)//下棋
	{
		PlayerMove(board, ROW, COL);//玩家落子
		DisplayBoard(board, ROW, COL);//打印棋盘
		ret = IsWin(board, ROW, COL);//判断玩家赢
		if (ret != 'C')
		{
			break;
		}
		ComputerMove(board, ROW, COL);//电脑落子
		DisplayBoard(board, ROW, COL);//打印棋盘
		ret = IsWin(board, ROW, COL);//判断电脑赢
		if (ret != 'C')
		{
			break;
		}
	}
	if (ret == '*')
	{
		printf("玩家赢\n");
	}
	else if (ret == '#')
	{
		printf("电脑赢\n");
	}
	else
	{
		printf("平局\n");
	}
}
void test()
{
	srand((unsigned int)time(NULL));
	int input = 0;
	do
	{
		menu();
		printf("请选择： \n");
		scanf("%d", &input);
		switch (input)
		{
		case 1:
			printf("进入三子棋\n");
			game();
			break;
		case 0:
			printf("退出游戏\n");
			break;
		default:
			printf("输入错误，请重新输入\n");
			break;
		}
	} while (input);
}
int main()
{
	test();
	return 0;
}
