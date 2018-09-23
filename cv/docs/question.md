The content is the mix of questions and exams (via http://codeshare.io/) that you can expect to be different, but the level and approach might be similar.

# C# .NET OOP:
## 1. In OOP (and C#), what is the difference between `Abstract class` and `Interface`?
Abstract class often used to declare the core function of an class, some method can be implemented, interface is a blueprint contract, it just declare functions which derived class must implement.

One class can extend just only one abstrac class but can implement many interface

Abstrac class can have fields, interface can not

## 2. What is the `Abstract method, Virtual Method`?
Abstract method is the method `just be declared` without implementation, the derived class have to implement this abstract method.

Vitual method is the method with `implementation`, but `can be overrided` by derived class by override keyword

## 3. What is `“protected internal”` access modifiers?
`protected internal` The type or member can be accessed by any code in the assembly in which it is declared, or from within a derived class in another assembly.

`private protected` The type or member can be accessed only within its declaring assembly, by code in the same class or in a type that is derived from that class.

internal by all the code in the same assembly with it.

## 4. What is a `static class`?
Static class is the class just have static members and could not have instance, it is sealed and just can access it's member by class name

## 5. What is a `static constructor`?
Static construcror is the constructor use to initial the static members of class,  It is called automatically before the first instance is created or any static members are referenced. Same with static method, it just can access to static member of class

## 6. What is the difference between `static class` and `singleton`?
singleton have instance, static class is not

singleton can inherit, static class is not

## 7. What is `overriding` and `overloading` in C#?

They are the tow type of Polymorphism in OOP and show through override/ overload method

overload mothod that is can have many method in one class with the same name but different parameters (the type of parameter or the number of parameter, or the order)
## 8. What are the `SOLID` principles? Can you explain each principles with an example?

SOLID is five OOP design principles to avoid code smell and make it easy to refactor. There ar:

* `S` in SOLID is for Single Responsibility Principle, which states that every object should have a single responsibility and that all of its services should be aligned with that responsibility.
* `O` in SOLID is for Open-Closed Principle, which states that software entities – such as classes, modules, functions and so on – should be open for extension but closed for modification.
* `L` in SOLID is for Liskov Substitution Principle, which states that subclases should be substitutable for the classes from which they were derived. For example, if MySubclass is a subclass of MyClass, you should be able to replace MyClass with MySubclass without bunging up the program.
* `I` in SOLID is for Interface Segregation Principle, which states that clients should not be forced to depend on methods they don’t use.
* `D` in SOLID is for Dependency Inversion Principle, which states that high-level modules shouldn’t depend on low-level modules, but both should depend on shared abstractions. In addition, abstractions should not depend on details – instead, details should depend on abstractions.

# JavaScript:


## 1. What is the name of this syntax (function(){ //body here })(); and why should we use it?
This is immediately invoked function expression (IIFE), like it name, it use to immediately invoked function, the environment inside this function is isolated, it also use to encapsulation the function
## 2. What is JavaScript Closure? 
A closure is the combination of a function and the lexical environment within which that function was declared
## 3. How to clone an object in JS?
JSON or iteration for deep clone and Object.assign for shallow clone or jquery 
```
var copiedObject = jQuery.extend(true, {}, originalObject)
```
## 4. In programming, what is Parallel vs. Asynchronous?
Asynchronous programming is a means of parallel programming in which a unit of work runs separately from the main application thread and notifies the calling thread of its completion, failure or progress.

Parallel is many task working on the same time by defferent thread, asynchronous use just one thread with non blocking mechanism

It has this about asynchronous programming:

`Asynchronous` calls are used to prevent “blocking” within an application. [Such a] call will spin-off in an already existing thread (such as an I/O thread) and do its task when it can.

this about parallel programming:

In `parallel` programming you still break up work or tasks, but the key differences is that you spin up new threads for each chunk of work

and this in summary:

`asynchronous calls will use threads already` in use by the system and parallel programming requires the developer to break the work up, spinup, and teardown threads needed.
## 5. Is JavaScript on browser single thread or multithread?
js in browser is single thread
## 6. If JavaScript is a single thread, how asynchronous working?
because it use message queue and have one events loop

## 7. what is 'use strict'
It syntax to enable strict mode that `avoid unsafe code` (obsolescence, var scope, ...)

Eliminates some JavaScript `silent errors` by changing them to `throw errors`.

`Forbidden` some `syntax likely to be defined in future` versions of ECMAScript.

## 8 what is export/import 
The `export` statement is used when `creating JavaScript modules` to export functions, objects, or primitive values from the module so they can be used by other programs with the `import` statement.

There are two different types of export, `named` and `default`. You can have `multiple named` exports per module but `only one default` export. Each type corresponds to one of the above syntax:

## 9. What is === operator?
=== is called as strict equality operator which returns true when the two operands are having the same value without any type conversion.
```javascript
// Name export
// exports a function declared earlier
export { myFunction }; 

// exports a constant
export const foo = Math.sqrt(2);

//=====================
// Default exports (function):
export default function() {}

//=====================
//Default exports (class):
export default class {}
```

## 9  What is Prototype in js

Prototypes. When a function is created in JavaScript, JavaScript engine adds a prototype property to the function. This prototype property is an object (called as prototype object) has a constructor property by default. constructor property points back to the function on which prototype object is a property

## 10 what is promise

A promise represents the eventual `result of an asynchronous operation`. It is a placeholder into which the `successful result value or reason for failure` will materialize.