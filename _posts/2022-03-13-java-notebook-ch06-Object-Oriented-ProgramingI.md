---
title: Java-Notebook_CH06 Object Oriented Programming I
author:
  name: James Syu
  link: https://github.com/n1046728
date: 2022-03-13 10:21:10 +0800
categories: [java, java-notebook]
tags: []     # TAG names should always be lowercase
excerpt_separator: <!--more-->
---
<!--more-->

## Class and Object
### Concept 
* Cass
> A Class is a user defined blueprint or prototype from which objects are created.It represents the set of properties or methods that are common to all objects of one type.

* Object
> It is a basic unit of Object-Oreinted Programming and represents the real life entities.Atypical Java program creates many objects ,which as you know

### Member variable
> Member variables in a class -these are called **fields** or **properties**.
 
![](../../assets/img/blog/java-notebook/ch06/Object_01.jpg)

### Initializing an object
```java
//Using new keyword
Cat cat1 = new Cat();

//Using Class.forName(String className)method
//consider class present in com.test package
Cat cat2 = (Cat)Class.forName("com.test.Cat").newInstance() ;

//Using clone() method
Cat cat3 = (Cat)cat1.clone();

//Deserialization:De-serialization is technique of reading an object from the saved state in a file.
FileInputStream file = new FileInputStream(filename);
ObjectInputStream in = in ObjectInputStream(file);
Object obj = in.readObject();
```

### Memory model
![](../../assets/img/blog/java-notebook/ch06/Object_02.jpg)

## Method
### Concept
![](../../assets/img/blog/java-notebook/ch06/Object_03.jpg)

### Memory model
![](../../assets/img/blog/java-notebook/ch06/Object_04.jpg)

## Java is Strictly Pass by Value
> Let us assume that a function change() is called from another function main().In this case main() is called the **"caller function"** and change() is called the **"called function or callee function"**

### primitive type
![](../../assets/img/blog/java-notebook/ch06/PassByValue_01.jpg)

### non-primitive type
* Changes are reflected back if we do not assign  reference to a new location or object
![](../../assets/img/blog/java-notebook/ch06/PassByValue_02.jpg)

* The changes are not reflected back if we change the object itself to refer some other location or object
![](../../assets/img/blog/java-notebook/ch06/PassByValue_03.jpg)

## Recursion
### What is Recursion
> The process in which a function calls  itself directly or indirectly is called recrusion and the corresponding function is called as recursive function.

### Rule
![](../../assets/img/blog/java-notebook/ch06/Recursion_01.jpg)
### Memory model
```java
//factorial
public int factorial(int n){
    if(n=1){
        return 1;
    }else{
        return factorial(n-1) *n;
    }
}
```
![](../../assets/img/blog/java-notebook/ch06/Recursion_02.jpg)

## Overloading
### Definition
> Overloading allows different methods to have the same name,but different signatures where the signature can differ by the number of input parameters or type of input parameters or both.

![](../../assets/img/blog/java-notebook/ch06/Overloading_01.jpg)

### Excersise
![](../../assets/img/blog/java-notebook/ch06/Overloading_02.jpg)


## Variable Arguments(Varargs)
### Definetion
> Variable Arguments(Varags) in java is a method that takes a variable number of arguments.
### Syntax of Varargs
```java
public void func(int ...a){ 
    //method body
}
```

### Detail
![](../../assets/img/blog/java-notebook/ch06/Varags_01.jpg)

## Scope of Variables 
> Scope of a variable is the part of the program where the variable is accessible.

### Concept
 ![](../../assets/img/blog/java-notebook/ch06/ScopeOfVariable_01.jpg)  

### Detail
![](../../assets/img/blog/java-notebook/ch06/ScopeOfVariable_02.jpg)

## Constructor
### Concept
> A constructor in java is a **special method** that is used to initialize objects.The constructor is called when an object of a  class is created.It can be used to set initial vlues for object attributes.

### Detail
![](../../assets/img/blog/java-notebook/ch06/Constructor_01.jpg)

### Copy Constructor
> Like C+,Java also supports copy constructor.But,unlike C++,Java doesn't create a default copy constructor if you don't write your own.

```java
class Dog{
    private String name;
    private String color;

    //A normal parameterized constructor
    public Dog(String name ,String color){
        this.name = name;
        this.color = color;
    }
    //Copy constructor
    Dog(Dog dog){
        System.out.println("Copy constructor called");
        name = dog.name;
        color = dog.color;
    }
    @Override
    public Strin toString(){
        return "name:"+ name +",color:"+color;
    }
}
public class Main{
    public static void main(String [] args){
        Dog d1 = new Dog("SuperStar","Yellow");
        //Following involves a copy constructor call
        Dod d2 = new Dog(d1);

        System.out.println(d2);
    }
}
```
```console
Copy constructor called
name:SuperStar,color:Yellow
```

## Private Constructors and Singleton Classes
> The constructor of singleton class would be private so there must be a nother way to get the instance of that class.This is resolved using a class member and a factory to return the class member.

```java
class Mysingleton{
    static MySingleton instance =null;
    private int x = 10;
    //private constructor cannot be accessed outside the class
    private MySingleton(){}
    //Factory method to provide the users with instances
    static public MySingleton getInstance(){
        if(instance == null)
            instance = new MySingleton)();
        return instance;
    }
}
class Main{
    public static void main(String args[]){
        MySingleton a = MySingleton.getInstance();
        MySingleton b = MySingleton.getInstance();
        a.x = a.x +10;
        System.out.println("value ofa a.x="+a.x); //20
        System.out.println("value ofa b.x="+b.x); //20
    }
}
```

## Create Object Flow
![](../../assets/img/blog/java-notebook/ch06/CreateObjectFlow_01.jpg)
![](../../assets/img/blog/java-notebook/ch06/CreateObjectFlow_02.jpg)

## this
### Concept
>  **this** is a reference variable that refers to the current object.

![](../../assets/img/blog/java-notebook/ch06/this_01.jpg)
### Memory model
![](../../assets/img/blog/java-notebook/ch06/this_02.jpg)
### Detail
![](../../assets/img/blog/java-notebook/ch06/this_03.jpg)
![](../../assets/img/blog/java-notebook/ch06/this_04.jpg)


## reference
* [Java is Strictly Pass by Value - **Geeks forGeeks**](https://www.geeksforgeeks.org/g-fact-31-java-is-strictly-pass-by-value/) 
* [C++ Pass by value vs Pass by reference - **MuLong PuYang**](https://medium.com/@racktar7743/c-c-%E6%8C%87%E6%A8%99%E6%95%99%E5%AD%B8-%E5%9B%9B-pass-by-value-vs-pass-by-reference-ed5882802789)
