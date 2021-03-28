# React路由



![image-20210328010149803](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210328010149803.png)





## SPA理解



- single page web application
- 整个应用只有一个完整的页面
- 数据都需要ajax请求，并在前端异步展现
- 点击链接不会刷新页面，只会局部组件更新



## Router



### 什么是路由？

- 一个路由就是一个key:value映射
- key为路径，value可能是function或者component



### 路由分类

#### 后端路由

- value是function，用来处理客户端提交的请求
- 注册路由：router.get(path,fuction(req,res))
-  node接受请求，匹配路径，执行函数，响应数据

### 前端路由

- 
- 注册路径：<Route path='/test' component={Test}>



## react-router-dom 的理解

- web, native, anywhere三个版本
- 路由器管理路由 Router => Route

- 专门用来实现一个SPA应用，基于react的项目基本都会用到此库‘



### 内置组件 

### 基本使用实例操作方法



> 路由组件放到Pages下，明确导航区和展示区

```jsx
import {Link,BrowserRouter,HashRouter,Route} from 'react-router-dom'
```



`组件最外侧可以 使用 BrowserRouter/HashRouter 封闭`

```jsx
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import App from "./App";
import { BrowserRouter } from "react-router-dom";

ReactDOM.render(
	<React.StrictMode>
		<BrowserRouter>
			<App />
		</BrowserRouter>
	</React.StrictMode>,
	document.getElementById("root")
);
```



```jsx
{/*编写路由链接*/}
<Link className= "list-group-item" to="/about">About</Link>
<Link className= "list-group-item" to="/home">Home</Link>
```



```jsx
{/*渲染阶段注册路由*/}
<Route path="/about" component={About}/ >
<Route path="/home" component={Home}/ >
```



### 路由组件接收参数



`一般组件`

- 位置：components
- 写法：</>
- 接收动态传递参数

`路由组件` 

- 写法 ：<Route path="/about" component={About}/ > 

- 位置 ：pages

- 接收参数固定：

  1. history: 

     ​	go:f go(n)

     ​	goBack:fgoBack()
     ​	goForward: f goForward() push: f push(path, state)
     ​	replace:f replace(path, state)

  2. location:
     	pathname: "/about"
     	search: 11
     	state: undefined

  3. match:
     	params:{}
     	path: "/about"
     	url:"/about"

> - history
>
> - location 
> - match 
> - staticContext





