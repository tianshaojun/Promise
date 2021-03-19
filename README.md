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

+ promise_base.html

### 9.为什么要使用Promise

+ 指定回调函数的方式更加灵活
   + 旧的：必须在启动异步任务前指定
   + promise：启动异步任务 => 返回promise对象 => 给promise对象绑定回调函数(甚至可以在异步任务结束后指定)
+ 支持链式调用，可以解决回调地狱问题
   + 什么是回调地狱？回调函数嵌套调用，外部回调函数异步执行的结果是嵌套的回调函数执行的条件
   + 解决方案？promise链式调用
   + 终极解决方案？async/await

### 10.Promise的API说明

+ Promise构造函数：Promise(excutor) {}
  + excutor函数：同步执行  (resolve, reject) => {}
  + resolve函数：内部定义成功时我们调用的函数  value => {}
  + reject函数：内部定义失败时我们调用的函数   reason => {}
  + 说明：excutor会在Promise内部立即同步回调，异步操作在执行器中执行

+ Promise.prototype.then方法：(onResolved, onRejected) => {}
  + onResolved函数：成功的回调函数  (value) => {}
  + onRejected函数：失败的回调函数  (reason) => {}
  + 说明：指定用于得到成功value的成功回调和用于得到失败reason的失败回调，返回一个新的promise对象

+ Promise.prototype.catch方法：(onRejected) => {}
  + onRejected函数：失败的回调函数  (reason) => {}
  + 说明：then()的语法糖，相当于：then(undefined, onRejected)

+ Promise.resolve方法：(value) => {}
  + value：成功的数据或promise对象
  + 说明：返回一个成功/失败的promise对象

+ Promise.reject方法：(reason) => {}
  + reason：失败的原因
  + 说明：返回一个失败的promise对象

+ Promise.all方法：(promises) => {}
  + promises：包含n个promise的数组
  + 说明：返回一个新的promise，只有所有的promise都成功才成功，只要有一个失败了就直接失败

+ Promise.race方法：(promises) => {}
  + promises：包含n个promise的数组
  + 说明：返回一个新的promise，第一个完成的promise的结果状态就是最终的结果状态

### 11.Promise的API使用1

### 12.Promise的API使用2
















