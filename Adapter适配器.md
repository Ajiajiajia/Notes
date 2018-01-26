# 适配器
![极客学院](http://www.jikexueyuan.com/course/1335_4.html?ss=1)

# 适配器模式原理

## 理解

### 1.插头与插座

每个国家的插头适配对应的插座，但是每个国家的插头都不同，我们去旅行的时候需要充电，搜一我们需要一个转换器，一面能插入外国的插座，一面能为我国插头提供叉口

### 2.点烟器转为USB接口，用于手机充电

## 原理

### 1.用火鸡冒充鸭子

对外界人看来是一只鸭子，继承自duck接口，对外形象是一只鸭子的实现。但是是调用了火鸡的方法和内容，功能和作用都是火鸡的。

### 我们想让一只鸭子 展现出 火鸡的特征
对外形象是一只鸭子，但是有火鸡的叫声，飞行距离

### 这是对象适配器方法

1.Duck.java

+ 定义方法

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/58823014.jpg)

2.GreenDuck.java

+ implement Dack 实现方法

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/2072539.jpg)

3.Turkey.java

+ 定义方法

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/71800455.jpg)

4.WildTurkey.java

+ implement Turkey 实现方法

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/8870628.jpg)

5.TurkeyAdapter.java

+ 对外展现为鸭子形象，所以实现的是 鸭子的接口
+ 对外展现为火鸡的功能，所以传入 火鸡的对象

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/42509734.jpg)

6.MainTest.java（测试）

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/23823188.jpg)

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/14209535.jpg)

7.运行呈现

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/23460680.jpg)




## 意义

1.将一个类的接口转换为另一种接口，让原本接口不兼容的类可以兼容

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/99905190.jpg)

2.用户看不到被适配者，看不到适配器之后的东西，解藕


3.用户调用适配器转化出来的目标接口方法（直接将国标插头插入适配器中进行使用，无需知道转换器后面是哪一个国家的插口）


4.适配器再调用被适配者的相关接口和方法

# 对象适配器与类适配器

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/24107483.jpg)

### 多重继承

继承 目标接口部分 达到适配目的（使对外呈现鸭子的形象）

继承 被适配者类的部分 通过调用 被适配者类里面的方法来实现接口的功能（使鸭子具有火鸡的功能）

## 对象是适配器 --组合方法

上面的火鸡例子

## 类适配器--继承方法

通过多重继承 目标接口 和 被适配的类方法 来实现适配

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/75016073.jpg)

因为类适配器 既 extend 又 implement ，所以在main 里面与 对象适配器的写法有所不同

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/48893307.jpg)

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/3052770.jpg)

（只飞了3次）

# 从枚举器到迭代器的适配

![](http://oz3rf0wt0.bkt.clouddn.com/18-1-7/15664568.jpg)

# 总结








