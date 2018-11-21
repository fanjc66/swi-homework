# part 1

1) **AND** : 
* Boolean Expression : X = A•B ;
* Logic Diagram Sybol : 

![](http://m.qpic.cn/psb?/V13dexGf2OLDRB/AflMy5TS0xFwuhL12xhtAxjXP7AzfTtipZSaDm8KAHc!/b/dDcBAAAAAAAA&bo=AQHOAAAAAAADF*w!&rf=viewer_4)

* Truth Table : 

 |   A   |   B   |   X   |
 |:------|:------|:------|
 |0      |0      |0      |
 |0      |1      |0      |
 |1      |0      |0      |
 |1      |1      |1      |

    当A/B都为一时，X为1；否则为0。

 2) **XOR**
 * Boolean Expression : X=A⊕B ;
 * Lofic Diagram Sybol : 

 ![](http://m.qpic.cn/psb?/V13dexGf2OLDRB/HkRVu3QJ2l.xKiQt0OE6VGN0J.WnAqhWpjAarBz0c.8!/b/dFIBAAAAAAAA&bo=YgERAQAAAAADF0E!&rf=viewer_4)

* Truth Table : 

|   A   |   B   |   C   |
|:------|:------|:------|
|0      |0      |0      |
|0      |1      |1      |
|1      |0      |1      |
|1      |1      |0      |

    当A/B相等时X为0；否则为1.

3) (A+B)(B+C):

![](http://m.qpic.cn/psb?/V13dexGf2OLDRB/IWv44z.9ylQ6ZYBxGUnD8TsdYQPfcicMSE9hhY*HIR4!/b/dCEBAAAAAAAA&bo=hAYYBAAAAAARF74!&rf=viewer_4)

4)  (A+B)⊕A'

|A|B|A'|A•B|X|
|:--|:--|:--|:--|:--|
|0|0|1|0|1|
|0|1|1|0|1|
|1|0|0|0|0|
|1|1|0|1|1|

5)  (AB)'=A'+B';

|A|B|A'|B'|A'+B'|AB|(AB)'|
|:--|:--|:--|:--|:--|:--|:--|
|0|0|1|1|1|0|1|
|0|1|1|0|1|0|1|
|1|0|0|1|1|0|1|
|1|1|0|0|0|1|0|

# part 2

6) 

7) (x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>x<sub>4</sub>x<sub>3</sub>x<sub>2</sub>x<sub>1</sub>)<sub>2</sub> or (0000 1111)<sub>2</sub> = (x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>1111)<sub>2</sub>


(x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>x<sub>4</sub>x<sub>3</sub>x<sub>2</sub>x<sub>1</sub>)<sub>2</sub> xor (0000 1111)<sub>2</sub> = (x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>0000)<sub>2</sub>


((x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>x<sub>4</sub>x<sub>3</sub>x<sub>2</sub>x<sub>1</sub>)<sub>2</sub> and (1111 0000)<sub>2</sub>) or (not(x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>x<sub>4</sub>x<sub>3</sub>x<sub>2</sub>x<sub>1</sub>)<sub>2</sub> and (oooo 1111)<sub>2</sub>)= (x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>0000)<sub>2</sub>  = (x<sub>8</sub>x<sub>7</sub>x<sub>6</sub>x<sub>5</sub>1-x<sub>4</sub>1-x<sub>3</sub>1-x<sub>2</sub>1-x<sub>1</sub>)<sub>2</sub>





# part 3

**Logic gate:**  In electronics, a logic gate is an idealized or physical device implementing a Boolean function; that is, it performs a logical operation on one or more binary inputs and produces a single binary output. Depending on the context, the term may refer to an ideal logic gate, one that has for instance zero rise time and unlimited fan-out, or it may refer to a non-ideal physical device.

**Boolean algebra:**  In mathematics and mathematical logic, Boolean algebra is the branch of algebra in which the values of the variables are the truth values true and false, usually denoted 1 and 0 respectively. Instead of elementary algebra where the values of the variables are numbers, and the prime operations are addition and multiplication, the main operations of Boolean algebra are the conjunction and denoted as ∧, the disjunction or denoted as ∨, and the negation not denoted as ¬. It is thus a formalism for describing logical relations in the same way that elementary algebra describes numeric relations. 

