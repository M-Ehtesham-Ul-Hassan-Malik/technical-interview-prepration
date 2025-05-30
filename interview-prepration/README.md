

### What is OOP? 
It is the programming paradigm that uses object to model real world entities and their interaction. It is used to design a software or write a program in a modular, reusable and scalable way.

### What are the pillars of OOP?
There are 4 pillars of Object-Oriented Programming.
1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

#### 1. Encapsulation
Encapsulation is the process of hiding the internal details of an object and only exposing a controlled interface.
* Bundling or wrapping of data and method into a single unit (Class).
* Keeps internal data hidden from outside interference.
* Protect data from direct access.
* Achieved through access modifiers like, ```public```,```private```, ```protected```.

#### 2.  Inheritance
Mechanism that allows one class(derived-class) to inherit the properties & methods of another class(super class or base class).
* Promotes the code reusability.
* Hierarchy — models "is-a" relationships.

#### 3. Polymorphism
Polymorphism means "many forms". The same function behaves differently based on context.
* Same method names behave differently in different class.
* Compile-Time(Method Overloading): Same method name, but different parameters.
* Run-Time(Method Overriding): Subclass or derived class changes the parent class method behaviour.
* Enhance flexibility and extensibility.

#### 4. Abstraction
The process of simplifying complex reality by modelling classes based on the essential properties and behaviours, while hiding irrelevant details.
* Hide complex implementation, and shows only essential features.
* Achieved though using Abstract classes or interfaces.

### 4. What is the difference between an abstract class and an interface?

#### Abstract Class
* Can have both concrete(implemented) and abstract(unimplemented) method.
* Allows constructors.
* Can have member variables.
* Support access modifiers.
* Used when you want to give common base class with some shared functionality for derived classes.

Use abstract class when:
- you want to provide a common base class with some shared functionality.
- you need to implement some methods in the base class.
- you want to define non-public members(fields or methods) in the base class.

#### Interface 
* Only contains methods signatures(no method implementation).
* Can not have constructors.
* Can not have member variables.
* All methods are implicitly public and abstract.
* Used when you want to implement common set of method across unrelated classes.

Use interface class when:
- you want to define a contract for classes that are not related by inheritance.
- you want to enforce a common set of methods across unrelated classes.
- you want to achieve multiple inheritance, as class can implement multiple interfaces but can inherit from only one class.