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


## 常用属性
```
color
background-color
font-family（字体）
font-size（字体大小）
text-align:center; (文本对齐方式)
```

