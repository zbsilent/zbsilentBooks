# Git

[![](https://img.shields.io/badge/Git-zbsilent-brightgreen)](Https://github.com/zbsilent)



## .gitignore文件无效解决方案

 > 使用git CLI命令，在IDEA中是Terminal输入git命令

 ```shell
 git rm -r --cached .（注意空格）
 git add .（注意空格）
 git commit -m "update .gitignore"
 ```

> 忽略放弃对.classpath对跟踪

```shell
git update-index --assume-unchanged .classpath
```

