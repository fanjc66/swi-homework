# **construct2 新手入门指南（简易版）**
跟着官方指南终于完成了入门教程小游戏，但同时也发现了不少bug，以及过于繁琐的问题。于是根据自己实践时体验，写一篇中文简易版指南，希望对其它小白有所帮助。

## 1、下载 construct2（暂不购买）

[construct2](https://www.scirra.com/construct2)

## 2、新建文件
　　点击文件（file)>>新建（new）>> new empty project >> open 

## 3、添加背景：
　　
下载图片至本地：

![](https://www.scirra.com/images/articles/bg.png)
　　


双击layout1的空白处 >> 选择Tiled Background >> 单击空白处 >> 点击第二个黄色文件图标（load an image from file) >> 选择保存到本地的背景图片 >> 关闭窗口

选中出现的图片 >> 在左侧的属性栏中将它的位置（position）改为0,0 >> 将它的大小（size）设置为1280,1024 

此时背景图片应布满整个布局
![](https://www.scirra.com/images/articles/tiledui.jpg)

## 4、添加图层

在右侧layers栏中右击layer 0 >> 重命名（rename）它为background >> 点击锁形图标锁定本图层

点击“+”新建一个图层 >> 重命名它为main 

## 5、添加其他对象
双击布局空白处 >> 双击mouse 以添加鼠标为对象


下载以下图片到本地

玩家（player)

![](https://www.scirra.com/images/articles/player.png)

怪（monster）

![](https://www.scirra.com/images/articles/monster.png)

子弹（bullet)

![](https://www.scirra.com/images/articles/Bullet.png)

爆破（explode)

![](https://www.scirra.com/images/articles/explode.png)

双击main图层空白处 >> 双击精灵（sprite) >> 单击空白处 >> （同导入背景图片）打开文件选择要插入的对象 >> 以相同方式插入所有对象 >> 在右侧object栏目中重命名他们（右击）

![](https://m.qpic.cn/psb?/V13dexGf2OLDRB/0QyNZlXt*KN4zrc4*JLsJa3KGN0Q05Fd.SZ.q6Czxyo!/b/dGYBAAAAAAAA&bo=RQEOAUUBDgEDCSw!&rf=viewer_4)


在右侧object栏中右击player >> 选择edit animations >> 点击靶心型十字键 >> 点击新弹出小窗口左上角的“+” >> 鼠标变成“+” >> 点击玩家（player）图片的枪口处将标点放在那里 >> 关闭窗口

![](https://www.scirra.com/images/articles/placingimagepoint.png)

选中explode >> 在左侧属性栏中将它的Blend mode改为Additive

## 6、设置动作

点击player >> 点击左侧属性栏中behaviors >> 点击小窗口左上角的“+” >> 双击movements栏下的8 derections >> 以相同方式为其添加Scroll To 和 Bound to layout >> 关闭小窗口

以相同方式为Bullet（子弹）添加 Bullet movement 和 Destroy outside layout；

以相同方式为monster （怪）添加Bullet movement；

以相同方式为explode （爆破）添加 Fade behavior；

选中monster >> 在左侧属性栏中将他的速度（speed）改为80；
以相同方式将bullet速度改为600；
将explode的fade out time改为0.5；

## 7、复制更多怪

拖动explode和bullet到布局外 >> 按住ctrl并拖动monster以复制 >> 以相同方式复制7/8个怪

![](https://www.scirra.com/images/articles/severalghosts.png)



## 8、创造事件

在上方点击event sheet 1 >>　双击空白处 >> 双击system >> 双击every tick >> 单击 Add action >> 双击player >> 在angle栏下选择 set angle toward position >> 填写x、y的参数分别为 Mouse.X 、 Mouse.Y 
添加Condition: Monster >> 选择Is outside layout >> 添加Action: Monster >> 选择Set angle toward position >> 填写x的参数 :Player.X ，y的参数：Player.Y

![](https://www.scirra.com/images/articles/alwayslookatmouse.png)

## 9、添加其他设置

添加condition >> 选择mouse >> 选择 on click >> 选择Left clicked >> 点击add action >> 选择Player >> 选择Spawn another object >> Object中, 选择Bullet >> Layer中填 1 (即 "Main"） >> Image point中填 1

![](https://www.scirra.com/images/articles/spawnbullet2.png)

添加Condition: Bullet >> 选择On collision with another object >> 选择 Monster >> 添加Action: Monster >> 选择Destroy >> 添加Action: Bullet >> 选择Spawn another object >> 选择Explosion >> layer填 1

添加Action: Bullet >> Destroy

## 10、设置变量

在右侧objects栏中选中 >> 点击instance variables >> 命名（name）为health >> value 为5

![](https://www.scirra.com/images/articles/healthinstvar.png)

在event sheet 1 中event bullet中右击"destroy monster" action 选择replace action >> 选择monster >> 在Instance variables category下选择Subtract from >> 选择变量"health" >> value 为1 >> 点击Done


![](https://www.scirra.com/images/articles/monsternohealth.png)

添加Condition: Monster >> 选择Compare instance variable >> 选择Health Less or equal, 0 >> 添加Action: Monster >> 选择Spawn another object >> Explosion >> layer 1 >> 添加Action: Monster >> Destroy

![](https://www.scirra.com/images/articles/monsternohealth.png)

## 10、记录分数

右击event sheet 空白处 >> 单击add global variable >> 命名（name）为score >> 点击ok

![](https://www.scirra.com/images/articles/addglobal.png)

在"Monster: health less or equal 0" event中 Add action： System >> 在Global & local variables中选择Add to >> Score, value 1

![](https://www.scirra.com/images/articles/scoreeevent.png)


## 11、创建分数提示

在界面右侧新建一个layout命名为HUD >> 设置它的参数parallax为0,0

![](https://m.qpic.cn/psb?/V13dexGf2OLDRB/SAog9VCxmbnXH3qe4xGvCfLrbm0ir*Msm4iTJaDmdMY!/b/dDEBAAAAAAAA&bo=LgHRAAAAAAADB9w!&rf=viewer_4)

双击界面 >> 选择text >> 单击界面左上角显示text >> 在左侧栏中将color设置为黄色 >> 转换至event >> 在Every tick后添加action： text >> 选择set text >> 输入"Score: " & Score >> done

## 12、自动生成怪

添加event （condition）：system >> 选择every x seconds >> 输入3 >> 添加action:System >> 选择Create object >> 选择Monster >> layer 1 >> X:1400 , Y:random(1024) 
添加condition：Monster >> 选择On collision with another object >> 选择 Player >> 添加Action: Player >> 选择Destroy


![](http://m.qpic.cn/psb?/V13dexGf2OLDRB/h4atU5gezQPKQrG*4Oq*M1enkLD0brho9Scqcfy7HS0!/b/dDYBAAAAAAAA&bo=pgNqAgAAAAADF*8!&rf=viewer_4)




现在游戏制作完毕了，点击run尝试运行它


[test](http://localhost:50001/)