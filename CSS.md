# CSS

## 第一段

### 基础选择器

根据不同需求选择标签

#### 1.标签选择器

更改某一种标签的属性

```html
p {
	color :red;
}
所有p标签都会变为红色
```

标签名 {

​		属性 ：东西；

}

#### 2.类选择题

更改一种或几种

```html
.red {
	color :red;
}
<div class="red">
    
</div>

<ul>
    <li class="red"> </li>
</ul>
```

多类名

一个标签可以指定多类名，中间用空格分开

```html
.font{
	font-size: 35;
	width: 100px;
	height: 100px;
}
.red{
	color: red;
}
.green{
	color: green;
}
```

#### 3. id选择器

样式#定义 ，结构id调用，只能调用一次，别人切勿使用

```html
#name{
	color: pink;
}
<div id="name">
    
</div>
```

#### 4.通配选择器

```html
<style>
    *{
        color: red;
        margin: 0;
        padding: 0;
    }
</style>
//将所有标签都改为红色
```

### 字体

#### 1.型号

```html
p{
	font-family:"微软雅黑"；
}
div{
	font-family:'微软雅黑'；
}
```

#### 2.大小

标题文字特殊设置

```html
p{
	font-size: 20px;
}
h2{
	font-size: 16px;
}
```

#### 3.文字粗细

```html
body{
	font-weight: bold;//加粗
}
.bold{
	font-weight: 700;//加粗,相当于bold
}
```

#### 4.文字斜体

```html
em {
	font-style: normal;//倾斜字体变正常
}
```

#### 5.字体复合属性

必须保留size 和 family属性

```html
div{
	font-style: italic;
	font-weight: 700;
	font-size: 16px;
	font-family: "微软雅黑"；
}
简写 font: font-style font-weight font-size/line-height font-family
div{
	font: italic 700 16px "微软雅黑";
}
```

#### 6.小姐

```html
font-size 	字号		px像素单位  
font-family 字体
font-weight 字体粗细	700加粗 400正常
font-style 	字体样式	倾斜 italic 正常normal
font 		字体连写
```

### 文本属性

颜色、对齐文本、装饰文本、文本缩进、行间距

#### 1.对齐文本

text-align设置水平对齐

left

right

center

```html
div{
	text-align: center;
}
```

#### 2.装饰文本

text-decoration  下划线 删除线 上划线

none 默认没有装饰线

underline 下划线

overline 上划线

line-through 删除线

```html
div{
	text-decoration:underline;
}
```

#### 3.文本缩进

text-indent

em是一个相对单位，当前元素一个文字大小

text-indent: 2em; 

```html
div{
	text-indent: 10px;
}
```

#### 4.行间距

line-height

```html
p{
	line-height: 26px;
}
```

#### 5.小姐

```html
color 文本颜色
text-align 文本对齐
text-indent 文本缩进
text-decoration 文本修饰
text-height 行高
```

### 引入方式

1.行内样式表	

2.内部样式表	

3.外部样式表	

#### 1.内部样式

跟html放在一起，放入<style>中

#### 2.行内样式

```html
<div style="color: red; font-size: 12px;">
    
</div>
```

#### 3.外部样式表

 引入

```html
<link rel="stylesheet" href="style.css">
```

## 第二段

### Emment 语法

1.生成标签 div+table

2. div*10
3. 父子级关系标签 ul > li +table
4. 兄弟关系 div+p+ table
5. div . sex +table=<div calss="sex"></div>或 .sex+table    .demo$5+table  生成五个有序的div
6. div{你}*5 +table

#### 快速生成 CSS 样式

tac+table = text-align: center;

w100 + table  = width:100px;

#### 快速格式化代码

shift+alt+f

### 复合选择器

后代选择器

子选择器

并集选择器

伪类选择器

#### 1.后代选择器(重要)

元素1 元素2 {样式说明}

```html
ol li {
	color: red;
}
```

改变 ol 中的 li 标签

#### 2.子(元素)选择器

只选亲儿子    
元素1 > 元素2 { }

```html
.class > p{

}
```

#### 3.并集选择器

用 逗号分割

元素1 , 元素2 { }

```html
div,p{
	color: red;
}
```

#### 4.伪类选择器

链接伪类选择器

```html
a:link		选择所有未被访问的链接
a:visited	选择所有被访问的链接	 点了之后的颜色
a:hover		选择鼠标指针位于之上的链接	鼠标经过的链接
a:active	活动链接  					按下不松开

a:link{		链接变色
	color: pink;
	text-decoration: none;
}
```

:focus伪类选择器

```html
input:focus{//获得光标的input表单元素选取
	background-color: pink;
	color: red; //字体颜色
}
```



### CSS 元素显示模式

#### 块元素

```html
h1 p div ul ol li 
```

独占一行

长宽高自己可设置

#### 行内元素

span a strong 

宽高默认，不能更改

#### 行内块元素

img  input td 

一行放多个，之间又空白缝隙

宽高可默认可更改

#### 元素显示模式转换

转化为块状元素		diplay:block

```html
a{
	width: 100px;
	height: 100px;
	background-color: red;
	dispaly: block;
}
```

块状转换行

```htm
div{
	display: inline;
}
```

转换为行内快元素

```html
span{
	display: inline-block;
}
```

#### 单行文字垂直居中

让文字行高等于盒子高

### 背景

#### 1.背景颜色

```html
background-color: transparent;			透明
```

#### 2.背景图片

```html
background-imag: none|| url(图片地址);
```

#### 3.背景平铺

默认平铺

```html
background-repeat: no-repeat;		不平铺
					repeat;
					repeat-x;		沿x平铺
					repeat-y
```

#### 4.背景图片位置

```html
background-position: x y;
1.方位名词
top center bottonn left right
2.精确坐标
只写一个，另一个默认居中
3.混合单位
```

#### 5.背景固定

```html
background-attachment:  
scroll 背景随图像移动
fixed	背景固定
```

#### 6.背景复合写法

背景颜色 背景图片 图片地址 背景平铺 背景图像滚动 背景图片位置

####  7.背景颜色半透明

```html
div{
	background: rgba(0,0,0,0.5)
}
alpha 透明度
0.5透明度
```

#### 8.小姐

```html
background-color		背景颜色
background-image		背景图片		url
background-repeat		是否平铺		repeat/no-repeat/repeaat-x/repeat-y
background-position		背景位置		
background-attachment	背景			scroll/fixed固定
背景简写
背景半透明
```

### CSS 三大特性

#### 1.层叠性

样式冲突：就近原则

#### 2.继承性

子标签继承父标签的某些样式 

font-size: 14px/1.5	行高是14的1.5倍	当前文字大小的1.5倍

#### 3.优先级

一个元素指定多个优先级

选择器相同就执行层叠行

不同根据选择器权重



继承 < 元素选择器 < 类选择器 <ID选择器 < style < !important



权重叠加

### 盒子模型

####  1.网页布局

准备网页元素，

利用css设置盒子样式，摆放到相应位置

往盒子放内容

#### 2.盒子模型组成

