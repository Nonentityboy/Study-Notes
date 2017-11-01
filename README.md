>#web前端：

####web应用被分类为分布式应用，一般是客户端和服务器结构，所以我们有一部分的代码运行在客户端，另一部分代码运行在服务器。那些客户端上的应用就是前端，通常指的是我们的浏览器。

###入门要求：了解什么是前端，了解基本的html css javascript语法（基本的语法是整个技术体系最重要的东西。）

前端开发语言共三种：

html（Hypertext Markup Language）——结构      超文本标记性语言 （ html相当于大楼的钢筋 水泥结构）

css（Cascading Style Sheets）         ——样式      层叠样式表   （ css可看作大楼的装修，它用来铺平样式）

js    （Javascript）            ——行为       （ js可理解为大楼的物业，它为这栋大楼供水供电）

>##HTML和CSS基础

###HTML（Hypertext Markup Language）是超文本标记语言。
####一·HTML特点：

1.HTML不需要编译，直接由浏览器执行。

2.HTML文件是一个文本文件。

3.HTML文件必须使用html或htm为文件名后缀。

4.HTML大小写不敏感，HTML与html一样。

####二·<!DOCRYPE>声明必须放在HTML文档第一行，该声明不是HTML标签。

####三·网页编码设置：

####四·当网页出现乱码时    

解决方式：

在<head></head>标签之间添加：

<meta http-equiv="Content-Type "contect="text/html;charse=utf-8"/>

注：常用utf-8· GB2312·gbk等编码

####五·文字和段落标签  
```
起始终止标签（创建一个HTML文档）：<html></html>  

头部标签（设置文档标题以及其它不在WEB网页上显示的信息）：`<head></head>

设置文档的可见部分：<body></body>

将题目放到标题栏中：<title></title>

快;盒子(装内容)：<div></div>

风格类型:<style></shyle>

位置：<link></link>

标题标签：<h1></h1>~<h6></h6>

段落标签：<p> </p>

align对齐属性值    例：<p >

left：左对齐内容

right：右对齐内容

center：居中对齐内容

justify：对行进行伸展，这样每行都可以有相等的长度

换行标签：</br>

空格标签:（必须在英文状态下进行）<pre></pre> :可以保证空格和换行（输入什么样，浏览器展出什么样）

<hr/>水平线

属性：

             width：设置水平线宽度，可以像素或百分比

              color：设置水平线颜色

               align：设置水平线居中对齐

           noshade：设置水平线无阴影

文字斜体： <i></i>    <em></em>

加粗：<b></b>  <strong></strong>

下标：<sub>  上标：<sup>

下划线：<ins>   删除线：<del>
```



```HTML
<!DOCTYPE html>

<html>

<head>

<title>文字和段落标准</title>

<meta http-equiv="Content-Type "contect="text/html;charse=utf-8"/>

</head>

<body>

hello  html!

HTML是超文本标记语言！

</body>

</html>
```

###CSS样式（宽度，高度，颜色，字体）

####一·行内样式（弊端：太繁琐）

`<div style="width:200px;height:100px;
background:reds"></div>`
则可出现宽度200，高度100的红色盒子
####二·内部样式（其好处为可将同名盒子同时控制，其坏处为若更改仅能一个一个改）
```
<style>
  .div1{wiidth:150px;height:100px;backgound:red;}
</style>
<body>
  <div class="div1"></div>
</body>
```
####三·外部样式（可方便一次性更改）

```
<link href="style.css"rel="stylesheet"1>
href="sthle.css"
rel=“stylesheet"`
```

>####我们一般而言主要用外部样式

###JavaScript
#####JavaScript是目前唯一一个被广泛使用的给予原型继承的语言。

####一·什么是原型？
JavaScript中，万物皆对象！但对象也是有区别的。分为普通对象和函数对象。
Object Function是JS自带的函数对象
每个对象都有原型（null和undefined除外），可将它理解为对象的默认属性和方法。

####二·什么是原型链？
在JavaScript中，每个对象都有个指向它的原型（prototype）对象的内部链接。这个原型对象又有自己的原型，直到某个对象的原型为null为止（也就是不再有原型指向），组成这条链的最后一环，这种一级一级的链结构就称为原型链。
 
#####原型链继承的例子：
```HTML
function A （）{
 this.name="Nonentity"
}
A.prototype.getName=function(){
return this name
}
function B (){ this.age=18;
}
B.prototype=newA()
```






>#前端面试题  
####什么是Webpack？Webpack可理解为什么？
Webpack可看作是模块打包机，也是一个前端资源加载/打包工具。它相当于一个媒介，将多种静态资源js.css./ess转换成一个静态文件，减少了页面的请求次数。
（个人认为类似于搬家工人的作用，减少了主人所需花费的时间与精力）
####CSS属性display中的block，inline和inline-block概念和区别？
设置了inline-block属性的元素既拥有了block元素可以设置width和height的特性，又保持了inline元素不换行的特性。
内联对象inline给它设置height width是没用的，致使它变宽变大的原因是：内部元素的宽高“padding”。
inline对象的前后元素不单独占一行，其它紧随其后。
block可设置宽高，“block”前后元素中“block”单独占一行。
