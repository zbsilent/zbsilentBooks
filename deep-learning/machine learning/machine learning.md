[toc]

# machine learning



## 机器学习应用

> _计算机，互联网领域_
>
> _传统行业（电力、勘探、地信行业）_
>
> _自然科学（生物、地球、气象科学）_
>
> _公共安全领域（灾害预警、社会安全）_



### 传统数据

- 文本分类
- ...

### 图形数据

- 超分辨率采样
- 物体检测
- 图像压缩

### 自然语言数据

- 文本摘要
- 自然语言翻译
- 对话机器人



- 高性能的矩阵计算 （CPU:OpenBLAS,GPU:CUDA)
- 快速实现算法模型

- 表格：

$$
X\in\R^{n{\times}m}
$$



 鸢尾花数据

```python
from sklearn import datasets

iris = datasets.load_iris()
iris_data = iris['data']
# type(iris_data)
# print(iris_data.shape)
print(iris_data[0]) # 取第一行
print(iris_data[0:150,0:1]) #取第一列
```

- 图像：
  - h 高
  - w 宽
  - c RGB颜色 RGBA RGBD(深度)

$$
X\in\R^{h{\times}w{\times}c} 
$$

$$
X\in\R^{k{\times}3}M^{3{\times}3} =\sum_{k=1}^3X_{ik}M_{kj}
$$

- - 转变为灰色 

$$
（X^{h{\times}w}_R+X^{h{\times}w}_G+X^{h{\times}w}_B)/3
$$

