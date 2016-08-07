# 建立一个package.json

## 初始化
`npm init` 这个命令的作用就是帮我们互动式地生成一份最简单的 package.json 文件，init 是 initialize 的意思，初始化。
`npm init`

## 安装依赖包
`npm install express utility --save`  
`--save` 参数的作用，就是会在你安装依赖的同时，自动把这些依赖写入 package.json。命令执行完成之后，查看 package.json，会发现多了一个 dependencies 字段。



