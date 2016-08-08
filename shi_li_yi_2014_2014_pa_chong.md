# 示例一——爬虫
## 准备工作
```
cd immoc-video-download
npm init // 建立package.json文件
npm install superagent cheerio --save //安装相关模块
touch app.js #新建一个名为 app.js 的文件
```


## 搭建框架，peudocode
```
var superagent = require('superagent');
var cheerio = require('cheerio');
var fs = require('fs');

var url = '慕课网课程'
var savePath = '保存文件路径'

superagent
    .get(url)
    .end(function(err, res) {

    })

// 获取视频 url
var getVideoUrl = function() {

}

// 下载视频
var downloadVideo = function() {

}

```

## 慕课网页面分析
http://www.imooc.com/learn/441

![](http://upload-images.jianshu.io/upload_images/1271031-70e69f952aa87f22.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 解析视频 id 和 filename


