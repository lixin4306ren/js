# cheerio
http://blog.gejiawen.com/2015/08/17/read-cheerio-doc/
node.js操作dom的模块，快速，灵活，在服务器端使用的jQuery。

## 加载html页面
```
var cheerio = require('cheerio');
var $ = cheerio.load('<div><p>一行文字</p><img id = "img1" src="/a.jpg"/><img src="/b.jpg"/></div>');
```

## 操作DOM
```
var p = $('p').text();
var img = $('#img1').attr('src');
console.log(p);
console.log(img);
```


## each函数的用法
```
$('img').each(function (i, item) {
    var src = $(item).attr('src'); //注意这里的item是用$处理为cheerio对象
    console.log(src);
});
```

## 