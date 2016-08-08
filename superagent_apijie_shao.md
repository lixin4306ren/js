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

## 设置请求头
```
方法 1:单独设置
superagent.get('http://www.baidu.com').set('Referer', 'http://www.example.com').set('Accept', 'text/json');
			
方法 2:一起设置
superagent.get('http://www.baidu.com').set({
				'Referer': 'http://www.example.com',
				'Accept': 'text/json'
			});			
```

## 设置请求主体
### GET 请求参数
我们可以通过 query() 方法来使 URL 后面带上参数
```
方法 1:
superagent.get('/').query({name:'lindz'}).query({age:21})

方法 2:
superagent.get('/').query('name=lindz').query('age=21');
	
方法 3:
superagent.get('/').query({name:'lindz', age: 21});
			
方法 4:
superagent.get('/').query('name=lindz&age=21');

```

### POST 请求主体
我们可以通过 send() 方法来发送 POST 请求主体

```
//比如传递 json 数据
superagent.post('/').send('{"name":"lindz","age":21');
      		
//或者
superagent.post('/').send({name:"lindz"}).send({age:21})
```

## HTTP 响应属性

1. res.text 包含被解析的响应数据 (如：html)
2. res.body 包含解析后的数据，目前只支持三种格式: (application/x-www-form-urlencoded、application/json 和 multipart/form-data)
3. res.header 响应头，是一个对象
4. res.type & res.charset 类型和编码格式
5. res.status状态码

## 中断请求 & 暂停请求
分别对应 req.abort() 和 req.timeout(ms);
