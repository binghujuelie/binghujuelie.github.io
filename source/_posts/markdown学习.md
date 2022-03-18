---
title: Markdown基本语法教程
date: 2022-02-25 21:07:00
tags: 
   - Markdown
   - 教程
categories: 教程
description: markdown的一个简单入门教程
---


## 标题语法
创建标题，在单词或短语前添加井号（#）。#的数量代表标题的大小，越多越小

## 段落语法
用空白行来分隔文本，不要用空格（spaces）或制表符（ tabs）缩进段落。

## Markdown换行语法
在一行的末尾添加两个或多个空格，然后按回车键,即可创建一个换行  
### 换行语法的最佳实践
几乎每个 Markdown 应用程序都支持两个或多个空格进行换行，称为 结尾空格（trailing whitespace) 的方式，但这是有争议的，因为很难在编辑器中直接看到空格，并且很多人在每个句子后面都会有意或无意地添加两个空格。由于这个原因，你可能要使用除结尾空格以外的其它方式来换行。幸运的是，几乎每个 Markdown 应用程序都支持另一种换行方式：HTML 的 <br> 标签。

为了兼容性，请在行尾添加“结尾空格”或 HTML 的 <br> 标签来实现换行。<br>还有两种其他方式我并不推荐使用。CommonMark 和其它几种轻量级标记语言支持在行尾添加反斜杠 (\) 的方式实现换行，但是并非所有 Markdown 应用程序都支持此种方式，因此从兼容性的角度来看，不推荐使用。并且至少有两种轻量级标记语言支持无须在行尾添加任何内容，只须键入回车键（return）即可实现换行。

## Markdown 强调语法
### 粗体
要加粗文本，请在单词或短语的前后各添加两个星号（asterisks）或下划线（underscores）。如需加粗一个单词或短语的中间部分用以表示强调的话，请在要加粗部分的两侧各添加两个星号（asterisks）。

### 斜体
要用斜体显示文本，请在单词或短语前后添加一个星号（asterisk）或下划线（underscore）。要斜体突出单词的中间部分，请在字母前后各添加一个星号，中间不要带空格。

### 同时粗体+斜体
要同时用粗体和斜体突出显示文本，请在单词或短语的前后各添加三个星号或下划线。要加粗并用斜体显示单词或短语的中间部分，请在要突出显示的部分前后各添加三个星号，中间不要带空格。

## Markdown 引用语法
要创建块引用，请在段落前添加一个 > 符号。
举例：
> Dorothy followed her through many of the beautiful rooms in her castle.

### 多个段落的块引用
块引用可以包含多个段落。为段落之间的空白行添加一个 > 符号
举例：
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### 嵌套块引用
块引用可以嵌套。在要嵌套的段落前添加一个 >> 符号。
举例：
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### 带有其他元素的块引用
块引用可以包含其他 Markdown 格式的元素。并非所有元素都可以使用，你需要进行实验以查看哪些元素有效。
举例：
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.

# Markdown列表语法
可以将多个条目组织成有序或无序列表。

### 有序列表
要创建有序列表，请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。
举例：
1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item

### 无序列表
要创建无序列表，请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。

### 在列表中嵌套其他元素
要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进四个空格或一个制表符，如下例所示：
*   This is the first list item.
*   Here's the second list item.

    I need to add another paragraph below the second list item.

*   And here's the third list item.

#### 引用块
*   This is the first list item.
*   Here's the second list item.

    > A blockquote would look great below the second list item.

*   And here's the third list item.

#### 代码块
代码块通常采用四个空格或一个制表符缩进。当它们被放在列表中时，请将它们缩进八个空格或两个制表符。

## Markdown 代码语法
要将单词或短语表示为代码，请将其包裹在反引号 (`) 中。

如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号(``)中。

### 代码块
要创建代码块，请将代码块的每一行缩进至少四个空格或一个制表符。
举例：
```
    <html>
      <head>
      </head>
    </html>
```
😊
### Markdown 围栏代码块
Markdown基本语法允许您通过将行缩进四个空格或一个制表符来创建代码块。如果发现不方便，请尝试使用受保护的代码块。根据Markdown处理器或编辑器的不同，您将在代码块之前和之后的行上使用三个反引号（(```）或三个波浪号（~~~）。

## Markdown分割线语法
要创建分隔线，请在单独一行上使用三个或多个星号 (***)、破折号 (---) 或下划线 (___) ，并且不能包含其他内容。
如：
***

---

___

## Markdown 链接语法
链接文本放在中括号内，链接地址放在后面的括号中，链接title可选。

超链接Markdown语法代码：[超链接显示名](超链接地址 "超链接title")

对应的HTML代码：<a href="超链接地址" title="超链接title">超链接显示名</a>
举例：
这是一个链接 [Markdown语法](https://markdown.com.cn)。

### 给链接增加 Title
链接title是当鼠标悬停在链接上时会出现的文字，这个title是可选的，它放在圆括号中链接地址后面，跟链接地址之间以空格分隔。
举例：
```
> 这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。
```
这是一个链接 [Markdown语法](https://markdown.com.cn "最好的markdown教程")。

### 网址和Email地址
使用尖括号可以很方便地把URL或者email地址变成可点击的链接
如：
<https://markdown.com.cn>
<fake@example.com>

### 格式化链接
强调链接, 在链接语法前后增加星号。 要将链接表示为代码，请在方括号中添加反引号。
举例：
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).

### 引用类型链接
1.放在括号中的标签，其后紧跟一个冒号和至少一个空格（例如[label]:）。
2.链接的URL，可以选择将其括在尖括号中。
3.链接的可选标题，可以将其括在双引号，单引号或括号中。
举例：
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'
[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)
[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"

### 注意：
不同的 Markdown 应用程序处理URL中间的空格方式不一样。为了兼容性，请尽量使用%20代替空格。

## Markdown 图片语法
要添加图像，请使用感叹号 (!), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。

插入图片Markdown语法代码：
```
\ ![图片alt](图片链接 "图片title")。
```

对应的HTML代码：
```
<img src="图片链接" alt="图片alt" title="图片title">
```
举例：
```
![这是图片](/img/a.jpg "风景图")
```
![这是图片](/img/a.jpg "风景图")
### 链接图片
给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。
举例：
```
[![图片](/img/a.jpg "Shiprock")](https://markdown.com.cn)
```
[![图片](/img/a.jpg "Shiprock")](https://markdown.com.cn)
## 转义字符语法
要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加反斜杠字符 \ 。
举例：
\* Without the backslash, this would be a bullet in an unordered list.

## Markdown内嵌 HTML 标签

### 行级內联标签
HTML 的行级內联标签如 `<span>、<cite>、<del>` 不受限制，可以在 Markdown 的段落、列表或是标题里任意使用。依照个人习惯，甚至可以不用 Markdown 格式，而采用 HTML 标签来格式化。例如：如果比较喜欢 HTML 的 `<a>` 或 `<img>` 标签，可以直接使用这些标签，而不用 Markdown 提供的链接或是图片语法。当你需要更改元素的属性时（例如为文本指定颜色或更改图像的宽度），使用 HTML 标签更方便些。

HTML 行级內联标签和区块标签不同，在內联标签的范围内， Markdown 的语法是可以解析的。
举例：
```
This **word** is bold. This <em>word</em> is italic.
```
This **word** is bold. This <em>word</em> is italic.

### 区块标签
区块元素──比如 \<div>、\<table>、\<pre>、\<p> 等标签，必须在前后加上空行，以便于内容区分。而且这些元素的开始与结尾标签，不可以用 tab 或是空白来缩进。Markdown 会自动识别这区块元素，避免在区块标签前后加上没有必要的 \<p> 标签。

## 扩展教程
markdown扩展语法](https://markdown.com.cn/extended-syntax/)
