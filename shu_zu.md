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




## 数组相关属性
```
myarray.length; //获得数组myarray的长度

```


