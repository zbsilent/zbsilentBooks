# Promise



## 说明

- success -> 决定做这个事
- error -> 放弃做这个事



- 参数：
  - resolve 决定
  - reject 放弃

- 静态方法
  - Promise.resolve()  走第一个函数
  - Promise.reject() 走catch
  - race 竞速

## 实例

```js
Promise.resolve(1).then((m)=>{console.log(m);})
Promise.reject('args').then(()=>{console.log('成功输出')},(m)=>{console.log(m)})	
```

```js
# 先进先出，失败就是失败
Promise.race([new Promise((resolve,reject)=>{
		setTimeout(resolve,300,'one');
	}),new Promise((resolve,reject)=>{
		setTimeout(resolve,500,'two');
	})]).then((l)=>console.log(l))
```
```js
Promise.all([Promise.resolve('1'),2,3]).then((m)=>console.log(m));
```

