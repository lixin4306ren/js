# URL详解

URL(Uniform Resource Locator) 地址用于描述一个网络上的资源，  基本格式如下：
```
schema://host[:port#]/path/.../[;url-params][?query-string][#anchor]
```

1. scheme 指定低层使用的协议(例如：http, https, ftp)  
2. host HTTP服务器的IP地址或者域名  
3. port# HTTP服务器的默认端口是80，这种情况下端口号可以省略。    如果使用了别的端口，必须指明，例如http://www.cnblogs.com:8080/
4. path 访问资源的路径
5. url-params
6. query-string       发送给http服务器的数据
7. anchor 锚
