[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Java Inheritance & Interfaces Tutorial

## Inheritance

**Inheritance is an important pillar of OOP(Object-Oriented Programming). It is the mechanism in java by which one class is allowed to inherit the features(fields and methods) of another class.**

**Important terminology:**

**1. Super Class: The class whose features are inherited is known as superclass(or a base class or a parent class).**

**2.Sub Class: The class that inherits the other class is known as a subclass(or a derived class, extended class, or child class). The subclass can add its own fields and methods in addition to the superclass fields and methods.**

**3.Reusability: Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. By doing this, we are reusing the fields and methods of the existing class.**

### How to use inheritance in Java

**The keyword used for inheritance is extends.**

**Syntax :**

**`class derived-class extends base-class`**
**`{`**
**`//methods and fields`**
**`}`**

![inheritance](https://media.geeksforgeeks.org/wp-content/uploads/inheritence1.png)

### Types of Inheritance in Java

**1. Single Inheritance: In single inheritance, subclasses inherit the features of one superclass. In the image below, class A serves as a base class for the derived class B.**
![single](https://media.geeksforgeeks.org/wp-content/uploads/inheritance1.png)

**2. Multilevel Inheritance: In Multilevel Inheritance, a derived class will be inheriting a base class and as well as the derived class also act as the base class to other class. In the below image, class A serves as a base class for the derived class B, which in turn serves as a base class for the derived class C. In Java, a class cannot directly access the grandparent’s members.**

![mul](https://media.geeksforgeeks.org/wp-content/uploads/inheritance3.png)

**3. Hierarchical Inheritance: In Hierarchical Inheritance, one class serves as a superclass (base class) for more than one subclass. In the below image, class A serves as a base class for the derived class B, C and D.**
![h](https://media.geeksforgeeks.org/wp-content/uploads/20210311224500/Untitled-300x269.png)

**4. Multiple Inheritance (Through Interfaces): In Multiple inheritances, one class can have more than one superclass and inherit features from all parent classes. Please note that Java does not support multiple inheritances with classes. In java, we can achieve multiple inheritances only through Interfaces. In the image below, Class C is derived from interface A and B.**

![multiple](https://media.geeksforgeeks.org/wp-content/uploads/inheritance2-1.png)

**5. Hybrid Inheritance(Through Interfaces): It is a mix of two or more of the above types of inheritance. Since java doesn’t support multiple inheritances with classes, hybrid inheritance is also not possible with classes. In java, we can achieve hybrid inheritance only through Interfaces.**

![hyb](https://media.geeksforgeeks.org/wp-content/uploads/inheritance-1.png)

## Interfaces

**Like a class, an interface can have methods and variables, but the methods declared in an interface are by default abstract (only method signature, no body).**

**1. Interfaces specify what a class must do and not how. It is the blueprint of the class.**

**2. An Interface is about capabilities like a Player may be an interface and any class implementing Player must be able to (or must implement) move(). So it specifies a set of methods that the class has to implement.**

**3. If a class implements an interface and does not provide method bodies for all functions specified in the interface, then the class must be declared abstract.**

**4. A Java library example is, Comparator Interface. If a class implements this interface, then it can be used to sort a collection.**

**Syntax :**

**`interface <interface_name> {`**
    **`// declare constant fields`**
    **`// declare methods that abstract`**
    **`// by default.`**
**`}`**

**To declare an interface, use interface keyword. It is used to provide total abstraction. That means all the methods in an interface are declared with an empty body and are public and all fields are public, static and final by default. A class that implements an interface must implement all the methods declared in the interface. To implement interface use implements keyword.**

### Why do we use interface ?

**1. It is used to achieve total abstraction.**

**2. Since java does not support multiple inheritance in case of class, but by using interface it can achieve multiple inheritance .**

**3. It is also used to achieve loose coupling.**

**4. Interfaces are used to implement abstraction. So the question arises why use interfaces when we have abstract classes?**

**References:**
[geeksforgeeks](https://www.geeksforgeeks.org/)