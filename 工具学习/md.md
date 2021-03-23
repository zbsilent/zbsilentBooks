[toc]

# MD语法说明

横线

***
---
___

效果：
***
---
___


标题

    # 一级标题
    ## 二级标题
    ### 三级标题
    #### 四级标题
    ##### 五级标题
    ###### 六级标题

效果：
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题


----------

普通文本

	这是普通文本

效果：

这是普通文本


----------

文本块

		a
		b
		c

效果：

	a
	b
	c

----------

代码

    ```c
    int main (void)
    {
    	return 0;
    }
    ```
效果：

```c
int main (void)
{
	return 0;
}
```

----------

高亮

`高亮文字` `tag`

效果：

`高亮文字` `tag`


----------

字体

	*斜体*
	_斜体_
	**粗体**
	__粗体__
	~~删除线~~
	***粗斜体***
	___粗斜体___
	**~~粗斜体~~**

效果：

*斜体*
_斜体_

**粗体**
__粗体__

~~删除线~~

***粗斜体***
___粗斜体___

**~~粗斜体~~**

----------

URL

	![哈哈](http://www.baidu.com/img/bdlogo.gif "百度logo")
	[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")

效果：

![哈哈](http://www.baidu.com/img/bdlogo.gif "百度logo")
[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")


----------

锚

	[跳至五级标题](#五级标题)

效果：

[跳至五级标题](#五级标题)


----------

无序列表

	* 硬件
	* 软件
		* 语言
		* 算法
			* 排序
			* 链表
效果：

* 硬件
* 软件
	* 语言
	* 算法
		* 排序
		* 链表

----------

有序列表

	1. 时间
	2. 地点
	3. 人物
		1. 张三
		2. 李四

效果：

1. 时间
2. 地点
3. 人物
	1. 张三
	2. 李四

----------

引用

	> 生物
	>> 动物
	>>> 人

效果

> 生物
> > 动物
> >
> > > 人

----------

表格

月份|收入|支出
----|----|----
8   |1000|500
9   |1200|600
10  |1400|650


月份（居中对齐）|收入（右对齐）|支出（左对齐）
:--------------:|-------------:|:------------
8               |1000          |500
9               |1200          |600
10              |1400          |650

效果：

月份|收入|支出
----|----|----
8   |1000|500
9   |1200|600
10  |1400|650


月份（居中对齐）|收入（右对齐）|支出（左对齐）
:--------------:|-------------:|:------------
8               |1000          |500
9               |1200          |600
10              |1400          |650


----------

复选框


- [ ] abc

- [x] xx

效果：

- [ ] abc
- [x] xx

[![](https://img.shields.io/badge/dynamic/json?url=https://baidu.com&label=React&query=27&color=brightgreen&prefix=100px&suffix=23px)]()

[![](https://img.shields.io/badge/React-zbsilent-brightgreen)](Https://github.com/zbsilent)

![GitHub issues](https://img.shields.io/github/issues/yonyou-sc-dev/garbo-nccloud-dev?logoColor=brightgreen)![GitHub commit merge status](https://img.shields.io/github/commit-status/yonyou-sc-dev/garbo-nccloud-dev/main/d07bdb79faf1b7465e154e1cc49c07c7562ff376)



![brightgreen](https://shields.io/badge/-brightgreen-brightgreen)![green](https://shields.io/badge/-green-green)![yellowgreen](https://shields.io/badge/-yellowgreen-yellowgreen)![yellow](https://shields.io/badge/-yellow-yellow)![orange](https://shields.io/badge/-orange-orange)![red](https://shields.io/badge/-red-red)![blue](https://shields.io/badge/-blue-blue)![lightgrey](https://shields.io/badge/-lightgrey-lightgrey)
![success](https://shields.io/badge/-success-success)![important](https://shields.io/badge/-important-important)![critical](https://shields.io/badge/-critical-critical)![informational](https://shields.io/badge/-informational-informational)![inactive](https://shields.io/badge/-inactive-inactive)
![blueviolet](https://shields.io/badge/-blueviolet-blueviolet)![ff69b4](https://shields.io/badge/-ff69b4-ff69b4)![9cf](https://shields.io/badge/-9cf-9cf)

![github (3)](/Users/zbsilent/Desktop/github%20(3).svg)

![](https://gitee.com/zbsilent/imag/raw/master/root/github%20(3).svg)

|                                      |                                                              |
| ------------------------------------ | ------------------------------------------------------------ |
| `?style=plastic&logo=appveyor`       | ![plastic](https://shields.io/badge/style-plastic-green?logo=appveyor&style=plastic) |
| `?style=flat&logo=appveyor`          | ![flat](https://shields.io/badge/style-flat-green?logo=appveyor&style=flat) |
| `?style=flat-square&logo=appveyor`   | ![flat-square](https://shields.io/badge/style-flat--square-green?logo=appveyor&style=flat-square) |
| `?style=for-the-badge&logo=appveyor` | ![for-the-badge](https://shields.io/badge/style-for--the--badge-green?logo=appveyor&style=for-the-badge) |
| `?style=social&logo=appveyor`        |                                                              |

## 常用按钮

<kbd>Ctrl/Cmd</kbd>+<kbd>Alt</kbd>+<kbd>A</kbd>, <kbd>C</kbd>

---

[跳至五级标题](##常用按钮)

*Reference: [Action System in IntelliJ SDK Docs][docs:actions]*


[docs]: https://www.jetbrains.org/intellij/sdk/docs
[docs:actions]: https://www.jetbrains.org/intellij/sdk/docs/basics/action_system.html
[docs:action-override]: https://www.jetbrains.org/intellij/sdk/docs/basics/action_system.html#setting-the-override-text-element-for-an-action
[docs:action-locale]: https://www.jetbrains.org/intellij/sdk/docs/basics/action_system.html#localizing-actions-and-groups

[file:PopupDialogAction]: ./src/main/java/org/intellij/sdk/action/PopupDialogAction.java
[file:CustomDefaultActionGroup]: ./src/main/java/org/intellij/sdk/action/CustomDefaultActionGroup.java

[file:DynamicActionGroup]: ./src/main/java/org/intellij/sdk/action/DynamicActionGroup.java -->

