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
