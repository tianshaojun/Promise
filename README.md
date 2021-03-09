# Promise

### 1. 函数对象与实例对象

+ 实例对象：new函数产生的对象，称为实例对象，简称为对象
+ 函数对象：将函数作为对象使用时，简称为函数对象

### 2. 两种回调函数

+ 同步回调：立即执行，完全执行完了才结束，不会放入回调队列中
+ 异步回调：不会立即执行，会放入回调队列中将来执行

### 3. 常见的内置错误

+ Error：所有错误的父类型
+ ReferenceError：引用的变量不存在
+ TypeError：数据类型不正确的错误
+ RangeError：数据值不在其允许的范围内
+ SyntaxError：语法错误

### 4.错误的处理(捕获与抛出)

+ 捕获错误
+ 抛出错误

### 5.Promise的理解

+ 抽象表达：Promise是JS中进行异步编程的新的解决方案
+ 具体表达
    + 从语法上来说：Promise是一个构造函数
    + 从功能上来说：Promise对象用来封装一个异步操作并可以获取其结果

### 6.Promise的状态和状态改变

+ Promise的状态
    + pending
    + resolved
    + rejected
+ Promise的状态改变
    + pending变为resolved
    + pending变为rejected
    + 说明：只有这两种，且一个Promise对象只能改变一次。无论变为成功还是失败，都会有一个结果数据。成功的结果数据一般称为value，失败的结果数据一般称为reason

### 7.Promise的运行流程

![](https://github.com/tianshaojun/Promise/blob/master/md_img/promise001.png)

### 8.Promise的基本使用

### 9.11111







