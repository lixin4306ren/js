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