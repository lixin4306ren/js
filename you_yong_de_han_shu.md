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

## parseFloat()
Parses a string and returns a floating point number

## parseInt()
Parses a string and returns an integer

## eval()
Evaluates a string and executes it as if it was script code
