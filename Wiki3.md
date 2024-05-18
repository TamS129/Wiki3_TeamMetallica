# <div align ="center"> Wiki 2: Compilers</br> <span style="font-size:0.5em;"> Written By: Jackson Kettel, Ken Cage, Kelvin Rajbhandari, Tamara Slone </span> </div>

## <div align = "center"> Introduction </div>

## <div align = "center"> Data Types [Kelvin] </div>

## <div align = "center"> Expressions [Ken] </div>

## <div align = "center"> Assignment Statements [Ken] </div>

## <div align = "center"> Statement-Level Control Structures [Kelvin] </div>

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




### <div align = "center"> Dynamic Binding  </div>


    
        
    

## <p align = "center"> Exception Handling and Event Handling [Jackson]</p>

## <p align = "center"> Example C++ Code </p>




