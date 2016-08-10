# node.js的全局对象
全局对象是指无需引入直接可以使用的对象。

## process 
`process`是一个全局变量，可通过`process.argv`获得命令行参数。由于`argv[0]`固定等于NodeJS执行程序的绝对路径，`argv[1]`固定等于主模块的绝对路径，因此第一个命令行参数从`argv[2]`这个位置开始。

`Process` 提供了很多有用的属性，便于我们更好的控制系统的交互：  
```
// 输出到终端
process.stdout.write("Hello World!" + "\n");

// 通过参数读取
process.argv.forEach(function(val, index, array) {
   console.log(index + ': ' + val);
});

// 获取执行路局
console.log(process.execPath);


// 平台信息
console.log(process.platform);

// 输出当前目录
console.log('当前目录: ' + process.cwd());

// 输出当前版本
console.log('当前版本: ' + process.version);

// 输出内存使用情况
console.log(process.memoryUsage());
```


## console

```
console.log('aaa','bbb','ccc','dddd');
console.error() 输出当前错误流.
console.trace() 输出当前调用栈.
```
## Buffer

## __filename
获取当前执行脚本所在的绝对路径。注意是两个下划线。

## __dirname
`__dirname` 表示当前执行脚本所在的目录。


## module

## exports
exports 和 module.exports 其实是一样的,但是为了简化使用,exports 是 module.exports 的一个引用,他们最终指向一个对象.

我们从一个模块导出一个方法 exports.myfunction 等价于 module.exports.myfunction 明显前面的用户很简单,书写更少的代码.

## setTimeout(cb, ms)
## setInterval(cb, ms)
## clearTimeout(t)


