# <div align ="center"> Wiki 2: Compilers</br> <span style="font-size:0.5em;"> Written By: Jackson Kettel, Ken Cage, Kelvin Rajbhandari, Tamara Slone </span> </div>

## <div align = "center"> Introduction </div>

## <div align = "center"> Data Types [Kelvin] </div>
&nbsp; &nbsp; &nbsp; &nbsp; Data types in C++, like in any other programming language, are essential for defining the kind of data that variables can store and manipulate. They specify the amount of memory to allocate for a variable and the operations that is allowed on the data. C++ includes several built-in types, categorized mainly into primitive and derived types.

### <div align = "center"> Primitive Data Types </div>

&nbsp; &nbsp; &nbsp; &nbsp; Primitive Data Types are the basic building blocks of a programming language. They are predefined by the language and represent simple values. They are fixed in size and are directly supported by the underlying hardware. Integer is a primitive data type, which can be represented as ‘int’, ‘short’, ‘long’, ‘long long’, depending on if it is known how big/small the number is. Ideally you want to pick the best fit with the least amount of unused bits in memory to minimize any waste of resources. The same principle follows with Floating-Point Types. Another example would be Character, a type used for single characters to store ASCII values.

### <div align = "center"> Derived Data Types </div>

&nbsp; &nbsp; &nbsp; &nbsp; Derived Data Types are constructed from primitive data types and allow more complex data structures and abstractions. Our first example will be Arrays, a collection of elements of the same data type that can be accessed via indices. Essentially, arrays facilitate handling multiple related data items as one and they require contiguous memory allocation. Another derived data type would be Pointers, variables that store memory addresses. They are crucial for dynamic memory allocation and the fundamental pieces to complex data structures like Linked Lists & Trees.

<br/>
Understanding C++ data types is crucial for efficient memory usage and error-free programming. Choosing the appropriate data type ensures optimal performance and resource management in software applications.

## <div align = "center"> Expressions [Ken] </div>

## <div align = "center"> Assignment Statements [Ken] </div>

## <div align = "center"> Statement-Level Control Structures [Kelvin] </div>

&nbsp; &nbsp; &nbsp; &nbsp; Statement-Level Control Structures in C++ are vital for directing the flow of program execution. They allow for conditional operations, repeated execution, and branching, making programs more dynamic and responsive.

### <div align = "center"> Conditional Statements </div>

&nbsp; &nbsp; &nbsp; &nbsp; Conditional statements, include “if-else if/else” statements which execute code blocks based on Boolean expressions. They are effectively enabling decision-making processes within programs. Another conditional would be a “switch”. A switch statement selects one out of all the code blocks to execute, based on the value of an expression. It is efficient for handling multiple conditions.

### <div align = "center"> Looping Constructs </div>

&nbsp; &nbsp; &nbsp; &nbsp; Looping constructs enable repeated execution of code blocks. An example, the “for Loop” is ideal for scenarios where the number of iterations is known beforehand. Another example, the “while Loop” repeats a block of code as long as the specified condition remains true, which is useful when the number of iterations is not known beforehand.

### <div align = "center"> Jump Statements </div>

&nbsp; &nbsp; &nbsp; &nbsp; Jump statements alter the normal flow of control. The “break” statement exits a loop or “switch” statement prematurely. The “continue” statement skips the current iteration of a loop and proceeds with the next. The “goto” statement transfers control to a labeled statement, though its use is generally discouraged due to readability concerns.

<br/>
Mastering control structures is essential for implementing logic and creating flexible, robust programs. They allow programmers to handle various scenarios and conditions, ensuring the program behaves as expected under different circumstances.


## <div align = "center"> Subprograms [Jackson] </div>

## <div align = "center"> Abstract Data Types and Encapsulation Concepts [Tamara] </div>

## <div align = "center"> Object-Oriented Programming[Tamara] </div>

&nbsp; &nbsp; &nbsp; &nbsp; In contrast to other C languages, C++ distinguishes itself through its structure, which is shaped by the principles of Object-Oriented Programming. Object-oriented programming (OOP) is a programming concept that focuses on objects in the form of data fields and code in the form of methods or procedures. OOP objects are typically instances of classes that define the structure and behavior of objects. A programming language that uses OOP must support three key features. These features are abstract data types, inheritance, and dynamic binding of method calls. C++ has a unique mix of OOP and class systems based on SIMULA 67. Along with allowing for backward combability in the C language, Making C++ a hybrid language of procedural programming and OOP.

&nbsp; &nbsp; &nbsp; &nbsp;  C++ can contain objects that are static, stack dynamic, and heap dynamic. However, because C does not have implicit storage allocation, heap dynamics must be reallocated to prevent memory leaks. Due to these memory leaks, many C++ classes tend to also implement destructor methods that allow for deallocating heap memory that is referenced by objects that no longer exist. These methods may also be used to record the state of an object before it ceases to exist.

### <div align = "center"> Inheritance  </div>
&nbsp; &nbsp; &nbsp; &nbsp; Since C++ is based around OOP, it allows for the use of inheritance to define relationships between classes. Inheritance is a fundamental structure within OOP that allows a newly created class (known as a derived class.) to inherit attributes and methods from an already existing class (known as a base class). Meaning that the derived class can reuse code from the base class, which reduces the redundancy and reusability of previous code. C++ classes can either be stand-alone without the need for inheritance or can have multiple references to base classes using multiple inheritance. However, C++ objects must be initialized before they are used, meaning that all C++ classes must include a constructor method that initializes all data fields. These constructor methods must be called when initiating an object within a base class or superclass.
    
        Example of C++ Inheritance:
            drieved_class(subclass parameters) : public base_class(superclass parameters){
            // Code for subclass is listed here that can call for methods within the base class.
        }



## <p align = "center"> Exception Handling and Event Handling [Jackson]</p>

## <p align = "center"> Example C++ Code </p>




