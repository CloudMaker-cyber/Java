# JavaSE加强

## 异常

![image-20260916172633793](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916172633793.png)

![image-20260916173400692](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916173400692.png)

### 作用

![image-20260916181034204](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916181034204.png)

### 自定义异常

![image-20260916181928410](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916181928410.png)

更多用运行时异常

### 异常的处理方案

![image-20260916185253274](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260916185253274.png)

第一种是常见方法

## 泛型

![image-20260917182910728](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917182910728.png)

### 自定义泛型类

![image-20260917183522937](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917183522937.png)

### 自定义泛型接口

![image-20260917184032366](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917184032366.png)

接口的不同的实现类在重写接口里的方法时，接口方法的参数一旦写死就不好操作其他类，比如对学生和老师类的增删改查，接口的add()方法里要传入的参数不能写死。所以用泛型接口比较好

### 泛型方法，通配符，上下限

![image-20260917185538204](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917185538204.png)

![image-20260917185512390](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917185512390.png)

### 支持的类型

泛型不支持基本数据类型，只支持对象类型（引用数据类型）

泛型擦除：泛型工作在编译阶段，编译后就没用了，所以泛型在编译后都会擦除，所有类型会恢复成Object类型。

java解决方法：包装类

### 包装类

![image-20260917191012862](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917191012862.png)

![image-20260917190822398](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917190822398.png)

Integer里缓存了-127——128的对象，所以图中it1==it2为true，一旦超过了就会new新的Integer对象，如it11==it22为false![image-20260917191316527](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917191316527.png)

### 包装类的常用功能

### ![image-20260917191855099](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917191855099.png)

![image-20260917191744895](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260917191744895.png)

记住valueOf就行，不用记parseInt，字符串转数据类型很有用，但是基本数据类型转字符串没啥用，因为完全可以这样：

int j = 23;

String rs = j + "";

空字符串和变量做 `+` 拼接，Java 会自动把后面的值转为字符串。双引号放前后都行。

## 集合框架

![image-20260918111340814](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918111340814.png)

### 集合特点

![image-20260918111655894](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918111655894.png)

### Collection常用功能

![image-20260918200954228](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918200954228.png)

### Collection三种遍历方式

#### 一，迭代器遍历

![image-20260918201850131](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918201850131.png)

![image-20260918222651855](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918222651855.png)

#### 二，增强for循环

![image-20260918223009168](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918223009168.png)

也能用来遍历数组

#### 三，Lambda表达式

![image-20260918223319623](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918223319623.png)

#### 三者的区别

![image-20260918225916892](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918225916892.png)

![image-20260918225433421](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918225433421.png)

**解决方案**

![image-20260918230012333](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260918230012333.png)

### List集合系列

#### 特点，功能

![image-20260919113732517](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260919113732517.png)

![image-20260919114532933](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260919114532933.png)

#### ArrayList底层原理（面试）

[相关视频](https://www.bilibili.com/video/BV1gb42177hm/?spm_id_from=333.788.videopod.episodes&vd_source=2f6779340fa9ff071614a3e2236898ea&p=126)

![image-20260919134950816](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260919134950816.png)

一开始是空数组，是在第一次添加数据时候扩容的，加满后扩容成原来的1.5倍

#### LinkList底层原理（面试）

![image-20260920205336179](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260920205336179.png)

实际上是基于双链表实现的![image-20260920205443851](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260920205443851.png)

![image-20260920205524618](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260920205524618.png)

#### Linklist应用场景

![image-20260920205800815](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260920205800815.png)

队列先进先出，后进后出

![image-20260920205937361](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260920205937361.png)

### Set集合

#### 特点

![image-20260921170142613](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921170142613.png)

#### HashSet集合的底层原理

[视频教程](https://www.bilibili.com/video/BV1gb42177hm/?spm_id_from=333.788.player.switch&vd_source=2f6779340fa9ff071614a3e2236898ea&p=130)

![image-20260921175905152](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921175905152.png)

![image-20260921180029698](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921180029698.png)

![image-20260921180918489](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921180918489.png)

扩容机制：数组存满数据到16*0.75=12个时，自动扩容，每次扩容到原来的两倍。如第一次扩容后数组长度为32

![image-20260921181210025](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921181210025.png)

红黑树就是可以自平衡的二叉树：每条路上的黑色数据个数要一样

#### 自定义对象去重

![image-20260921182707844](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921182707844.png)

![image-20260921183442703](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921183442703.png)

#### LinkedHashSet集合的底层原理

![image-20260921183903201](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921183903201.png)

#### TreeSet集合

![image-20260921184924824](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921184924824.png)

默认不能给自定义对象排序，因为不知道大小规则。

解决方法:

![image-20260921190627592](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921190627592.png)

![image-20260921185902190](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921185902190.png)

第二种方法

![image-20260921190126168](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921190126168.png)

![image-20260921190421437](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921190421437.png)

![image-20260921190808848](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921190808848.png)

实际开发中常用ArrayLIst和HashSet

## Map集合

![image-20260921230025428](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260921230025428.png)