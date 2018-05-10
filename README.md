# the-road-of-leaarn-Java
Record the process of my study of Java
## 1Java的基础知识
### 1.1Java的主类结构
1.1.1第一个java程序
```java
public class First{
    static String s1 = "你好";
    public static void main(String[] args){
        String s2 = 'Java';
        System.out.println(s1);
        System.out.println(s2);
    }

}
```
1.1.2包声名-关键字package
1.1.3声名成员变量和局部变量
全局变量（成员变量）类的属性-声明在类体中-s1；
局部变量：方法中的属性-声明在方法体中-s2;
1.1.4编写主方法
main（）方法是类主体的主方法，public，static和void分别是main（）方法的权限修饰符，静态修饰符和返回值修饰符，main（）方法必须声明为public static void;
String[]args是一个字符串类型的数组，它是main()方法的参数；
注：main（）方法是程序开始执行的位置
1.1.5 导入API类库-import

### 1.2基本的数据类型
-  数值型
    - 整数类型：byte,short,int,long
    - 浮点型： float,double
 - 字符型
 - 布尔型
 
1.2.1整数类型
在java中可以用十进制，八进制，十六进制来表示整数；
注：不能以0开头表示整数；
定义int变量的实例
int x   # 定义int型变量x
int x,y # 定义int型变量x,y
int x=450,y=-462  # 定义int型变量x,y并赋值

```java
public class Number{
    public static void main(String[] args){
    byte mybyte = 124;
    short myshort = 3264;
    int myint = 45784612;
    long mylong = 4678451;
    long result = mybyte + myshort + myint + mylong;
    System.out.println("结果为：" + result）;
    }
}
```
1.2.2浮点类型
注：默认情况下小数都被看作为double类型，若使用float型小数，则需要在小数后面添加F或者f；
float类型的小数在声明的时候必须加"f",由于默认为d，不加的话会报错；
float f1 = 13.23f;
double d2 = 45678.1564;

1.2.3字符串类型
char型-存储的那个字符串，占用16位的内存空间，定义的时候用‘’表示
char x = 'a'
```java
package Number;

public class Gess {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		char word = 'd',word2 = '@';
		int p =23405,p2 = 45213;
		System.out.println("d在Unicode表中的顺序位置是："+(int)word);
		System.out.println("@在在Unicode表中的顺序位置是："+(int)word2);
		System.out.println("Unicode表中的第23045位置是："+(char)p);
		System.out.println("Unicode表中的第45213位置是："+(char)p2);
	}
}
```
转义字符

1.2.4布尔类型

boolean b;  #定义布尔类型变量b
boolean b1,b2;  #定义布尔变量b1,b2
boolean b=true;  #定义布尔类型变量b,并赋予初始值为true;

#todo变量与常量
### 1.3变量与常量
1.3.1标识符与关键字
标识符构成规则：
- 可以由任意字母，下划线，$符合数字组成；
- 第一个字符不能是数字；
- 标识符不能是保留的关键字；
1.3.2关键字
关键字就是已经被赋予特定意义的一些单词，不可以把它作为标识符使用；
1.3.3声明变量-告诉编辑器数据的类型，然后分配空间，以及能存储额数据类型；
```java
int age;   //声明int型变量
char char1 = 'r'；   //声明har型变量并赋值
```
1.3.4声明常量
常量-在程序执行过程中不会改变的量成为常量，通常也被称为“final变量”；
声明常量的标准形式
```java
//final 数据类型 常量名称[=值]
final double PI = 3.1415926D;   //声明double型常量PI并赋值
final boolean BOOL = true;      //声明boolean型常量BOOL并赋值
```
**注**：
常名称通常大写；
当定义的常量为全局变量时，必须在定义时就设定它的初值，否则将会产生编译错误；
1.3.5变量的有效范围
成员变量：类的成员变量分为静态变量和实例变量
```java
class var{
    int x = 45;     //声明x为实例变量
    static int 与= 90；    //声明y为静态变量（也称为类变量）
}
```
静态变量的有效范围可以跨类，甚至可以达到整个运用程序之类；其他类可以通过‘类名.静态变量’的方式在其他类内使用；
局部变量-在累的方法中定义的变量，局部变量只在当前的代码块中有效；
