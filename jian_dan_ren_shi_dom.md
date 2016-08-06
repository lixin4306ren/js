# 简单认识DOM

文档对象模型DOM（Document Object Model）定义访问和处理HTML文档的标准方法。DOM 将HTML文档呈现为带有元素、属性和文本的树结构（节点树）。

## 通过ID获取元素
```document.getElementById(“id”) ```

## 通过innerHTML获取或替换 HTML 元素的内容
```
<script type="text/javascript">
  var mychar= document.getElementById(“con”)          ;
  document.write("原标题:"+mychar.innerHTML+"<br>"); //输出原h2标签内容
  con.innerHTML = "nex text";
  document.write("修改后的标题:"+mychar.innerHTML); //输出修改后h2标签内容
</script>
```

## 改变 HTML 样式
HTML DOM 允许 JavaScript 改变 HTML 元素的样式。如何改变 HTML 元素的样式呢？

改变 <p> 元素的样式，将颜色改为红色，字号改为20,背景颜色改为蓝：
```
<p id="pcon">Hello World!</p>
<script>
   var mychar = document.getElementById("pcon");
   mychar.style.color="red";
   mychar.style.fontSize="20";
   mychar.style.backgroundColor ="blue";
</script>
```

## 显示和隐藏
`display`属性

```
    <script type="text/javascript"> 
        function hidetext()  
		{  
		var mychar = document.getElementById("con");
        mychar.style.display =  "none";
        
		}  
		function showtext()  
		{  
		var mychar = document.getElementById("con");
        mychar.style.display = "block";
		}
    </script> 
```

## 控制类名
`object.className = classname`

## 结构
HTML文档可以说由节点构成的集合，DOM节点有:

1. 元素节点：上图中`<html>`、`<body>`、`<p>`等都是元素节点，即标签。

2. 文本节点:向用户展示的内容，如`<li>...</li>`中的JavaScript、DOM、CSS等文本。

3. 属性节点:元素属性，如`<a>`标签的链接属性href="http://www.imooc.com"。

![](http://img.imooc.com/5375ca7e0001dd8d04830279.jpg)

### 节点属性:

![](http://img.imooc.com/5375c953000117ee05240129.jpg)


### 遍历节点树:
![](http://img.imooc.com/53f17a6400017d2905230219.jpg)

### DOM操作:

![](http://img.imooc.com/538d29da000152db05360278.jpg)

注意:前两个是document方法。