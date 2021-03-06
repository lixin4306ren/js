# 浏览器对象

## window对象
window对象是BOM的核心，window对象指当前的浏览器窗口。

window对象方法:
![](http://img.imooc.com/535483720001a54506670563.jpg)



## JavaScript 计时器

在JavaScript中，我们可以在设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行。  
计时器类型：  
一次性计时器：仅在指定的延迟时间之后触发一次。  
间隔性触发计时器：每隔一定的时间间隔就触发一次。  
计时器方法：  
![](http://img.imooc.com/56976e1700014fc504090143.jpg)

我们设置一个计时器，每隔 100 毫秒调用 clock() 函数,并显示时间。当点击按钮时，停止时间,代码如下:

```
<!DOCTYPE HTML>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>计时器</title>
<script type="text/javascript">
   function clock(){
      var time=new Date();                     
      document.getElementById("clock").value = time;
   }
// 每隔100毫秒调用clock函数，并将返回值赋值给i
     var i=setInterval("clock()",100);
</script>
</head>
<body>
  <form>
    <input type="text" id="clock" size="50"  />
    <input type="button" value="Stop" onclick="clearInterval(i)"  />
  </form>
</body>
</html>
```

## History 对象

History 对象属性

![](http://img.imooc.com/53548c030001759e05840068.jpg)


History 对象方法

![](http://img.imooc.com/53548c200001228206210123.jpg)

 
参数：

![](http://img.imooc.com/5354947e00011a9a06490153.jpg)


## Location对象

location用于获取或设置窗体的URL，并且可以用于解析URL。


location 对象属性：
![](http://img.imooc.com/5354b1d00001c4ec06220271.jpg)

location 对象方法:

![](http://img.imooc.com/5354b1eb00016a2405170126.jpg)

## Navigator对象

Navigator 对象包含有关浏览器的信息，通常用于检测浏览器与操作系统的版本。


![](http://img.imooc.com/5354cff70001428b06880190.jpg)

## screen对象
screen对象用于获取用户的屏幕信息。  
对象属性: 


![](http://img.imooc.com/5354d2810001a47706210213.jpg)


