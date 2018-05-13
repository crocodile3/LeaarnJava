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
### 1.4 运算符
1.4.1赋值运算符：‘=’
```java
int a=10;      //声明int类型变量a
int b =5;      //声明int型变量b
int c = a+b;    // 将变量a与变量b运算后的结果赋值给c
```
1.4.2 算术运算符
除：/
取余：%
```java
public class Arith {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		float number1 = 45.56f;
		int number2 = 152;
		System.out.println("和为："+number1+number2);
		System.out.println("差为："+(number2-number1));
		System.out.println("积为："+number1*number2);
		System.out.println("商为："+number1/number2);
	}

}
```
1.4.3自增自减运算符
```java
++a(-a)      //表示在使用变量a之前，先使a的值增加（减）1
a++(a+)      //表示在使用 变量a之后,使a的值增加（减）1
b=++a ;       //表示先将a的值加1，然后赋值给b，此时a的值为5，b的值为5（假设a=4）
b=a++;        //表示先将a的值赋给b，再将a的值变为5，此时a的值为5，b的值为4；
```
1.4.4 比较运算符
```java
public class Compare {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int number1 = 4;
		int number2 = 5;
		System.out.println("number1>number2的返回值为："+(number1>number2));
		System.out.println("number1==number2的返回值为："+(number1==number2));
		System.out.println("number1!=number2的返回值为："+(number1!=number2));
		System.out.println("number1>=number2的返回值为："+(number1>=number2));
		System.out.println("number1<=number2的返回值为："+(number1<=number2));

	}

}
```
1.4.5 逻辑运算符
逻辑运算符：与：&（&&），或：||，非:!
##注##：&与&&的区别-&&当判断第一个表达式为false时就不会往下判断，可以节省计算判断的次数 ；
```java
public class Caculation {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int a = 2 ;
		int b = 5;
		boolean result1 = ((a>b))&&(a!=b);
		boolean result2 = ((a>b)||(a!=b));
		System.out.println(result1);
		System.out.println(result2);

	}

}
```

1.4.6 位运算符
<1>“按位与”运算-&
运算法则：如果两个整型的数据a，b对应的位都是1，则解雇位才是1，否则为0；
<2>“按位或”运算-|
运算法则：如果两个操作数对应的位都是0,则结果为才是0，否则为1；
<3>”按位取反(按位非)“运算-~
运算法则：将操作数二进制中的1改为0,0改为1；
<4>“按位异或”-^
运算法则：当两个操作数的二进制表示相同（同为0,或同为1）时，结果才为0，否则为1；
<5>移位操作
<<:左移
>>:右移
>>>:无符号移动
移位运算支持的数据类型：byte,short,char,int,log;

### 1.5数据类型转换
1.5.1 隐式转换：从低级类型向高级类型的转换，系统自动执行，无需人为操作
类型按精度由低到高的排序为：byte<short<int<long<float<double
```java
public class Cover {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		byte mybyte = 127;
		int myint = 150;
		float myfloat = 452.12f;
		char mychar = 10;
		double mydouble = 4.46546;
		System.out.println("byte型与float型数据进行运算的结果为："+(mybyte+myfloat));
		System.out.println("byte型与int型数据进行运算的结果为："+(mybyte*myint));
		System.out.println("byte型与char型数据进行运算的结果为："+(mybyte/mychar));
		System.out.println("char型与double型数据进行运算的结果为："+(mydouble*mychar));
	}
```
1.5.2 显式类型转换
显示转换（强制转换）：高精度转换为低精度
```java
int a =(int)45.23;       //此时输出a的值为45
long y = (long)456.6f    //此时输出y的值456d
int b =(int)''             //此时输出b的值为100
```

### 1.6代码的注释与编码规范
1.6.1 注释
<1>单行注释-"//"
<2>多行注释-"/**/":多行注释可以嵌套单行注释，但是多行注释不能嵌套多行注释
```java
/*
注释1
注释2
......
注释n
*/
<3>文档注释
"/**文档注释内容*/"
``` 
1.6.2 编码规范
- 每条语句独占一行，一条命令要以分号结束；
- 在声明变脸过的时候，尽量使每个变量的声明独占一行；
- 关键字与关键字之间如果有多个空格的话，这些空格均被视为一个；

### 1.7流程控制
1.7.1复合语句
复合语句以开括号"{"开始，闭括号"}"结束；
```java
public class Compound {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int x =20;
		{
			int y =40;
			System.out.println(y);
			int z = 245;
			boolean b;
			{
				b = y >z;
				System.out.println(b);
			}
		}
		String word = "hello Java";
		System.out.println(word);

	}

}
```
1.7.2 条件语句
<1>if条件语句
语句语法
```java
if(布尔表达式){
    语句序列
}
```
注：当只有一条语句时，可以省略条件语句中的"{}"
```java
int a =100;
    if(a==100)
    System.out.print("a的值是100")
```
```java
public class Getif {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int x = 45;
		int y =12;
		if(x>y){
			System.out.println("变量x大于变量y");
		}
		if(x<y){
			System.out.println("变量x大于变量y");
		}

	}

}
```
1.7.3 if...else语句
语法
```java
if(表达式){
     若干语句
}
else{
    若干语句
}
```
```java
public class Getifelse {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int math = 95;
		int english =56;
		if (math>60){
			System.out.println("数学及格");
		}else{
			System.out.println("数学没有及格");
		}
		if(english>60){
			System.out.println("英语及格");
		}else{
			System.out.println("英语没有及格");
		}

	}

}

```

1.7.4 if...else if多分支语句
语法
```java
if（条件表达式1）{
    语句序列1}
else if(条件表达式2){
    语句序列2
}
...
else if(表达式n){
    语句序列n
}
```
```java
public class GetTerm {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int x =20;
		if(x>30){
			System.out.println("a的值大于30");
		}
		else if(x>10){
			System.out.println("a的值大于10，但小于30");
		}
		else if(x>0){
			System.out.println("a的值大于0，但小于10");
		}
		else{
			System.out.println("a的值小于0");
		}

	}

}
```

1.7.5switch多分支语句
使用if语句来检测变量是否符合某个条件，实现多选一的选择效果
语法
```java
switch(表达式）
{
case 常量值1：
    语句块1
    [break;]
......
case 常量值n:
    语块句n
    [break;]
defaulf;
    语块句n+1:
    [break]
}
```
switch语句首先计算表达式的值，如果表达式的值和某个case后面的变量值相同，则执行case语句后的若干个语句直到遇到break语句为止，如果该case语句中没有break语句，将继续执行后面case中的若干个语句，直到遇到break语句为止，若没有一个常量值与表达式的值相同，则执行default后面额语句，default语句为可选语句，如果不存在，且switch语句中表达式值不予任何case的常量值相同，switch不做任何处理。
```java
public class GetSwitch {

	public static void main(String[] args) {
		// TODO 自动生成的方法存根
		int week = 2;
		switch (week){
			case 1:
				System.out.println("Monday");
				break;
			case 2:
				System.out.println("Tuesday");
			case 3:
				System.out.println("Wednesday");
				break;
			default:
				System.out.println("Sorry,i don't know");
		}

	}

}
```
