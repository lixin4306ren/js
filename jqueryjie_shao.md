# jQuery介绍

jQuery简单易用，容易上手。拥有轻量级的库，强大的选择器，出色的DOM操作，各种事件处理，兼容性解决方案等等特性。

## 初识jQuery
`$()`，美元符号，这个是jQuery的工厂函数。能做选择器来用，也能用来创建节点。示例代码中的`$(“button”)`就是选中下面文档里`<button></button>`这个节点。同理，`$(“#box”)`是选中ID为box的节点。这里括号里面的选择方法和CSS是一样的。Click还有append就是jQuery的一系列方法中的两个。前者是监测点击事件，后者是用来向HTML中添加字符串或者各种元素。

```

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
	"http://www.w3.org/TR/html4/loose.dtd">
<html>
	<head>
		<title>基本示例</title>
		<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
		<script type="text/javascript" src="jquery.js"></script>
		<script type="text/javascript">
			$(document).ready(function(){
				$("button").click(function(){
					$("#box").append("OK! ");
				});
			});
		</script>
	</head>
	<body>
		<button>It works!</button>
        <p>点击这个按钮，会在下面添加“OK！”</p>
		<div id="box"></div>
	</body>
	
</html>
```

## DOM对象/API vs. jQuery对象/API

为什么要用jQuery？   
1. 难用  
　　要想拿到一个对象，要写很长的代码比如`document.getElementById('xxx')`,但是如果是Jquery的话可以直接`$('#xxx')`。

2. 存在兼容性问题  
　　采用DOM操作的时候往往需要兼容IE和非IE浏览器问题。

3. 功能太少，不能与时俱进  
　 DOM可以获取第一个子元素却不能获取第二个子元素，而且有时候还要搞一个判断语句，很麻烦。

Jquery API优势  
1. 兼容性好
2. API友好  
　比如在做事件监听的时候DOM需要`addEventListener`和`attachEvent`等等；而Jquery直接为我们封装为`on()`,`bind()`。 还有就是它可以链式操作。

