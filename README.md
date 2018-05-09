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
