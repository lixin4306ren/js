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

我们设置一个计时器，每隔100毫秒调用clock()函数，并将时间显示出来，代码如下:


```
<script type="text/javascript">
  var int=setInterval(clock, 100)
  function clock(){
    var time=new Date();
    document.getElementById("clock").value = time;
  }
</script>
```

