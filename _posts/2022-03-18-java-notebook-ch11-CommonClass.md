---
title: Java-Notebook_CH11 Common Class
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-16 11:05:10 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->
## Wrapper Class
### boxing and unboxing
![](../../assets/img/blog/java-notebook/ch11/wrapper_01.jpg
.jpg)
![](../../assets/img/blog/java-notebook/ch11/wrapper_02.jpg
.jpg)
```java
//demo int <->Integer boxing and unboxing
//before jdk1.5 
//boxing int->Integer
int n1 = 100;
Integer integer = new Integer(n1);
Integer integer1 = Integer.valueOf(n1);

//unboxing Integer->int
int i = Integer.intValue();

//after jdk1.5 autoboxing and unboxing
int n2 = 100;
//auto boxing
Integer integer2 = n2; //behind using Integer.valueOf(n2)
//auto unboxing
int n3 = Integer2; //behind using Integer2.intValue 
```
### wrapper and string conversion
```java
//wrapper(Integer) ->String
Integer i = 100;
//mehtod 1
String str1 = i+"";
//method 2
String str2 = i.toString();
//method 3
String str3 = String.valueOf(i);

//String ->wrapper(Integer)
String str4 = "123";
Integer i2 = Integer.parseInt(str4);//using auto boxing
Integer i3 = new Integer(str4);
```
### Integer and Character
```java
System.out.println(Integer.MIN_VALUE); 
System.out.println(Integer.MAX_VALUE);

System.out.println(Character.isDigit('a'));//number test
System.out.println(Character.isLetter('a'));
System.out.println(Character.isUpperCase('a'));
System.out.println(Character.isLowerCase('a'));
System.out.println(Character.isWhitespace('a'));
System.out.println(Character.toUpperCase('a'));
System.out.println(Character.toLowerCase('A'));
```
### Integer test for interview
```java
Integer i = new Integer(1);
Integer j = new Integer(1);
System.out.println(i == j); //False

//cause Integer.valueOf() method 
//if number between -128~127 will direct return ,or new Integer(i)
Integer i2 = 1;
Integer j2 = 1;
System.out.println(i2 == j2); //True

Integer i3 = 128;
Integer j3 = 128;
System.out.println(i3 == j3); //False

//primitive type == mean value equal not reference equal
Integer i4 =127;
int j4 = 127;
System.out.println(i4 == j4); //True

Integer i5 =128;
int j5 = 128;
System.out.println(i5 == j5); //True
```

## String Class
![](../../assets/img/blog/java-notebook/ch11/string_01.jpg
.jpg)
## String Buffer

## Math class

## Date Class
