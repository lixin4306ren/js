# node.js操作dom模块 cheerio
快速，灵活，在服务器端使用的jQuery。

## 测试你的服务器端HTML
```
var cheerio = require('cheerio'),
$ = cheerio.load('<h2 class="title">Hello world</h2>');
$('h2.title').text('Hello there!');
$('h2').addClass('welcome');
$.html();
```


