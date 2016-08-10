# 数组

## 定义及赋值
### 一维数组
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

### 二维数组
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

## 遍历

`forEach`
```
var fruits = ["Apple", "Banana"];
fruits.forEach(function (item, index, array) {
  console.log(item, index);
});
```

## 操作
### 添加元素到数组的末尾
```
var newLength = fruits.push("Orange");
```

### 删除数组末尾的元素
```
var last = fruits.pop();
```
### 删除数组前面的元素
```
var first = fruits.shift(); // remove Apple from the front
```
### 添加到数组的前面
```
var newLength = fruits.unshift("Strawberry") // add to the front
```

### 找到某个元素在数组中的索引
```
fruits.push("Mango");
// ["Strawberry", "Banana", "Mango"]

var pos = fruits.indexOf("Banana");
// 1
```
### 通过索引删除某个元素

```
var removedItem = fruits.splice(pos, 1); // this is how to remove an item
```

### 计算数组长度
```
myarray.length; //获得数组myarray的长度

```

## 数组对象方法
```
Array.from() 
从类数组或者迭代对象（iterable object）中创建一个新的数组实例。
Array.isArray()
假如一个变量是数组则返回true，否则返回false。
Array.observe() 
异步监视数组的修改情况，与对象的Object.observe()方法类似。该方法会根据修改事件发生顺序提供一个修改流。
Array.of() 
创建一个有可变数量的参数的新的数组实例，无论参数有多少数量，而且可以是任意类型。
```

## 数组实例
所有数组实例继承自 `Array.prototype`。`Array` 构造函数的原型对象是可修改的，其会影响所有的数组实例。

方法：  
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

## map/reduce方法

## filter方法
传入函数过滤数组
```
var arr = [1, 2, 4, 5, 6, 9, 10, 15];
var r = arr.filter(function (x) {
    return x % 2 !== 0;
});
r; // [1, 5, 9, 15]
```

## sort排序
```
// 无法理解的结果:
[10, 20, 1, 2].sort(); // [1, 10, 2, 20]
```

这是因为Array的`sort()`方法默认把所有元素先转换为String再排序，结果'10'排在了'2'的前面，因为字符'1'比字符'2'的ASCII码小。

幸运的是，sort()方法也是一个高阶函数，它还可以接收一个比较函数来实现自定义的排序。

要按数字大小排序，我们可以这么写：

```
var arr = [10, 20, 1, 2];
arr.sort(function (x, y) {
    if (x < y) {
        return -1;
    }
    if (x > y) {
        return 1;
    }
    return 0;
}); // [1, 2, 10, 20]

```

