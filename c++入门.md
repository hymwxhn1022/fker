# c++入门

## 目录
- [c++入门](#c入门)
  - [目录](#目录)
  - [1 初时c++](#1-初时c)
    - [1.1 基础格式](#11-基础格式)
    - [1.2 注释](#12-注释)
    - [1.3 变量常量](#13-变量常量)
    - [1.4 关键字](#14-关键字)
    - [1.5 标识符命令规则](#15-标识符命令规则)
  - [2 数据类型](#2-数据类型)
    - [2.1 整形](#21-整形)
    - [2.2 浮点型](#22-浮点型)
    - [2.3 字符型](#23-字符型)
    - [2.4 转义字符](#24-转义字符)
    - [2.5 字符串型](#25-字符串型)
    - [2.6 布尔类型](#26-布尔类型)
    - [2.7 数据的输入](#27-数据的输入)
  - [3 运算符](#3-运算符)
    - [3.1 算数运算符](#31-算数运算符)
    - [3.2赋值运算符](#32赋值运算符)
    - [3.3 比较运算符](#33-比较运算符)
    - [3.4 逻辑运算符](#34-逻辑运算符)
  - [4 程序流程结构](#4-程序流程结构)
    - [4.1 选择结构](#41-选择结构)
      - [4.1.1 if语句](#411-if语句)
      - [4.1.2 三目运算符](#412-三目运算符)
      - [4.1.3 switch语句](#413-switch语句)
    - [4.2 循环结构](#42-循环结构)
      - [4.2.1 while循环语句](#421-while循环语句)
      - [4.2.2 do...while 循环](#422-dowhile-循环)
      - [4.2.3 for循环](#423-for循环)
      - [4.2.4 嵌套循环](#424-嵌套循环)
    - [4.3 跳转语句](#43-跳转语句)
      - [4.3.1 break语句](#431-break语句)
      - [4.3.2 continue语句](#432-continue语句)
      - [4.3.3 goto语句](#433-goto语句)
  - [5 数组](#5-数组)
    - [5.1 概述](#51-概述)
    - [5.2 一维数组](#52-一维数组)
      - [5.2.1 一维数组的定义方式](#521-一维数组的定义方式)
      - [5.2.2 一维数组数组名](#522-一维数组数组名)
      - [5.2.3 冒泡排序](#523-冒泡排序)
    - [5.3 二维数组](#53-二维数组)
      - [5.3.1 二维数组的定义方式](#531-二维数组的定义方式)
      - [5.3.2 二维数组数组名](#532-二维数组数组名)
      - [5.3.3 二维数组应用案例](#533-二维数组应用案例)
  - [6 函数](#6-函数)
    - [6.1 函数概述](#61-函数概述)
    - [6.2函数定义](#62函数定义)
    - [6.3 函数的调用](#63-函数的调用)
    - [6.4 值传递](#64-值传递)
    - [6.5 函数的常见样式](#65-函数的常见样式)
    - [6.6 函数的声明](#66-函数的声明)
    - [6.7 函数的分文件编写](#67-函数的分文件编写)
    - [6.8 函数重载](#68-函数重载)
      - [6.8.1 函数重载概述](#681-函数重载概述)
    - [7.3 指针所占内存空间](#73-指针所占内存空间)
    - [7.4 const修饰指针](#74-const修饰指针)
    - [7.6 指针和数组](#76-指针和数组)
    - [7.7 指针和函数](#77-指针和函数)
    - [7.8 指针、数组、函数](#78-指针数组函数)
  - [8 结构体](#8-结构体)
    - [8.1 结构体基本概念](#81-结构体基本概念)
    - [8.2 结构体定义和使用](#82-结构体定义和使用)
    - [8.3 结构体数组](#83-结构体数组)
    - [8.4 结构体指针](#84-结构体指针)
    - [8.5 结构体嵌套结构体](#85-结构体嵌套结构体)
    - [8.6 结构体做函数参数](#86-结构体做函数参数)
    - [8.7 结构体中const使用场景](#87-结构体中const使用场景)
    - [8.8 结构体案例](#88-结构体案例)
      - [8.8.1 案例1](#881-案例1)
      - [8.8.2 案例2](#882-案例2)



## 1 初时c++

###  1.1 基础格式

```cpp
#include "iostream"

int main(){

}
```





###  1.2 注释

**单行注释**: `  // 注释内容  `
**多行注释**: `  /* 注释内容 */  `





### 1.3 变量常量

**变量**:  数据类型 变量名 = 初始值
```cpp
#include "iostream"

int main(){

  int a = 10;

  return 0;
}
```

**常量**: 用于记录不可更改的数据
**两种定义方式**:  
  1.  #define  宏常量: ` #define 常量名 常量值 `  > 通常在文件上方定义，表示一个常量 
  2.  const 修饰的变量: ` const 数据类型 常量名 = 常量值 `  > 通常在变量定义前加上关键字const==，修饰该变量为常量，不可修改 

```cpp
//  宏常量
#define day 7

#include "iostream"

int main(){
  
  std::cout << day <<std::endl;

//  const修饰变量
  
  const int month = 12;
  
  std::cout << month <<std::endl;

  return 0;
}
```
- [目录](#目录)





### 1.4 关键字

**作用**: c++中预先保留的单词(标识符)  > 在定义变量或常量时，不要使用关键字 

ex:

 int,double,if,while,else,main
- [目录](#目录)





###  1.5 标识符命令规则

**规则**: 
* 不能时关键字
* 只能由数字，字母，下划线组成 
* 第一个字符必须为字母或者下划线
* 字母必须区分大小写
- [目录](#目录)





## 2 数据类型

### 2.1 整形

**作用**: 表示整数类型的数据
- [目录](#目录)





### 2.2 浮点型

**作用**: 表示小数

浮点型变量分为两种: 
* 单精度float
* 双精度double

两者的区别在于表示有效数字范围的不同。

float 4字节 7位有效数字

double 8字节 15~16位有效数字
- [目录](#目录)





### 2.3 字符型

**作用**: 用于显示单个字符

>显示字符型变量时，用单括号将字符括起来，不要用双引号，单引号内只能有一个字符，不能是字符串

>字符型变量存储时将对应的ASCII编码放入到存储单元
 
- [目录](#目录)





### 2.4 转义字符
**作用**: 用于表示一些不能显示出来的ASCII字符

**常见的转义字符**: 
* \n 换行
* \t 水平制表符
* \\\\ 代表一个 \ 字符
* \' 代表一个 '
* \" 代表一个 "
* \? 代表一个 ? 
* \ddd 八进制转移字符
* \xhh 十六进制转义字符
- [目录](#目录)





### 2.5 字符串型

**作用**: 用于表示一串字符

**两种风格**

* ` c语言风格: char 变量名[] = "字符串" `

ex: 

```cpp
#include "iostream"

int main(){
  char str1[] = "fuck you";

  std::cout << str1 <<std::endl;

}
```   
> c风格字符串需要用双引号括起来 

```cpp
#include "iostream"

#include "string"

int main(){
  
  string ch = "fuck you";

  std::cout << ch << std::endl;

}
```
> c++风格字符串，需要在加入头文件 #include "string" 
- [目录](#目录)





### 2.6 布尔类型

**作用**: 代表真或假的值

bool类型只有两个值: 
* true  ---- 真(本质是1)
* false ---- 假(本质是0)
  
**bool类型占一个字节**

- [目录](#目录)





### 2.7 数据的输入

**作用**: 从键盘获取数据

**关键字**: cin

**语法**: ` cin >> 变量 `

ex:

```cpp
#include "iostream"

int main(){

  int a = 0;

  cin >> a;

  std::cout << a << std::endl;

}
```
- [目录](#目录)





## 3 运算符

**作用**: 用于执行代码的运算

算数运算符    用于处理四则运算
赋值运算符    用于将表达式的值赋值给变量
比较运算符    用于表达式的比较，并返回一个真或假值
逻辑运算符    根据表达式的值返回真或假值





### 3.1 算数运算符

*  +: 加法
*  -: 减法
*  *: 乘法
*  /: 除法
*  %: 取模  > 只有整型变量可以取模 
* ++: 自加运算符
* --: 自减运算符

- [目录](#目录)





### 3.2赋值运算符

| **运算符** | **术语** | **示例**   | **结果**  |
| ---------- | -------- | ---------- | --------- |
| =          | 赋值     | a=2; b=3;  | a=2; b=3; |
| +=         | 加等于   | a=0; a+=2; | a=2;      |
| -=         | 减等于   | a=5; a-=3; | a=2;      |
| *=         | 乘等于   | a=2; a*=2; | a=4;      |
| /=         | 除等于   | a=4; a/=2; | a=2;      |
| %=         | 模等于   | a=3; a%2;  | a=1;      |

- [目录](#目录)





### 3.3 比较运算符

| **运算符** | **术语** | **示例** | **结果** |
| ---------- | -------- | -------- | -------- |
| ==         | 相等于   | 4 == 3   | 0        |
| !=         | 不等于   | 4 != 3   | 1        |
| <          | 小于     | 4 < 3    | 0        |
| \>         | 大于     | 4 > 3    | 1        |
| <=         | 小于等于 | 4 <= 3   | 0        |
| \>=        | 大于等于 | 4 >= 1   | 1        |





### 3.4 逻辑运算符

* !: 非
* &&： 与
* ||：或
- [目录](#目录)
  



  
## 4 程序流程结构

* 顺序结构: 程序按顺序执行，不发生跳转
* 选择结构: 依据条件是否满足，有选择的执行相应功能
* 循环结构: 依据条件是否满足，循环多次执行某段代码
  




### 4.1 选择结构

#### 4.1.1 if语句

**执行满足条件的语句**

if语句的三种形式

* 单行格式if语句
* 多行格式if语句
* 多条件if语句

1.单行格式if语句 : ` if(条件){ 条件满足时执行的语句 } `

ex: 

```cpp
#include "iostream"

int main(){

  int score = 0;

  std::cout << "输入你的分数:" << std::endl;

  cin >> score;

  // if语句后不要加分号
  if (score > 440){

    std::cout << "成功录取" << std::endl;

  }
}

```

2.多行格式if语句: ` if(条件){条件满足执行语句} else{条件不满足执行语句} `

ex: 

```cpp
#include "iostream"

int main(){

  int score = 0;

  std::cout << "输入你的分数:" << std::endl;

  cin >> score;

  if (score > 440){

    std::cout << "恭喜录取" << std::endl;
  
  }

  else{

    std::cout << "落榜惹" << std::endl;

  }
}

```

3.多条件if语句: ` if(条件1){条件1满足执行语句} else if(条件2){条件2满足执行语句} else{都不满足执行语句} `

ex: 

```cpp
#include "iostream"

int main(){

  int score = 0;

  std::cout << "输入你的分数" << std::endl;

  cin >> score;

  if (score > 500){

    std::cout << "录取一本" << std::endl;

  }

  else if (score > 440){

    std::cout << "录取二本" <<  std::endl;

  }

  else{

    std::cout << "落榜惹" << std::endl;

  }
}
```

**嵌套if语句**: 在if语句中，可以嵌套使用if语句，达到更精准的条件判断

案例需求: 

* 提示用户输入一个高考分数，根据分数做出一下判断
* 分数高于600视为考上一本，大于500视为考上二本，大于400视为考上三本，其余视为落榜
* 在一本分数中，如果大于700分，考入清华，大于650，考入北大，大于600，考入人大
  
ex: 
```cpp
#include "iostream"

int main(){

  int score = 0;

  std::cout << "输入你的分数:" << std::endl;

  cin >> score;

  if (score > 600){

    if (score > 700){

      std::cout << "录取清华" << std::endl;

    }
    else if (score > 650){

      std::cout << "录取北大" << std::endl;

    }
    else {

      std::cout << "录取人大" << std::endl;

    }
  }
  else if (score > 500){

    std::cout << "录取二本" << std::endl;

  }
  else if (score > 400){

    std::cout << "录取三本" << std::endl;

  }
  else{

    std::cout << "落榜惹" << std::endl;
    
  }
}
```
- [目录](#目录)
  





#### 4.1.2 三目运算符

**作用**: 实现简单的判断

**语法**: ` 表达式1 ? 表达式2 : 表达式3 `

**解释**: 如果表达式1的值为真,执行表达式2,并返回表达式2的结果；

          如果表达式1的值为假,执行表达式3,并返回表达式3的结果.

ex: 
```cpp
#include "iostream"

int main(){

  int a = 10;
  int b = 20;
  int c = 0;

  c = (a > b ? a : b);
  
  std::cout << "c = " << c << std::endl;

  //c++中三目运算符返回的是变量，可以继续赋值

  (a > b ? a : b) = 100;

  std::cout << "a = " << a << std::endl;

  std::cout << "b = " << b << std::endl;

  std::cout << "c = " << c << std::endl;
}
```
>与if语句比较，三目运算符优点短小整洁，缺点如果使用嵌套，结构不清晰
- [目录](#目录)





#### 4.1.3 switch语句

**作用**: 执行多条件分支语句

**语法**: 
  ```cpp
    switch(表达式){

      case 结果1: 执行语句;break;

      case 结果2: 执行语句;break;

      default: 执行语句;break;
    }

  ```

ex:
```cpp
#include "iostream"

int main(){

  // 给电影评分
  // 10 ~ 9 经典
  //  8 ~ 7 非常好
  //  6 ~ 5 一般
  //  5分一下 烂片

  int score = 0;

  std::cout << "请给电影打分" << std::endl;

  cin >> score;

  switch (score){

    case 10:
    case 9:
      std::cout << "经典" << std::endl;
      break;  
    case 8:
    case 7:
      std::cout << "非常好" << std::endl;
      break;
    case 6:
    case 5:
      std::cout << "一般" << std::endl;
      break;
    default:
      std::cout << "烂片" << std::endl;
      break;
  }
}
```

>switch语句中表达式类型只能是整形或者字符型

>case里如果没有break，那么程序会一直向下执行，直到碰到break

>与if语句相比，对于多条件判断时，switch的结构清晰，执行效率高，缺点不能判断期间

- [目录](#目录)





### 4.2 循环结构

#### 4.2.1 while循环语句

**作用**: 满足循环条件，执行循环语句

**语法**: ` while(循环条件){循环语句} `

只要循环条件结果为真，就执行循环语句

ex: 

```cpp
#include "iostream"

int main(){

  int num = 0;

  while (num = 0){

    std::cout << "num = " << num << std::endl;
    num++;
  }
}
```
 >在执行循环语句时候，程序必须提供跳出循环的出口，否则出现死循环


案例需求: 系统随机生成一个1到100之间的数字，玩家进行猜测，如果猜错，提示玩家数字过大或过小，如果猜对恭喜玩家胜利，并且退出游戏。


```cpp
#include "iostream"
#include "cstdlib"

int main(){

	int res = rand()%100+1; //生成随机数

	std::cout << res << std::endl;

	int x = 0;

	std::cout << "从1~100猜测一个数字" << std::endl;
	cin >> x;

	while ( x != res){

		if (x > res){
			std::cout << "数字过大" << std::endl;
			std::cout << "从1~100猜测一个数字" << std::endl;
			cin >> x;
		}

		if (x < res){
			std::cout << "数字过小" << std::endl;
			std::cout << "从1~100猜测一个数字" << std::endl;
			cin >> x;
		}
	}

	std::cout << "恭喜猜对" << std::endl;

}

```
- [目录](#目录)





#### 4.2.2 do...while 循环

**作用**: 满足循环条件，执行循环语句

**语法**: ` do{循环语句} while(循环条件) `

**注意**: 与while的区别在于，do...while会先执行以次循环语句，再判断循环条件

 
```cpp
#include "iostream"

int main(){

  int num = 0;

  do{

    std::cout << num << std::endl;
    num++;

  }

  while (num < 10);
}
```
> 与while循环的区别，do...while先执行一次循环语句，再判断循环条件 

**案例**: 水仙花数

**描述**: 水仙花数是指一个三位数，它的每位上的数字的三次幂之和等于他本身 

ex: 1^3 + 5^3 + 3^3 = 153

```cpp
#include "iostream"

int main(){

	int i = 100;

	while (i < 1000){
		int a,b,c;
		a = i % 10;
		b = i / 10 % 10;
		c = i / 100;

		if (a*a*a + b*b*b + c*c*c == i)
			std::cout << i << std::endl;

		i++;
	}
}
```
- [目录](#目录)





#### 4.2.3 for循环

**作用**: 满足循环条件，执行循环语句

**语法**: ` for(起始表达式;条件表达式;末尾循环体) {循环语句;} `

ex:

```cpp
#include "iostream"

int main(){

  for (int i = 0;i < 10;i++){

    std::cout << i << std::endl;
  }

}
```

>for循环中的表达式，要用分号进行分隔   

>for循环结构比较清晰，比较常用 

**案例**: 敲桌子

**描述**: 从1开始数到数字100，如果数字个位含有7，或者数字十位含有7，或者数字是7的倍数，打印敲桌子，其余直接打印输出

```cpp
#include "iostream"

int main(){
	for (int i = 1;i < 100;i++){

		int x,y;

		if (i < 10){
			y = i;
			x = i;
		}	

		else{
			x = i % 10;
			y = i / 10;
		}	

		int z = i % 7;

		if (x == 7 || y == 7 || z == 0)
			std::cout << "敲桌子" << std::endl;

		else 
			std::cout << i << std::endl;

	}		
}
```
- [目录](#目录)





#### 4.2.4 嵌套循环

**作用** : 循环体中再嵌套一层循环，解决一些问题

ex:
```cpp
#include "iostream"

int main(){

  for (int i = 0;i < 10;i++){
    for (int j = 0;j < 10;j++){
      std::cout << "*" << " ";
    }
    std::cout << std::endl;
  }
}
```

**案例** : 乘法口诀表

描述: 利用嵌套循环，实现九九乘法表

```cpp
#include "iostream"

int main(){

	for (int i = 1; i < 10; i++){
		for (int j = 1; j < i+1; j++){
			std::cout << i << "*" << j << "=" << i*j << "  ";
		}
		std::cout << std::endl;

	}

}

```
- [目录](#目录)





### 4.3 跳转语句

#### 4.3.1 break语句

**作用** : 用于跳出==选择结构==或者==循环结构

break使用的时机

* 出现在switch条件语句中，中止case并跳出switch
* 出现在循环语句中，跳出循环
* 出现在嵌套循环，跳出最近的内层循环语句

ex1: 

```cpp
#include "iostream"

int main() {
	//1、在switch 语句中使用break
	std::cout << "请选择您挑战副本的难度：" << std::endl;
	std::cout << "1、普通" << std::endl;
	std::cout << "2、中等" << std::endl;
	std::cout << "3、困难" << std::endl;

	int num = 0;

	cin >> num;

	switch (num)
	{
	case 1:

		std::cout << "您选择的是普通难度" << std::endl;
		break;

	case 2:

		std::cout << "您选择的是中等难度" << std::endl;
		break;

	case 3:

		std::cout << "您选择的是困难难度" << std::endl;
		break;

	}
}
```

ex2:

```cpp
#include "iostream"

int main() {
	//2、在循环语句中用break
	for (int i = 0; i < 10; i++)
	{
		if (i == 5)
		{
			break; //跳出循环语句
		}
		std::cout << i << std::endl;
	}
}
```

ex3: 

```cpp
#include "iostream"

int main() {
	//在嵌套循环语句中使用break，退出内层循环
	for (int i = 0; i < 10; i++)
	{
		for (int j = 0; j < 10; j++)
		{
			if (j == 5)
			{
				break;
			}
			std::cout << "*" << " ";
		}
		std::cout << std::endl;
	}
}
```
- [目录](#目录)





#### 4.3.2 continue语句

**作用**: 在循环语句中，跳过本次循环中剩下的语句，继续执行下一次循环

ex:

```cpp
#include "iostream"

int main(){

  for (int i = 0; i < 100; i++){

    if (i % 2 == 0) continue;
    std::cout << i << std::endl;
  }

}
```
> continue没有使循环终止，而break会跳出循环 
- [目录](#目录)





#### 4.3.3 goto语句

**作用**: 可以无条件跳转语句

**语句**: ` goto 标记; `

**解释**: 如果标记的名称存在，执行到goto语句时，会跳转到标记的位置

ex:

```cpp
#include "iostream"

int main(){

  std::cout << "1" << std::endl;

  goto FLAG;  // 设置标签

  std::cout << "2" << std::endl;
  std::cout << "3" << std::endl;
  std::cout << "4" << std::endl;

  FlAG:  // 跳转标签

  std::cout << "5" << std::endl;
  //输出内容 1 5
}
```
> 不推荐使用，易造成程序流程混乱 
- [目录](#目录)





## 5 数组

### 5.1 概述

数组: 就是一个集合，存放了相同类型的元素

**特点**: 数组中每个数据都是相同的数据类型，数组是由连续的内存组成的
- [目录](#目录)





### 5.2 一维数组

#### 5.2.1 一维数组的定义方式

三种方式:

* ` 数据类型 数组名[数组长度]; `
* ` 数据类型 数组名[数组长度] = {值1, 值2 ...} `
* ` 数据类型 数组名[] = {值1, 值2 ...} `

ex:

```cpp
#include "iostream"

int main(){

  //定义方式1
  //数据类型 数组名[元素个数];
  int score[10];

  //利用下标赋值
  score[0] = 100;  //数组第一个下标为0
  score[1] = 90;
  score[2] = 80;

  //利用下标输出
  std::cout << score[0] << std::endl;
	std::cout << score[1] << std::endl;
	std::cout << score[2] << std::endl;


  //第二种定义方式
  //数据类型 数组名[元素个数] = {值1, 值2...}
  //如果 {} 内数据数量不足，其余会用0补全
  int score[10] = {1,2,3,4,5}

  //逐个输出
  //std::cout << score2[0] << std::endl;
	//std::cout << score2[1] << std::endl;

  //利用循环输出
  for (int i = 0; i < 10; i++)
    std::cout << score2[i] << std::endl;

  //定义方式3
  //数据类型 数组名[] = {值1, 值2...}
  int score3[] = {1,2,3,4,5} //不会产生数据溢出

  for (int i = 0; i < 10; i++)
    std::cout << score3[i] << std::endl;
}
```


>1.数组名的命名规范与变量命名规范一致，不要与变量重名
- [目录](#目录)





#### 5.2.2 一维数组数组名

* 可以统计整个数组在内存的长度
* 可以获取数组在内存中的首地址

ex: 
```cpp
#include "iostream"

int main(){
  
  //数组名的作用
  //可以获取整个数组占用内存空间的大小

  int arr[10] = {1,2,3,4,5,6,7,8,9,10};
  
  std::cout << "整个数组所占用的空间" << sizeof(arr) << std::endl;  
  std::cout << "每个元素所占用的空间" << sizeof(arr[0]) << std::endl;
  std::cout << "数组的元素个数为" << sizeof(arr) / sizeof(arr[0]) << std::endl;

  //通过数组名获取数组首地址
  std::cout << "数组首地址" << arr << std::endl;
  std::cout << "数组中第一个元素地址"<< arr[0] << std::endl;

  //arr = 100; 错误，数组名是常量，因此不可以赋值
}
```


>注意: 数组名是常量，不可以赋值

>直接打印数组名，可以查看数组所占内存的首地址

>对数组名进行sizeof，可以获取整个数组占内存空间的大小


**练习案例1**: 五只小猪称体重

**案例描述**: 

在一个数组中记录了五只小猪的体重，如int arr[5] = {300, 350, 200, 400, 250};

找出并打印最重的小猪体重。

```cpp
#include "iostream" 

int main(){

	int a[] = {300, 350, 200, 400, 250};
	int x;
	int y;
	int i;

	while (i < 5){

		if (a[i] > a[i + 1]){
			x = a[i];
			y = i;
			i++;

		} 

		else {
			x = a[i + 1];
			y = i + 1;
			i++;
		}	

	}

	std::cout << "第" << y << "只" << "重" << x;

}

```

**练习案例2**: 数组元素逆置

**案例描述**: 请声明一个5个元素的数组，并将元素逆置

(如果原数组元素为: 1,3,2,5,4;  逆置后输出结果为: 4,5,2,3,1)

```cpp

#include "iostream"

int main(){
	
	int a[5] = {1, 2, 3, 4, 5};
	
	int len;
	
	len = sizeof(a) / sizeof(a[0]);   // len = 5
	
	int b[len];
		
	for (int i = 0; i < len; i++){
		b[i] = a[i];
	}
	
	for (int i = 0; i < len; i++){
		a[i] = b[len-1-i];
		std::cout << a[i]<< std::endl;
	}
}
```
- [目录](#目录)





#### 5.2.3 冒泡排序

**作用**: 最常用的排序算法，对数组内元素进行排序

1. 比较相邻的元素。如果第一个比第二个大，就交换他们两个
2. 对每对相邻的元素做同样的工作，执行完毕后，找到第一个最大值
3. 重复以上步骤每次比较次数-1，直到不需要比较

**ex:** 将数组{4, 2, 8, 0, 5, 7, 1, 3, 9}

```cpp

#include "iostream"

int main(){

	int arr[9] = {4, 2, 8, 0, 5, 7, 1, 3, 9};

	for (int i = 0; i < 9-1; i++){    //i到7就要截止，否则会出现arr[8]与arr[9]的情况，则会多出一个0，少一个9
		for (int j = 0; j < 9-1-i; j++){
			if (arr[j] > arr[j+1]){
				int temp;
				temp = arr[j];
				arr[j] = arr[j+1];
				arr[j+1] = temp;
			} 
		}
	}

	for (int i = 0; i < 9; i++)
		std::cout << arr[i] << std::endl;

}
```
- [目录](#目录)





### 5.3 二维数组

在一维数组的基础上，多加上一个维度


#### 5.3.1 二维数组的定义方式

四种方式:

* ` 数据类型 数组名[ 行数 ][ 列数 ]; `
* ` 数据类型 数组名[ 行数 ][ 列数 ] = { {值1, 值2}, {值3, 值4} }; `
* ` 数据类型 数组名[ 行数 ][ 列数 ] = {值1, 值2, 值3, 值4}; `
* ` 数据类型 数组名[  ][ 列数 ] = {值1, 值2, 值3, 值4}; `


> 以上4种定义方式，利用第二种更加直观，提高代码可读性


 ex:
 
```cpp

#include "iostream"

int main() {

	//方式1  
	//数组类型 数组名 [行数][列数]
	int arr[2][3];
	arr[0][0] = 1;
	arr[0][1] = 2;
	arr[0][2] = 3;
	arr[1][0] = 4;
	arr[1][1] = 5;
	arr[1][2] = 6;

	for (int i = 0; i < 2; i++)  //行数
	{
		for (int j = 0; j < 3; j++)  //列数
		{
			std::cout << arr[i][j] << " ";
		}
		std::cout << std::endl;
	}

	//方式2 
	//数据类型 数组名[行数][列数] = { {数据1，数据2 } ，{数据3，数据4 } };
	int arr2[2][3] =
	{
		{1,2,3},
		{4,5,6}
	};

	//方式3
	//数据类型 数组名[行数][列数] = { 数据1，数据2 ,数据3，数据4  };
	int arr3[2][3] = { 1,2,3,4,5,6 }; 

	//方式4 
	//数据类型 数组名[][列数] = { 数据1，数据2 ,数据3，数据4  };
	int arr4[][3] = { 1,2,3,4,5,6 };  // 通过列数会自动计算行数
}
```

> 在定义二维数组时，如果初始化了数据，可以省略行数

-[目录](#目录)





#### 5.3.2 二维数组数组名

* 查看二维数组所占内存空间
* 获取二维数组的首地址

ex:

```cpp

#include "iostream"

int main(){

  //二维数组数组名

  int arr[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
  };

  std::cout << "二维数组大小" << sizeof(arr) << std::endl;

  std::cout << "二维数组一行元素大小" << sizeof(arr[0]) << std::endl;

  std::cout << "二维数组元素大小" << sizeof(arr[0][0]) << std::endl;

  std::cout << "二维数组行数" << sizeof(arr) / sizeof(arr[0]) << std::endl;

	std::cout << "二维数组列数" << sizeof(arr[0]) / sizeof(arr[0][0]) << std::endl;

  // 地址

  std::cout << "二维数组首地址" << arr << std::endl;

	std::cout << "二维数组第一行地址" << arr[0] << std::endl;

	std::cout << "二维数组第二行地址" << arr[1] << std::endl;

	std::cout << "二维数组第一个元素地址" << &arr[0][0] << std::endl;

	std::cout << "二维数组第二个元素地址" << &arr[0][1] << std::endl;

}
```

>二维数组名就是数组首地址

>对二维数组名进行sizeof时，可以获取整个二维数组占用的内存空间大小

-[目录](#目录)





#### 5.3.3 二维数组应用案例

**考试成绩统计**: 

案例描述: 有三名同学(张三，李四，王五)，在一次考试中成绩如下，**请分别输出三名同学的总成绩**

|      | 语文 | 数学 | 英语 |
| ---- | ---- | ---- | ---- |
| 张三 | 100  | 100  | 100  |
| 李四 | 90   | 50   | 100  |
| 王五 | 60   | 70   | 80   |

```cpp
#include "iostream"
#include "string"
int main(){
	
	int scores[3][3] = {
		{100, 100, 100},
		{90, 50, 100},
		{60, 70, 80}
	};
	
  string name[3] = {"张三", "李四", "王五"};

	for (int i = 0; i < 3; i++){
    int sum = 0; 
		for (int j = 0; j < 3; j++){
			sum += scores[i][j];
		}
    std::cout << name[i] << "成绩为" << sum << std::endl;
	}
}
```
-[目录](#目录)





## 6 函数

### 6.1 函数概述

**作用**: 将一段经常使用的代码封装起来，减少重复代码

一个较大的程序，一般分为若干个程序块，每个模块实现特定功能

-[目录](#目录)







### 6.2函数定义

函数定义一般为5个步骤

 1. 返回值类型
 2. 函数名
 3. 参数列表
 4. 函数体语句
 5. return表达式

**语法**: 

```cpp 
返回值类型 函数名 (参数列表){

  函数体语句

  return表达式

}
```

* 返回值类型: 一个函数可以返回一个值。
* 函数名: 函数的名称
* 函数体语句: 函数内需要执行的语句
* return表达式: 与返回值类型相同，函数执行完后，返回相应的数据


**案例**: 定义一个加法函数，实现两数相加

```cpp

int add(int num1, int num2){

  int sum = num1 + num2;

  return sum;
}
```

-[目录](#目录)




### 6.3 函数的调用

**功能**: 使用定义好的函数

**语法**: ` 函数名(参数) `

ex:

```cpp

#include "iostream"

int add(int num1, int num2){  //定义中的num1, num2为形参

  int sum = num1 + num2;

  return sum;

} 

int main(){

  int a = 10;
  
  int b = 20;
  
  int sum = add(a, b);  //调用时的a, b为实参

  std::cout << "sum=" << sum << std::endl;

}

```

> 注意: 函数定义内称为形参，调用时传入的参数称为实参

-[目录](#目录)






### 6.4 值传递

* 值传递，就是函数调用时，实参的数值传入给形参
* 值传递时，如果形参发生改变，并不会影响实参

ex:

```cpp

#include "iostream"

void swap(int num1, int num2){  //void 函数没有返回值

  std::cout << "交换前" << std::endl;

  std::cout << "num1" << num1 << std::endl;

  std::cout << "num2" << num2 << std::endl;

  int temp;

  temp = num1;

  num1 = num2;

  num2 = temp;

  std::cout << "交换后：" << std::endl;

	std::cout << "num1 = " << num1 << std::endl;

	std::cout << "num2 = " << num2 << std::endl;
}

int main(){

  int a = 10;

  int b = 20;

  swap(a, b);

  std::cout << "a = " << a << std::endl;

  std::cout << "b = " << b << std::endl; 
}
```

> 值传递，形参改变不了实参

-[目录](#目录)





### 6.5 函数的常见样式

常见的函数样式有4种

1. 无参无返
2. 有参无返
3. 无参有返
4. 有参有返

ex:

```cpp

// 1. 无参无返

void test1(){

  //void a = 10;  //无类型不可以创建变量，原因无法分配内存

  std::cout << "this is test1" << std::endl;
}

// 2. 有参无返

void test2(int a){

  std::cout << "this is test2" << std::endl;

  std::cout << "a = " << a << std::endl;
}

// 3. 无参有返

int test3(){

  std::cout << "this is test3" << std::endl;

  return 10;
}

// 4. 有参有返

int test4(int a, int b){

  std::cout << "this is test4" << std::endl;

  int sum = a + b;

  return sum;
}
```

-[目录](#目录)





### 6.6 函数的声明

**作用**: 告诉编译器函数名称以及如何调用函数。函数的实际主体可以单独定义。

* 函数的**声明可以多次**，但是函数的**定义只能有一次**

ex:

```cpp

//声明
int max(int a, int b);

int max(int a, int b);

//定义

int max(int a, int b){

  return a > b ? a : b;
}

int main(){

  int a = 100;

  int b = 200;

  std::cout << max(a, b) << std::endl;
}
```
-[目录](#目录)





### 6.7 函数的分文件编写

**作用**: 让代码结构更加清晰

函数分文件编写一般有4个步骤

1. 创建后缀名为.h的头文件
2. 创建后缀名为.cpp的文件
3. 在头文件中写函数的声明
4. 在源文件中写函数的定义


ex:

```cpp

//swap.h文件
#include "iostream"

//实现两个数字交换的函数声明
void swap(int a, int b);
```

```cpp

//swap.cpp文件
#include "swap.h"

void swap(int a, int b){

  int temp = a;

  a = b;

  b = temp;

  std::cout << "a = " << a << std::endl;

  std::cout << "b = " << b << std::endl;
}
```

```cpp

//main函数文件
#include "swap.h"

int main(){

  int a = 100;

  int b = 200;

  swap(a, b);

}
```

-[目录](#目录)





### 6.8 函数重载

#### 6.8.1 函数重载概述

**作用:** 函数名可以相同，提高复用性

**函数重载满足条件:** 

* 同一个作用域下

* 函数名称相同

* 函数参数**类型不同** 或者**个数不同** 或者**顺序不同**

**注意:** 函数的返回值不可以作为函数重载的条件

ex:

```cpp

#include "iostream"

void func(){

  std::cout << "func的调用" << std::endl;

}

void func(int a){

  std::cout << "func (int a) 的调用" << std::endl;

}

void func(double a){

  std::cout << "func (double a) 的调用" << std::endl;

}

void func(int a, double a){

  cout << "func (int a, double a) 的调用" << std::endl;

}

void func(int b, double a){

  cout << "func (int b, double a) 的调用" << std::endl;

}

/*有返回值的函数不可重载

int func(double a, int b){
  
  std::cout << "func (double a, int b) 的调用" << std::endl;

}
*/

int main(){

  func();
  func(10);
  func(3.14);
  func(10, 3.14);
  func(3.14, 10);
  
}

```

-[目录](#目录)




#### 6.8.2 函数重载注意事项

* 引用可以作为重载条件

* 函数重载碰到函数默认参数

ex:

```cpp
//1.引用作为重载条件
void func(int &a){

  std::cout << " func (int &a) 调用 " << std::endl;

}

void func(const int &a){

  std::cout << " func (const int &a) 调用 " << std::endl;

}


//2.函数重载碰到函数默认参数

void func2(int a, int b = 10){

  std::cout << " func2(int a, int b = 10) 调用 " << std::endl;
  
}
```

## 7 指针

### 7.1 指针的基本概念

**作用**: 可以通过指针直接访问内存

* 内存编号是从0开始记录的，一般用十六进制数字表示
* 可以利用指针变量保存地址





### 7.2 指针变量的定义和使用

定义语法: ` 数据类型 *p;`

ex:

```cpp

#include "iostream"

int main(){

  // 指针的定义
  int a = 10;  //定义整形变量

  int *p;  //定义指针变量

  p = &a;  //指针变量指向a的地址

  std::cout << &a << std::endl;  //打印数据a的地址,十六进制数

  std::cout << p << std::endl;  //打印指针变量p

  // 指针的使用
  // 通过 * 操作指针变量指向内存
  std::cout << "*p = " << *p << std::endl;  //输出10
}
```

指针变量和普通变量的区别

* 普通变量存放的是数据，指针变量存放的是地址
* 指针变量可以通过" * "操作符，使指针变量指向内存空间，这个过程称为解引用

>通过 & 符号，获取变量的地址

>利用指针可以记录地址

>对指针变量解引用，可以操作指针指向的内存

-[目录](#目录)





### 7.3 指针所占内存空间

指针在32位系统中占4字节，在64位系统中占8字节

```cpp
int main() {

	int a = 10;

	int * p;

	p = &a; //指针指向数据a的地址

	cout << *p << endl; //* 解引用

	cout << sizeof(p) << endl;

	cout << sizeof(char *) << endl;

	cout << sizeof(float *) << endl;

	cout << sizeof(double *) << endl;

```

-[目录](#目录)





### 7.4 const修饰指针

**作用**: 定义常量或者限制变量的可修改性

三种情况

1. const修饰指针   --- 常量指针
2. const修饰常量   --- 指针常量
3. const即修饰指针，又修饰常量


ex:

```cpp

#include "iostream"

int main(){

  int a = 10;

  int b = 20;

  //const修饰的是指针，指针指向可以修改，指针指向的值不可以修改

  const int *p1 = &a;
  p1 = &b;  //True
  // *p1 = 100;  False

  //const修饰的是常量，指针指向不可以改，指针指向的值可以改

  int *const p2 = &a;
  //p2 = &b;  Flase
  *p2 = 100;  //True

  //const即修饰指针又修饰常量

  const int *const p3 = &a;
  //p3 = &b;   False
  //*p3 = 100;   False
}
```

>看const右侧紧跟着的是指针还是常量，是指针就是常量指针，是常量就是指针常量

-[目录](#目录)






### 7.6 指针和数组

**作用**: 利用指针访问数组中的元素

ex:

```cpp

#include "iostream"

int main(){

  int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

  int *p = arr;  //指向数组的指针

  std::cout << "第一个元素" << arr[0] << std::endl;

  std::cout << "指针访问第一个元素" << *p << std::endl;

  for (int i = 0; i < 10; i++){

    //利用指针遍历数组
    std::cout << *p << endl;
    p++;
    
  }
}
```

-[目录](#目录)





### 7.7 指针和函数

**作用**: 利用指针作函数参数，可以修改实参的值

ex:

```cpp

#include "iostream"

//值传递
void swap1(int a, int b){

  int temp = a;
  a = b;
  b = temp;

}

//地址传递
void swap2(int *p1, int *p2){

  int temp = *p1;
  *p1 = *p2;
  *p2 = temp;

  }

int main(){

  int a = 10;

  int b = 20;

  swap1(a, b);  //实参不改变
  cout << "a = " << a << endl;
	cout << "b = " << b << endl;

  swap2(a, b);  //实参改变
  cout << "a = " << a << endl;
	cout << "b = " << b << endl;

}
}
```

> 如果不想改变实参，就用值传递。如果想要改变实参，就用地址传递

 -[目录](#目录)





### 7.8 指针、数组、函数

**案例描述**: 封装一个函数，利用冒泡排序，实现对整形数组的升序排序

数组: int arr[10] = {4, 3, 6, 9, 1, 2, 10, 8, 7, 5};

ex:

```cpp

#include "iostream"

void sort(int *arr, int len){

  for (int i = 0; i < len - 1; i++){
    
    for (int j = 0; j < len - 1 - i; j++){

      if (a[j] > a[j + 1]){

        int temp = a[j];
        a[j] = a[j + 1];
        a[j + 1] = temp;
      
      }

    }
  }
}

void print(int *arr, int len){

  for (int i = 0;i < len; i++){

    std::cout << arr[i] << std::endl;
  }
}

int main(){

  int arr[10] = {4, 3, 6, 9, 1, 2, 10, 8, 7, 5};

  int len = sizeof(arr) / sizeof(arr[0]);

  sort(arr, len);

  print(arr, len);
}
```

>当数组名转入到函数作为参数时，被退化为指向首元素的指针

-[目录](#目录)





## 8 结构体

### 8.1 结构体基本概念

结构体属于用户自定义的数据类型，允许用户存储不同的数据类型





### 8.2 结构体定义和使用

**语法**: ` struct 结构体名 { 结构体成员列表 }; `

通过结构体创建变量的方式有三种:

1. struct 结构体名 变量名
2. struct 结构体名 变量名 = {成员1值, 成员2值...};
3. 定义结构体时顺便创建变量

ex:

```cpp

#include "iostream"
#include "string"

//结构体定义
struct student{

  std::string name;
  int age;
  int score;

}stu3;   //结构体变量创建方式3

int main(){

  //结构体变量创建方式1
  struct student stu1;  //struct关键字可以省略

  stu1.name = "张三";
  stu1.age = "18"
  stu1.score = 100;

  std::cout << "姓名：" << stu1.name << " 年龄：" << stu1.age  << " 分数：" << stu1.score << std::endl;

  //结构体变量创建方式2
  struct student stu2 = {"李四", 19, 90};

  std::cout << "姓名：" << stu2.name << " 年龄：" << stu2.age  << " 分数：" << stu2.score << std::endl;

  stu3.name = "王五";
	stu3.age = 18;
	stu3.score = 80;
	
	std::cout << "姓名：" << stu3.name << " 年龄：" << stu3.age  << " 分数：" << stu3.score << std::endl;
}
```

> 定义结构体时，关键字struct不可省略

> 创建结构体变量时，关键字struct可以省略

> 结构体变量利用操作符 ' 结构体变量名 ' . ' 变量名 ' 访问 

-[目录](#目录)





### 8.3 结构体数组

**作用**: 将自定义的结构体放入到数组中方便维护

**语法**: ` struct 结构体名 数组名[元素个数] = {{}, {}, {}...}; `

ex:

```cpp

#include "iostream"
#include "string"

struct student{

  std::string name;
  int age;
  int score;

};

int main(){

  //结构体数组
  struct student arr[3] = 
  {

    {"张三", 18, 80},
    {"李四", 19, 70},
    {"王五", 20, 90}

  };

  //遍历输出
  for (int i = 0; i < 3; i++){

    std::cout << "姓名：" << arr[i].name << " 年龄：" << arr[i].age << " 分数：" << arr[i].score << std::endl;

  }
}
```

-[目录](#目录)





### 8.4 结构体指针

**作用**: 通过指针访问结构体中的成员

* 利用操作符' -> '可以通过结构体指针访问结构体属性

ex:

```cpp

#include "iostream"
#include "string"

struct student{

  std::string name;
  int age;
  int score

};

int main(){

  struct student stu = { "张三", 18, 100};

  struct student *p = &stu;

  p -> score = 80;  //指针通过 -> 操作符可以访问成员

  std::cout << "姓名：" << p->name << " 年龄：" << p->age << " 分数：" << p->score << std::endl;
}
```

-[目录](#目录)





### 8.5 结构体嵌套结构体

**作用**: 结构体中的成员可以是另一个结构体

**例如**: 每个老师辅导一个学员，一个老师的结构体中，记录一个学生的结构体

ex:

```cpp

#include "iostream"
#include "string"

struct student{

  std::string name;
  int age;
  int score;

};

struct teacher{

  int id;
  std::string name;
  int age;
  struct student stu;

};

int main(){

  teacher t1;
  t1.id = 10000;
  t1.name = "老王";
  t1.age = 40;

  t1.stu.name = "张三"
  t1.stu.age = 18;
  t1.stu.score = 100;

  std::cout << "教师 职工编号： " << t1.id << " 姓名： " << t1.name << " 年龄： " << t1.age << std::endl;
	
	std::cout << "辅导学员 姓名： " << t1.stu.name << " 年龄：" << t1.stu.age << " 考试分数： " << t1.stu.score << std::endl;
}
```

-[目录](#目录)





### 8.6 结构体做函数参数

**作用**:  将结构体作为参数像函数中传递

传递方式有两种:

1. 值传递
2. 地址传递

ex:

```cpp

#include "iostream"
#include "string"

struct student{

  std::string name;
  int age;
  int score;

};

//值传递
void printstudent(student stu){
  
  stu.age = 28;
  
  std::cout << "子函数中 姓名：" << stu.name << " 年龄： " << stu.age  << " 分数：" << stu.score << std::endl;

}

//地址传递
void printstudent2(student *stu){

  stu.age = 30;

  std::cout << "子函数中 姓名：" << stu->name << " 年龄： " << stu->age  << " 分数：" << stu->score << std::endl;

}

int main(){

  student stu = {"张三", 18 ,100};
  //值传递
  printStudent(stu);

  std::cout << "主函数中 姓名" << stu.name << "年龄" << stu.age << "分数" << stu.score << std::endl;

  //地址传递
  printstudent2(&stu);

  std::cout << "主函数中 姓名" << stu.name << "年龄" << stu.age << "分数" << stu.score << std::endl;
}
```

-[目录](#目录)





### 8.7 结构体中const使用场景

**作用**: 用const来防止误操作

ex:

```cpp

#include "iostream"
#include "string"

struct student{

  std::string name;
  int age;
  int score;

};

void printstudent(const student *stu){  //加上const防止函数体中的误操作

  //stu->age = 100;   操作失败，因为加上了const修饰

  std::cout << "姓名：" << stu->name << " 年龄：" << stu->age << " 分数：" << stu->score << std::endl;

}

int main(){

  student stu = {"张三", 18, 100};

  printstudent{&stu};

}
```
-[目录](#目录)







### 8.8 结构体案例

#### 8.8.1 案例1

**案例描述**

学校正在做毕设项目，每名老师带领5个学生，总共有三名老师，需求如下

设计学生和老师的结构体，其中在老师的结构体中，有老师姓名和一个存放5名学生的数组作为成员

学生的成员有姓名，考试成绩，创建数组存放三名老师，通过函数给每个老师及所带的学生赋值

最终打印出老师数据以及老师所带学生的数据

ex:

```cpp

#include "iostream"
#include "string"
#include "ctime"
#include "cstdlib"

struct student{

	std::string name;
	int score;

};

struct teacher{

	std::string name;
	student Sarr[5];

};

void input(teacher Tarr[], int len){
	
  std::string tname = "教师";
	std::string sname = "学生";
	std::string nameSeed = "ABCDE"; 
	
	for (int i = 0; i < len; i++){

		Tarr[i].name = tname + nameSeed[i];  //添加老师名字

		for (int j = 0; j < 5; j++){

			Tarr[i].Sarr[j].name = sname + nameSeed[j];  //在老师下添加学生信息

			Tarr[i].Sarr[j].score = rand() % 100;  //100以内的随机数
			
		}
	}
	
}

void print(teacher Tarr[], int len){

	for (int i = 0; i < len; i++){

		std::cout << Tarr[i].name << std::endl;

		for (int j = 0; j < 5; j++){

			std::cout << "\t姓名" << Tarr[i].Sarr[j].score << std::endl;

		}
	}
}

int main(){

	std::srand((unsigned int)time(NULL));  //生成随机数，头文件要加上<ctime> <cstdlib>

	teacher tarr[3];

	student S;

	int len;

	len = sizeof(tarr) / sizeof(tarr[0]);

	input(tarr, len);
	print(tarr, len);

} 

```

* 根据案例需求定义结构体，需要什么数据就定义什么数据

-[目录](#目录)





#### 8.8.2 案例2

**案例描述**

设计一个英雄的结构体，包括成员姓名，年龄，性别;创建结构体数组，数组中存放5名英雄

通过冒泡排序的算法，将数组中的英雄进行升序排序，最终打印排序后的结果

五名英雄信息如下:

```cpp
  {"刘备", 23, "男"}
  {"关羽", 22, "男"}
  {"张飞", 20, "男"}
  {"赵云", 21, "男"}
  {"貂蝉", 19, "女"}
```

ex: 

```cpp

#include "iostream"
#include "string"

struct hero{

	std::string name;
	int age;
	std::string sex;

};

void Bubblesort(int len, hero arr[]){

	for (int i = 0; i < len - 1; i++){

		for (int j = 0; j < len - 1; j++){

			if (arr[j].age < arr[j + 1].age){

				std::swap(arr[j], arr[j + 1]);

      }  
		}
	}
}

void print(hero arr[]){

	for (int i = 0; i < 5; i++){
		std::cout << arr[i].name <<	arr[i].sex << arr[i].age <<  std::endl;
	}

} 

int main(){

	hero hero1[5] = {

		{"刘备",23,"男"},
		{"关羽",22,"男"},
		{"张飞",20,"男"},
		{"赵云",21,"男"},
		{"貂蝉",19,"女"}

	};

	Bubblesort(5, hero1);
  
	print(hero1);
	
}

```