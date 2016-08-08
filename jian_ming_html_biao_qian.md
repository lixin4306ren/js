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


## 表单和输入
表单是一个包含表单元素的区域。
表单元素是允许用户在表单中（比如：文本域、下拉列表、单选框、复选框等等）输入信息的元素。
表单使用表单标签`<form>`定义。

```
<form>
...
  input 元素
...
</form>
```

多数情况下被用到的表单标签是输入标签`<input>`。输入类型是由类型属性（type）定义的。大多数经常被用到的输入类型如下：

### 文本域（Text Fields）type="text"
```
<form>
First name: 
<input type="text" name="firstname" />
<br />
Last name: 
<input type="text" name="lastname" />
</form>
```

### 单选按钮（Radio Buttons）type="radio"
```
<form>
<input type="radio" name="sex" value="male" /> Male
<br />
<input type="radio" name="sex" value="female" /> Female
</form>
```
### 复选框（Checkboxes）type="checkbox"
```
<form>
<input type="checkbox" name="bike" />
I have a bike
<br />
<input type="checkbox" name="car" />
I have a car
</form>
```

### 下拉菜单
```
<form>
<select name="cars">
<option value="volvo">Volvo</option>
<option value="saab">Saab</option>
<option value="fiat">Fiat</option>
<option value="audi">Audi</option>
</select>
</form>
```


### 多行文本框
```
<textarea rows="10" cols="30">
The cat was playing in the garden.
</textarea>
```

### 按钮 type="button"
```
<form>
<input type="button" value="Hello world!">
</form>
```

### label标签
label 元素不会向用户呈现任何特殊效果。不过，它为鼠标用户改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。
```
<form>
  <label for="male">Male</label>
</form>
```


## 注释
`<!-- This is a comment -->`





