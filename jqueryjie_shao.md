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

### 两者比较
### jQuery   
1. 难用  
　　要想拿到一个对象，要写很长的代码比如`document.getElementById('xxx')`,但是如果是Jquery的话可以直接`$('#xxx')`。

2. 存在兼容性问题  
　　采用DOM操作的时候往往需要兼容IE和非IE浏览器问题。

3. 功能太少，不能与时俱进  
　 DOM可以获取第一个子元素却不能获取第二个子元素，而且有时候还要搞一个判断语句，很麻烦。

#### Jquery API
1. 兼容性好
2. API友好  
　比如在做事件监听的时候DOM需要`addEventListener`和`attachEvent`等等；而Jquery直接为我们封装为`on()`,`bind()`。 还有就是它可以链式操作。
3. 功能强大，与时俱进  

### 什么时候适合用Jquery?
![](http://upload-images.jianshu.io/upload_images/1181204-61c2cd0d2b1bcd8f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### Jquery对象与DOM对象可以相互转换
![](http://upload-images.jianshu.io/upload_images/1181204-94835b6421a17dd3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### Jquery对象与DOM对象的调用方法不一样
![](http://upload-images.jianshu.io/upload_images/1181204-969f05e669d83e23.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

DOM对象只能用DOM API调用，Jquery对象只能用Jquery API来调用。

## jQuery实现动画
### show / hide
直接以无参数形式调用show()和hide()，会显示和隐藏DOM元素。但是，只要传递一个时间参数进去，就变成了动画：

```
var div = $('#test-show-hide');
div.hide(3000); // 在3秒钟内逐渐消失
var div = $('#test-show-hide');
div.show('slow'); // 在0.6秒钟内逐渐显示
```
toggle()方法则根据当前状态决定是show()还是hide()。

### slideUp/slideDown
你可能已经看出来了，show()和hide()是从左上角逐渐展开或收缩的，而slideUp()和slideDown()则是在垂直方向逐渐展开或收缩的。

slideUp()把一个可见的DOM元素收起来，效果跟拉上窗帘似的，slideDown()相反，而slideToggle()则根据元素是否可见来决定下一步动作：
```
var div = $('#test-slide');
div.slideUp(3000); // 在3秒钟内逐渐向上消失
```

