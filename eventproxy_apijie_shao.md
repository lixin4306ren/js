# eventproxy 

# async


什么时候用 eventproxy，什么时候使用 async 呢？  

当你需要去多个源(一般是小于 10 个)汇总数据的时候，用 eventproxy 方便；当你需要用到队列，需要控制并发数，或者你喜欢函数式编程思维时，使用 async。大部分场景是前者，所以我个人大部分时间是用 eventproxy 的。



