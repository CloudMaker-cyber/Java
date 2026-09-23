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

![image-20260922205914678](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922205914678.png)

### 常用方法

![image-20260922210413430](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922210413430.png)

put方法：当key一样时，可以覆盖前面相同的key的值，即可完成值的更新

### 遍历方式

1.键找值：先获取Map集合全部的键，再通过遍历键来找值

![image-20260922211750751](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922211750751.png)

![image-20260922211913539](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922211913539.png)

2.把键值对看成一个整体进行遍历（难度较大）

![image-20260922212504992](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922212504992.png)

3.Lambda（很简单）

![image-20260922214447501](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922214447501.png)

理解源码：

![image-20260922215034415](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922215034415.png)

函数式编程的Lambda简化![image-20260922215254569](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922215254569.png)

### 实现类

![image-20260922220842618](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922220842618.png)

![image-20260922223628158](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922223628158.png)

![image-20260922224357088](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260922224357088.png)

## Stream流

![image-20260923094343276](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923094343276.png)

![image-20260923094407929](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923094407929.png)

![image-20260923094317990](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923094317990.png)

### 获取Stream流

![image-20260923094836236](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923094836236.png)

![image-20260923095447877](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923095447877.png)

### 常用中间方法

![image-20260923105720415](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923105720415.png)

### 常用终结方法

![image-20260923111935693](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923111935693.png)

![image-20260923161417840](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923161417840.png)

流只能收集一次

![image-20260923163605606](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923163605606.png)

![image-20260923163700168](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923163700168.png)

![image-20260923163428755](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923163428755.png)

### 可变参数

![image-20260923164306192](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923164306192.png)

> [!CAUTION]
>
> 可变参数在方法内部就是一个数组；可变参数在形参列表中只能有一个；可变参数必须放在形参列表的最后面

### Collections工具类

![image-20260923165606615](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923165606615.png)

## 存储&读写数据的方案

### File

![image-20260923183639230](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923183639230.png)

### 操作

![image-20260923183901324](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923183901324.png)

第一种用的最多

![image-20260923194127129](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923194127129.png)

> [!NOTE]
>
> java默认不能删除非空文件夹，但是可以通过方法递归，把文件夹下的文件都删除后，再删除此文件夹

![image-20260923194656909](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923194656909.png)

listFiles更常用

### 方法递归（多级文件搜索）

![image-20260923202210441](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923202210441.png)

![image-20260923202239694](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923202239694.png)

![image-20260923202258592](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923202258592.png)

Runtime那一段是弄了个虚拟机对象，运行代码时可以直接启动qq程序，但是只能运行可执行文件，图片什么的不行

### 字符集

a 97;    A 65

![image-20260923204627870](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923204627870.png)

![image-20260923204959357](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923204959357.png)

UTF-8

![image-20260923205556807](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923205556807.png)

### 字符集的编码解码操作

![image-20260923211342271](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923211342271.png)

![image-20260923210526544](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923210526544.png)

编码解码都是第二个方法用的多

![image-20260923210714059](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923210714059.png)

![image-20260923210912327](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923210912327.png)

![image-20260923211255335](C:\Users\唐诗涵\AppData\Roaming\Typora\typora-user-images\image-20260923211255335.png)