# 牧师与恶魔过河

 [牧师与恶魔过河](http://www.17yy.com/f/69854.html)


– 游戏涉及哪些类。请列表说明 

| object class |
|:-------------|
|   shore          | 
|   sprites        |
|   Text           |


– 游戏中有哪些对象，各几个。例如，船（一个）

| object |
|:--------|
| river  1 |
| boat   1 |
| priest 3 |
| devil  3 |
| countdown meter |

– 类和对象的区别是什么？举一个例子说明 


所有的类都有属性，是一个抽象概念。类是一组具有相同属性和方法的对象的一个抽象概念。

一个对象是一个具有状态、行为和标识符的实体。是它所在的类中的一个实例。

A group of similar objects is described by an object class, or class
结构和行为类似的对象定义在他们共同的类中。

例如，游戏中的魔鬼、牧师有相似的属性、行为，他们都属于精灵（sprite）类。

[类与对象](https://blog.csdn.net/wangfei_edu/article/details/40372917?utm_source=blogxgwz0
)

– 游戏中的魔鬼，有哪些属性和方法？ 

name：devil

size ：unknown

angle：0 / 180

魔鬼上船

魔鬼下船

魔鬼杀掉牧师

– 假设魔鬼被鼠标点中，会执行onclick事件，请用文字 （伪代码）描述这个事件中魔鬼与其他对象沟通的过 程。 

```
点击魔鬼
IF 魔鬼在河岸 并且 船上有空位 THEN
    魔鬼上船
ENDIF

IF 魔鬼在船上 THEN
    魔鬼下船
ENDIF

get 河岸上魔鬼与牧师的数量
IF 魔鬼的数量大于牧师的数量 THEN
    魔鬼杀掉牧师
    游戏结束
ENDIF

```
– 类或对象会是动词吗？

类可以是动词，将相似的对象归为一类。

