
## What is OOP? 
It is the programming paradigm that uses object to model real world entities and their interaction. It is used to design a software or write a program in a modular, reusable and scalable way.

## What are the pillars of OOP?
There are 4 pillars of Object-Oriented Programming.
1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

### 1. Encapsulation
Encapsulation is the process of hiding the internal details of an object and only exposing a controlled interface.
* Bundling or wrapping of data and method into a single unit (Class).
* Keeps internal data hidden from outside interference.
* Protect data from direct access.
* Achieved through access modifiers like, ```public```,```private```, ```protected```.

### 2.  Inheritance
Mechanism that allows one class(derived-class) to inherit the properties & methods of another class(super class or base class).
* Promotes the code reusability.
* Hierarchy — models "is-a" relationships.

#### Types of Inheritance
1. Single Inheritance
   - One subclass inherit from one super-class eg: Dog class ==> Animal class
   - supported in java
2. Multilevel Inheritance
   - A class inherit from a class that is already inherited from another class eg: puppy class ==> dog class ==> animal class
   - supported in java.
3. Hierarchical Inheritance
   - Multiple classes inherit from a single parent class.
   - supported in java.
   - dog class ==> animal class
   - cat class ==> animal class
   - rabbit class ==> animal class
4. Multiple Inheritance
   - one class inherit from more than one class
   - not supported in java (using class) to avoid ambiguity (Diamond Problem).
   - Achieved using interfaces in java.
   - e.g: document class implements showable interface, Printable interface
5. Hybrid Inheritance
   - combination of two or more types of inheritance like Single + Multiple inheritance or Hierarchical + Multilevel inheritance etc.
   - not directly supported in java, but can be simulated using interfaces
   - e.g: class D extends C (class) implements A(interface), B (interface)
   


### 3. Polymorphism
Polymorphism means "many forms". The same function behaves differently based on context.
* Same method names behave differently in different class.
* Compile-Time(Method Overloading): Same method name, but different parameters.
* Run-Time(Method Overriding): Subclass or derived class changes the parent class method behaviour.
* Enhance flexibility and extensibility.

### 4. Abstraction
The process of simplifying complex reality by modelling classes based on the essential properties and behaviours, while hiding irrelevant details.
* Hide complex implementation, and shows only essential features.
* Achieved though using Abstract classes or interfaces.

## What is the difference between an abstract class and an interface?

### Abstract Class
* Can have both concrete(implemented) and abstract(unimplemented) method.
* Allows constructors.
* Can have member variables.
* Support access modifiers.
* Used when you want to give common base class with some shared functionality for derived classes.

Use abstract class when:
- you want to provide a common base class with some shared functionality.
- you need to implement some methods in the base class.
- you want to define non-public members(fields or methods) in the base class.

### Interface 
* Only contains methods signatures(no method implementation).
* Can not have constructors.
* Can not have member variables.
* All methods are implicitly public and abstract.
* Used when you want to implement common set of method across unrelated classes.

Use interface class when:
- you want to define a contract for classes that are not related by inheritance.
- you want to enforce a common set of methods across unrelated classes.
- you want to achieve multiple inheritance, as class can implement multiple interfaces but can inherit from only one class.

## What is the purpose of the `final` keyword in Java, and how does it affect classes and methods?
The `final` keyword used to make classes or methods immutable or to prevent unintentional modification or extension. In Java `final` keyword serves different purposes.
* `final` variable: once assigned, the value can not be changed. it is a constant now.
* `final` method: it can not be overridden by subclasses. 
  * It ensures that the method's implementation remains unchangeable in all subclasses.
* `final` class: It can not be inherited or extended by subclasses.
  * It prevents any further inheritance of that class.

## What is method overloading and method overriding?
### Method Overloading (Compile Time Polymorphism)
It is the practice of defining multiple methods with the same name, but having different parameters(number, type, order). The compiler determine which method to be run based on the method signature and the arguments provided.
### Method Overriding (Run Time Polymorphism)
It occurs when the derived or subclass provides its own specific implementation of a method that is already defined in the super class. The method of subclass must have the similar method signature(name, parameters, return type) as the one in the parent or superclass.

## Discuss the concept of ‘super’ and ‘this’ keywords in OOP.
### `this` keyword
- refers to the current class object.
- access current class methods and variables.
- calls constructor of the same class.
### `super` keyword
- refers to the parent class object.
- access superclass methods and fields when they are hidden by a subclass.
- calls constructor of parent class

##  What is a constructor, and how is it different from a method?
A constructor is special type of method that is responsible for the initialization of an object. It is automatically called/invoked when the object is created.
- it must have the same name of the class it belongs to
- constructor have no return type, not even `void`
- automatically invoked when the object of the class is created using `new` keyword
- a class can have the multiple constructors with different parameters (constructor overloading)

There are 3 types of constructors:
1. Default Constructor (No Arguments)
2. Parameterized Constructor (Accept Arguments)
3. Copy Constructor (copy values from another Constructor)

## What is the difference between shallow copy and deep copy?
### Shallow Copy
In a shallow copy only the references to the objects are duplicated not the actual objects themselves.
- two object references to the same data
- copy reference to the original object
- changes in one effects the other(for shared data)
- faster & less memory 
### Deep Copy
In a deep copy not only the references are duplicated, new objects are created for the referenced objects, recursively.
- two completely different objects (no shared data)
- copies all fields and sub-objects recursively 
- changes are independent 
- slower & more memory is used 

## How do you prevent inheritance in a class?
To prevent inheritance in a class, we can declare it as `final`. This will restrict other classes from inheriting from it.

## Explain the Singleton design pattern.
It is a creational design pattern that ensure that a class has only one instance throughout the program. Provide global point of access to that instance. It is achieved by making class constructor private to avoid instantiation from outside of the class. It is used in the scenarios where there should be a single point of control like database connections, configuration settings etc.

Real Life Analogy: Think of prime minister(instance) of a country(class) there is one at anytime(single instance). All operations and access go through that one office (single point of control).

## What is the difference between composition and inheritance, and when would you choose one over the other?
In general composition is favoured over inheritance because it allows code reusability and flexibility without creating tight coupling between classes. 
### Inheritance 
Inheritance is a mechanism in which subclass inherit properties from the superclass. It establishes `is-a` relationship between classes. It is useful when use want to reuse and extend an existing class.
### Composition 
Composition is a mechanism in which a class contains instance of another class as one of its members. It establishes `has-a` relationship between classes. It is useful when you want to create complex objects by combining simpler objects.