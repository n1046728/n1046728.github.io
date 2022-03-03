---
title: Java-Notebook_CH01 intro
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-04 00:43:00 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->


## What is JDK,JRE
1. JDK : Java Development Kit
    > JDK = JRE + [JDK Tools](https://docs.oracle.com/javase/8/docs/technotes/tools/)(java, javac,javadoc,javap,..etc)
2. JRE : Java Runtime Enviroment
    > JVM + Java SE

## [PATH Variable](https://docs.oracle.com/cd/E19683-01/806-4073/userconcept-39855/index.html)
1. JAVA_HOME : Setting jdk path
2. PATH : Add %JAVA_HOME%\bin

## Comment
1. Single-line Comments ： //
2. Multi-line Comments : /* */
3. Doc Comments : /** */
```java
/**
  @Author James
  @version 1.0
*/
public static void main(String []args){
  //this is single-line comments
  /*
      this is multi-line comments
  */
  System.out.println("Hello world");
}
```