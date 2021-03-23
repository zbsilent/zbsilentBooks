# Mac

## 2

### 3

#### MAC查看端口命令

```text
lsof -i tcp:9080
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

