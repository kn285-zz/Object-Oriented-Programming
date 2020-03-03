# Object Oriented Programming

There four different kinds of Object Oriented Programming: Encapsulation, Abstraction, Inheritance, and Polymorphism. 

This Repository is here to help explain what each kind of Object Oriented Programming(OOP) is and what it is used for.

#### Encapsulation

 Encapsulation is used when we have a program that has few logically different objects which communicate with each others
 
 You achieve encapsulation when you keep each object private inside the class. This means that objects don't have direct access to this state. They have to call a list of public functions called methods.
 
 The object manages its own state via methods — and no other class can touch it unless explicitly allowed. If you want to communicate with the object, you should use the methods provided. But (by default), you can’t change the state.
 
 An example of Encapsulation is as shown:
 ````
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