# Object Oriented Programming

There four different kinds of Object Oriented Programming: Encapsulation, Abstraction, Inheritance, and Polymorphism. 

This Repository is here to help explain what each kind of Object Oriented Programming(OOP) is and what it is used for.

### Encapsulation

 Encapsulation is used when we have a program that has few logically different objects which communicate with each others
 
 You achieve encapsulation when you keep each object private inside the class. This means that objects don't have direct access to this state. They have to call a list of public functions called methods.
 
 The object manages its own state via methods — and no other class can touch it unless explicitly allowed. If you want to communicate with the object, you should use the methods provided. But (by default), you can’t change the state.
 
 An example of Encapsulation is as shown:
 ```
 class Addition:

    @staticmethod
    def sum(augend, addend=None):
        if isinstance(augend, list):
            return Addition.sumList(augend)
        return augend + addend

    @staticmethod
    def sumList(valueList):
        result = 0
        for value in valueList:
            result = Addition.sum(result, value)

        return result
```
### Abstraction

Abstraction is considered to be a natural extension of encapsulation.

Typically when using OOP programs get extremely large, and objects communicate with each other more often than not. So, to maintain it is very difficult. This is where abstraction comes into play.

Applying abstraction means that each object should *only* expose a high-level mechanism for using it. This mechanism should hide internal implementation details. It should only reveal operations relevant for the other objects.

Preferably, this mechanism should be easy to use and should rarely change over time. Think of it as a small set of public methods which any other class can call without “knowing” how they work.

```
from MathOperations.Addition import Addition;
from MathOperations.Subtraction import Subtraction;

class Calculator:
    Result = 0
    def __init__(self):
        pass

    def addition(self, a, b):
        return float(a) + float(b)

    def subtraction(self, a, b):
        return float(a) - float(b)
```

### Inheritance

Objects are often very similar, they typically common logic. However they are not entirely the same. If they share common logic but also have uniquie logic, how can we create two different classes. This is where inheritance comes into play.

Inheritance is when you create a (child) class by deriving from another (parent) class. So we form a heirarchy. The child uses all the fields and methods from the parent class but implements its own fields and methods.

```
from Calculator.calculator import Calculator
from MathOperations.mean import Mean

class Statistics(Calculator):

def mean(self, data):
    self.Result = Mean(data)
    return self.Result
```



