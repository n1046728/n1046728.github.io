---
title: Java-Notebook_CH03 Operators
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-07 23:43:00 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Arithmetic Operators
### 1.
![](../../assets/img/blog/java-notebook/ch03/ArithmeticOperator_01.jpg)  
![](../../assets/img/blog/java-notebook/ch03/ArithmeticOperator_02.jpg)  
```java
//mod a% b = a - a/b *b
//-10 - (-10) / 3 * 3 = -10 + 9 = -1
System.out.println(-10 % 3); // -1
System.out.println(10 % -3); //1
System.out.println(-10 % -3);//-1

//
```
### 2. Detail
![](../../assets/img/blog/java-notebook/ch03/ArithmeticOperator_03.jpg)  

### 3. Example
![](../../assets/img/blog/java-notebook/ch03/ArithmeticOperator_04.jpg)  

## Relation Operators
### 1. 
![](../../assets/img/blog/java-notebook/ch03/ArithmeticOperator_04.jpg)  

## Logic Operators
![](../../assets/img/blog/java-notebook/ch03/LogicalOperator_01.jpg)  
![](../../assets/img/blog/java-notebook/ch03/LogicalOperator_02.jpg) 
![](../../assets/img/blog/java-notebook/ch03/LogicalOperator_03.jpg) 
![](../../assets/img/blog/java-notebook/ch03/LogicalOperator_04.jpg) 


```java
int a = 4;
int b = 9;
//对于&&短路与而言，如果第一个条件为false ,后面的条件不再判断
//对于&逻辑与而言，如果第一个条件为false ,后面的条件仍然会判断
if(a < 1 & ++b < 50) {
  System.out.println("ok300");
}
if( a > 1 || ++b > 4) { // 可以换成| 测试
  System.out.println("ok300");
}
```

## Assignment Operators
![](../../assets/img/blog/java-notebook/ch03/AssignmentOperator_01.jpg)  
![](../../assets/img/blog/java-notebook/ch03/AssignmentOperator_02.jpg)  
```java
//复合赋值运算符会进行类型转换
byte b = 3;
b += 2; // 等价b = (byte)(b + 2);
b++; // b = (byte)(b+1);
```
## Ternary Operators
![](../../assets/img/blog/java-notebook/ch03/TernaryOperator_01.jpg)  
![](../../assets/img/blog/java-notebook/ch03/TernaryOperator_02.jpg)  
```java
//表达式1 和表达式2 要为可以赋给接收变量的类型
//(或可以自动转换/或者强制转换)
int a = 3;
int b = 8;
int c = a > b ? (int)1.1 : (int)3.4;//可以的
double d = a > b ? a : b + 3;//可以的，满足int -> double
```

## Operator Precedence
![](../../assets/img/blog/java-notebook/ch03/OperatorPrecedence _01.jpg) 

## Naming Convention
![](../../assets/img/blog/java-notebook/ch03/Naming_01.jpg) 
* package：lower dot case
* class：Upper camel case
* variables：lower camel case
* constants：screaming snake case i.e.DEFAULT_PI

## Keyword
![](../../assets/img/blog/java-notebook/ch03/Keyword_01.jpg) 
![](../../assets/img/blog/java-notebook/ch03/Keyword_02.jpg)

## Reserved words
![](../../assets/img/blog/java-notebook/ch03/Preserve_01.jpg)

## Base
### Base description
![](../../assets/img/blog/java-notebook/ch03/Base_01.jpg)

### Base conversion
![](../../assets/img/blog/java-notebook/ch03/Base_01.jpg)
#### 1. Group1 - Binary to Decimal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_01.jpg)
#### 2. Group1 - Octal to Decimal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_02.jpg)
#### 3. Group1 - Hexadecimal to Decimal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_03.jpg)

#### 4. Group2 - Decimal to Binary
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_04.jpg)
#### 5. Group2 - Decimal to Octal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_05.jpg)
#### 6. Group2 - Decimal to Hexadecimal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_06.jpg)

#### 7. Group3 - Binary to Octal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_07.jpg)
#### 8. Group3 - Binary to Hexadecimal
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_08.jpg)

#### 9. Group4 - Octal to Binary
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_09.jpg)
#### 10. Group4 - Hexadecimal to Binary
![](../../assets/img/blog/java-notebook/ch03/BaseConvert_10.jpg)

## Binary Detail
### 1. introduction
![](../../assets/img/blog/java-notebook/ch03/Binary_01.jpg)
### 2. 原碼、反碼、補碼
![](../../assets/img/blog/java-notebook/ch03/Binary_02.jpg)

## Bitwise and Bit Shift Operators
![](../../assets/img/blog/java-notebook/ch03/BitShiftOperator_01.jpg)
![](../../assets/img/blog/java-notebook/ch03/BitShiftOperator_02.jpg)
![](../../assets/img/blog/java-notebook/ch03/BitShiftOperator_03.jpg)
