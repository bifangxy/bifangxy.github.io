---
title: Markdown语法
date: 2016-09-03 15:15:51
categories: blog
tags: [MarkDown]
---
# Markdown的入门与认识  
 
## 认识Markdown
Markdown 是一种用来写作的轻量级「标记语言」，它用简洁的语法代替排版，而不像一般我们用的字处理软件 Word 或 Pages 有大量的排版、字体设置。它使我们专心于码字，用「标记」语法，来代替常见的排版格式。例如此文从内容到格式，甚至插图，键盘就可以通通搞定了。目前来看，支持 Markdown 语法的编辑器有很多，包括很多网站（例如简书）也支持了 Markdown 的文字录入。Markdown 从写作到完成，导出格式随心所欲，你可以导出 HTML 格式的文件用来网站发布，也可以十分方便的导出 PDF 格式，这种格式写出的简历更能得到 HR 的好感。甚至可以利用 CloudApp 这种云服务工具直接上传至网页用来分享你的文章，全球最大的轻博客平台 Tumblr，也支持使用 Mou 这类 Markdown 工具进行编辑并直接上传。我们在使用hexo进行博客书写的时候，也需要用到Markdown  
### Markdown官方文档  
>官方的Markdown语法规则文档：  

* [创始人John Gruber的MarkDown语法说明](http://daringfireball.net/projects/markdown/syntax)  
* [Markdown 中文版语法说明](http://wowubuntu.com/markdown/#list)  


### 使用Markdown的优点
* 专注你的文字内容而不是排版样式
* 轻松地到处HTML，PDF和本身的.md文件
* 纯文本内容，兼容所有的文本编辑器与文字处理软件
* 语法简洁
* 简单，轻量级
* 标签有行业标准
* 应用广泛（GIThub，Reddit，StackOverFlow,Jianshu,Hexo）


### 工具
* Mac平台：Mou，Ulysses Ⅲ等
* Windows平台：MarkdownPad，MarkDown等
* Web平台：简书，Draftin等  


## Markdown语法的简要规则

### 换行
	在markdown的语法中，单个回车视为空格，连续回车才是换行。  
	（行尾加两个空格，可以段内强制换行，一般用户可以忽略。）
### 标题
	在文字前面添加#+空格，一共6级，#为一级标签。  
	# 一级标题  
	## 二级标题
	## 三级标题
	Tips:建议在#号后面加一个空格，这是最标准的MArkdown语法.  
### 列表
	在MarkDown下，列表的的显示只需要在文字前加上-或者*就可以变成无序列表。  
	有序列表则直接在文字前加1. 2 . 3.  符号和文字之间要加上一个字符的空格  
无序列表  

* 1
* 2  
* 3

有序列表  
1. 1  
2. 2  
3. 3  

### 引用
	只需在引用的文字前面加上>即可表示为引用（>XXXXXX）
> 这是我需要引用的地方

### 粗体与斜体

粗体：两端用两个*或者__包裹


斜体：两端用*或者_包裹


**粗体** or __粗体__
*斜体* or _斜体_

### 链接
Markdown支持两种形式的链接语法：行内式和参考式两种形式
行内式：只要在方括号后面紧接着圆括号并插入网址链接即可，如果你还想加上链接的title文字，
只要在网址后面，用双引号把title文字包起来即可,下面是行内式链接语法：
`[链接](http://www.baidu.com"标题")`
`[链接](http://www.baidu.com)`

这是一个行内式[例子](http://www.baidu.com "百度")有title的  
这是一个行内式[例子](http://www.baidu.com)没title的

参考式：参考式链接实在连接的方括号后面再接上另一个方括号，而在第二个方括号后面填入用以辨识的标记。
(格式[链接] [标记]) 然后在文件的任意处你可以把这个标记的链接内容定义出来 （格式[标记]： http://www.baidu.com "标题"）  

下面是一个参考式链接的范例：  
		
`I get 10 times more traffic from [Google] [1] than from[Yahoo] [2] or [MSN] [3].  `
`[1]: http://google.com/        "Google"`
`[2]: http://search.yahoo.com/  "Yahoo Search"`
`[3]: http://search.msn.com/    "MSN Search"`
链接内容定义的形式为：

* 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
* 接着一个冒号
* 接着一个以上的空格或制表符
* 接着链接的网址
* 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着  

这是一个参考式[例子][id]  
[id]: http://www.baidu.com "百度"

### 图片
Markdown中使用一种和链接很相似的语法来标记图片，同样也允许两种形式：行内式和参考式。  
行内式的图片语法：
`![Alt text](/path/to/img.jpg)`
`![Alt text](/path/to/img.jpg "Optional title")`
详细叙述如下:

* 一个惊叹号！
* 接着一个方括号，里面放上图片的替代文字
* 接着一个普通括号，里面放上图片的网址，最后还以用引导好包住并加上选择性的“title”文字

参考式的图片语法：
`![Alt text][id]`
「id」是图片参考的名称，图片参考的定义方式则和链接参考一样:
`[id]: url/to/image  "Optional title attribute"`
### 代码框
作为一个程序猿，在文章里优雅的引用代码框是十分必要的，在Markdown下实现也非常简单，只需要用三个 ` 把中间的代码包裹起来,如:  

```
public class HelloWorld{
	public static void main(String[] args){
		System.out.print("Hello World");
		}
	}
```
效果如下：

```
public class HelloWorld{
	public static void main(String[] args){
		System.out.print("Hello World");
		}
}
```

### 分割线
分割线的语法只需要另起一行，联系输入三个星号***即可
***

