# Markdown 简易手册
## .概述

* 兼容HTML
* 特殊字符自动转换

		如 < 和 & 等

***
## .区块元素
* Markdown段落前后要有一个以上的空行  
* 强制换行

		在插入处按入两个以上空格, 然后回车
***

## .标题
Markdown支持两种标题语法:
	1. 类Setext, 使用底线形式(=最高阶标题, -第二阶标题)
		
		This is an H1
		=============
		This is an H2
		-------------

	2. 类Atx, 行首插入1~6个 #，对应1~6阶标题
***

## .区块引用 Blockquotes
	1. 使用 >标识引用
	2. 引用可嵌套
		> the first 
		> > the second
	3. 引用区块也可使用其他markdown语法
		> ## 标题
		> 1. 列表
		......
***

## .列表
Markdown支持有序列表和无序列表
	1. 无序列表 (*, +, - 三种符号作为列表标记)
		* Red
		* Green
		* Blue
		
		+ Red
		+ Green
		+ Blue
		
		- Red
		- Green
		- Blue
	2. 有序列表 (数字. 形式)
		1. Red
		2. Green
		3. Blue

Markdown列表项目标记通常放于最左边, 但可以缩进, 最多**3个空格**, 项目标记后一定要接着**至少一个空格或制表符**


Markdown列表项目可包含多个段落, 每个项目下的段落都必须缩进**4个空格或1个tab**
	1. Paragraph 1 xxx
		xxxxx
	
	   Paragraph 2 xxx

	2. Paragraph xxx

Markdown列表项目内放入代码区块, 代码区块要缩进两次(2个tab或8空格)
***

## .代码区块
代码区块常用于放入程序相关的代码
Markdown中建立代码区块需要缩进**4个空格或1个tab**，代码区块会一直持续到没有缩进的那一行(或文件结尾)
**Ps: 代码区块中的markdown相关语法不会被转换**
***
## .分隔线
在一行中以**3个及以上**的星号、减号、底线建立一个分隔线, 行内不能有其他东西，符号之间可插入空格
***

## .区段元素
### .链接
Markdown支持两种形式的链接:
	1. 行内式： []后面()内接入网址链接
		[exampel](http://www.xxx  "Title")
	2. 参考式： []后面另一个[]内填入识别链接标记
		[example][id]
		[id]: http://www.xxx.com/ "Title"

		链接标记的写法:
		1.方括号中输入链接文字
		2.接着一个冒号
		3.接着一个以上的空格或制表符
		4.链接网址
		5.title内容

		Ps: []中的链接识别标签不区分大小写
			当链接标记等于链接文字时, 可省略链接文字后方括号中的链接标记
				[Google][]
				[Google]: http://google.com/
### .自动链接
Markdown自动将尖括号中的url转为链接

	<http://www.google.com/>

### .图片
图片链接与文字链接相似, 只是[]之前加入了!

	![Alt text](url "title")
	![Alt text][id]
	[id]: url/to/image "Title"

### .强调
Markdown使用\*和 _ 作为强调字词的符号

	*single asterisks*
	_single underscores_

	**double asterisks**
	__double underscores__

**Ps: 在文字中插入Markdown特殊符号, 使用\转义**

## .代码
	1. 标记小段行内代码(单行), 使用反引号(`)括起来
		the function `printf()` is used to xxxx
	2. 使用**3个及以上**反引号包含代码多行
			```C++
			int main()
			{
				printf("hello, world\n");
				return 0;
			}
			```
	3. 如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段
***

## .表格
表格使用|分隔

	|Col1|Col2|Col3|
	|-|:-|:-:|-:|
	|默认左对齐|左对齐|居中|右对齐|
	

## .其它
### .反斜杠 \
Markdown使用反斜杠转义具有特殊功能的markdown符号
***
参考链接
[Markdown语法说明][id]
[id]: http://wowubuntu.com/markdown/#list "中文简体"