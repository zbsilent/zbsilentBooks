# ES6

es2015的缩写

[![](https://img.shields.io/badge/GitBook-zbsilent-brightgreen)](Https://github.com/zbsilent)

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

```javascript
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

```javascript
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

> 1996年 es1诞生 网景浏览器 支持es1 提出了javascript支持 actioncript - &gt;flash
>
> 1997 年 es2 ie6 支持 网景支持 浏览器大战
>
> 1998年 es3 火狐不支持 其他支持
>
> 2007年 es4 激进 无法支持
>
> 2008年 es3.1 退化版 html5
>
> 2009年 es5草案
>
> 2010年 es5通过
>
> 2011年 es6草案
>
> 2013年 es6通过
>
> 2014年 chrome30% html 全面支持
>
> 2015年 es6 chrome 60% 火狐30%
>
> 2016年 es6 chrome 60% +
>
> node.js

es6 $\rightarrow$ es2015 $\longrightarrow$ecma

```javascript
{/*封装jqery*/} ECMAscipt->ecma/es
测试
```

> 块级作用域

```markup
<script type='text/javascript'>
  {/*
      var i = 0
  */}
  {
    let allInput = document.getElementsByTarName('input')；
    for(let i = 0;i<allIput;i++){
      allIput[i].onclick = function{
         console.log(i);
      }
    }
  }
</script>
```

> 结构赋值 前后结构一致即可

```javascript
<script type='text/javascript'>
    let [a,b,c] = [10,20,30]
    console.log(a,b,c)
    let [a,[b,d],c] = [10,[20,21],30]
</script>
```

> Json {key对应key}

```javascript
var json ={'a':20,'b':30}

let {a,b} = json;
```

> 传参

```javascript
function show (x=[30,50,10]){
  console.log(a)
  var b = a[0];
  # let [b,c,d,e] = a
};
show([20,21])
```

```javascript
var data = {
  'ok':1,
  'data':{

  },
  'mis':'请求成功'
}
if(data.ok == 1){

}
let (ok,data,mis) = data
```

### bind

> 任何函数都可以用call调用自己 call的第一个参数就是函数的\`this\`,第二个参数是函数的\`形参\`

```javascript
function show(){
  console.log(this) > window对象
}
show.call(1)  > 1 对象本身
show.call(1,2) > 2

alert.call(whindow,1) > 1
setTimeOut.call(window,()=>{
  alert.call(window,1)
},1000);
show.bind(1) #函数本身 没有进行调用 
show.band(1)() #调用时候
```

> 任何函数都可以用call调用自己 call的第一个参数就是函数的\`this\`,第二个参数是函数的\`形参\`,正常不会会自己调用

## 面向对象

### 类

* 通过类找到原型 Array.prototype

![image-20210323141136686](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323141136686.png)

* typeof 'asdsda'
  * \[1,2,3\].constructor =&gt; function Array\( \)    {    \[native code\]    }
* call/bind所有方法都通用

![image-20210323141530612](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323141530612.png)

![image-20210323141822756](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323141822756.png)

![image-20210323141226630](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323141226630.png)

### 原型

* prototype  
  * 人 - 手 
  * String - substring/indexof
  * function - call/bind
  * array - concat join

### 原型链

* 继承的 

```javascript
function show(){
  console.log(1)
}
var c = show;
> new c() >> 1
> console.log(c)
> console.log(c.prototype) __proto__  下的东西 就是原型链
```

![image-20210323152414386](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323152414386.png)

#### es6 class类标准概念

```javascript
<script type="text/javascript">
  class a{
    {/*构造函数*/}
    constructor() { 
      this.x =10; {/*私有属性*/}
      consol.log(this.x);
    }
    ffff(){
      alert('原型->其实就是方法')
    }
  }
  new a();
</script>
```

![image-20210323163117493](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323163117493.png)



![image-20210323163146412](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210323163146412.png)

> 支持继承 extends
>
> ```javascript
>   class a extends aparent{
>     constructor(props) {
>       //这里用父类属性必须从构造方法super过来
>       super(props); 
>     }
>   }
> ```
>
> 箭头函数不改变this指向

### es6jquery

jquery

```javascript
$('div').addClass()
$('')
```

#### css

```javascript
css({'width':'200px','heigth':'300px'})
```

