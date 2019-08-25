![在这里插入图片描述](https://img-blog.csdnimg.cn/20190825105031744.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzY5MjUwNA==,size_16,color_FFFFFF,t_70)

**1、输入字符串是“%s”
   2、或：“||”
   3、数组输入时，可以没有中括号
   4、空的斜杠与换行相同：'\0'
   5、输出后要减减**

**我的代码：**

```
#include<stdio.h>
int main()
{
	int numP=0,numA=0,numT=0,nume=0,nums=0,numt=0;
	char str[10001];
	int i;
	scanf("%s",str);

	for(i=0;str[i]!='\0';i++)
	{
		if(str[i]=='P')
		{
			numP++;
		}else
			if(str[i]=='A'){
				numA++;
			}else
			if(str[i]=='T'){
				numT++;
			}else
			if(str[i]=='e'){
				nume++;
			}else
			if(str[i]=='s'){
				nums++;
			}else
			if(str[i]=='t'){
				numt++;
			}
	}

	while(numP||numA||numT||nume||nums||numt)
	{
		if(numP)
		{
			printf("P");
			numP--;
		}
		if(numA){
			printf("A");
			numA--;
			}
		if(numT){
			printf("T");
			numT--;
			}
		if(nume){
			printf("e");
			nume--;
			}
		if(nums){
			printf("s");
			nums--;
			}
		if(numt){
			printf("t");
			numt--;
			}
	}
	printf("\n");
	return 0;
}
```

