# Java-Foundation

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

**4.Java数据类型转换（对于除了boolean之外的七种基础数据类型）**

​	分为自动类型提升和强制类型转换。

​	自动类型提升：容量小的数据类型的变量与容量大的数据类型的变量做运算自动往容量大的数据类							   型的变量转换。

​		                       char、byte、short----->int------>long------>float------>double

​							   当byte、short、char三种数据类型的变量做运算时，结果为int型。

​	强制类型转换：容量大的数据类型的变量往容量小的数据类型的变量转换。

​		