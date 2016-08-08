# 流（stream）
## 4种类型的流
1. Readable - Stream which is used for read operation.

2. Writable - Stream which is used for write operation.

3. Duplex - Stream which can be used for both read and write operation.

4. Transform - A type of duplex stream where the output is computed based on input.

## 流的事件
所有的流都是EventEmitter实例，共享的事件有：

1. data - This event is fired when there is data is available to read.

2. end - This event is fired when there is no more data to read.

3. error - This event is fired when there is any error receiving or writing data.

4. finish - This event is fired when all data has been flushed to underlying system

## Reading from stream
```
var fs = require("fs");
var data = '';

// Create a readable stream
var readerStream = fs.createReadStream('input.txt');

// Set the encoding to be utf8. 
readerStream.setEncoding('UTF8');

// Handle stream events --> data, end, and error
readerStream.on('data', function(chunk) {
   data += chunk;
});

readerStream.on('end',function(){
   console.log(data);
});

readerStream.on('error', function(err){
   console.log(err.stack);
});

console.log("Program Ended");
```


## Writing to stream
```
var fs = require("fs");
var data = 'Simply Easy Learning';

// Create a writable stream
var writerStream = fs.createWriteStream('output.txt');

// Write the data to stream with encoding to be utf8
writerStream.write(data,'UTF8');

// Mark the end of file
writerStream.end();

// Handle stream events --> finish, and error
writerStream.on('finish', function() {
    console.log("Write completed.");
});

writerStream.on('error', function(err){
   console.log(err.stack);
});

console.log("Program Ended");
```

### Piping streams

```
var fs = require("fs");

// Create a readable stream
var readerStream = fs.createReadStream('input.txt');

// Create a writable stream
var writerStream = fs.createWriteStream('output.txt');

// Pipe the read and write operations
// read input.txt and write data to output.txt
readerStream.pipe(writerStream);

console.log("Program Ended");
```

