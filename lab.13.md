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