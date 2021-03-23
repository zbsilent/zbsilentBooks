# es6学习
---
es2015的缩写

---



```jsx
{/*块状作用域 以前都是function为作用域*/}
{
  alert(1);
}
{/*let 变量不允许重复申明 */}

let time = 10;

let time = function(){} 

{/*可以重复赋值*/}
time = 20 
{/*变量泄漏*/}
for(var i =0; i< 10;i++){ 
};
consol.log(i)
{/*可以讲i定义为let*/} 
```



```jsx
{/*这个是常量 不允许赋值、重复申明*/}
const a = 10 ;
console.log(a);

```



```js
{/*charcodeAt 获取ecoding 编码 多少进制的 比如2232*/}
let a = 'asd';
console.log(a.charCodeAt(0 ));
String.fromCharCode()
'\u4e00 - \u9fa5'
for(let i = 0x4e00;i<0x9fa5;i++){
  19688~40865
}
 
```

```jsx
{/*无法在上方调用*/}
函数名 x = 参数 => 或者执行
x = x => x

var x = function(x){
  return x;
}
 
show=()=> {}

function(x){
  console.log(x)
}
[1,2,3].find(x=>{console.log(x)})

document.onclick = function(){document.body.style
  .background = 'black'}
document['onclick']=()=>{document.body.style
  .background = 'black'}
```

```jsx
{/*匿名函数*/}
(function(){

Alert(1)

})()
let x = 10;
((x)=>{alert(x)})()
```



```jsx
{/*延展参数 可以延展任何类型*/}

function show(x=5,y=3){
  console.log(x)
};
show();
> 参数默认default 为5
var obj ={a:3}
function show{x={a:5,b:5}){
  console.log(x)
};
show(obj);
show'obj'
> 参数为obj
              
```



```jsx
/*扩展运算符 ...箭头函数没有arguments*/
show=()=>{
  console.log(arguments)
}
show``;

show( ){
  console.log(arguments)
}
show()
> 
show(1,2,3,4)
>1,2,3,4
show(...x){
  console.log(x)
}
>[1,2,3,4]
show(y,...x){
  console.log(x)
}
>1,[2,3,4]
{/*函数中的参数用 代表实参为数组 进来的x变量*/}
var a =[1]
var b =[2]
var c =[3]
cconsole.log(a.conncat(b.concat(c)));

cconsole.log(a.conncat(b.concat(c)));
{/*合并数组*/}
cconsole.log([...a,...b,...c]);

let a = `<div></div>`
doccument.write(a.repeat(5));

console.log([...document.querySelectorAll('div')])

```

```jsx
<style>
  div{display:none;width:200px;heigth:200px;background:#ccc}
  div:first-of_type{
    display:block
  }
</style>
<input vaule='1' type='button'/>
<input vaule='2' type='button'/>
<input vaule='3' type='button'/>
<div>aaa</div>
<div>bbb</div>
<div>ccc</div>
      
      
[...document.querySelectorAll('inpnt')].find((x,y)=>{
  x['onclick']()=>{
    [...document.querySelectorAll('div')].find(d=>{
      d.style.display='none';
    });
    [...document.querySelectorAll('div')].[y].style.display='block';
  }
})
```

```jsx
{/*生成器函数 function* 函数名() */}
function show(){
  alert(1)
};
show()

&
function* show(){
  alert(1)
};
> show不可以用了 

需要用 show.next() 使用生成器函数 函数只有1个return 
                  生成器可以不断next  不叫return 叫做yield
                  
                  
function* show(){
  yield function(){
    alert(1);
  };
  yield function(){
    alert(2);
  };
  yield() =>{
     alert(3);
  }
};
var k = show();
k.next().value() #第一个
k.next().value() #第二个
document.onclick = x=>{
  k.next().value() #第三次
}
```

​	

```json
json ={a:2,b:2,c:3}

json ={};
json={
  a(){
    console.log(1);
  }
}
json.a();

> 1
get/set

json = {
   set Reno(a){
     console.log(a)
   },
  	get Reno(){
      console.log(2)
    }
};
> json.Reno = 1;# 不赋值，走get 给值走set
```

> 1996年 es1诞生 网景浏览器 支持es1 提出了javascript支持 actioncript - >flash
>
> 1997 年 es2 ie6 支持 网景支持 浏览器大战 
>
> 1998年 es3 火狐不支持 其他支持
>
> 2007年 es4 激进 无法支持

```js
{/*封装jqery*/} ECMAscipt->ecma/es
测试
```

