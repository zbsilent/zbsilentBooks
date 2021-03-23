# Serverless框架

------

## 选择合适的FaaS平台

![](/Users/Repostory/gitbook/image/1609231212286.jpg)
- FaaS 平台都支持 Node.js、Python 、Java 等编程语言；

- FaaS 平台都支持 HTTP 和定时触发器（这两个触发器最常用）。此外各厂商的 FaaS 支持与自己云产品相关的触发器，函数计算支持阿里云表格存储等触发器；

- FaaS 的计费都差不多，且每个月都提供一定的免费额度。其中 GB-s 是指函数每秒消耗的内存大小，比如1G-s 的含义就是函数以 1G 内存执行 1 秒钟。超出免费额度后，费用基本都是 0.0133元/万次，0.00003167元/GB-s。所以，用 FaaS 整体费用非常便宜，对一个小应用来说，几乎是免费的。

总的来说，国外开发者经常用 Lambda，相关的第三方产品和社区更完善，国内经常用函数计算，因为函数计算使用方式更符合国内开发者的习惯


> 代码开发

这个 Serverless 应用的功能是： 提供一个所有人都可访问的 “Hello World!” 接口，并且能够根据请求参数进行响应（比如请求 http://example.com/?name=Serverless 返回 Hello, Serverless ）。
```js
// index.js
const express = require('express')
const app = express()
const port = 3000
// 定义路由
app.get('/hello', (req, res) => {
  const { name } = req.request.query;
  res.send(`Hello ${name}!`);
});
// 启动服务
app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
});
```
>> 代码部署（FaaS函数）
`sdfsd`

>>> 创建触发器
