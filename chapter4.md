# Modules should be deep

One of the most important techniques for managing software complexity is to design systems so that developers only need to face a small fraction of the overall complexity at any time. This is called modular design. The goal of modular design is to minimize the dependencies between modules. 

We can think of each module in 2 parts:

(1) An interface

Consists of everything that a developer working in a different module must known in order to use the given module.
Typically describes *what* the module does but not *how* it does it. 

(2) An implementation

Consists of the code that carries out the promises made by the interface. 

NB a class is a blueprint of what an object is; an interface is a contract that says what a class will do. An interface therefore is seemingly concerned with functionality. Classes can have state/variable/data; interfaces simply specify behaviours.

'For the purposes of this book, a module is any unit of code that has an interface and an implementation'. 

The best modules are those whose interfaces are much simpler than their implementations. These modules have 2 advantages:

(a) A simple interface minimizes the complexity that a module imposes on the rest of the system.
(b) If a module is modified in a way that doesn't change its interface, then no other module will be affected by the modification. 

### A bit on interfaces

A key principle in software design, especially in OOP, is to prohibit access to all resources by default, allowing access only through well-defined entry points - interfaces. 

## 4.2 What's in an interface?

The interface to a module contains 2 kinds of information: formal and informal. The formal parts of an interface are specified explicitly in the code.

## 4.3 Abstractions

An abstraction is a simplified view of an entity, which omits unimportant details. 

In modular programming, each module provides an abstraction in the form of its interface. The interface is an abstraciton. The more unimportant details we can omit from an abstraction, the better. But, importantly, a detail can only be omitted from the abstraction if it is unimportant. Thus the abstraction can go wrong in 2 ways:
(i) It can omit details that are actually important (overly complex)
(ii) It can include details that could be omitted (overly obscure)

## 4.4 Deep Modules

The best modules are those that provide powerful functionality yet have simple interfaces. These are termed 'deep'. 

The mechanism for file I/O provided by Unix and its descendants e.g. Linux is a beautiful example of a deep interface. 

## 4.5 Shallow Modules

A shallow module is one whose interface is relatively complex in comparision to the functionality it provides. 

## 4.6 Classitis

There exists a sort of fetishisation around making classes smaller:

'The conventional wisdom in programming is that classes should be small, not deep... In systems suffering from classitis, developers are encouraged to minimize the amount of functionality in each new class: if you want more functionality, introduce more classes'. 

Smaller classes also result in a verbose programming style due to the large amount of boilerplate required for each class. 

## 4.8 Conclusion

Seperateing the interface of a module from its implementation hides the complexity of the implementation from the rest of the system. 

'The most important issue in designing classes and other modules is to make them deep, so that they have simple interfaces for the common use cases, yet still provide significant functionality. This maximises the amount of complexity that is concealed'. 


