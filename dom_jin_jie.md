# DOM

## 三种获得节点的方法
`getElementByID`有唯一性  
`getElementsByName` 返回的是数组  
`getElementsByTagName` 返回的是数

## 节点的三个重要属性
在文档对象模型 (DOM) 中，每个节点都是一个对象。DOM 节点有三个重要的属性 ：

1. nodeName : 节点的名称

2. nodeValue ：节点的值

3. nodeType ：节点的类型

### nodeName 属性: 节点的名称，是只读的。

1. 元素节点的 nodeName 与标签名相同
2. 属性节点的 nodeName 是属性的名称
3. 文本节点的 nodeName 永远是 #text
4. 文档节点的 nodeName 永远是 #document

### nodeValue 属性：节点的值

1. 元素节点的 nodeValue 是 undefined 或 null
2. 文本节点的 nodeValue 是文本自身
3. 属性节点的 nodeValue 是属性的值

### nodeType 属性: 节点的类型，是只读的。  
以下常用的几种结点类型:

| 元素类型 | 节点类型 |
| -- | -- |
| 元素 | 1 |
| 属性 | 2 |
| 文本 | 3 |
| 注释 | 8 |
| 文档 | 9 |

  
## 获得和设置元素节点的属性

`elementNode.getAttribute(name)`  

`elementNode.setAttribute(name,value)`  
## 访问子节点,父节点,兄弟节点

访问选定元素节点下的所有子节点的列表，返回的值可以看作是一个数组，他具有length属性。  
`elementNode.childNodes`  

注意:

1. IE全系列、firefox、chrome、opera、safari兼容问题

2. 节点之间的空白符，在firefox、chrome、opera、safari浏览器是文本节点，所以IE是3，其它浏览器是7，如下图所示:

![](http://img.mukewang.com/538d2b8a000163e303430127.jpg)

如果把代码改成这样:

`<ul><li>javascript</li><li>jQuery</li><li>PHP</li</ul>`

运行结果:（IE和其它浏览器结果是一样的）


### 访问子结点的第一和最后项
`node.firstChild`  
`node.lastChild`  
说明：与`elementNode.childNodes[elementNode.childNodes.length-1]`是同样的效果。

### 获取指定节点的父节点

`elementNode.parentNode`  
注意:父节点只能有一个。

### 访问兄弟节点
1. `nextSibling` 属性可返回某个节点之后紧跟的节点（处于同一树层级中）。

2. `previousSibling` 属性可返回某个节点之前紧跟的节点（处于同一树层级中）。  

说明：如果无此节点，则该属性返回 null。


## 其他节点操作

### 创建元素节点createElement
`document.createElement(tagName)`  


### 插入节点appendChild(newnode)

```
<ul id="test">
  <li>JavaScript</li>
  <li>HTML</li>
</ul> 
 
<script type="text/javascript">
  var otest = document.getElementById("test");  
  var newnode=document.createElement("li");
  newnode.innerHTML="Perl";
  otest.appendChild(newnode);
</script> 
```


### 插入节点insertBefore()

`insertBefore(newnode, node)` 方法可在已有的子节点前插入一个新的子节点。


### 删除节点removeChild()

`nodeObject.removeChild(node)`  

```
<div id="content">
  <h1>html</h1>
  <h1>php</h1>
  <h1>javascript</h1>
  <h1>jquery</h1>
  <h1>java</h1>
</div>

<script type="text/javascript">

function clearText() {
  var content=document.getElementById("content");
  var num=content.childNodes.length;
  for(var i=0;i<num;i++){
      tmp=content.removeChild(content.childNodes[0]);//每次删除第一个节点    
  }  
}
</script>
```

### 替换元素节点replaceChild()

`node.replaceChild (newnode,oldnew )`  

注意: 

1. 当 oldnode 被替换时，所有与之相关的属性内容都将被移除。 

2. newnode 必须先被建立。 

只有父结点才能调用  replaceChild(newnode,oldnode).这个方法，所以，要想替换当前结点的内容或者属性，那么首先得获得父节点，才可以操作，这就是为什么 oldnode.parentNode.replaceChild(newnode,oldnode); 这句代码的写法。

```
<div><b id="oldnode">JavaScript</b>是一个很常用的技术，为网页添加动态效果。</div>
  <a href="javascript:replaceMessage()"> 将加粗改为斜体</a>
  
    <script type="text/javascript">
      function replaceMessage(){
       var test = document.getElementById("oldnode");
       var newnode=document.createElement("i");
       newnode.innerHTML="JavaScript";
       oldnode.parentNode.replaceChild(newnode,oldnode);
		   
       }    
  </script>
```









