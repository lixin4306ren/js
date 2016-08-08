# superagent API介绍

http://www.jianshu.com/p/98b854322260  

轻量级HTTP模块，主要是用来充当 http 客户端，专注于处理服务器 / 客户端的 http 请求。

## 用法展示，和http模块区别

```
//superagent
var superagent = require('supeagent');
superagent.get('http://www.baidu.com').end(function(req, res){
				console.log(res.text);
			});

//http 
var http = require('http');
http.get('http://www.baidu.com', function(res){
    var html = "";
    res.on('data', function(chunk){
        html += chunk.toString();
    });
    res.on('end', function(){
        console.log(html);
    });
})
```


## 发起 HTTP 请求

我们常见的 HTTP 请求有 GET、POST、DELETE、HEAD 等，在发送请求时一般有下列两种方式：

```
//这里以 GET 举例，其他类似
//方法 1:
superagent.get('http://www.baidu.com').end(function(req, res){
	//do something
});

//方法 2:
superagent('GET', 'http://www.baidu.com').end(function(req, res){
	//do something
});

```

