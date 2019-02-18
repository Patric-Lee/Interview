# 面试cheatsheet——Java篇

## 基础运算

### 求最值

对于两个数（int, long, double, float等），可以使用：
最大值：Math.max方法
最小值：Math.min方法

对于一个collection，可以使用：
(注意，需要import java.util.Collections;)
最大值：Collections.max方法
最小值：Collections.min方法
对于这两个方法，都可以传入一个Comparator实例作为第二个参数。
注意，需要catch以下两种Exception：
ClassCastException（集合元素间无法比较）和NoSuchElementException（集合为空）

逆序：Collections模块中已有一个reverseOrder()方法可以作为Comparator使用。

### 取整

以下几个函数均不需要


向下取整：Math.floor()方法


向上取整: 

### 幂与对数

求幂：Math.pow()方法

求常用对数：Math.log10(int)方法




### 循环

可以使用标签对循环进行标记，方便break和continue

## 数据结构

### 字符串

#### String

常量，不可改变

读第i个字符：charAt方法

子串（连续）：subString(begin, end)方法，其中包括begin所在的字符而不包括end所在的字符



### Map
查找是否包含特定键：containsKey方法，返回Boolean

#### TreeMap
底层实现：红黑树

时间复杂度分析：
插入 删除 查找 均为O(log n)

查找比带查询值小的最大值：lowerKey方法
查找比带查询值不小的最小值：ceilingKey方法

## 算法

## 面向对象

面向对象的基本特征：封装（encapsulation），继承（Inheritance），多态（polymorphism）
