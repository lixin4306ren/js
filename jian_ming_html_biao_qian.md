# 简明html标签


## 文本相关
### 段落`<p></p>`
```
<p>This is a paragraph</p>
<p>This is another paragraph</p>
```
### 换行 `<br>`  
### 水平线 `<hr/>`
效果如下：  
<hr>

## 格式

### 黑体

`<b>This text is bold</b>`
<b>This text is bold</b>

### 大号字体  
`<big>This text is big</big>` <big>This text is big</big>

### 小号字体
`<small>This text is small</small>` <small>This text is small</small>

### 斜体
`<i>This text is italic</i>`
<i>This text is italic</i>

### 下标
```
This text contains
<sub>subscript</sub>
```
This text contains
<sub>subscript</sub>

### 上标
```
This text contains
<sup>superscript</sup>
```
This text contains
<sup>superscript</sup>


## 链接
`<a href="http://www.w3school.com.cn/">Visit W3School</a>`

<a href="http://www.w3school.com.cn/">Visit W3School</a>

target属性  
`<a href="http://www.w3school.com.cn/" target="_blank">Visit W3School!</a>`

name 属性  
```
<a name="tips">基本的注意事项 - 有用的提示</a>
<a href="#tips">有用的提示</a>
```
## 插入图片
`<img src="url" />`

## 列表
### 无序列表
```
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
```

<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>

### 有序列表
```
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```

<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>

### 自定义列表
```
<dl>
<dt>Coffee</dt>
<dd>Black hot drink</dd>
<dt>Milk</dt>
<dd>White cold drink</dd>
</dl>
```

<dl>
<dt>Coffee</dt>
<dd>Black hot drink</dd>
<dt>Milk</dt>
<dd>White cold drink</dd>
</dl>


## HTML 块元素
大多数 HTML 元素被定义为块级元素或内联元素。
编者注：“块级元素”译为 block level element，“内联元素”译为 inline element。
块级元素在浏览器显示时，通常会以新行来开始（和结束）。
例子：
` <h1>, <p>, <ul>, <table>`  

HTML `<div>` 元素是块级元素，它是可用于组合其他 HTML 元素的容器。
`<div>` 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。
如果与 CSS 一同使用，`<div>` 元素可用于对大的内容块设置样式属性。
`<div>` 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 `<table>` 元素进行文档布局不是表格的正确用法。`<table>` 元素的作用是显示表格化的数据。  


## HTML 内联元素
内联元素在显示时通常不会以新行开始。
例子：`<b>, <td>, <a>, <img>`  

HTML `<span>` 元素是内联元素，可用作文本的容器。
`<span>` 元素也没有特定的含义。
当与 CSS 一同使用时，`<span>` 元素可用于为部分文本设置样式属性。








## 注释
`<!-- This is a comment -->`




