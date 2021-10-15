# Java-Foundation

2021/10/7

**1.Java语言的特点**

​	1）面向对象（封装、继承、多态）

​	2）健壮性

​	3）跨平台（一次编译，多处运行）

**2.JDK与JRE的区别**

​	JDK包括JRE和java开发工具，可以用于开发和运行Java程序。

​	JRE包括JVM和Java标准类库，只能用于运行Java程序。

**3.数据类型**

​	分为基础数据类型和引用数据类型。

​	基础数据类型包括**byte、short、int、long、float、double、char、boolean**

​	引用数据类型包括**类（class）、接口（interface）、数组（[]）**

​	整型常量默认类型为int型，浮点常量默认类型为double型。

**4.Java数据类型转换（对于除了boolean之外的七种基础数据类型）**

​	分为自动类型提升和强制类型转换。

​	自动类型提升：容量小的数据类型的变量与容量大的数据类型的变量做运算自动往容量大的数据类							   型的变量转换。

​		                       char、byte、short----->int------>long------>float------>double

​							   当byte、short、char三种数据类型的变量做运算时，结果为int型。

​	强制类型转换：容量大的数据类型的变量往容量小的数据类型的变量转换。

2021/10/8

**5.String类型变量的使用**

​	1）String属于引用数据类型

​	2）声明String类型变量时，使用“”，同char不同，char是用‘’

​	3）String可以和其他8种基本数据类型做运算，且运算只能是连接运算 “+”

​	4）运算的结果仍然是String类型

**6.一维数组**

​	**6.1一维数组的声明和初始化**

​		int [] arr;//一维数组的声明

​		arr = new int[]{1,2,3,4,5};//静态初始化

​		int[] arr1 = new int[5];//动态初始化

​		ps：无论是哪种初始化方式，只要初始化完成，数组的长度便已确定了。

​	**6.2一维数组的调用方式**

​		采用角标访问方式，例如 Int[] nums = new nums[]{1,2,3}; nums[0]访问数组的第一个元素

​	**6.3一维数组获取数组长度的方法**

​		使用数组名.length的方法获取数组长度

​	**6.4一维数组如何遍历**

​		for(int i=0;i<arrName.length;i++){

​			//在此进行操作

​		}

​	**6.5一维数组元素的默认值**

​		1）基础数据类型

​			①整型元素：包括byte、short、int、long类型的数组元素的默认值均为0

​			②浮点型元素：包括float、double类型的数组元素的默认值均为0.0

​			③char型元素：默认值为ASCII的0

​			④boolean型元素：默认值为false

​		2）引用数据类型

​			引用数据类型的默认值均为null

​	2021/10/9

​	**6.6一维数组内存解析**

​		1）内存结构

​		![image-20211009092105499](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211009092105499.png)

​			局部变量存放在栈中，在方法中声明的变量都是局部变量。

​			new出来的对象存放在堆中，数组等

​			常量池存放常量，静态域存放静态成员（static定义的）

​		2）数组内存解析![image-20211009091536747](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211009091536747.png)

**7.二维数组**

​	**7.1二维数组的生命和初始化**

​		int[] [] arr ;//初始化

​		arr = new int[] []{{1,2,3},{1,2,4}};//静态初始化

​		int[] [] arr1 = new int[3] [2];//动态初始化一

​		int [] [] arr2 = new int[3] [];//动态初始化二

​	**7.2二维数组的调用方式**

​		arr[0] [1];

​	**7.3二维数组获取数组长度的方式**

​		1）获取外层数组的长度

​		arrName.length;

​		2）获取内层数组的长度

​		arrName[i].length;//第i行有多少个元素

​	**7.4二维数组如何遍历**

​		for(int i = 0;i<arrName.length;i++){

​			for(int j = 0;j<arrName[i].length;j++){

​				//在此进行操作

​			}

​		}

​	**7.5二维数组元素的默认值**

​		1）对于动态初始化一来说：

​			①外层元素的初始值为地址值

​			②内层元素的初始值同一维数组元素初始值

​		2）对于动态初始化二来说：

​			①外层元素的初始值为null，因为是空数组，数组是引用类型元素

​			②内层元素的初始值没有，报错，指针没有指向任何地方

​	**7.6二维数组内存解析**

​		1）动态初始化一内存结构![image-20211009100044121](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211009100044121.png)

​		2）动态初始化二内存结构

![image-20211009100527651](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211009100527651.png)

**8.数组使用中的常见异常**

​	**8.1数组角标越界异常：ArrayIndexOutOfBoundsException**

​		角标不在规定范围内，比如数组有5个元素，访问5处的元素，出现越界，因为索引最大为元素数		量-1

​	**8.2空指针异常：NullPointerException**

​		1）声明数组并且静态初始化之后，再给数组赋值为null，此时访问数组元素会出现空指针异常

​		2）二维数组动态初始化二之后访问内层元素出现空指针异常

​		3）索引对应的数组元素为空，此时访问出现空指针异常

2021/10/10

**9.Java面向对象和面向过程的区别**

​	面向对象强调了具备功能的对象，以类/对象为最小单位

​	面向过程强调了功能行为，以函数为最小单位

**10.对象声明内存解析**

​	写一个Person类，类中有name、age、isMale三个属性，age赋值为1。

​	Person p1 = new Person();

​	p1.name = "Tom";

​	p1.isMale = true;

​	Person p2 = new Person();

​	Person p3 = p1;

​	在方法中声明的变量为布局变量，存放在内存的栈中，所以：p1、p2、p3均在栈中；

​	new出来的对象均存放在内存的堆中；

​	属性是成员变量，因此存放在内存中的堆中；

​	新声明的对象令其等于之前声明的对象，实则是将之前对象的地址赋给此对象，因此对于人和修改	两个对象都是共通的。

​	![image-20211010105017066](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211010105017066.png)

**11.成员变量（属性）和局部变量的区别**

​	1）在类中的声明位置不同

​		属性直接定义在类的一对{}中

​		局部变量声明在方法内、方法形参、代码块内、构造器形参、构造器内部的变量

​	2）默认初始化值不同

​		属性根据其类型默认初始化

​		局部变量没有初始化值，一定要显式赋值

​	3）内存中加载的位置不同

​		属性加载到堆空间中（非static）

​		局部变量加载到栈空间中

202110/11

**12.return关键字的使用**

​	使用范围：方法体内使用

​	作用：结束方法、返回数据、

​	ps：return后面不能声明执行语句

**13.对象数据的内存解析**

​	Student[] stus = new Student[5];//声明一个Student类型的数组，Student类型为引用型

​	stus[0] = new Student();

​	Student类中有number、state、score属性

​	![image-20211011141747521](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211011141747521.png)

**14.匿名对象使用**

​	创建的没有显式地赋值给变量的对象，即为匿名对象。

​	例如：new Student.getNumber();

​				new Student.getNumber();

​	这两个不是同一个对象，匿名对象只能调用一次

**15.方法重载**

​	在**同一个类**中允许存在**同一个名**的方法，只要参数个数或者参数类型不同（**参数列表** 有顺序，类似排列）

**16.可变个数形参**

​	public void Show(String .. str){

​		

​	}

​	调用此方法时，传入的参数个数可以为1-n个

​	可变形参必须在最后声明且只能声明一个，同名的方法之间构成重载

​	不能和 public void Show(String [] str)共存

**17.封装与隐藏（面向对象特征1）**

​	将属性声明为私有的，通过方法进行限制条件的添加是封装的体现之一。

​	将属性声明为私有的，给其添加get、set方法。

​	封装性的体现：①属性私有化；②不对外暴露私有的方法；③构造方法...

**18.Java规定的四种权限**

​	![image-20211015160014549](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20211015160014549.png)



**19.权限修饰符修饰的结构**

​	类及类的内部结构：属性、方法、构造器、内部类。

​	ps：修饰类只能用public或者缺省。

20.构造器

​	待续...
