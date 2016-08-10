# 基本语法

## 变量
```
var myname = 8;
```


变量名字区分大小写，必须以字母、下划线或美元符号开头，后面可以跟字母、下划线、美元符号和数字。
> 正确:           
    mysum            
    _mychar         
    $numa1          



## 操作符
算术操作符(+、-、*、/等)，＋＋， －－   
比较操作符(<、>、>=、<=等)，＝＝， !=   
逻辑操作符(&&、||、！)  

==, ===, !=, !==  
这里有一点要解释，当这个逻辑运算符长度为 2 的时候（==, !=），只是判断外在的值是不是一样的，而不会判断类型。如
```
var a = 1, b = "1";
console.log(a == b); // true

var a = 1, b = "1";
console.log(a === b); // false
```

`typeof`判读变量类型  
```
function foo() {}

var a = 0;
var b = '嘘~蛋花汤在睡觉。';
var c = 1.0;
var d = foo;
var e = { "a" : a };
var f = [ 1, 2, 3 ];
var g = null;
var h = undefined;

console.log(typeof a);
console.log(typeof b);
console.log(typeof c);
console.log(typeof d);
console.log(typeof e);
console.log(typeof f);
console.log(typeof g);
console.log(typeof h);
```


## 判断
### if () else {}

```
<script type="text/javascript">
   var myage = 18;
   if(myage>=18)  //myage>=18是判断条件
   { document.write("你是成年人。");}
   else  //否则年龄小于18
   { document.write("未满18岁，你不是成年人。");}
</script>
```

### 多重判断
```
if(条件1)
{ 条件1成立时执行的代码}
else  if(条件2)
{ 条件2成立时执行的代码}
...
else  if(条件n)
{ 条件n成立时执行的代码}
else
{ 条件1、2至n不成立时执行的代码}
```

## 循环
### for循环
```
<script type="text/javascript">
var num=1;
for (num=1;num<=6;num++)  //初始化值；循环条件；循环后条件值更新
{   document.write("取出第"+num+"个球<br />");
}
</script>
```

还有类似于hash的  
```
var foo = {
    "hello"     : "world",
    "node"      : "js",
    "blahblah"  : "bar"
};
for(var key in foo) {
    console.log(key + ": " + foo[key]);
}
```


### while循环
```
<script type="text/javascript">
var num=0;  //初始化值
while (num<=6)   //条件判断
{
  document.write("取出第"+num+"个球<br />");
  num=num+1;  //条件值更新
}
</script>
```

### Do...while循环
```
<script type="text/javascript">
   num= 1;
   do
   {
     document.write("数值为:" +  num+"<br />");
     num++; //更新条件
   }
   while (num<=5)
</script>
```

### 循环控制
退出循环`break`  
跳过本次循环`continue`



## 函数 
### 定义函数
```
function add2(a,b){
   var sum = a + b;
   alert(sum(2,3));
}
```

### 调用函数
第一种情况:在<script\>标签内调用。
```
  <script type="text/javascript">
    function add2()
    {
         sum = 1 + 1;
         alert(sum);
    }
  add2();//调用函数，直接写函数名。
</SCRIPT>
```

第二种情况:在HTML文件中调用，如通过点击按钮后调用定义好的函数。
```
<html>
<head>
<script type="text/javascript">
   function add2()
   {
         sum = 5 + 6;
         alert(sum);
   }
</script>
</head>
<body>
<form>
<input type="button" value="click it" onclick="add2()">  //按钮,onclick点击事件，直接写函数名
</form>
</body>
</html>
```
### 函数内部的关键字`arguments`
JavaScript还有一个免费赠送的关键字arguments，它只在函数内部起作用，并且永远指向当前函数的调用者传入的所有参数。  
利用arguments，你可以获得调用者传入的所有参数。也就是说，即使函数不定义任何参数，还是可以拿到参数的值：
```
function abs() {
    if (arguments.length === 0) {
        return 0;
    }
    var x = arguments[0];
    return x >= 0 ? x : -x;
}

abs(); // 0
abs(10); // 10
abs(-9); // 9
```

## 输出内容
### 页面输入
`document.write()`
### 跳出警告窗
`alert()`
### 确认对话框
`confirm()`
### 询问对话框
`prompt(str1, str2)`
### 打开窗口和关闭窗口
例如: 打开 http://www.imooc.com 网站，大小为300px \* 200px，无菜单，无工具栏，无状态栏，有滚动条窗口：
```
<script type="text/javascript"> window.open('http://www.imooc.com','_blank','width=300,height=200,menubar=no,toolbar=no, status=no,scrollbars=yes')
</script>
```
例如:关闭新建的窗口。
```
<script type="text/javascript">
   var mywin=window.open('http://www.imooc.com'); //将新打的窗口对象，存储在变量mywin中
   mywin.close();
</script>
```

