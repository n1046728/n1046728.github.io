---
title: Java-Notebook_CH05 Array、Sorting、Search
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-12 21:21:10 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Array
### about array
![](../../assets/img/blog/java-notebook/ch05/Array_01.jpg)
* In java,all arrays are dynamically allocated.
* The variables in the array are ordered,and each has an index beginning from 0.
* The elements in the array allocated by **new** will automatically be initialized **zero**(for numeric type),**false**(for boolean),or **null**(for reference types).
* 
### One-Dimensional Arrays
> type var-name[];
> or
> type [] var-name;

### Instantiating an Array
> var-name = new type[size]

### Array Literal
> int [] intArray = new int[]{1,2,3,4,5}
> or
> int [] intArray = {1,2,3,4,5}

### Array memory model
![memory model](../../assets/img/blog/java-notebook/ch05/Array_02.jpg)

### Cloning of arrays
> A **deep copy** is performed with the new array containing copies of the original's elements as opposed to references.

```java
int[] arr = {1,2,3}

//method 1
int[] cloneArr = arr.clone();
will pring false as deep copy is created
System.out.println(arr == cloneArr);

//method 2
int cloneArr2 = new int[arr.length];
for(int i = 0 ; i<cloneArr2.lenght ; i++){
  cloneArr2[i] = arr[i];
}
```
### Reverse an array

```java
int[] arr = {1,2,3};
int[] arr2 = int [arr.length];

for(int i = arr.length-1,j=0;j<arr2.length;i--,j++){
   arr2[j] = arr[i];
}
arr = arr2

```
### Extend an array
```java
int[] arr = {1,2,3};

Scanner sc = new Scanner(System.in);
while(true){
  System.out.println("pls enter a number:");
  int newNum = sc.nextInt();
  int[] newArr = new[arr.length+1];
  for(int i = 0 ,i< arr.lenght ; i++){
    newArr[i] = arr[i];
  }
  newArr[arr.length+1] = newNum;
  arr = newArr;
  System.out.println("Do u want to exit this program?Y/N");
  char decision = sc.next().charAt(0);
  if(decision == 'N'){
    break;
  }
}

```
## Two-Dimensional Arrays
### memory model
![two-dimension](../../assets/img/blog/java-notebook/ch05/Array_03.jpg)
### pascal triangle
```java
/*
1
1 1
1 2 1
1 3 3 1
*/
//print 10 level pascal triangle
int [][] arr = new int[10][];
for(int i = 0 ;i<arr.length;i++){
  arr[i] = new int[i+1];
  for(int j =0;j<arr[i].length;j++){
    if(j==0 ||j ==arr[i].length-1){
      arr[i][j] = 1;
    }else{
      arr[i][j] = arr[i-1][j] + arr[i-1][j-1];
    }
  }
}

```

## Jagged array
> A jagged array is an array of arrays such that memberarrays can be of different sizes

![jagged array](../../assets/img/blog/java-notebook/ch05/Array_04.jpg)

## Sorting - Bubble Sort
```java
//acending
//1st round 21,65,55,12,79 
//2nd round 21,55,12,65,79
//3nd round 21,12,55,65,79
//4nd round,12,21,55,65,79

int[] arr = {21,65,79,55,12};
for(int i =0,i<arr.length-1;i++){
  for(int j=0 ;j<arr.length-i-1;j++){
    if(arr[j] > arr[j+1]){
      int tmp = arr[j];
      arr[j] = arr[j+1];
      arr[j+1] = tmp;
    }
  }
}

```
