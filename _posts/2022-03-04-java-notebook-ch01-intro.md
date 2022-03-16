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


## [What is JDK,JRE](https://docs.oracle.com/javase/8/docs/)
1. JDK : Java Development Kit
    > JDK = JRE + [JDK Tools](https://docs.oracle.com/javase/8/docs/technotes/tools/)(java, javac,javadoc,javap,..etc)
2. JRE : Java Runtime Enviroment
    > JVM + Java SE
3. jdk 8 document [download](https://www.oracle.com/java/technologies/javase-jdk8-doc-downloads.html)
4. java execution flow  
![exeution flow](../../assets/img/blog/java-notebook/ch01/java-execution-flow.png)

## [PATH Variable](https://docs.oracle.com/cd/E19683-01/806-4073/userconcept-39855/index.html)
1. JAVA_HOME : Setting jdk path
2. PATH : Add %JAVA_HOME%\bin
3. validate java path setting using **java -verion** in command line

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


## Develop Detail
* Java main method is the entry point of any java porgram. It's syntax is always **public static void main(String [] args)**
* Each source file should contain **only one public class or interface** and the name of that public class should be similar to the name of the source file.
  
## reference
* [Java Platform Standard Edition 8 Documentation - **Oracle**](https://docs.oracle.com/javase/8/docs/)
* [Why a Single Java Source File Can Not Have More Than One Public Class - **Java Zone**](https://dzone.com/articles/why-single-java-source-file-can-not-have-more-than)
* [Java main method - **JournalDev**](https://www.journaldev.com/12552/public-static-void-main-string-args-java-main-method)

