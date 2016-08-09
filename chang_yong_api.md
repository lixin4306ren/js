# 网络操作API

## URL
http://nodejs.org/api/url.html

### URL对象属性
1. urlObject.href
2. urlObject.protocol
3. urlObject.slashes
4. urlObject.host
5. urlObject.auth
6. urlObject.hostname
7. urlObject.port
8. urlObject.pathname
9. urlObject.search
10. urlObject.path
11. urlObject.query
12. urlObject.hash

### URL格式操作
1. url.parse(urlString[, parseQueryString[, slashesDenoteHost]])
2. url.resolve(from, to)

baseURL + HREF URL
```
url.resolve('/one/two/three', 'four')         // '/one/two/four'
url.resolve('http://example.com/', '/one')    // 'http://example.com/one'
url.resolve('http://example.com/one', '/two') // 'http://example.com/two'
```


## QueryString
用于实现URL参数字符串与参数对象的互相转换  
http://nodejs.org/api/querystring.html
```
querystring.parse('foo=bar&baz=qux&baz=quux&corge');
/* =>
{ foo: 'bar', baz: ['qux', 'quux'], corge: '' }
*/

querystring.stringify({ foo: 'bar', baz: ['qux', 'quux'], corge: '' });
/* =>
'foo=bar&baz=qux&baz=quux&corge='
*/
```



## HTTP
http://nodejs.org/api/http.html
### get/request

## Net
用于创建Socket服务器或Socket客户端。  
