# 1

## 2

### 3

#### MAC查看端口命令

```shell
lsof -i tcp:9080
```

##### 管理员权限

```shell
sudo chown -R $(whoami) $(brew --prefix)/*
```

##### 显示隐藏文件

```bash
command+shift+.
```

##### shell看到隐藏文件

```
ls -ah
```

##### 硬盘热插拔无法加载问题 

```
ps aux | grep fsck
sudo pkill -f fsck
```

