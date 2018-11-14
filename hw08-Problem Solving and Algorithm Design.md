
## 作业 1/2

1、

 1）用伪代码描述将十进制转换成16进制的方法
```
    READ DecNum

    COMPUTE HexNum

        IF DecNum > 0 THEN
            CALL computeHex with DecNum
        ELSE
            IF DecNum = 0 THEN
                PRINT 0
            ELSE
                PRINT -
                CALL computeHex with  - DexNum
            ENDIF
        ENDIF

    PRINT HexNum

    BEGIN
    computeHex
    Set digit to 0
    WHILE DecNum > 0 
        IF DecNum > 9 THEN
            CASE DecNum OF
                10 : HexNum[digit] = 'A'
                11 : HexNum[digit] = 'B'
                12 : HexNum[digit] = 'C'
                13 : HexNum[digit] = 'D'
                14 : HexNum[digit] = 'E'
                15 : HexNum[digit] = 'F'
            ENDCASE
        ELSE
            Set HexNum[digit] to DecNum % 16 + '0'
        Set DecNum to DecNum / 16
        INCREMENT digit
    ENDWHILE

    PRINT HexNum
    END


```

 
 2）C语言实现（先用注释写好算法，然后翻译）

 ```

 #include <stdio.h>
void computeHex(int);
int main()
{
	int dec;
	char hex[100];
	int digit = 0; 
	
	scanf("%d", &dec);				/* READ DecNum
									COMPUTE HexNum
								    	IF DecNum > 0 THEN
             						    CALL computeHex with DecNum
       									    ELSE
									            IF DecNum = 0 THEN
									                PRINT 0
									            ELSE
									                PRINT -
									                CALL computeHex with  - DexNum
									            ENDIF
									    ENDIF*/
	if (dec > 0)				
		computeHex(dec);
	else if (dec == 0)
		printf("0");
	else
	{
		printf("-");
		dec = 0 - dec;
		computeHex(dec);
	}
	putchar('\n'); 					//PRINT HexNum
}   
									/* BEGIN
								    computeHex
								    Set digit to 0
								    WHILE DecNum > 0 
								        IF DecNum > 9 THEN
								            CASE DecNum OF
								                10 : HexNum[digit] = 'A'
								                11 : HexNum[digit] = 'B'
								                12 : HexNum[digit] = 'C'
								                13 : HexNum[digit] = 'D'
								                14 : HexNum[digit] = 'E'
								                15 : HexNum[digit] = 'F'
								            ENDCASE
								        ELSE
								            Set HexNum[digit] to DecNum % 16 + '0'
								        Set DecNum to DecNum / 16
								        INCREMENT digit
								    ENDWHILE
								
								    PRINT HexNum
								    END*/

void computeHex(int dec)  
{
	int digit = 0; 
	char hex[100];			
	while (dec > 0)			
	{						 
		if (dec % 16 > 9)		
			{ 
				switch (dec % 16)
				{
					case 10: hex[digit] = 'A';	break;
					case 11: hex[digit] = 'B';	break;
					case 12: hex[digit] = 'C';	break;
					case 13: hex[digit] = 'D';	break;
					case 14: hex[digit] = 'E';	break;
					case 15: hex[digit] = 'F';	break;
				}
			}
		else 
			hex[digit] = dec % 16 + '0';
		digit++;
		dec /= 16;
	}
	for (digit--; digit >= 0; digit--)
	{
		printf("%c", hex[digit]);
	}
}	

```
 
  3）使用 -1,  0,  1,  15,   26，3265 最为输入测试你的程序





  ![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZItt5FuQeXMuNAEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541721600%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)







  ![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZIxt5Ft1NWYPUgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)








![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZIxt5FtkDok3UwEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI1t5Fv2NbcOZgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI5t5FubE5wKRwEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


## 2、名词解释与对比 

 1）Top-down desig（自上而下的设计）

	A top-down approach (also known as stepwise design and in some cases used as a synonym of decomposition) is essentially the breaking down of a system to gain insight into its compositional sub-systems in a reverse engineering fashion.
	自上而下的方法（也称为逐步设计）本质上是系统分解，以便以逆向工程的方式深入了解其组成子系统。

   In a top-down approach an overview of the system is formulated, specifying, but not detailing, any first-level subsystems.
   自项向下的方法中，系统的概述被指定，制定，但并不详细说明任何一级子系统。

    Each subsystem is then refined in yet greater detail, sometimes in many additional subsystem levels, until the entire specification is reduced to base elements.然后，对每个子系统进行更详细的细化，优势在许多附加的子系统级别中进行细化，知道整个概述被简化为基本元素。
   
    A top-down model is often specified with the assistance of "black boxes", which makes it easier to manipulate. 自上而下的模型通常是在“黑箱”的帮助下指定的，这使得操作更加容易。
	
	However, black boxes may fail to clarify elementary mechanisms or be detailed enough to realistically validate the model. 但是，黑箱可能根本无法说明基本机制或细节足够逼真地验证模型。

	Top down approach starts with the big picture. It breaks down from there into smaller segments.自上而下的方法从整体蓝图开始，分解成更小的片段。

	计算机科学中:
	Top-down approaches emphasize planning and a complete understanding of the system. It is inherent that no coding can begin until a sufficient level of detail has been reached in the design of at least some part of the system. 自上而下的方法强调计划何对系统的完全理解。至少在系统用的一些部分的设计中，在达到足够的细节水平之前，无法开始编码是固有的。
	
	Top-down approaches are implemented by attaching the stubs in place of the module. This, however, delays testing of the ultimate functional units of a system until significant design is complete.自上而下的方法是通过连接存根代替模块来实现的。然而，这回延迟系统的最终功能单元的测试，直到重要的设计完成为止。 
	
	
 
 2） Work breakdown structure (WBS)工作分解结构

	A work-breakdown structure (WBS) in project management and systems engineering, is a deliverable-oriented breakdown of a project into smaller components. A work breakdown structure is a key project deliverable that organizes the team's work into manageable sections.在项目管理和系统工程中，工作分解结构（WBS）是将面向交付的项目分解成更小的组件。工作分解结构的重要可交付项目是组织团队项目分解成可管理的部分。
	
	A work-breakdown structure element may be a product, data, service, or any combination thereof. A WBS also provides the necessary framework for detailed cost estimating and control along with providing guidance for schedule development and control.工作分解结构的元素可是产品、数据、服务或其他有关组合。WBS提供了详细的成本估计和供职的必要框架，并未进度开发和控制提供指导。
	
	WBS is a hierarchical and incremental decomposition of the project into phases, deliverables and work packages. It is a tree structure, which shows a subdivision of effort required to achieve an objective; for example a program, project, and contract.[4] In a project or contract, the WBS is developed by starting with the end objective and successively subdividing it into manageable components in terms of size, duration, and responsibility (e.g., systems, subsystems, components, tasks, subtasks, and work packages) which include all steps necessary to achieve the objective.WBS是将项目分为阶段、递送、和工作包的分层递增分解，它是一个树形结构，它显示了实现目标所需的工作的具体细分，例如程序、项目和合同。（例如，系统、子系统、组件、任务、子任务和工作块）包括实现目标所需的所有步骤。

	The WBS is organized around the primary products of the project (or planned outcomes) instead of the work needed to produce the products (planned actions).工作分解结构WBS是围绕项目的主要产品（或计划成果）组织的，而不是围绕生产产品（计划行动）所需的工作。

	The development of the WBS normally occurs at the start of a project and precedes detailed project and task planning.WBS的开发通常在项目开始时，并在详细的项目和任务规划之前进行。

 3）简述管理学WBS 与 信息学Top-down设计 的异同

	同：将系统整体划分为更小的部分；
	异：自上而下是按逻辑结构由概述到具体，WBS是按功能类别分块为子任务。

3、仔细观察您洗衣机的运作过程，运用Top-down设计方法和Pseudocode 描述洗衣机控制程序。假设洗衣机可执行的基本操作如下

water_in_switch(open_close)  // open 打开上水开关，close关闭 water_out_switch(open_close)  // open 打开排水开关，close关闭 get_water_volume()  //返回洗衣机内部水的高度
motor_run(direction) // 电机转动。left左转，right右转，stop停 time_counter()  // 返回当前时间计数，以秒为单位 halt(returncode) //停机，success 成功 failure 失败


1）请使用伪代码分解“正常洗衣”程序的大步骤。包括注水、浸泡等 
```
READ	用户选择的洗衣模式

COMPUTE 对应洗衣时长

water_in_switch(open_close)

REPEAT
	浸泡
UNTIL 时间 等于 浸泡时长需求

WHILE	时间 > 0
	motor_run(direction) 
ENDWHILE	

water_out_switch(open_cloce)


```



2）进一步用基本操作、控制语句（IF、FOR、WHILE等）、变量与表达式，写出每 个步骤的伪代码 

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
3）根据你的实践，请分析“正常洗衣”与“快速洗衣”在用户目标和程序上的异同。 你认为是否存在改进（创新）空间，简单说明你的改进意见？ 

	“正常洗衣”与“快速洗衣”在用户目标上都是在尽可能短的时长内洗干净衣服，其中，“正常洗衣”是清洗程度的最优方案，而快速洗衣是时间长度上的最优方案。

	存在。改进意见：快速洗衣模块中增加洗衣时长的用户选项，根据用户选择的洗衣时长选择不同的电动机起动模式。


4）通过步骤3），提取一些共性功能模块（函数），简化“正常洗衣”程序，使程序 变得更利于人类理解和修改维护。

```
READ	用户选择的洗衣模式
IF  洗衣模式为快速洗衣 THEN
	READ 用户能接受的洗衣时长
	CONPUTE　对应合理发动机启动模式
ENDIF