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


## 判断
```
<script type="text/javascript">
   var myage = 18;
   if(myage>=18)  //myage>=18是判断条件
   { document.write("你是成年人。");}
   else  //否则年龄小于18
   { document.write("未满18岁，你不是成年人。");}
</script>
```
## 定义函数
```
function add2(){
   var sum = 3 + 2;
   alert(sum);
}
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
## 认识DOM
文档对象模型DOM（Document Object Model）定义访问和处理HTML文档的标准方法。DOM 将HTML文档呈现为带有元素、属性和文本的树结构（节点树）。

### 通过ID获取元素
```document.getElementById(“id”) ```

### 通过innerHTML获取或替换 HTML 元素的内容
```
<script type="text/javascript">
  var mychar= document.getElementById(“con”)          ;
  document.write("原标题:"+mychar.innerHTML+"<br>"); //输出原h2标签内容
  con.innerHTML = "nex text";
  document.write("修改后的标题:"+mychar.innerHTML); //输出修改后h2标签内容
</script>
```

### 改变 HTML 样式
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

### 显示和隐藏
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

### 控制类名
`object.className = classname`

