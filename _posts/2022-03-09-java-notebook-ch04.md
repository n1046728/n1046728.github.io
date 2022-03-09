---
title: Java-Notebook_CH04 Flow Control
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-09 22:33:00 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Decision making
### if
### if-else
### nested-if
### if-else-if
### switch
![](../../assets/img/blog/java-notebook/ch04/switch_01.jpg)
![](../../assets/img/blog/java-notebook/ch04/switch_02.jpg)
```java
//get season from months
// 3,4,5->spring 6,7,8->summer 9,10,11->fall 12,1,2->winter
Scanner sc = new Scanner(System.in);
System.out.println("please enter month");

int month = sc.nextInt();

switch(month){
    case 3:
    case 4:
    case 5:
        System.out.println("spring");
        break;
    case 6:
    case 7:
    case 8:
        System.out.println("summer");
        break;
    case 9:
    case 10:
    case 11:
        System.out.println("fall");
        break;
    case 12:
    case 1:
    case 2:
        System.out.println("winter");
        break;
    default:
        System.out.prinln("u enter wrong month");
}
```
## Loops
### for loop
![](../../assets/img/blog/java-notebook/ch04/ForLoop_01.jpg)
![](../../assets/img/blog/java-notebook/ch04/ForLoop_02.jpg)

### for each loop
> Instead of declaring and initizing a loop ocunter variable ,you declare a variable that is the same type as the base type of the array,folloed by a colon,which is then followed by the array name.
![](../../assets/img/blog/java-notebook/ch04/ForEachLoop_01.jpg)
```java
int [] nums = {12,3,6,9,18,7};
for(int num : nums){
    System.out.println(num);
}
```
### while loop
![](../../assets/img/blog/java-notebook/ch04/WhileLoop_01.jpg)

### do..while loop
![](../../assets/img/blog/java-notebook/ch04/DoWhileLoop_01.jpg)

## Jump statement
### Continue Statement
> Continue statement is encountered the control directly **jumps to the beginning of the loop** for the next iteration instead of executing the statements of the current iteration.  

### Break Statement
> Break Statement is a loop control statement that is used to **terminate the loop**.

![](../../assets/img/blog/java-notebook/ch04/Break_01.jpg)

### return Statement
> It is used to **exit from a method**,with or without a value.

## Homework
* Program to print multiplication table
* Program to print hollow pyramid
