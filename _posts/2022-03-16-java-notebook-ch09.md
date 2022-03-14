---
title: Java-Notebook_CH09 Enumeration(enum)
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-16 11:05:10 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Concept
* Enum serve the purpose of representing a group of named constants in a  programming language.
* Enums are used when we know all possible values at compile-time,such as choices on a menu,rounding mode,etc.

## Simulate a class of type enum
![](../../assets/img/blog/java-notebook/ch09/enum_01.jpg)
```java
class Season{
  private String name;
  private String desc;

  //public access 
  public static final Season SPRING = new Season("Spring","warm");
  public static final Season WINTER = new Season("Winter","cold");
  public static final Season AUTUMN = new Season("Autumn","cool");
  public static final Season SUMMER = new Season("Summer","hot");

  //private constructor to prevent new object
  private Season(String name,String desc){
    this.name = name;
    this.desc = desc;
  }

  //no setter prevent attribute revised
  public String getName(){
    return name;
  }
  
  public String getDesc(){
    return name;
  }
}
```

## enum
### quick start
```java
enum Season{
  SPRING("Spring","warm"),WINTER("Winter","cold"),AUTUMN("Autumn","cool"),SUMMER("Summer","hot");

  private String name;
  private String desc;

  private Season(String name,String desc){
    this.name = name;
    this.desc = desc;
  }

  public String getName(){return name;}
  public String getDesc(){return desc;}
}
```
### Detail
![](../../assets/img/blog/java-notebook/ch09/enum_02.jpg)
![](../../assets/img/blog/java-notebook/ch09/enum_03.jpg)
### method
![](../../assets/img/blog/java-notebook/ch09/enum_04.jpg)