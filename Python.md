# 面试知识点——Python篇


所谓“好记性不如烂笔头”，虽然一直以来凭恃自己博闻强识，做的笔记少之又少，不过提纲挈领地总结一下，
既有造福大众之功，又有佛脚之用，好处甚多。本篇主要总结一些自己觉得需要注意的Python知识，其中有一些自己平时的知识盲点。

## 基础运算

整数不同进制的转换：bin

整数与浮点数的转换：

int() -------> 接受数字；接受合法字符串；返回更靠近0的整数值（整数类型）;对于非法字符串抛出ValueError

round() -------> round to even;返回浮点类型

math.floor() ------> 返回最大的小于等于它的整数（浮点类型）

math.ceil() -------> 返回最小的大于等于它的整数（浮点类型）

浮点数取整数小数部分：math.modf() -------> 返回tuple，分别为小数部分和整数部分

无穷大与负无穷大：float("inf")和float("-inf")

两种除法运算符：//与/

指数运算符：**

### 字符串操作

字符与ascii码相互转换：chr与ord

字符串复制，插入，倒转，合并

### 列表（list）操作

列表复制，插入，删除，倒转，合并

### 字典（dict）操作

### 集合（set）操作

集合初始化：空集合 set()

集合添加元素：add

集合删除元素：remove

检查元素a是否在集合b中：a in b（返回True或者False） a not in b

交集：a&b

并集：a|b

差集：a - b（在集合a中而不在b中的元素组成的集合）

对称差：a^b

## 数据结构与算法

### 队列

使用双端队列时使用collections模块的deque类。

在末尾（右侧）添加：append

在左侧添加：appendleft

在右侧删除：pop

在左侧删除：popleft

在右侧合并：extend

在左侧合并:extendleft

清空：clear

倒转：reverse方法，返回值为None。

旋转移动：rotate方法（参数为负时可以向左旋转移动）。

注意：deque自带max_len属性。初始化时定义该属性可以控制deque的长度，如果添加元素后超出长度，另一端的值将被舍弃。

### 二分查找

利用bisect模块。注意，list应为已经排好序的列表；lo-->inclusive;hi-->exclusive。

查找：bisect.bisect_left(list, item, lo, hi)
    bisect.bisect_right(list, item, lo, hi)
    返回待插入的位置的index，范围为0到len(list)。
    
查找并插入：bisect.insort_left(list, item, lo, hi)
  bisect.insort_right(list, item, lo, hi)
  不返回值，直接在原列表中插入。

### 排序

### 哈希

## 读写

## 面向对象

__new__方法与__init__的区别

@classmethod与@staticmethod的区别
