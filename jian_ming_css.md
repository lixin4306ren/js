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
.center {text-align:center;}
```


## 常用属性
```
color
background-color
font-family（字体）
font-size（字体大小）
text-align:center; (文本对齐方式)
```

