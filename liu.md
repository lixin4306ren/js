# 流（stream）
## 4种类型的流
1. Readable - Stream which is used for read operation.

2. Writable - Stream which is used for write operation.

3. Duplex - Stream which can be used for both read and write operation.

4. Transform - A type of duplex stream where the output is computed based on input.

所有的流都是EventEmitter实例。