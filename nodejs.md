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





