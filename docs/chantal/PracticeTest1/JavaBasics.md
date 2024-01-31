# Java Basics

## The Platform

Java is platform independent because the compiled bytecode can be executed on any platform by the runtime engine, the Java Virtual Machine (JVM). 

**JRE** stands for the Java Runtime Environment, which is a software layer in which programs compiled for a typical JVM implementation can be run. It is part of a JDK. A JRE consists of a JVM, Java class libraries, and the Java class loader.

## The main method

Acceptable declarations of main:  

* final public static void main(String[] args)
* public static void main(String[] args)
* static public void main(String[] args)

The **public** and **static** keywords can be written in either order, though we use 'public static' by convention, and the modifiers *final* and *synchronized* are allowed for the main method. It must always be public, so the JVM can access it. The return type of the main method must always be *void* (int main is only allowed in C++), and must only have the String[] args argument.

## Access modifiers

* public - can be accessed within classes by any package
* private - can only be accessed within its own class
* protected - can be accessed within its own package and also by subclasses (of its containing class) in other packages.

By default, if you don't give a member an access modifier it can only be accessed in its own package.

## Object-Oriented Programming Principles

### Abstraction

A class's implementation details should be hidden, so only the functionality is exposed to the outside world. This also applies to functions. This helps with code reuse, as you can provide a generic function or object to serve multiple places/with multiple concerns, as long as the functionality is what you need to happen.

### Encapsulation

 a class/object should be able to hide its data and methods from other classes. The class encapsulates data fields relating to the object, allowing it to control its own state through its methods - this is why we have getters and setters, to control read/write access to properties. This improves the application's security.

### Inheritance

Classes can inherit commonly used behaviour and data from other classes, promoting reusability. A subclass can inherit its superclasses members (fields, methods, and nested classes) depending on their access modifiers. Parent and child classes should have high cohesion - the subclass should require most of the parent's functionality.

The **Liskov Substitution Principle** of SOLID deals with this, stating that you should be able to use a parent class anywhere you use its child.

### Polymorphism

Advantages:

* Reusability - subclasses can define their own methods and also share some of the functionality of their parent class
* Flexibility - objects can respond in different ways to the same message. Multiple methods can be defined with the same name (as long as they have different method signatures), which can behave in unique ways and return different values. New objects can be added without modifying existing methods, this flexibility makes programs easier to maintain.

## Things Java doesn't support

* The goto statement - the keyword is reserved but unused
* Pointers
* Operator overloading - only methods can be overloaded
