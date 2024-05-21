# <div align ="center"> Wiki 3: C++ Deep Dive</br> <span style="font-size:0.5em;"> Written By: Jackson Kettel, Ken Cage, Kelvin Rajbhandari, Tamara Slone </span> </div>

## <div align = "center"> Introduction </div>

## <div align = "center"> Data Types [Kelvin] </div>
&nbsp; &nbsp; &nbsp; &nbsp; Data types in C++, like in any other programming language, are essential for defining the kind of data that variables can store and manipulate. They specify the amount of memory to allocate for a variable and the operations that is allowed on the data. C++ includes several built-in types, categorized mainly into primitive and derived types.

### <div align = "center"> Primitive Data Types </div>

&nbsp; &nbsp; &nbsp; &nbsp; Primitive Data Types are the basic building blocks of a programming language. They are predefined by the language and represent simple values. They are fixed in size and are directly supported by the underlying hardware. Integer is a primitive data type, which can be represented as ‘int’, ‘short’, ‘long’, ‘long long’, depending on if it is known how big/small the number is. Ideally you want to pick the best fit with the least amount of unused bits in memory to minimize any waste of resources. The same principle follows with Floating-Point Types. Another example would be Character, a type used for single characters to store ASCII values.  

```cpp
             int anInteger = 10;          // Integer (whole number)
             float aFloat = 3.142;        // Floating point number
             short aShort = 1.1;          // Short Integer
             char aCharacter = 'K';       // Character
             bool aBoolean = true;        // Boolean
             string text = "Lets go!";    // String
```

### <div align = "center"> Derived Data Types </div>

&nbsp; &nbsp; &nbsp; &nbsp; Derived Data Types are constructed from primitive data types and allow more complex data structures and abstractions. Our first example will be Arrays, a collection of elements of the same data type that can be accessed via indices. Essentially, arrays facilitate handling multiple related data items as one and they require contiguous memory allocation. Another derived data type would be Pointers, variables that store memory addresses. They are crucial for dynamic memory allocation and the fundamental pieces to complex data structures like Linked Lists & Trees.  

```cpp
             int arr[3];        // Array, type Integer of size 3
             int* ptr;          // Pointer of type Integer
             int& ref;          // Reference of type Integer
```

<br/>
Understanding C++ data types is crucial for efficient memory usage and error-free programming. Choosing the appropriate data type ensures optimal performance and resource management in software applications.

## <div align = "center"> Expressions [Ken] </div>

&nbsp; &nbsp; &nbsp; &nbsp; C++ expressions are a fundamental aspect of the C++ programming language, representing the combination of variables, operators, and function calls to produce a value. Expressions are the building blocks of any C++ program, enabling developers to perform computations, assign values, and control the flow of the program. There are various types of expressions in C++, including arithmetic, logical, relational, and assignment expressions, each serving a distinct purpose in the language's syntax and functionality.

### <div align = "center"> Arithmetic Expressions </div>

Arithmetic expressions in C++ involve operators like addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`). These expressions are used to perform mathematical operations on variables and constants. For example, an arithmetic expression like `int result = a + b * c;` computes the product of `b` and `c`, and then adds `a` to the result. The order of operations in C++ follows the standard mathematical precedence, ensuring that expressions are evaluated correctly.

### <div align = "center"> Logical Expressions </div>

Logical expressions, on the other hand, involve logical operators such as `&&` (logical AND), `||` (logical OR), and `!` (logical NOT). These expressions are crucial for decision-making in C++ programs, as they evaluate to either true or false. For instance, the expression `(a > b) && (c < d)` will be true only if both conditions `a > b` and `c < d` are true. Logical expressions are commonly used in control structures like `if` statements and loops to determine the flow of execution based on specific conditions.

### <div align = "center"> Relational Expressions </div>

Relational expressions compare the values of two operands using relational operators like `==` (equal to), `!=` (not equal to), `<` (less than), `>` (greater than), `<=` (less than or equal to), and `>=` (greater than or equal to). These expressions are essential for evaluating conditions and making decisions within a program. For example, the expression `if (a == b)` checks if the value of `a` is equal to `b`, and if so, executes the corresponding block of code. Relational expressions are integral to the logical flow and control structures in C++.

### <div align = "center"> Assignment Expressions </div>

Assignment expressions are used to assign values to variables. The most basic assignment operator is `=`, but C++ also provides compound assignment operators like `+=`, `-=`, `*=`, and `/=`. An assignment expression not only assigns a value but also returns that value, making it possible to use assignment expressions in more complex expressions. For example, `a = b = 5;` assigns the value 5 to both `a` and `b`. Understanding these various types of expressions is crucial for writing efficient and effective C++ code.

## <div align = "center"> Assignment Statements [Ken] </div>

&nbsp; &nbsp; &nbsp; &nbsp; C++ assignment statements, closely related to expressions, are fundamental components of the language, allowing developers to set or update the value of variables. While expressions in C++ form the foundation for computations and control flow, assignment statements specifically handle the task of storing values in variables. The simplest form of an assignment statement uses the `=` operator to assign a value to a variable, such as `int a = 5;`. This statement assigns the integer value 5 to the variable `a`. Assignment statements are essential for initializing variables, updating their values, and managing the state of a program.

In addition to the basic assignment operator, C++ offers several compound assignment operators that combine arithmetic or bitwise operations with assignment. These include `+=`, `-=`, `*=`, `/=`, and `%=`, among others. For example, the statement `a += 5;` is equivalent to `a = a + 5;`, adding 5 to the current value of `a` and then storing the result back in `a`. These operators provide a concise and efficient way to perform common arithmetic operations while updating the value of a variable.

C++ also supports assignment statements involving multiple variables. A chained assignment allows a single value to be assigned to multiple variables simultaneously. For instance, `int a, b, c; a = b = c = 10;` assigns the value 10 to all three variables `a`, `b`, and `c`. This feature is particularly useful for initializing multiple variables to the same value in a single statement, improving code readability and reducing redundancy.

Another important aspect of C++ assignment statements is the use of the copy assignment operator and the move assignment operator. The copy assignment operator (`=`) is used to copy the value from one object to another of the same type, while the move assignment operator (`=` with `std::move`) transfers ownership of resources from one object to another. These operators are crucial for managing dynamic memory and resource management in C++, especially when dealing with complex data structures like classes and objects.

These statements not only allow developers to manage the values of variables but also enable more complex operations and optimizations. Mastery of assignment operators and their nuances ensures that a programmer can write concise, efficient, and maintainable code.


## <div align = "center"> Statement-Level Control Structures [Kelvin] </div>

&nbsp; &nbsp; &nbsp; &nbsp; Statement-Level Control Structures in C++ are vital for directing the flow of program execution. They allow for conditional operations, repeated execution, and branching, making programs more dynamic and responsive.

### <div align = "center"> Conditional Statements </div>

&nbsp; &nbsp; &nbsp; &nbsp; Conditional statements, include “if-else if/else” statements which execute code blocks based on Boolean expressions. They are effectively enabling decision-making processes within programs. Another conditional would be a “switch”. A switch statement selects one out of all the code blocks to execute, based on the value of an expression. It is efficient for handling multiple conditions.  

```cpp
             if (execute == True) {
                cout << "Condition is True, this block is executed!";
                //Code
             else {
                cout << "Condition evaluated to false, this is run.";
                //Code
             }
```

### <div align = "center"> Looping Constructs </div>

&nbsp; &nbsp; &nbsp; &nbsp; Looping constructs enable repeated execution of code blocks. An example, the “for Loop” is ideal for scenarios where the number of iterations is known beforehand. Another example, the “while Loop” repeats a block of code as long as the specified condition remains true, which is useful when the number of iterations is not known beforehand.  

```cpp
             for (int timesExecuted = 0; timesExecuted < 10; timesExecuted++) {
                cout << "This is one single execution out of 10! \n";
                //Code
             }
```

### <div align = "center"> Jump Statements </div>

&nbsp; &nbsp; &nbsp; &nbsp; Jump statements alter the normal flow of control. The “break” statement exits a loop or “switch” statement prematurely. The “continue” statement skips the current iteration of a loop and proceeds with the next. The “goto” statement transfers control to a labeled statement, though its use is generally discouraged due to readability concerns.  

```cpp
             for (int timesExecuted = 0; timesExecuted < 10; timesExecuted++) {
                if (timesExecuted = 5) {
                    cout << "Let's break this iteration.";
                    break;
             }
```

<br/>
Mastering control structures is essential for implementing logic and creating flexible, robust programs. They allow programmers to handle various scenarios and conditions, ensuring the program behaves as expected under different circumstances.


## <div align = "center"> Subprograms [Jackson] </div>

&nbsp; &nbsp; &nbsp; &nbsp; Subprograms are a key component of C++, and allow for repeating code blocks, abstracting functions, and improving the readability of the code. When code blocks are put into a subprogram, it allows the program to reuse the code block multiple times and with different parameters. When you put code blocks into subprograms, it allows you to abstract tasks that need to be performed, which makes it so those using the subprogram don’t have to understand the logic inside the subprogram. This consequently makes the program more readable by reducing redundancy and encapsulating different tasks. We will now go over the different properties of subprograms in C++.

### <div align = "center"> Procedures </div>

&nbsp; &nbsp; &nbsp; &nbsp;Procedures in C++ allow you to execute a block of code, but not have the subprogram return anything. In order to make a procedure, you must begin your method declaration with the void keyword as shown below. This indicates that the subprogram will not return any value when it finishes executing. 
```cpp
             void myProcedure() {
	            // Code
            }
```
### <div align = "center"> Functions </div>

&nbsp; &nbsp; &nbsp; &nbsp;Functions in C++ allow you to return a function after executing the code in a subprogram. This can be very useful for delegating a task to a function, and then having that function return something. In order to make a function, replace the void in a procedure with the return type and include a return call at the end of execution. The below code shows a function that will return the Integer 1 when called.
```cpp
             int myFunction() {
	            //Code
	            return 1;
            }
```

### <div align = "center"> Arguments and Parameters </div>

&nbsp; &nbsp; &nbsp; &nbsp;In order to pass values into a subprogram in C++, you can include the value type in the subprogram declaration and when it is called. C++ also offers overloading subprograms, where you can have multiple subprograms with the same name, but different parameters.
```cpp
             double multiply(double x, double y) {
	            return x * y;
            }

            double multiply(double x, double y, double z) {
                return x * y * z;
            }

            int main() {
                double product1 = multiply(5.5, 8.5);
                double product2 = multiply(4.5, 7.5, 9.5);
            }
```

### <div align = "center"> Declaration </div>

&nbsp; &nbsp; &nbsp; &nbsp;If you want to call a method in C++, you must define it before calling it. In C++, you may define a subprogram before you provide the definition of that subprogram. This is useful because if you wish to put the definition of a function below another for readability, then you only need to declare the function before as shown below.
```cpp
             int myFuction();

            int main() {
                int number = myFunction();
            }

            int myFunction() {
                    return 5;
            }
```

## <div align = "center"> Abstract Data Types and Encapsulation Concepts [Tamara] </div>
### <div align = "center"> Abstract Data Types
&nbsp; &nbsp; &nbsp; &nbsp; C++ excels at defining custom data structures through its support for classes, allowing developers to create clear interfaces and hidden implementations for their data.  For programmers to create these clear interfaces by using abstract data types and encapsulation. Abstract Data Types (ADT’s) are data types that represent a concept rather than an object. C++ supports the creation of abstract data types by using a function known as pure virtual function. Pure virtual functions are functions that must be overridden within a new class called a derived class.  In C++ a program can implement multiple virtual functions depending on what the programmer needs. However, pure virtual functions must always be overridden within the derived class and the class that contains these functions cannot be created into objects rather its purpose is to be called within the derived class.

### <div align = "center"> Encapsulation </div>
&nbsp; &nbsp; &nbsp; &nbsp; Encapsulation is a fundamental principle of object-oriented programming (Which will be discussed in the section below.) and is well-supported in C++. Encapsulation refers to the bundling of data and the methods that operate on that data into a single class. The primary goals of encapsulation are to protect the internal state of an object from unintended interference and to provide a clear interface for interacting with that object. Encapsulation provides many benefits such as data hiding, modularity, and maintenance. Data hiding protects data by restricting access to the internal state of an object. Modularity allows for different parts of a program to be developed, tested, and maintained independently from the rest of the code. Maintenance in encapsulated code allows for the programmer to change and rearrange code internally without causing issues outside of that specific code.
 
In C++ encapsulated code can be found using 3 types of entities called private, protected, and public clauses. Private clauses allow for their respected objects to be specifically available within the class itself, these objects cannot be changed or modified outside their dedicated classes. Protected clause objects are available within their own classes and any of the derived classes (also known as subclasses) that include these protected objects. Public clauses are accessible from anywhere throughout the program where the objects are available.

Like other programming languages that allow for encapsulation, C++ can create constructor methods in class definitions. Constructor methods are functions or methods that initialize data members of newly created objects. In C++ these constructor methods can also be implemented for allocation of heap-dynamic data that contain references to pointers in the newly created object. Due to C++’s ability to allocate memory, the program language can also implement destructor methods that allow for deallocating heap memory that is referenced by objects that no longer exist. These methods may also be used to record the state of an object before it ceases to exist.


## <div align = "center"> Object-Oriented Programming [Tamara] </div>

&nbsp; &nbsp; &nbsp; &nbsp; In contrast to its base language C, C++ distinguishes itself through its structure, which is shaped by the principles of Object-Oriented Programming. Object-oriented programming (OOP) is a programming concept that focuses on objects in the form of data fields and code in the form of methods or procedures. OOP objects are typically instances of classes that define the structure and behavior of objects. A programming language that uses OOP must support three key features. These features are abstract data types, inheritance, and dynamic binding of method calls. C++ has a unique mix of OOP and class systems based on SIMULA 67. Along with allowing for backward combability in the C language, Making C++ a hybrid language of procedural programming and OOP. C++ can contain objects that are static, stack dynamic, and heap dynamic. However, because C does not have implicit storage allocation, heap dynamics must be reallocated to prevent memory leaks.

C++ can contain objects that are static, stack dynamic, and heap dynamic. However, because C does not have implicit storage allocation, heap dynamics must be reallocated to prevent memory leaks. Due to these memory leaks, many C++ classes tend to also implement destructor methods that allow for deallocating heap memory that is referenced by objects that no longer exist. These methods may also be used to record the state of an object before it ceases to exist.

### <div align = "center"> Inheritance  </div>
&nbsp; &nbsp; &nbsp; &nbsp; Since C++ is based around OOP, it allows for the use of inheritance to define relationships between classes. Inheritance is a fundamental structure within OOP that allows a newly created class (known as a derived class.) to inherit attributes and methods from an already existing class (known as a base class). Meaning that the derived class can reuse code from the base class, which reduces the redundancy and reusability of previous code. C++ classes can either be stand-alone without the need for inheritance or can have multiple references to base classes using multiple inheritance. However, C++ objects must be initialized before they are used, meaning that all C++ classes must include a constructor method that initializes all data fields. These constructor methods must be called when initiating an object within a base class or superclass.
    
        Example of C++ Inheritance:
            drieved_class(subclass parameters) : public base_class(superclass parameters){
            // Code for subclass is listed here that can call for methods within the base class.
        }

## <p align = "center"> Exception Handling and Event Handling [Jackson]</p>

&nbsp; &nbsp; &nbsp; &nbsp;Exception handling in C++ is done using a try catch block. Exception handling is useful for handling unexpected problems that arise when executing a program. In the try block, you put the code you wish to execute and a throw statement if the code produces an unexpected output. In the catch block, you put the code that handles the exception specified in the throw statement. This can be useful for terminating a program if something goes wrong, and can help give a detailed error message to let the user know what went wrong.
```cpp
            try {    	 
                // Code that might throw an exception
                throw ExceptionType("Error message");
            }
            catch( ExceptionName e1 )  {   
                // code to handle exception
            }
```

## <p align = "center"> Example C++ Prgoram </p>
```cpp
            #include <iostream>
            #include <iostream>
            #include <cstdlib>
            #include <stdexcept>

            class ParentClass {
            public:
                virtual void Introduction() = 0;
                virtual void PlayGame() = 0;
                virtual void GetGuesses() = 0;
                virtual void CheckGuess(int guess) = 0;
                virtual void EndGame() = 0;
            };


            class ChildClass : public ParentClass {
            private:
                int randomNumber;
                int guess;

            public:
                void Introduction() {
                    std::cout << "Welcome to the game!\n";
                }

                void PlayGame() {
                    std::cout << "Let's play a game!\n";
                    srand((unsigned)time(NULL));
                    randomNumber = rand() % 100 + 1;
                    GetGuesses();
                }

                void GetGuesses() {

                    try {
                        while (guess != randomNumber) {
                            std::cout << "Enter a number between 1 and 100: ";
                            std::cin >> guess;

                            if (!std::cin) {
                                throw std::runtime_error("Goofball");
                            }
                            else if (guess < 1 || guess > 100) {
                                std::cout << "Invalid guess.";
                            }
                            else {
                                CheckGuess(guess);
                            }
                        }
                    }
                    catch (std::runtime_error& e) {
                        std::cout << "Invalid input. Do not enter a string goofball.\n";
                        std::cin.clear();
                        std::cin.ignore(10000, '\n');
                    }
                }

                void CheckGuess(int guess) {
                    if (guess == randomNumber) {
                        EndGame();
                    }
                    else {
                        std::string message = (guess > randomNumber) ? "Guess lower\n" : "Guess higher\n";
                        std::cout << message;
                    }
                }

                void EndGame() {
                    std::cout << "Congratulations! You guessed the number!\n";
                }
            };
            int main()
            {
                ChildClass child;
                child.Introduction();
                child.PlayGame();
            }
```





