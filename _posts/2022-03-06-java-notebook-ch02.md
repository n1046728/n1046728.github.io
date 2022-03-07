---
title: Java-Notebook_CH02 Variables
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-06 10:22:00 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Data Types in Java  
![](../../assets/img/blog/java-notebook/ch02/DataTypesInJava.jpg)

## Primitive Type
### Integer
#### 1. Range of values
![](../../assets/img/blog/java-notebook/ch02/DataTypesNumeric-IntegerRangeOfValues.jpg)
#### 2. Detail
![](../../assets/img/blog/java-notebook/ch02/DataTypesNumeric-IntegerDetail.jpg)

### Floating-Point 
#### 1. Range of values
![](../../assets/img/blog/java-notebook/ch02/DataTypesNumeric-FloatRangeOfValues.jpg)

##### 2. Detail
![](../../assets/img/blog/java-notebook/ch02/DataTypesNumeric-FloatDetail.jpg)

##### 3. Example
```java
float num1 = 1.1; //wrong
float num2 = 1.1F; //ok

//decimal system
double num3 = .456;//equals 0.456

//scientific notation
System.out.println(5.12e2); //512.0
System.out.println(5.12E-2); //0.0512

//float trap
double num4 = 2.7;
double num5 = 8.1/3 //2.6999999999999997;

//wrong
//if(num4 == num5){
//  System.out.println("num4 equal num5");
//}

//correct
if(Math.abs(num4 - num5) < 0.000001>){
  System.out.println("num4 equal num5");
}
```

### char data type
#### 1. definition
> The char data type is a single 16-bit Unicode character. It has minimum value of '\u0000'(or 0) and mazimum value of 'uffff'(or 65,535 inclusive)

![](../../assets/img/blog/java-notebook/ch02/DataTypesCharacter-Char.jpg)

#### 2. example
```java
char c1 = 97;
System.out.println(c1); //a

char c2 = 'a';
System.out.println((int)c2); //97

System.out.println('a'+10); //107
char c3 = 'b'+1; //99
System.out.println(c3); //c
System.out.println((int)c3); //99
```

### boolean data type
![](../../assets/img/blog/java-notebook/ch02/DataTypesCharacter-Char.jpg)

## Conversions and Promotions 
### [Widening or Automatic Type Conversion](https://www.geeksforgeeks.org/type-conversion-java-examples/)
#### 1. Introduction
![](../../assets/img/blog/java-notebook/ch02/Promotions.jpg)

#### 2. Deatail 
![](../../assets/img/blog/java-notebook/ch02/PromotionsDetail.jpg)

#### 2. Example
```java
//detail 1
int n1 = 10; //ok
//float d1 = n1 + 1.1;//error 1 + 1.1 => result is double
//double d1 = n1 + 1.1;//ok n1 + 1.1 => result is double
float d1 = n1 + 1.1F;//ok n1 + 1.1 => result is float

//detail 2
//int n2 = 1.1;//error double -> int

//detail 3
byte b1 = 10 ;
//char c1 = b1 ; // error byte can not covert to char

//detail 4
byte b2 = 1;
byte b3 = 2;
short s1 = 1;
//short s2 = b2 + s1;//错, b2 + s1 => int
int s2 = b2 + s1;//对, b2 + s1 => int

//detail 5
boolean pass = true;
//int num100 = pass;// boolean can't convert to any data type

//detail 6
byte b4 = 1;
short s3 = 100;
int num200 = 1;
float num300 = 1.1F;
double num500 = b4 + s3 + num200 + num300; //float -> double
```
### [Narrowing or Explicit Conversion](https://www.geeksforgeeks.org/type-conversion-java-examples/)
#### 1. Introduction
> If we want to assign a value of a larger data type to a smaller data type must using "()".A narrowing conversion may lose precision and range.

#### 2. Detail
![](../../assets/img/blog/java-notebook/ch02/ConversionsDetail.jpg)

### Promotion
> While evaluating expressions, the intermediate value may exceed the range of operands and hence the expression value will be promoted. Some conditions for type promotion are:  

1. Java automatically promotes each byte, short, or char operand to int when evaluating an expression.
2. If one operand is long, float or double the whole expression is promoted to long, float, or double respectively.

## [Converting Between Numbers and Strings](https://docs.oracle.com/javase/tutorial/java/data/converting.html)
![](../../assets/img/blog/java-notebook/ch02/ConvertingBetweenNumbersAndStrings.jpg)

```java
//String to char
String str ="123";
char c = str.charAt(0);
```

