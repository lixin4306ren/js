# Node.js

## 安装
### 安裝 NVM （Node Version Manager）
使用 brew 安裝 NVM  
`$ brew install nvm`

將下列指令加入 .bash_profile（或 .bashrc）檔案   
```
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

重新載入 .bash_profile 設定+  

找出目前所有可安裝的 Node.js 版本  
`$ nvm ls-remote`  

安裝 Node.js (0.11.16)  
`$ nvm install 0.11.16`  
指定nvm使用的 Node.js版本  
`nvm use 0.11.16`  
測試 Node.js

```
$ node -v
npm -v
```

## package的安装和管理
### 安装
安装分为全局和和本地安装  
全局安装：npm install --global xxx  
本地安装：npm install xxx  

### 设置NODE_PATH

## 构建自己的包

### 初始化
`npm init` 这个命令的作用就是帮我们互动式地生成一份最简单的 package.json 文件，init 是 initialize 的意思，初始化。
`npm init`

### 安装依赖包
`npm install express utility --save`  
`--save` 参数的作用，就是会在你安装依赖的同时，自动把这些依赖写入 package.json。命令执行完成之后，查看 package.json，会发现多了一个 dependencies 字段。



