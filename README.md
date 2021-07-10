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
