# 有用的函数
## JSON
1. `JSON.stringify`将一个值转为字符串  

```
JSON.stringify('abc') // ""abc""
JSON.stringify(1) // "1"
JSON.stringify(false) // "false"
JSON.stringify([]) // "[]"
JSON.stringify({}) // "{}"
JSON.stringify([1, "false", false]) // '[1,"false",false]'
JSON.stringify({ name: "张三" }) // '{"name":"张三"}'
JSON.stringify({
  f: function(){},
  a: [ function(){}, undefined ] //值不能是函数
});

```

2. `JSON.parse()`将JSON字符串转化成对象。

```
var o = JSON.parse('{"name": "张三"}');
o.name // 张三
```

## Number()
Converts an object's value to a number
```
var x1 = true;
var x2 = false;
var x3 = new Date();
var x4 = "999";
var x5 = "999 888";

var n = 
Number(x1) + "<br>" + 
Number(x2) + "<br>" + 
Number(x3) + "<br>" + 
Number(x4) + "<br>" + 
Number(x5);

```
## String()
Converts an object's value to a string
```
var x1 = Boolean(0);
var x2 = Boolean(1);
var x3 = new Date();
var x4 = "12345";
var x5 = 12345;

var res =
String(x1) + "<br>" +
String(x2) + "<br>" +
String(x3) + "<br>"	+
String(x4) + "<br>" +
String(x5);
```
## parseFloat()
Parses a string and returns a floating point number
```
var a = parseFloat("10") + "<br>";
var b = parseFloat("10.00") + "<br>";
var c = parseFloat("10.33") + "<br>";
var d = parseFloat("34 45 66") + "<br>";
var e = parseFloat(" 60 ") + "<br>";
var f = parseFloat("40 years") + "<br>";
var g = parseFloat("He was 40") + "<br>";

var n = a + b + c + d + e + f + g;
```
## parseInt()
Parses a string and returns an integer
```
var a = parseInt("10") + "<br>";
var b = parseInt("10.00") + "<br>";
var c = parseInt("10.33") + "<br>";
var d = parseInt("34 45 66") + "<br>";
var e = parseInt(" 60 ") + "<br>";
var f = parseInt("40 years") + "<br>";
var g = parseInt("He was 40") + "<br>";

var h = parseInt("10",10)+ "<br>";
var i = parseInt("010")+ "<br>";
var j = parseInt("10",8)+ "<br>";
var k = parseInt("0x10")+ "<br>";
var l = parseInt("10",16)+ "<br>";

var n = a + b + c + d + e + f + g + "<br>" + h + i + j + k +l;
```
## eval()
Evaluates a string and executes it as if it was script code
```
var x = 10;
var y = 20;
var a = eval("x * y") + "<br>";
var b = eval("2 + 2") + "<br>";
var c = eval("x + 17") + "<br>";

var res = a + b + c;
```
