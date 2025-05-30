
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

## 4. What is the difference between an abstract class and an interface?

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

