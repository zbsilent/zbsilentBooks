# Axios



### axis 基本用法



```js
Axios.get("http://localhost:5000/students").then(
			(response) => {
				console.log(response.data);
			},
			(error) => {
				console.log(error);
			}
		);
```

### Server 设置

```js
const express = require('express')
const app = express()

app.use((request,response,next)=>{
	console.log('有人请求服务器1了');
	console.log('请求来自于',request.get('Host'));
	console.log('请求的地址',request.url);
	next()
})

app.get('/students',(request,response)=>{
	const students = [
		{id:'001',name:'tom',age:18},
		{id:'002',name:'jerry',age:19},
		{id:'003',name:'tony',age:120},
	]
	response.send(students)
})

app.listen(5000,(err)=>{
	if(!err) console.log('服务器1启动成功了,请求学生信息地址为：http://localhost:5000/students');
})

```

> 使用 node  server1.js 启动服务 

### 跨域问题 设置代理 代理端口和客户端端口一致



### 配置代理服务器

> package.json  末尾 增加 `` "proxy":"http://localhost:5000"``

```js
//这里要特别注意ip地址的坑  localhost 和 127.0.0.1不一样
	const getInfo = () => {
		axios.get("http://localhost:3000/students").then(
			(response) => {
				console.log(response.data);
			},
			(error) => {
				console.log(error);
			}
		);
```

