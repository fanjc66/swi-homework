
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


  ![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZItt5FuQeXMuNAEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)



  ![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZIxt5Ft1NWYPUgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZIxt5FtkDok3UwEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI1t5Fv2NbcOZgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI5t5FubE5wKRwEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)


![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZI5t5FuBzkU6UgEAAAAAAAA!_1541696906280000_4&pre=http%3A%2F%2Fa3.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FxZtnb1kzloXsM65M3TBoK6Sjfo2yEpRxD5Ac5wiXa*o!%2Fm%2FdFIBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3DUgLXAAAAAAADF7U!%26tl%3D1%26vuin%3D1678062456%26tm%3D1541696400%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)

