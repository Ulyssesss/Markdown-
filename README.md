# Markdown 简明教程

## 主要内容

>（一）[Markdown 是什么](#1)
  
>（二）[为什么要使用 Markdown](#2)

>（三）[如何使用 Markdown](#3)

>（四）[Markdown 编辑器](#4)  

## 正文

### <span id="1"> （一）Markdown是什么 <span/>

Markdown 是一种轻量级的 **标记语言**，以 **纯文本** 的形式编写文档，通过简洁的语法代替排版，并且可以导出 **HTML**、**PDF** 等格式。

### <span id="2"> （二）为什么要使用 Markdown </span>
  
* 格式清晰，读起来很舒服
* 语法简洁，编写时可以更**专注于内容**而非排版格式  
* **纯文本**形式，兼容所有的文本编辑器
* 可导出 HTML、PDF 等常见格式  

### <span id="3"> （三）如何使用 Markdown </span>

Markdown 的语法非常简单，主要包含以下几个部分：[**标题**](#header)，[**段落**](#paragraph)，[**列表**](#list)，[**强调**](#emphasis)，[**区块引用**](#block)，[**代码区块**](#code-block)，[**行内代码**](#code-inline)，[**分割线**](#hr)，[**链接**](link)，[**自动链接**](#auto-link)，[**图片**](#image)，[**反斜杠**](#backslash)，[**表格（扩展）**](#table)。

#### <span id="header"> 1. 标题 </span>

标题有两种形式，一种形式为在文字下方添加 `=====` 或 `-----`，分别表示一级标题和二级标题，如
>一级标题  
>`=====`  
>二级标题  
>`-----`  

效果为
>一级标题
>=====
>二级标题
>-----  

另一种形式在标题前添加 `#`，添加一个 `#` 为一级标题，两个为二级标题，最多可至六级标题，如
>`# 一级标题`  
>`## 二级标题`  
>`### 三级标题`  
>`#### 四级标题`  
>`##### 五级标题`  
>`###### 六级标题`  

效果为
>#一级标题
>##二级标题
>###三级标题
>####四级标题
>#####五级标题
>######六级标题

#### <span id="paragraph"> 2. 段落 </span>

一个 Markdown 段落是由一个或多个连续的文本行组成，**段落前后要有一个以上没有文字的空行**。使用 **两个以上的空格加回车** 可强制在 **段落内换行**。

段落的开头 **不应该使用空格或者制表符（Tab）缩进**。

#### <span id="list"> 3. 列表 </span>

Markdown 支持无序列表和有序列表。无序列表使用**星号`*`、加号`+`或减号`-`加至少一个空格或制表符（Tab）**作为列表标记，如
>`* 第一项`  
>`* 第二项`  
>`* 第三项`

效果为
>* 第一项
>* 第二项
>* 第三项

有序列表使用**数字加点`.`再加至少一个空格或制表符**作为列表标记，如
>`1. 第一项`  
>`2. 第二项`  
>`3. 第三项`

效果为
>1. 第一项
>2. 第二项
>3. 第三项

#### <span id="emphasis"> 4. 强调 </span>

内容前后加上 **星号 `*` 或 下划线`_`** 表示 **强调**。前后加一个星号或下划线为 *斜体*，两个为 **粗体**，三个为 ***粗斜体***。如
>`*强调*`  
>`**强调**`  
>`***强调***`

效果为
>*强调*  
>**强调**  
>***强调***

#### <span id="block"> 5. 区块引用 </span>

在段落的 **第一行或每行开头** 使用 `>` 表示引用，多个 `>` 表示嵌套，如
>`>区块引用`  
>`>>嵌套引用`

效果为
>区块引用
>>嵌套引用


#### <span id="code-block"> 6. 代码区块 </span>

每行前加 **4个空格或1个制表符（Tab）** 表示代码区块，效果为

	public static void main(string[] args){
		System.out.println("Hello, world");
	}

#### <span id="code-inline"> 7. 行内代码 </span>

前后含 **反引号( ` )** 的内容为行内代码，如
	
>		`System.out.println("Hello, world")` 表示输出"Hello, world"。

效果为

>`System.out.println("Hello, world")` 表示输出"Hello, world"。

#### <span id="hr"> 8. 分割线 </span>

三个或三个以上的星号 `*`、减号 `-`及下划线 `_`表示 **分割线**，中间可插入空格，如
>`***`  
>`- - -`

效果为
>***
>- - - 

#### <span id="link"> 9. 链接 </span>

Markdown 支持两种形式的链接，**行内式** 和 **参考式**。  
**行内式** 的链接文字用中括号 `[]` 标记，方括号后紧接小括号 `()` 标记网址链接，可在网址链接后用引号标记链接的 title 文字，如
>`[GitHub](https://github.com/ "Github")`

效果为
>[GitHub](https://github.com/ "GitHub")

**参考式** 的链接文字同样使用中括号 `[]` 标记，后面再接一个中括号标记链接的标识，需要在文件的任意处通过 `[id]:url "title"` 标记链接，如
>`[GitHub][1]`  
>`[1]:https://github.com/ "GitHub"`

效果为
>[GitHub][1]  
[1]:https://github.com/ "GitHub"

#### <span id="auto-link"> 10. 自动链接 </span>

Markdown 支持以 **简短的自动链接** 形式处理网址和电子邮箱，用尖括号 `<>` 标记，如
>`<https://github.com>`

效果为
><https://github.com>

#### <span id="image"> 11. 图片 </span>

Markdown 中标记图片的方式与标记链接类似，同样允许 **行内式** 和 **参考式** 两种形式，只需在链接文字的标记前加一个感叹号 `!`，如
>`![GitHub Icon](https://github.com/fluidicon.png "GitHub Icon")`

效果为
>![GitHub Icon](https://github.com/fluidicon.png "GitHub Icon")

***遗憾的是 Markdown 不支持指定图片的宽高***

#### <span id="backslash"> 12. 反斜杠 </span>

通过反斜杠 `\` 可插入一些在 Markdown 语法中有其他意义的符号，如
>`\*前后为星号\*`

效果为
>\*前后为星号\*

Markdown 支持在以下符号前加反斜杠 `\` 来帮助插入普通的符号：

	\	反斜杠   
	`	反引号
	*	星号
	_	下划线
	{}	大括号
	[]	中括号
	()	小括号
	#	井号
	+	加好
	-	减号
	.	英文句号
	!	感叹号
	
#### <span id="table"> 13. 表格(扩展) </span>

表格为 **扩展** 的 Markdown 语法，`|` 表示纵向的边界，表头和内容之间用 **三个或三个以上减号 `-` 隔开**，可以使用冒号 `:` 设置 **对齐方式**。冒号 `:` 在左边表示左对齐，在右边表示右对齐，两边都有冒号 `:` 表示居中，不使用冒号 `:` 时默认 **左对齐**，如
	
>	| name | gender | age |  
>	| :---: | :---: | :---: |    
>	| Jack | boy | 4 |    
>	| Amy | girl | 5 | 

效果为

>| name | gender | age |  
>| :---: | :---: | :---: |  
>| Jack | boy | 4 |
>| Amy | girl | 5 |  

### <span id="4"> （四）Markdown 编辑器 </span>

Mac 下好用的 Markdown 编辑器有很多，如 [MacDown](http://macdown.uranusjr.com/)，[Mou](http://25.io/mou/)，[Typora](https://typora.io/) 等。

Windows 下可以使用 [MarkdownPad](http://www.markdownpad.com/)，[马克飞象](https://maxiang.io/)，[有道云笔记](https://note.youdao.com/) 等。