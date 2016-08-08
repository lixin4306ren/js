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


