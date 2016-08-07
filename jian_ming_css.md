# 简明CSS

## CSS引入html
CSS 可以通过以下方式添加到HTML中:  
1. 内联样式- 在HTML元素中使用"style" 属性  
`<p style="color:blue;margin-left:20px;">This is a paragraph.</p>`  
2. 内部样式表 -在HTML文档头部 `<head>` 区域使用`<style>` 元素 来包含CSS  
```
<head>
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
</head>
```
3. 外部引用 - 使用外部 CSS 文件
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

## 语法
CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:
![](http://www.runoob.com/images/selector.gif)

CSS声明总是以分号(;)结束，声明组以大括号({})括起来，为了让CSS可读性更强，一般每行只描述一个属性。

CSS 注释
```
/*这是个注释*/
p
{
text-align:center;
/*这是另一个注释*/
color:black;
font-family:arial;
}
```

## CSS Id 和 Class
### id 选择器
id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。
HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 `#` 来定义。
以下的样式规则应用于元素属性 id="para1":
```
#para1
{
text-align:center;
color:red;
}
```
### class 选择器

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。
class 选择器在HTML中以class属性表示, 在 CSS 中，类选择器以一个点`.`号显示：
在以下的例子中，所有拥有 center 类的 HTML 元素均为居中。

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<style>
.test
{
	text-align:center;
}
</style>
</head>

<body>
<h1 class="test">标题居中</h1>
<p class="test">段落居中。</p> 
</body>
</html>
```
你也可以指定特定的HTML元素使用class。
在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<style>
p.center
{
	text-align:center;
}
</style>
</head>

<body>
<h1 class="center">This heading will not be affected</h1>
<p class="center">This paragraph will be center-aligned.</p> 
</body>
</html>
```

## 常用属性

### 背景
```
background-color
background-image
background-repeat
background-position
```
### 文字
```
color
font-family（字体）
font-size（字体大小）
text-align:center; (文本对齐方式)
text-decoration:none; 从设计的角度看 text-decoration属性主要是用来删除链接的下划线。
text-transform:uppercase;
text-indent:50px; 文本缩进属性是用来指定文本的第一行的缩进。
word-spacing 设置字间距
```

### 链接样式
1. a:link - 正常，未访问过的链接  
2. a:visited - 用户已访问过的链接  
3. a:hover - 当用户鼠标放在链接上时  
4. a:active - 链接被点击的那一刻  

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<style>
a:link {color:#FF0000;}    /* unvisited link */
a:visited {color:#00FF00;} /* visited link */
a:hover {color:#FF00FF;}   /* mouse over link */
a:active {color:#0000FF;}  /* selected link */
</style>
</head>

<body>
<p><b><a href="/css/" target="_blank">这是一个链接</a></b></p>
<p><b>注意：</b> a:hover 必须在 a:link 和 a:visited 之后，需要严格按顺序才能看到效果。</p>
<p><b>注意：</b> a:active 必须在 a:hover 之后。</p>
</body>
</html>
```

### CSS边框
#### border-style
```
dotted: dotted:定义一个点线框
dashed: 定义一个虚线框
solid: 定义实线边界
double: 定义两个边界。 两个边界的宽度和border-width的值相同
groove: 定义3D沟槽边界。效果取决于边界的颜色值
ridge: 定义3D脊边界。效果取决于边界的颜色值
inset:定义一个3D的嵌入边框。效果取决于边界的颜色值
outset: 定义一个3D突出边框。 效果取决于边界的颜色值
```
### border-radius
#### border-width
#### border-color

### 尺寸
```
height	设置元素的高度。
line-height	设置行高。
max-height	设置元素的最大高度。
max-width	设置元素的最大宽度。
min-height	设置元素的最小高度。
min-width	设置元素的最小宽度。
width	设置元素的宽度。
```
### Display(显示) 与 Visibility（可见性）
```
h1.hidden {visibility:hidden;}
h1.hidden {display:none;}
```





