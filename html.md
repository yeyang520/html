



# HTML5

### 目标

能够说出网页的基本组成

能够说出什么是HTML

能够说出常用的浏览器

能够说出Web标准的三大组成部分

### 1.网页

#### 1.1什么是网页

网站是指因特网根据一定的规则，使用HTML等制作的的用于显示特定内容的网页集合

网页时网站中的一页，通常是HTML格式的文件，通过浏览器来阅读

网页是构成网站的基本元素，通常由图片、链接、文字、声音等元素组成。

常见以.html或.htm后缀结尾的文件，因此命名为HTML文件

#### 1.2什么是HTML

HTML是超文本标记语言，用来描述网页的一种语言

HTML不是一种编程语言，而是一种超文本标记语言

 HTML是一套标记标签（markup tag)



超文本含义：

 1.它可以加入图片、动画、声音、多媒体等内容（超越文本限制）

2.它还可以从一个文件跳跃到另一个文件，与世界各地的主机的文件连接（超级链接文本）

#### 1.3网页的形成

网页是由网页元素组成，这些元素是利用html标签描述出来，然后通过浏览器解析来显示给用户的



前端人员开发 ---> 浏览器显示代码（解析、渲染）---> 生成最后的Web页面

### 总结

网页时图片、连接、文字、声音、视频等元素组成，其实是一个HTML文件（后缀名为.html）

网页生成制作，有前端人员书写HTML文件，然后浏览器打开，就能可看到了网页

HTML：超文本标记语言，用来制作网页的一门语言，有标签组成，比如：图片标签、连接标签、视频标签等...

### 2.常用的浏览器

浏览器是网页显示，运行的平台.常用的浏览器有Edg、火狐、谷歌、sfari、Opera

##### 浏览器内核

i浏览器内核（渲染引擎）：负责读取网页内容，整理讯息，计算网页的显示方式并显示页面。

### 3.Web标准（重点）

#### 	3.1为什么需要Web标准

​		浏览器不同，显示的页面或排版就不同

#### 	3.2Web标准的构成

​		主要包括结构、表现行、为三个方面

​		标准		说明

​		1.结构		结构用于对网页元素进行整理和分类，现阶段主要学的是HTML

​		2.表现		表现用于网页元素的版式、颜色、大小等我i管样式，主要指的是cs

​		3.行为		行为是指网页模型的定义及交互的编写，现阶段主要学的是javascript



​		Web标准提出的最佳体验方案：结构、样式、行为分离

​		简单理解：结构写到HTML文，表现写到CSS文件，行为写到javascript文件

## HTML（上）

#### 目标

能够说出标签的书写注意规范

能够写出HTML骨架标签

能够写出超链接标签

能够写出图片标签并说出alt和title的区别

能够说出相对路径的三种形式

### 1.HTML语法规范

#### 1.1基本语法概述

```html
<html></html>
<br />
```



#### 1.2标签关系

包含

```html
<html>
    <title></title>
</html>
```

并列

```html
<head></head>
<body></body>
```



### 2.基本结构标签

#### 	2.1第一个HTML页面

​	每个网页都会有一个基本的结构标签，页面内容也是在这些基本标签上书写

HTML页面也称HTML文档

```html
<html>
    <head>
        <title>我的第一个页面</title>
    </head>
    <body>
    	一身清贫，怎敢入繁华；
        两袖清风，岂敢误佳人。
    </body>
</html>
```



```html
<html></html>		HTML标签		页面中最大的标签，称为根标签
<head></head>		文档的头部		注意在head标签中我们必须设置时标签是title
<title></title>		文档的标签		让页面拥有一个属于自己的网页标题
<body></body>		文档的主体		元素包含文档的所有内容，页面内容基本都是放到body里卖弄的
```



### 3.开发工具

VSCode

#### 3.1文档类型声明标签

<!DOCTYPE>文档类型声名，作用是告诉浏览器使用那种HTML版本来显示网页

```html
<!DOCTYPE html>
```

<!DOCTYPE>文档类型声名，作用是告诉浏览器使用那种HTML版本来显示网页

这句话意思：当前页面采取的是HTML5版本来显示网页

注意：

 1. .<!DOCTYPE>声明位于文档中的最前面位置，处于<html>标签之前

	1. <!DOCTYPE>不是一个HTML标签，它就是文档类型声明标签



#### 3.2 lang语言种类

​	用来定义当前文档显示的语言

 	1. en定义语言为英文
 	2. zh-CH定义语言为中文

#### 3.3字符集

字符集（character set）是多个字符的集合。以便计算机能够识别和存储各种文字

在<head>标签内，可以通过<meta>标签的charset属性来规定HTML文档应该使用哪种字符编码

```html
<meta charset="UTF-8">
```

注意：上面语法是必须要写的代码，否则会出现引起乱码的现象。一般情况下，统一使用 UTF-8 编码，尽量统一写成“UTF-8”



### 4.HTML标签

#### 4.1标签语义

#### 4.2标题标签<h1> - <h6>(重要)

​	为了使网页能具有语义化，我们经常会在页面中用到标题标签。HTML提供了 6 个等级的网页标题，即<h1> - <h6>。

```html
<h1>我是一级标题</h1>
```



单词head的缩写，意味头部、标题

**标签语义** ：作为标题使用，并且依据重要性递减

特点：

1.加了标题的文字会变得更粗，字号更大

2.一个标题独占一行

#### 4.3段落和换行标签(重要)

 在网页中，要把文字有条理的显示出来，就需要将这些文字分段显示。在HTML标签中，<p>标签用于定义段落，它可以将整个网页分为若干个段落

```html
<p>这是一个段落标签</p>			pargraph
```





```
<br/>这是一个换行标签 打断、换行   break
```



#### 4.4文本格式化标签

粗体、斜体、下划线

```html
加粗  <strong></strong>  或      加粗  <b></b>
倾斜	<em></em>		   或	   倾斜<i></i>
删除线	<del></del>		   或      删除<s></s>
下划线	<ins></ins>		   或      下划线<u></u>
```





#### 4.5<div>和<span>

这两个标签是没有语义的，它们就是一个盒子，用来装内容



#### 4.6图像标签和路径(重点)

1.图像标签

```html
<img src="图像url"/>
```

src是<img>的必须属性，它用于指定图像文件的路径和文件名

所谓属性，可简单理解就是属于这个图像标签的特性



```html
属性
	替换  <alt>  <img src="imag.jgp" alt="这张图片">无法加载时替换
	提示  <title>   鼠标放到图像上，提示文字
	像素	<width>		设置图像宽度
	像素	<height>	设置图像高度
    像素	<border>	设置图像的边框粗细
```

 

2.路径

​      先导：目录文件夹和根目录

目录文件夹：普通文件夹，里面不过存放了我们做页面需要的相关素材

根目录：打开目录文件夹的第一层就是根目录

​	1.相对路径：
​		图片相对于HTML页面的位置

```html
同一级路径		<img src="img.jgp"/>
下一级路径		<img src="images/img.jgp"/>
上一级路径		<img src="../img.jgp"/>  ../返回上一级
```

​	2.绝对路径

​	是指根目录下的绝对位置，直接到达目录位置，通常从盘符开始

```
C:\Users\boy\go\vscode\MyFirstHtml\imag
```

​    还有 网络绝对路径



#### 4.7超链接标签

<a>

1.规范

```html
<a href="跳转目标" target="目标弹出方式">文本或图像</a>
```

```html
href	用于·指定木匾的url地址 必须
target	用于链接页面的打开方式，其中_self为默认值,_blank为在新窗口中打开
```



2.分类

​	1.外部链接	例如 

```html
<a href="https://www.baidu.com" target="_blank">百度</a>
```



​	2.内部链接

网站内部页面之间的相互链接

```html
<a href="newhtml.html">第一个页面</a>
```



​	3.空链接

```html
<a href="#">这是空连接</a>
```



​	4.下载链接

```html
<a href="img.zip">这是下崽链接</a>
```

​	

​	5.网页元素都可以添加链接



​	6.锚点链接

​		在连接文本的href属性中，设置属性值为 #名字 的形式，如

```html
<a href="two">第二集</a>
```

​		找到目标位置的标签，在面添加一个id属性，如 <h3 id="two">第二集</h3>

```html
<a href="#live">个人生活</a>
<h1 id="live">个人生活</h1>
```

### 	



### 5.HTML中的注释标签和特殊字符

#### 5.1注释

注释标签  快捷键 ctrl + /

```html
<!--我想喝可乐-->
```



#### 5.2特殊字符

```
空格			&nbsp;
小于号			&lt;
大于号			&gt;
```



## HTML(下)

#### 目标

能够书写表格

能够写出无序列表

能够写出3~4个常用的input 表单类型

能够写出下拉表单单表

能够使用表单元素实现注册页面

能够独立阅读W3C文档



### 1.表格

#### 1.1表格的主要作用

​	用来显示、展示数据

#### 1.2表格的基本语法

​	

```html
<table>
    <tr>		<!-- 行-->
        <td>				</td>	<!--单元格-->
    </tr>
    
    
</table>
```



#### 1.3表头单元格

<th>加粗居中的标题</th>

#### 1.4表格属性

可以用CSS设置

```html
属性名				  属性值					描述
align	  			left center right 	固定对齐方式
border	  			1 或 “”				加边框
cellpadding  		内容与单元格之间的距离
cellspacing  		单元格和单元格之间的内容
width height	    表格的宽度
```



#### 1.5表格结构标签

头部区域和主题区域

```html
<thead></thead>
<tbody></tbody>
```

#### 1.6合并单元格

跨行合并  rowspan="合并单元格的个数"

​                  colspan

目标单元格

跨行：最上侧单元格为目标单元格，写合并代码

跨列：最左侧单元格为目标单元格，写合并代码



合并单元格三部曲：
1.先确定是跨行还是跨列

2.找到目标单元格。写上合并方式 = 合并单元格的数量  比如 <td colspan="2"></td>

3.删除多余单元格



#### 1.7表格总结

1.表格的相关标签

```html
<table>
    <thead>
        <tr>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
        	<td></td>
    	</tr>
    </tbody>

</table>

```

2.表格的相关属性

### 2.列表标签

无序列表	有序列表	自定义列表

#### 2.1无序列表(重点)

ul里只能放li ， li里面随便放

```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
</ul>
```



#### 2.2有序列表

```html
<ol>
    <li></li>
</ol>
```



#### 2.3自定义列表

自定义列表经常用与对术语的解释和描述

```html
<dl>
    <dt>名词1</dt>
    <dd>名词解释1</dd>
    <dd>名词解释2</dd>
</dl>
```



#### 2.4标签总结

```html
标签总结			定义			说明
<ul>			  无序标签		里面只能包含li 没有顺序
<ol>			  有序列表		只包含<li>
<dl>			  自定义列表		<dt><dd>
```



### 3.表单标签

#### 3.1为什么需要信息

收集信息

#### 3.2表单的组成

表单域、表单元素、提示信息

#### 3.3表单域

表单域是一个·包含表单元素的区域

在HTML中，<form>标签定义表单域

```html
<form action="地址" method="提交方式" name="表单域名称">
    
</form>
```

#### 3.4表单元素

##### 	3.4.1 input表单元素	

type属性

```
text				text是文本框，可以输入任何值
password			密码
radio				定义单选按钮
checkbox			定义复选框，多选
checked				单选按钮和复选按钮 默认选择
maxlength			规定输入的最大长度
submit				提交
reset				重置按钮
button				后期结合js
file				文件上传
```

name属性

性别按钮有一个相同的名字就可以实现多选一

value属性

规定input的值

##### 3.4.2 label标签

label标签为Input元素标注



```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex">
```

label当中的for属性应当与相关元素的id相同



##### 3.4.3 下拉表单 select

```html
<body>
    美女
    <select>
        <option>黑丝</option>
        <option>jk</option>
	</select>
</body>
```

option中定义 select="selected" 表示默认选择

##### 3.4.4  textarea表单元素

特大号文本框

```html
今日反馈
<textarea cols="每行的字数" rows="显示的行数">
    默认有的内容
</textarea>
```







## 写在最后

#### 1.HTML页面不能加载图片



原因：由于在imag文件夹前面加了/导致图片不能加载

```
<img src="/imag/2.png" />
```

改进：去掉后即可

```
<img src="imag/2.png" />
```

如果跟.html文件在同一文件中，直接用名称就可以，不用加别的

2.png跟.html在同一文件夹中

```
<img src="2.png" />
```
