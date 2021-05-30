[toc]

# AI基础

[![](https://img.shields.io/badge/AISTU-zbsilent-brightgreen)](Https://github.com/zbsilent)

## 概念篇

### 基础概念

#### 1 CV

#### 2 NLP

#### 3 基本概念剖析

- 人工智能
- 机器学习
  - 统计机器学习
- 深度学习
  - 神经网络
    - 卷积神经网络
    - 循环神经网络

- python
  - 语言

- sklearn
  - 机器学习库
- TensorFlow
  - 深度学习
- PyTorch
  - 深度学习



#### 4 编程基础

- _Dev Base_
  - [_Study Points for Attention_](#4.1学习注意事项)
  - [_ptyhon base_](#4.2 python基础类型)
  - 
- 数学基础
  - 导数
- 算法基础
- 机器学习算法
- 深度学习算法
- 实践



##### 4.1 学习注意事项

- 累计英文单词
- 所有标点符号全是英文
- <kbd>tab</kbd> 补全
- <kbd>Ctrl（Command）</kbd>+ <kbd>Enter</kbd> 运行代码不跳转行
- <kbd>Shift</kbd> + <kbd>Enter</kbd> 运行当前代码并跳转行
- <kbd>Shift</kbd>+<kbd> Type</kbd> 查看API
- python 学习三部曲
    - print 打印
    - type 类型
    - dir 封装了哪些功能



##### 4.2 python基础类型

> 脚本性语言，尝试性写看着结果再来写

- int

- float

- bool

- str

- list 列表 什么都可以放入

  ```python
  lt = ['2','你好',3]
  # 切片
  lt[0:1] # 可以开闭区间
  # 排序
  # ascending 升序
  # descending 降序
  # reverse 翻转
  lt.sort() 
  ```

- tuple 元组

  ```python
  # 只读list
  t1 =(1,2,3)
  ```

- set 集合 

  > 唯一性、无序性、互异性

  ```python
  lt = {1,2,3,4,5}
  ```

- dict 字典

- 循环

  - _for循环的使用场景_
    - 固定次数
    - 遍历容器
  - while循环的使用场景
    - 无限循环
    - 不太清楚具体的循环次数

* class

  ```python
  # -*- encoding: utf-8 -*-
  class Car(object):
      def __init__(self,name,age,gender):
          # 初始化方法 (挂数据) 类似构造方法  self代表本身
          self.name = name;
          self.age = age;
          self.gender = gender;
      
      def run(self):# 这里还是需要调用self 相当于this指针
          print("运行");
  class Stu(object):
      def show(self):
          print("i am a student...")
  class MyModel(object):
      def __init__(self,k=5):
          self.k = k
  
      def fit(self):
          pass
  car = Car("梅赛德斯",15,"23")
  print(car.gender)
  # car.gender
  car.run()
  
  stu = Stu();
  stu.show()""
  	
  ```
  
  
  
* 科学计算

  ```python
  # a的b次方
  def my_power(a,b):
      return a**b
  print(my_power(2,32))
  ```

  * 向量计算
  * 矢量计算
  * 科学计算

  > 基本容器无法满足，必须使用numpy了 

  ```python
  ls =[1,2,3]
  arrys = np.array(ls);
  print(type(arrys));# <class 'numpy.ndarray'>
  my_power(arrys,3) # [1,8,27]
  ```

* 数据结构

  * 单个数 标量
  * 一维向量 向量 一维张量
  * 矩阵 二维张量
    * Shape 形状
    * 
  * Tensor
    * 均值 `mean`
    * 均值 `average`
    * 方差 `variance`
    * 标准差  standard<sup>`std` `deviation`</sup>  
  
* 图表

  * 描点法画图

    ```python
    form matplotlib import pyplot as plt
    x = np.array([1,7,8,19])
    y = np.array([2,3,4,23])
    plt.plot(x,y)
    plt.show()
    ```

  - 散点图

    ```python
    plt.scatter(x,y)
    ```

    ```python
    def fmyc(x):
        return 2 * (x ** 2) + 5;
    x1 = np.linspace(-5,5,30);
    y1 = np.array(fmyc(x1))
    plt.plot(x1,y1)
    plt.show()
    ```

   

#### 5 KNN  <sup> K-Nearest Neighbor algorithm 近邻算法</sup>

---

> algorithm 计算机解决问题的步骤



- 数据结构和算法
  - 底层算法
  - 时间复杂度
  - 空间复杂度
  - ...
- 机器学习算法
  - 业务算法	
    - 解决问题的步骤

- 近朱者赤、近墨者黑
  - 跟什么样的人在一起，就会变成什么样的人
  - 判断你是一个人，从你身边的朋友就可以看出来



#### 6 机器学习

---

- 分类问题

  - 预测的结果是离散结果 `classification`

    - 如何操作`流程`
      - 输入一个<font color='green'>红色</font>样本
      - 寻找距离样[本最](https://www.baidu.com)近的K个样本
      - 统计K个样本中类别最多的类

    

- 回归问题

  - 预测的结果是连续性变量` regressor`
    - 如何操作
      - 输入一个样本
      - 寻找距离样本最近的K个样本
      - 计算K个样本的均值
      - 该均值就是待预测样本的类别

- 聚类问题

  - 无标签的分类，无监督学习 

- 推荐问题

  - 单论



#### 7 机器学习解决问题的套路

---

> 数据集

> 流程

> 预测



#### 8 爬虫

---

- 网页数据：爬去网页，解析网页，获取数据
- 接口数据：找到接口，爬取接口，获取数据
