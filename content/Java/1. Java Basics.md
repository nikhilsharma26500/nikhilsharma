---
title: Java Basics
draft: false
tags:
---
 ## Java
Java is a high-level, class-based, object-oriented programming language. It is a general-purpose programming language intended to let application developers write once, run anywhere, meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.

![Java Conceptual Diagram](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*24AnOEHXbTQxcm1XIPkm-A.png)

## JVM (Java Virtual Machine)
The Java Virtual Machine (JVM) is a virtual machine that enables a computer to run Java programs as well as programs written in other languages that are also compiled to Java bytecode. The JVM is detailed by a specification that formally describes what is required in a JVM implementation.

## JRE (Java Runtime Environment)
The Java Runtime Environment (JRE) is a set of software tools for development of Java applications. It combines the Java Virtual Machine (JVM), platform core classes, and supporting libraries. The JRE is the runtime portion of Java software, which is all you need to run it in your web browser.

## JDK (Java Development Kit)
The Java Development Kit (JDK) is a software development kit used to develop Java applications. It includes the JRE, an interpreter/loader (Java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), and other tools needed for Java development.

## Variables in Java
Variables are containers for storing data values. In Java, there are different types of variables, for example:

### Primitive Variables
Primitive variables are the most basic data types available in Java. There are 8 primitive data types:
- `byte`: 8-bit integer
- `short`: 16-bit integer
- `int`: 32-bit integer
- `long`: 64-bit integer
- `float`: single-precision 32-bit floating point
- `double`: double-precision 64-bit floating point
- `boolean`: true or false
- `char`: single 16-bit Unicode character

### Non-Primitive Variables
Non-primitive variables are called reference variables because they store references to objects. The reference variables are declared with a specific type that cannot be changed. The reference variables can be used to refer to any object of the declared type or any compatible type.
- `String`: a sequence of characters
- `Array`: a collection of similar type of elements
- `Class`: a user-defined blueprint from which objects are created

### Local Variables
Local variables are declared in methods, constructors, or blocks. They are created when the method, constructor, or block is entered and the variable will be destroyed once it exits the method, constructor, or block. Access modifiers cannot be used for local variables.

### Local Variable Example
```java
public class Example {
    public void myMethod() {
        int localVar = 10; // Local variable
        System.out.println(localVar);
    }
}
```

### Global Variables
Global variables, also known as instance variables, are declared in a class, but outside a method, constructor, or any block. They are created when an object of the class is created and destroyed when the object is destroyed. Unlike local variables, global variables can have access modifiers.

### Global Variable Example
```java
public class Example {
    int globalVar = 20; // Global variable

    public void myMethod() {
        System.out.println(globalVar);
    }
}
```