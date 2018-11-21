HTML5游戏设计与制作(进阶篇)

软件开发的基本步骤：
* 游戏策划
* 游戏分析与设计
* 编码
* 玩家测试与发布

1. 游戏策划
 concept 文档

Settings: 公元2018年，王思聪在韩国仁川文鹤竞技场现场，观看自己组建的IG电竞俱乐部打比赛
。然鹅！他还有一分钟的时间吃热狗！......

Gameplay: 帮助校长在一分钟内吃尽可能多的热狗任务完成。玩家通过移动王思聪的位置接热狗。

Game Sprites：
player：王思聪。只能竖直上下移动。

food: hotdog只能水平向左移动。

2. 游戏设计
![](
https://s1.ax1x.com/2018/11/19/FpNKi9.png)


|     CRC   |       |
|:----------|:------|
|Object Name| 王思聪 player |
|Attributes | size：65，63|
||maxs speed : 600|
||directions : up & down |
|collaborator|event: time <= 0|
||action: destory|
||event: on destroyed|
||action: Creat object trophy|

![](https://s1.ax1x.com/2018/11/19/FpNeZF.png)

|     CRC   |       |
|:----------|:------|
|Object Name| Hotdog|
|Attrubutes | siza: 55, 29|
||Speed: 400|
|collaborator|event:on collision with player|
||action: Destroy|
||  Addss 10 to score|
|| Set text to "Text:"&score|





![](https://s1.ax1x.com/2018/11/19/FpU7ct.gif)


