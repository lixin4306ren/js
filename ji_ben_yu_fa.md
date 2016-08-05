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

## 数组
### 定义及赋值
#### 一维数组
```
var myarray=new Array(); //创建一个新的空数组
myarray[0]=66; //存储第1个人的成绩
myarray[1]=80; //存储第2个人的成绩
myarray[2]=90; //存储第3个人的成绩
myarray[3]=77; //存储第4个人的成绩
myarray[4]=59; //存储第5个人的成绩
```
或者
```
var myarray = new Array(66,80,90,77,59);//创建数组同时赋值
var myarray = [66,80,90,77,59];//直接输入一个数组（称 “字面量数组”）
```

#### 二维数组
方法一
```
var myarr=new Array();  //先声明一维 
for(var i=0;i<2;i++){   //一维长度为2
   myarr[i]=new Array();  //再声明二维 
   for(var j=0;j<3;j++){   //二维长度为3
   myarr[i][j]=i+j;   // 赋值，每个数组元素的值为i+j
   }
 }
```

方法二
```
var Myarr = [[0 , 1 , 2 ],[1 , 2 , 3, ]]
```


### 数组相关属性
```
myarray.length; //获得数组myarray的长度

```


## 操作符
算术操作符(+、-、*、/等)，＋＋， －－   
比较操作符(<、>、>=、<=等)，＝＝， !=   
逻辑操作符(&&、||、！)  


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

### for循环
```
<script type="text/javascript">
var num=1;
for (num=1;num<=6;num++)  //初始化值；循环条件；循环后条件值更新
{   document.write("取出第"+num+"个球<br />");
}
</script>
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

