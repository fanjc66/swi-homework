# 字符游戏—贪吃蛇

一、实验目的
* 了解字符游戏的表示
* 体验自顶向下的设计方法实现问题求解
* 使用伪代码表示算法
* 使用函数抽象过程


1. 整体伪代码

```
	输出字符矩阵
	WHILE not 游戏结束 DO
		ch＝等待输入
		CASE ch DO
		‘A’:左前进一步，break 
		‘D’:右前进一步，break    
		‘W’:上前进一步，break    
		‘S’:下前进一步，break    
		END CASE
		输出字符矩阵
	END WHILE
	输出 Game Over!!! 
```


c语言实现（任务一）会动的蛇 

第一部分：函数原型 初始化

```
/*snake_move.c*/
#include <stdio.h>
#include <stdlib.h>

#define SNAKE_HEAD 'H'
#define SNAKE_BODY 'X'
#define FOOD '$'
#define BACKGROUND ' '
#define MAX_LENGTH 20

void snakeMove(int, int);

void putFood();

void output();

int isgameover();

int y_position[MAX_LENGTH] = {1, 1, 1, 1, 1};  // 纵坐标
int x_position[MAX_LENGTH] = {1, 2, 3, 4, 5};  // 横坐标
int snake_length = 5;

char map[12][13] = 
	{"************",
	 "*XXXXH     *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "*          *",
	 "************",};     			//初始化
```
第二部分： 根据伪代码写出main函数
```
int main()
{
	char ch;
	output();

	while (!isgameover())			// 判断游戏是否结束 
	{
		scanf(" %c", &ch);						
		switch (ch)			//读取操作指令
		{
			case 'A': snakeMove(1,  1);    break; // 左 
			case 'D': snakeMove(1, -1);	   break; // 右
			case 'W': snakeMove(-1, 1);    break; // 上
			case 'S': snakeMove(-1,-1);	   break; // 下
		}
		output();			//输入移动后的图标
	}
	printf("Game Over!!!\n"); //游戏结束
	return 0;
}

```
第三部分： 完成功能函数

（1） 移动
```
void snakeMove(int direction1, int direction2)		
{
	int i, j;
	map[y_position[0]][x_position[0]] = BACKGROUND; // 将蛇尾变为空白

	if (direction1 == 1)
	{
		if (direction2 == 1)  // 左
		{
			for (i = 0; i < snake_length-1; ++i)
			{
				y_position[i] = y_position[i+1];
				x_position[i] = x_position[i+1];
			}
			x_position[i]--;
		}
		else	       		//右
		{
			for (i = 0; i < snake_length-1; ++i)
			{
				y_position[i] = y_position[i+1];
				x_position[i] = x_position[i+1];
			}
			x_position[i]++;
		}
			
	}
	else    
	{
		if(direction2 == 1)   //上
		{
			for (i = 0; i < snake_length-1; ++i)
			{
				y_position[i] = y_position[i+1];
				x_position[i] = x_position[i+1];
			}
			y_position[i]--;
		}
		else      		//下
		{
			for (i = 0; i < snake_length-1; ++i)
			{
				y_position[i] = y_position[i+1];
				x_position[i] = x_position[i+1];
			}
			y_position[i]++;
		}
	}


}

```
（2）输出
```
void output(void)
{
	int i, j;

	for (i = 1; i < snake_length-1; ++i)
		map[y_position[i]][x_position[i]] = SNAKE_BODY; //蛇身
	map[y_position[i]][x_position[i]] = SNAKE_HEAD;         //蛇头
	
	for (i = 0; i < 12; ++i)
	{
		for (j = 0; j < 12; ++j)
			printf("%c", map[i][j]);
		putchar('\n');
	}
}
```
（3）判断游戏是否结束
```
int isgameover(void)  //蛇头碰到墙，则游戏结束
{
	int i, j;
	for (i = 0; i < snake_length; ++i)   
	{
		if (y_position[i] == 0 || x_position[i] == 0 || y_position[i] == 11 || x_position[i] == 11)
			return 1;
	}
	return 0;
}
```

![Fl59OI.gif](https://s1.ax1x.com/2018/12/05/Fl59OI.gif)