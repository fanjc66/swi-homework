#Top-down desig（自上而下的设计）

	A top-down approach (also known as stepwise design and in some cases used as a synonym of decomposition) is essentially the breaking down of a system to gain insight into its compositional sub-systems in a reverse engineering fashion.
	自上而下的方法（也称为逐步设计）本质上是系统分解，以便以逆向工程的方式深入了解其组成子系统。

    In a top-down approach an overview of the system is formulated, specifying, but not detailing, any first-level subsystems.
    自项向下的方法中，系统的概述被指定，制定，但并不详细说明任何一级子系统。

    Each subsystem is then refined in yet greater detail, sometimes in many additional subsystem levels, until the entire specification is reduced to base elements.然后，对每个子系统进行更详细的细化，优势在许多附加的子系统级别中进行细化，知道整个概述被简化为基本元素。
   
    A top-down model is often specified with the assistance of "black boxes", which makes it easier to manipulate. 自上而下的模型通常是在“黑箱”的帮助下指定的，这使得操作更加容易。
	
	However, black boxes may fail to clarify elementary mechanisms or be detailed enough to realistically validate the model. 但是，黑箱可能根本无法说明基本机制或细节足够逼真地验证模型。

	Top down approach starts with the big picture. It breaks down from there into smaller segments.自上而下的方法从整体蓝图开始，分解成更小的片段。

##计算机科学中:  
	Top-down approaches emphasize planning and a complete understanding of the system. It is inherent that no coding can begin until a sufficient level of detail has been reached in the design of at least some part of the system. 自上而下的方法强调计划何对系统的完全理解。至少在系统用的一些部分的设计中，在达到足够的细节水平之前，无法开始编码是固有的。
	
	Top-down approaches are implemented by attaching the stubs in place of the module. This, however, delays testing of the ultimate functional units of a system until significant design is complete.自上而下的方法是通过连接存根代替模块来实现的。然而，这回延迟系统的最终功能单元的测试，直到重要的设计完成为止。

#洗衣机工作伪代码

```
READ	用户选择的洗衣模式

COMPUTE 对应洗衣时长
	IF  洗衣模式为快速洗衣 THEN
		注水需求为B1
		浸泡时长需求需求为B2
		时间为B3
	ENDIF
	IF  洗衣模式为正常洗衣 THEN
		注水需求为A1
		浸泡时长需求需求为A2
		时间为A3
	ENDIF

water_in_switch(open_close)
open
REPEAT
	volume	
UNTIL 水位 等于 注水需求
close

REPEAT
	浸泡
UNTIL 时间 等于 浸泡时长需求

WHILE	时间 > 0
	motor_run(direction) 
		left
		left
		right
		right
		stop
		时间自减1
	time_counter()
ENDWHILE	

water_out_switch(open_cloce)
REPEAT 
	放水
UNTIL 水位 大于 0

```