# Redux学习





## 作用

> 管理共享状态，某个组件的状态，需要让其他组件随时可以拿到
>
> 一个组件需要改变另一个组件的状态
>
> 总体原则：能不用则不用



## 工作流程





![image-20210325225108197](https://raw.githubusercontent.com/zbsilent/imag/main/rootimage-20210325225108197.png)

## 三大核心

###  action

1. 动作的对象

2. 包含2个属性

3. - type：标识属性, 值为字符串, 唯一, 必要属性
   - data：数据属性, 值类型任意, 可选属性

1. 例子：{ type: 'ADD_STUDENT',data:{name: 'tom',age:18} }

### reducer

1. 用于初始化状态、加工状态。
2. 加工时，根据旧的state和action， 产生新的state的``纯函数``

### store

1. 将state、action、reducer联系在一起的对象

2. 如何得到此对象?

   1. import {createStore} from 'redux'
   2. import reducer from './reducers'
   3. const store = createStore(reducer)

   1. 1. 1. 

3. 此对象的功能?
   1. getState(): 得到state
   2. dispatch(action): 分发action, 触发reducer调用, 产生新的state
   3. subscribe(listener): 注册监听, 当产生了新的state时, 自动调用

## redux 的核心API

**7.3.1. createstore()**

作用：创建包含指定reducer的store对象

**7.3.2. store****对象**

1. 作用: redux库最核心的管理对象
2. 它内部维护着:
3. 1. 1. 1. 1. state
            2. reducer

1. 核心方法:

1. 1. 1. 1. 1. getState()
            2. dispatch(action)
            3. subscribe(listener)

1. 具体编码:

1. 1. 1. 1. 1. store.getState()
            2. store.dispatch({type:'INCREMENT', number})
            3. store.subscribe(render)