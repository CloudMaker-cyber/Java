# Java语言基础

## 类的基本语法

### 实体类

（对应业务对象/数据库表，职责偏向持久化数据承载）（JavaBean 风格）

![image-20260911102824246](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260911102824246.png)

必须有无参构造器，有参构造器可选

### static

#### static修饰成员变量

![image-20260912130533818](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912130533818.png)

![image-20260912131008743](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912131008743.png)

#### static修饰方法

静态方法不能访问实例变量。![image-20260912131634014](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912131634014.png)

![image-20260912131906635](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912131906635.png)

##### 静态方法的应用![image-20260912132050203](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912132050203.png)

![image-20260912132637328](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912132637328.png)

工具类的构造器进行私有就是说在构造方法前加private

##### 静态方法的注意事项

![image-20260912132851306](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912132851306.png)

## 继承

### 权限修饰符

![image-20260912134802329](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912134802329.png)

### 继承的特点

![image-20260912135825367](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912135825367.png)

### 方法重写

![image-20260912140116655](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912140116655.png)

#### 应用场景

![image-20260912140735390](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260912140735390.png)

#### 子类构造器特点

![image-20260913111332551](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913111332551.png)

![image-20260913111200814](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913111200814.png)

this调用兄弟构造器

![image-20260913112002229](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913112002229.png)

## 多态

![image-20260913112856288](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913112856288.png)

对于成员变量来说，编译看左，运行也看左；

对于对象，行为来说，编译看左，运行看右：编译时p1.run()会先看People类里有没有run()方法，运行时则会按照student类里重写的run()方法来跑

![image-20260913113847766](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913113847766.png)

解决方法：强转：

![image-20260913114506912](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913114506912.png)

## final关键字

![image-20260913120430750](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913120430750.png)

### 常量

### ![image-20260913120830519](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913120830519.png)

## 单例类（单例设计模式）

饿汉式单例（用对象时，对象已经创建好）

![image-20260913121254285](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913121254285.png)

懒汉式单例

![image-20260913121939858](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913121939858.png)

## 枚举类

![image-20260913122502063](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913122502063.png)

### 特点

![image-20260913124146918](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913124146918.png)

![image-20260913124510989](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913124510989.png)

### 应用场景

![image-20260913125641621](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260913125641621.png)

## 抽象类

### 特点![image-20260914165547472](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914165547472.png)

### 好处及应用场景

![image-20260914165935687](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914165935687.png)

### 模板方法设计模式

![image-20260914170742573](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914170742573.png)

![image-20260914170901762](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914170901762.png)

## 接口

![image-20260914171551105](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914171551105.png)

JDK 8 之前，接口里只能有隐式 `public static final` 的常量，以及隐式 `public abstract` 的抽象方法。

![image-20260914172441835](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914172441835.png)

### jdk8开始，新增的三种方法

![image-20260914182559246](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914182559246.png)

### 注意事项

![image-20260914183408145](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914183408145.png)

具体例子见视频:[Java基础-11-接口-JDK8新增的三个方法，几点注意事项_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1gb42177hm/?spm_id_from=333.788.videopod.episodes&vd_source=2f6779340fa9ff071614a3e2236898ea&p=80)13min

### 抽象类和方法的区别

![image-20260914190630624](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914190630624.png)

## 代码块

![image-20260914191527911](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914191527911.png)

## 内部类

（开发中很少要自己写，能看懂别人的源码即可）

![image-20260914192024685](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914192024685.png)

### 成员内部类

![image-20260914192915641](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914192915641.png)

![image-20260914192815421](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914192815421.png)

### 静态内部类

![image-20260914210103701](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914210103701.png)

### 局部内部类（鸡肋语法，看看就行）

### **匿名内部类**

![image-20260914210948150](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914210948150.png)

![image-20260914211559815](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914211559815.png)

### 常见使用形式

作为一个对象参数传输给方法使用

![image-20260914215446361](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914215446361.png)

### 使用场景

![image-20260914220308677](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260914220308677.png)

## 函数式编程（简化匿名内部类）

### Lambda表达式

![image-20260916110044077](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916110044077.png)

![image-20260916110647112](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916110647112.png)

#### 简化规则

![image-20260916111928538](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916111928538.png)

### 方法引用

#### 静态方法引用

![image-20260916112151685](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916112151685.png)

#### 实例方法的引用

![image-20260916112748096](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916112748096.png)

#### 特定类型的方法引用

![image-20260916113846495](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916113846495.png)

![image-20260916113811797](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916113811797.png)

#### 构造器引用

![image-20260916160614952](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916160614952.png)

![image-20260916160712166](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916160712166.png)

## 常用API

### String

![image-20260916161253097](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916161253097.png)

两种方法区别：![image-20260916162345391](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916162345391.png)



所以开发过程中更常用第一种方法，更节省内存。

参考即可：

![image-20260916162754853](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916162754853.png)

![image-20260916163119612](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916163119612.png)

### **ArrayList集合**

![image-20260916165702604](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916165702604.png)

![image-20260916165851261](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916165851261.png)

> [!NOTE]
>
> 未完成：GUI编程，项目实战2：石头迷阵小项目

