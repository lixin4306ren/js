# 内建对象
JavaScript 提供多个内建对象，比如 String、Date、Array 等等。
## 日期对象
```
var mydate=new Date();//当前时间2014年3月6日
document.write(mydate+"<br>");//输出当前时间
document.write(mydate.getFullYear()+"<br>");//输出当前年份
mydate.setFullYear(81); //设置年份
document.write(mydate+"<br>"); //输出年份被设定为 0081年。
```

Date对象中处理时间和日期的常用方法：

![](http://img.imooc.com/555c650d0001ae7b04180297.jpg)

## 字符串对象
```
var mystr = new String()   //定义
mystr="I love JavaScript!" //赋值
mystr.length               //长度
mystr.toUpperCase()        //大写
mystr.charAt(2));          //输出mystr的第三个元素
str.indexOf("I")           //字符串里字母'I'首次出现的位置
mystr.split("-",1)         //字符串按'-' split
mystr.substring(startPos,stopPos) //字符串提取 （按位置）
mystr.substr(stratPos,length)     //还是字符串提取 （按长度）
```

## Math固有对象
用来进行数学运算  
Math 对象属性

![](http://img.imooc.com/532fe7cf0001e7b505170269.jpg)

Math 对象方法

![](http://img.imooc.com/532fe841000174db05160622.jpg)

## 数组对象
数组方法：  
![](http://img.imooc.com/533295ab0001dead05190599.jpg)

示例，数组连接：
```
<script type="text/javascript">
  var mya1= new Array("hello!")
  var mya2= new Array("I","love");
  var mya3= new Array("JavaScript","!");
  var mya4=mya1.concat(mya2,mya3);
  document.write(mya4);
</script>
```





