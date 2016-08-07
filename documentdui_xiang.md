# document对象

每个载入浏览器的 HTML 文档都会成为 Document 对象。
Document 对象使我们可以从脚本中对 HTML 页面中的所有元素进行访问。

提示：Document 对象是 Window 对象的一部分，可通过 window.document 属性对其进行访问。

## Document 对象属性
| 属性 | 描述 |
| -- | -- |
| body | 提供对 `<body>` 元素的直接访问。 |
| cookie | 设置或返回与当前文档有关的所有 cookie|
| domain | 返回当前文档的域名|
| lastModified| 返回文档被最后修改的日期和时间|
| referrer| 返回载入当前文档的文档的 URL|
| title | 返回当前文档的标题|
| URL | 返回当前文档的 URL|
|images|返回对文档中所有 Image 对象引用|


## Document 对象方法

| 方法 | 描述|
| -- | -- |
| close()| 关闭用 document.open() 方法打开的输出流，并显示选定的数据。 |
| getElementById() | 返回对拥有指定 id 的第一个对象的引用。|
| getElementsByName()| 返回带有指定名称的对象集合。 |
| getElementsByTagName()| 返回带有指定标签名的对象集合。 |
|document.getElementsByClassName()|返回文档中所有指定类名的元素集合，作为 NodeList 对象|
| open()| 打开一个流，以收集来自任何 document.write() 或 document.writeln() 方法的输出。 |
| write()| 向文档写 HTML 表达式 或 JavaScript 代码。 |
| writeln()	| 等同于 write() 方法，不同的是在每个表达式之后写一个换行符。 |
|document.activeElement	|返回当前获取焦点元素|
|document.addEventListener()|向文档添加句柄|
|document.createElement()|创建元素节点|
|document.createAttribute()|创建一个属性节点|
|document.createTextNode()|创建文本节点|
|document.querySelector()|返回文档中匹配指定的CSS选择器的第一元素|


