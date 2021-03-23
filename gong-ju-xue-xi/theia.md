# Theia学习

* 更改目录权限

  ```text
  cd /data/www/default/your_dir
  sudo chmod -R 777 your_dir
  ok
  ```

* 安装nodejs指定版本

  ```text
  n 12.14.1
  ```

* `安装 theia`
* 原来的安装是基于GITHUB的，由于访问原因更换地址

  ```text
  git clone https://github.com/eclipse-theia/theia \
  && cd theia \
  && yarn \
  && cd examples/browser \
  && yarn run start
  ```

* gitt地址安装

  ```text
  git clone https://gitee.com/zbsilent/theia \
  && cd theia \
  && yarn \
  && cd examples/browser \
  && yarn run start
  ```

* 启动命令

  、、、shell

  yarn start /my-workspace --hostname 0.0.0.0 --port 8080

  、、、

