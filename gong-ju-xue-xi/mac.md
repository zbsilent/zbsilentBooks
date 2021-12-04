# Mac

## 2

### 3

#### MAC查看端口命令

```text
sudo lsof -nP | grep LISTEN | grep 8080
```

**管理员权限**

```text
sudo chown -R $(whoami) $(brew --prefix)/*
```

**显示隐藏文件**

```bash
command+shift+.
```

**shell看到隐藏文件**

```text
ls -ah
```

**硬盘热插拔无法加载问题**

```text
ps aux | grep fsck
sudo pkill -f fsck
```

**启动MAC的TOMCAT**

```js
# 修改catalina.sh文件
export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_281.jdk/Contents/Home
export JRE_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_261.jdk/Contents/Home
# 进入下面目录
/Users/zbsilent/apache-tomcat-9.0.44/bin
# 授权
sudo chmod 755 *.sh
# 启动
sudo sh ./startup.sh
# 修改密码
conf/tomcat-users.xml
<user username="root" password="281992" roles="manager-gui" />

```

### 管理node

```shell
 sudo n 14.14.0
 
 https://github.com/nodejs/node/blob/master/doc/changelogs/CHANGELOG_V14.md
```





sudo lsof -nP | grep LISTEN | grep 8080
