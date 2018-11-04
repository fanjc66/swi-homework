## 1、
1、Program with machine language according to the following c. int_8 a = 1;  int_8 c = a  3; 


1）Write your assembly code & machine code

LOD # 1–>STO X –> LOD X –> ADD#3 –> STO Y –> HLT

2）Explain machine code execution with the fetch-decode-execute cycle

Main memory –> fetch instruction –> Decode instruction –>Registers –>Get data –>Execute the instruction –> Main memory

3）Explain functions about  IR, PC, ACC registers in a CPU

IR: The instruction register(指令寄存器), which contains a copy of the instruction being executed.（保存当前正在执行的一条指令）

PC: The program counter(程序计数器) , which contains the address of the next instruction to be executed.(存放下一条指令在内存中的地址)

ACC：The accumulator.累加寄存器，功能是当运算器的算术逻辑单元(ALU)执行全部算术和逻辑运算时，为ALU提供一个工作区，暂时存放ALU运算结果

4）Explain physical meaning about vars a & c in a machine

## 2、
1） What are stored in memory? 

instructions and data

2）Can a data or a instruction stored in the same place? 

yes

3） Explain Instruction Format with example instructions.

example: 
instruction specifier ：1100 0000

operand specifier : 0000 0000 0000 0111

## 3.名词解释
1）（Assembly Language）：A low-lever programming language in which a mnemonic represents each of the machine-language instructions for a particular computer.

一种低级编程语言,其中助记符表示特定计算机的每个机器语言指令。 

2）（Compiler）:A program that translates a high-level language program into machine code

编译器（一种高级语言程序转换成机器代码的程序） 

3）（Imperative programming）In computer science, imperative programming is a programming paradigm that uses statements that change a program's state. 

在计算机科学中，命令式编程是使用改变程序状态的语句的编程范例。

4）（Functional programming） 

in computer science, functional programming is a programming paradigm—a style of building the structure and elements of computer programs—that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. It is a declarative programming paradigm, which means programming is done with expressions or declarations[1] instead of statements. In functional code, the output value of a function depends only on the arguments that are passed to the function, so calling a function f twice with the same value for an argument x produces the same result f(x) each time; this is in contrast to procedures depending on a local or global state, which may produce different results at different times when called with the same arguments but a different program state. Eliminating side effects, i.e., changes in state that do not depend on the function inputs, can make it much easier to understand and predict the behavior of a program, which is one of the key motivations for the development of functional programming. 

在计算机科学中，函数式编程是一种编程范例，一种构建计算机程序结构和元素的方式，它把计算看成对数学函数的评估，并且避免状态变化和数据可变。它是一种声明式编程范例，这意味着用表达式或声明[1]而不是语句进行编程。在函数代码中，函数的输出值仅取决于传递给函数的参数，因此每次调用函数f两次，参数x的值相同，结果f(x)相同；这与依赖于本地或全局状态的过程相反，在相同的参数但不同的程序状态调用时，H可能在不同的时间产生不同的结果。消除副作用，即不依赖于函数输入的状态变化，可以使得更容易理解和预测程序的行为，这是函数编程开发的关键动机之一。 


5）（Procedural programming）

Procedural programming is a programming paradigm, derived from structured programming, based upon the concept of the procedure call. Procedures, also known as routines, subroutines, or functions, simply contain a series of computational steps to be carried out. Any given procedure might be called at any point during a program's execution, including by other procedures or itself.

过程编程是基于过程调用的概念从结构化编程派生出来的编程范例。程序，也称为例程，子程序，或函数，简单地包含一系列的计算步骤要执行。任何给定的过程都可以在程序执行过程中的任意点调用，包括其他过程或本身。