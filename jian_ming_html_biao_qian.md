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

### form的属性
#### action属性
action 属性规定当提交表单时，向何处发送表单数据。

可能的值：
1. 绝对 URL - 指向其他站点（比如 src="www.example.com/example.htm"）
2. 相对 URL - 指向站点内的文件（比如 src="example.htm"）


#### method属性
浏览器使用 method 属性设置的方法将表单中的数据传送给服务器进行处理。共有两种方法：`POST` 方法和 `GET`方法。  

如果采用 `POST` 方法，浏览器将会按照下面两步来发送数据。首先，浏览器将与 action 属性中指定的表单处理服务器建立联系，一旦建立连接之后，浏览器就会按分段传输的方法将数据发送给服务器。
在服务器端，一旦 `POST` 样式的应用程序开始执行时，就应该从一个标志位置读取参数，而一旦读到参数，在应用程序能够使用这些表单值以前，必须对这些参数进行解码。用户特定的服务器会明确指定应用程序应该如何接受这些参数。  

另一种情况是采用 `GET` 方法，这时浏览器会与表单处理服务器建立连接，然后直接在一个传输步骤中发送所有的表单数据：浏览器会将数据直接附在表单的 action URL 之后。这两者之间用问号进行分隔。

一般浏览器通过上述任何一种方法都可以传输表单信息，而有些服务器只接受其中一种方法提供的数据。可以在 `<form>` 标签的 `method`属性中指明表单处理服务器要用方法来处理数据，使 `POST` 还是 `GET`。


`POST` 还是 `GET`？
如果表单处理服务器既支持 POST 方法又支持 GET 方法，那么你该选择哪种方法呢？下面是有关这方面的一些规律：  

如果希望获得最佳表单传输性能，可以采用 GET 方法发送只有少数简短字段的小表单。
一些服务器操作系统在处理可以立即传递给应用程序的命令行参数时，会限制其数目和长度，在这种情况下，对那些有许多字段或是很长的文本域的表单来说，就应该采用 POST 方法来发送。
如果你在编写服务器端的表单处理应用程序方面经验不足，应该选择 GET 方法。如果采用 POST 方法，就要在读取和解码方法做些额外的工作，也许这并不很难，但是也许你不太愿意去处理这些问题。
如果安全性是个问题，那么我们建议选用 POST 方法。GET 方法将表单参数直接放在应用程序的 URL 中，这样网络窥探者可以很轻松地捕获它们，还可以从服务器的日志文件中进行摘录。如果参数中包含了信用卡帐号这样的敏感信息，就会在不知不觉中危及用户的安全。而 POST 应用程序就没有安全方面的漏洞，在将参数作为单独的事务传输给服务器进行处理时，至少还可以采用加密的方法。  

如果想在表单之外调用服务器端的应用程序，而且包括向其传递参数的过程，就要采用 GET 方法，因为该方法允许把表单这样的参数包括进来作为 URL 的一部分。而另一方面，使用 POST 样式的应用程序却希望在 URL 后还能有一个来自浏览器额外的传输过程，其中传输的内容不能作为传统 `<a>` 标签的内容。


<hr>

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

### 提交按钮 type="submit"
```
<form name=""><input type="submit" value="确定" /></form> 
```
## 注释
`<!-- This is a comment -->`





