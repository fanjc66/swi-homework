## 色彩表示与编码


### 1、颜色
颜色是通过颜色类别描述的人类 视觉感知的特征。颜色实质上由刺激导出视锥细胞在人眼通过电磁辐射在可见光谱。颜色类别和颜色的物理规格通过从它们反射的光的波长与对象相关联。这种反射受物体的物理特性控制，如光吸收，发射光谱等。

通过定义颜色空间，颜色可以通过坐标进行数字识别，在1931年也被国际照明委员会与国际商定的颜色名称（红色，橙色等）全球协议命名。在RGB色彩空间例如是对应于人的颜色空间三色视和该光的三个频带响应三种视锥细胞类型：长波长，接近564-580峰值波长（红色）; 中波长，在534-545 nm附近达到峰值（绿色）; 和短波长光，接近420-440纳米（蓝色）。[1] [2] 在其他颜色空间中也可以有三个以上的颜色尺寸，例如在CMYK颜色模型中，其中一个尺寸与颜色的色彩相关。

##   The colors of the visible light spectrum       
|        |                     |                    |
|:-------|:--------------------|:-------------------|
|Color	 | Wavelength interval | Frequency interval |
|Red	 |~ 700–635 nm|	~ 430–480 THz|
|Orange	|~ 635–590 nm|	~ 480–510 THz|
|Yellow	|~ 590–560 nm|	~ 510–540 THz|
|Green	|~ 560–520 nm|	~ 540–580 THz|
|Cyan	|~ 520–490 nm|	~ 580–610 THz|
|Blue	|~ 490–450 nm|	~ 610–670 THz|
|Violet or Purple|	~ 450–400 nm|	~ 670–750 THz|

![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f3/CIExy1931_fixed.svg/476px-CIExy1931_fixed.svg.png)

## 2、 RGB 色彩模型

要形成RGB颜色，必须叠加三个光束（一个红色，一个绿色和一个蓝色）（例如，通过黑色屏幕发射或通过白色屏幕反射）。三个光束中的每一个被称为该颜色的分量，并且它们中的每一个可以在混合物中具有从完全关闭到完全开启的任意强度。

RGB颜色模式是添加剂在这个意义上，这三个光束加在一起，它们的光谱增加，波长波长，使最终颜色的光谱。[1] [2] 这与减色模型基本相反，减色模型适用于油漆，油墨，染料和其他物质，其颜色取决于反射我们看到它们的光线。由于性质，这三种颜色产生白色，这与物理颜色形成鲜明对比，例如混合时产生黑色的染料。

![](https://en.wikipedia.org/wiki/File:AdditiveColor.svg)





## 3、色彩深度


颜色深度或颜色深度，也称为位深度，可以是用于指示单个像素颜色的位数，位图图像或视频帧缓冲区中的位数，也可以是每个位数使用的位数单个像素的颜色分量。对于消费者视频标准，例如高效视频编码（H.265），比特深度指定用于每个颜色分量的比特数。当引用像素时，该概念可以定义为每像素位数（bpp），其指定所使用的位数。当提及一个颜色分量，该概念可以被定义为每个分量的比特，每个信道比特，每个颜色位（所有三个缩写BPC），并且还每像素分量的比特，每个颜色信道比特或每采样的比特（BPS）。颜色深度只是颜色表示的一个方面，表达了如何表达精细的颜色水平（又称颜色精度）; 另一方面是多么广泛可以表达一系列颜色（色域）。色彩精度和色域的定义是通过颜色编码规范实现的，该规范将数字代码值分配给颜色空间中的位置。

![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/16777216colors.png/300px-16777216colors.png)

## 4、RGB

**RGB格式**


对一种颜色进行编码的方法统称为“颜色空间”或“色域”。用最简单的话说，世界上任何一种颜色的“颜色空间”都可定义成一个固定的数字或变量。RGB（红、绿、蓝）只是众多颜色空间的一种。采用这种编码方法，每种颜色都可用三个变量来表示-红色绿色以及蓝色的强度。记录及显示彩色图像时，RGB是最常见的一种方案。但是，它缺乏与早期黑白显示系统的良好兼容性。因此，许多电子电器厂商普遍采用的做法是，将RGB转换成YUV颜色空间，以维持兼容，再根据需要换回RGB格式，以便在电脑显示器上显示彩色图形。




网页格式
由于网页(WEB)是基于计算机浏览器开发的媒体，所以颜色以光学颜色RGB（红、绿、蓝）为主。网页颜色是以16进制代码表示，一般格式为#DEFABC （字母范围从A-F,数字从0-9 ）；如黑色，在网页代码中便是：#000000(在css编写中可简写为#000)。当颜色代码为#AABB11时，可以简写为#AB1表示，如#135与#113355表示同样的颜色。
RGB1、RGB4、RGB8都是调色板类型的RGB格式，在描述这些媒体类型的格式细节时，通常会在BITMAPINFOHEADER数据结构后面跟着一个调色板（定义一系列颜色）。它们的图像数据并不是真正的颜色值，而是当前像素颜色值在调色板中的索引。以RGB1（2色位图）为例，比如它的调色板中定义的两种颜色值依次为0x000000（黑色）和0xFFFFFF（白色）…（每个像素用1位表示）表示对应各像素的颜色为：黑黑白白黑白黑白黑白白白…。



RGB555
RGB555是另一种16位的RGB格式，RGB分量都用5位表示（剩下的1位不用）。使用一个字读出一个像素后，这个字的各个位意义如下：
高字节 低字节
X R R R R R G G G G G B B B B B （X表示不用，可以忽略）
可以组合使用屏蔽字和移位操作来得到RGB各分量的值：
#define RGB555_MASK_RED 0x7C00
#define RGB555_MASK_GREEN 0x03E0
#define RGB555_MASK_BLUE 0x001F
R = (wPixel & RGB555_MASK_RED) >> 10; // 取值范围0-31
G = (wPixel & RGB555_MASK_GREEN) >> 5; // 取值范围0-31
B = wPixel & RGB555_MASK_BLUE; // 取值范围0-31

![](https://en.wikipedia.org/wiki/File:CIExy1931_sRGB_gamut_D65.png)

RGB565
RGB565使用16位表示一个像素，这16位中的5位用于R，6位用于G，5位用于B。程序中通常使用一个字（WORD，一个字等于两个字节）来操作一个像素。当读出一个像素后，这个字的各个位意义如下：
高字节 低字节
R R R R R G G G G G G B B B B B
可以组合使用屏蔽字和移位操作来得到RGB各分量的值：
#define RGB565_MASK_RED 0xF800
#define RGB565_MASK_GREEN 0x07E0
#define RGB565_MASK_BLUE 0x001F
R = (wPixel & RGB565_MASK_RED) >> 11; // 取值范围0-31
G = (wPixel & RGB565_MASK_GREEN) >> 5; // 取值范围0-63
B = wPixel & RGB565_MASK_BLUE; // 取值范围0-31
#define RGB(r,g,b) (unsigned int)( (r|0x08 << 11) | (g|0x08 << 6) | b|0x08 )
#define RGB(r,g,b) (unsigned int)( (r|0x08 << 10) | (g|0x08 << 5) | b|0x08 )
该代码可以解决24位与16位相互转换的问题



RGB24
RGB24使用24位来表示一个像素，RGB分量都用8位表示，取值范围为0-255。注意在内存中RGB各分量的排列顺序为：BGR BGR BGR…。通常可以使用RGBTRIPLE数据结构来操作一个像素，它的定义为：
typedef struct tagRGBTRIPLE {
BYTE rgbtBlue; // 蓝色分量
BYTE rgbtGreen; // 绿色分量
BYTE rgbtRed; // 红色分量
} RGBTRIPLE;




RGB32
RGB32使用32位来表示一个像素，RGB分量各用去8位，剩下的8位用作Alpha通道或者不用。（ARGB32就是带Alpha通道的RGB24。）注意在内存中RGB各分量的排列顺序为：BGRA BGRA BGRA…。通常可以使用RGBQUAD数据结构来操作一个像素，它的定义为：
typedef struct tagRGBQUAD {
BYTE rgbBlue; // 蓝色分量
BYTE rgbGreen; // 绿色分量
BYTE rgbRed; // 红色分量
BYTE rgbReserved; // 保留字节（用作Alpha通道或忽略）
} RGBQ

![](https://h5.qzone.qq.com/page/photo?init=photo.v7/common/viewer2/index&picKey=NDR0eDMFZAkex1sBgGoANwEAAAAAAAA!&ownerUin=1678062456&appid=4&topicId=V13dexGf2OLDRB_NDR0eDMFZAkex1sBgGoANwEAAAAAAAA!_0_0&pre=http%3A%2F%2Fa4.qpic.cn%2Fpsb%3F%2FV13dexGf2OLDRB%2FVOY8sY3w5M8co2qaOV6D8GMZ.RODlcPyH3daP.dk.jM!%2Fm%2FdDcBAAAAAAAA%26ek%3D1%26kp%3D1%26pt%3D0%26bo%3D2wE7AgAAAAARF8M!%26tl%3D1%26vuin%3D1678062456%26tm%3D1539774000%26sce%3D60-3-3%26rf%3D0-0&useqzfl=1&useinterface=1&noCloseBtn=0&inqq=1)




**RGB宏**

#define RGB(r,g,b) ((COLORREF)(((BYTE)(r)|((WORD)((BYTE)(g))<<8))|(((DWORD)(BYTE)(b))<<16)))
这是个带三个参数的宏，
　

　首先将r,g,b强制转换成BYTE型，之后g左移8位，b左移16位，并把结果分别强制转换成DWORD型，最后将r,左移8位后的g，还有左移16位后的b三者做按位或，所得的结果强制转换成COLORREF类型。 


TheRGBmacro selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.
COLORREF RGB( BYTE byRed, BYTE byGreen, BYTE byBlue );
The return value is the resultant RGB color as aCOLORREFvalue.
byRed
The intensity of the red color.
byGreen
The intensity of the green color.
byBlue
The intensity of the blue color.



**RGB颜色函数**

RGB函数执行成功时返回由指定分量确定的颜色，用长整数表示。用于表示一个RGB（红绿蓝）颜色值.




  **语法**
RGB (RedAs Integer ,GreenAs Integer ,BlueAs Integer )
|部分|描述|
|:---|:---|
|red|必要参数；Integer类型。数值范围从 0 到 255，表示颜色的红色成份。|
|green|必要参数；Integer类型。数值范围从 0 到 255，表示颜色的绿色成份。|
|blue|必要参数；Integer类型。数值范围从 0 到 255，表示颜色的蓝色成份。|
注意: 如果其中有一个参数的值超过 255 ，不会显示任何错误，但这个参数会被当做 255。




**函数说明**


可以接受颜色说明的应用程序的方法和属性期望这个说明是一个代表 RGB 颜色值的数值。一个 RGB 颜色值指定红、绿、蓝三原色的相对亮度，生成一个用于显示的特定颜色。
用法RGB()函数使用下述公式计算表示颜色的长整数：Red+ 256 * Green+65536 *Blue其中，Blue代表蓝色分量，Green代表绿色分量，Red代表红色分量。各分量中，数值越小，亮度越低，数值越大，亮度越高。