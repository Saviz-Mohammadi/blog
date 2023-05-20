---
title: "C++ Variables"
date: 2023-05-12T14:06:22-07:00
draft: true
---

<br>
<br>

### Intro

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;One of the most important abilities of a computer is its capability to manipulate and work with data or information. Data is utilized in every operation or process performed by a computer. In order for a computer to use data, it needs to store it in a location called RAM (Random Access Memory). RAM is a volatile form of memory that loses its contents when the computer shuts down or restarts. Data cannot persist on RAM, but it can be transferred and manipulated faster than other types of storage units. This unique capability is what makes RAM so important, as programs often need to process enormous amounts of data quickly. Furthermore, It is organized as a contiguous block consisting of multiple memory cells, each capable of storing and referencing a piece of data (In this case refered to as a word). To allow other processes and programs to access and manipulate these cells of data, each cell is assigned a unique address that can be used for referencing. These addresses typically appear in a format similar to the following:
</div>

<br>

```C++ {linenos=false}
Typical format of an address: 0x7fff5fbff6c8
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;If a programmer needs to modify the contents of a specific cell in RAM, referring to the address can indeed be challenging, especially when dealing with a large magnitude of data. It would be troublesome for the programmer to memorize a significant number of complex addresses in order to reference each piece of data individually. The human brain is not naturally designed for remembering and managing such detailed information. To address this challenge, more convenient ways have been developed for accessing and manipulating data.
</div>

<br>
<br>

### Variables

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<ins style="font-weight: 700;text-underline-offset: 5px;">A variable serves as a mechanism for programmers to store, manipulate, and reference data in computer memory.</ins> Variables play a crucial role as they enable us to interact with data in a convenient and straightforward manner. Variables accomplish this by assigning meaningful names and labels to the memory locations where the data is stored. The beauty of variables lies in their flexibility; their content can be modified and changed, hence the term "variable". Instead of directly dealing with memory addresses, which can be complex and cumbersome, variables provide a more intuitive and human-readable way of referencing and manipulating data.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;An illustrative example of utilizing variables for storing and referencing data is the representation of a player character in a game. In this scenario, a player typically has X, Y, and Z coordinates, which indicate their position within the game world. Let's consider an example showcasing how these values can be stored and accessed using the C++ programming language:
</div>

<br>

```C++
main(int argc, char* argv[])
{
	// Declaration & Initialization.
	int coordinate_x = 100;
	int coordinate_y = 0;
	int coordinate_z = 50;
	
	// Outputing the content & address.
	std::cout << "The content of x variable is: " << coordinate_x << "\n";
	std::cout << "The address of x variable is: " << &coordinate_x << "\n\n";
	
	std::cout << "The content of y variable is: " << coordinate_y << "\n";
	std::cout << "The address of y variable is: " << &coordinate_y << "\n\n";
	
	std::cout << "The content of z variable is: " << coordinate_z << "\n";
	std::cout << "The address of z variable is: " << &coordinate_z << std::endl;
	
	return (0);
}
```

<br>

```C++ {linenos=false}
The content of x variable is: 100
The address of x variable is: 0x7fff5fbff6cc

The content of y variable is: 0
The address of y variable is: 0x7fff5fbff6c8

The content of z variable is: 50
The address of z variable is: 0x7fff5fbff6c4
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In C++, the ampersand (&) symbol is used to obtain the address of a variable. By using the address-of operator, we can retrieve the memory location where a variable is stored. The ability to acquire the address of a variable is valuable for debugging and memory analysis purposes. By inspecting memory addresses, programmers can track the location and value of variables during program execution
</div>

<br>
<br>

### Declaration & Initialization

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Now that we have acquired a basic understanding of variables, let's discuss the different stages involved in creating and working with them. The process of creating and utilizing a variable can be divided into two general steps:
</div>

<br>

- Declaration
- Initialization

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In programming, it is important to understand that declaration and initialization are two distinct concepts with different meanings and purposes. While these terms are sometimes used interchangeably, it is essential to recognize and comprehend their differences to ensure accurate communication and understanding within the programming community.
</div>

<br>
<br>

###### What is Declaration?

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<ins style="font-weight: 700;text-underline-offset: 5px;">Declaration is a fundamental process in programming where we, as programmers, inform the compiler about the existence and characteristics of a variable.</ins> When we declare a variable, we are instructing the compiler to allocate memory for that variable according to its data type. The name we provide serves as a unique identifier for accessing and manipulating the variable throughout the program. At a fundemental level, declaration is the only requirement to create and interact with variables. The syntax structure for declaring variables in C++ follows this general pattern:
</div>

<br>

```C++ {linenos=false}
Syntax for Declaring variables:

[Access modifier] [data_type] [identifier];
```

<br>

```C++
main(int argc, char* argv[])
{
	// The "number" variable will store whole numbers.
	int number;
	
	return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In the given example, we can observe the declaration of a variable without the use of any access modifiers. (Access modifiers will be explained in later discussions). During variable declaration, we start by specifying the data type, which informs the compiler about the type of data that will be stored in the variable. In the example, the data type specified is "int", indicating that the variable will hold whole numbers (It's important to note that different data types can hold different kinds of data, and we'll delve into more details about data types in later discussions). In addition to the data type, we assign a label or name to the variable. In this case, the identifier "number" is used to uniquely identify and refer to the variable. The chosen name should be meaningful and indicative of the purpose or content of the variable. Lastly, it's essential to end the declaration statement with a semicolon (;). The semicolon serves as a statement terminator, indicating the end of the line of code. It is a crucial syntax element in C++ and many other programming languages.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;At this point, you may wonder, "What is Initialization?" Moreover, if declaration is sufficient for creating and interacting with variables, why is it essential to understand Initialization? To address these questions, let's begin by understanding what Initialization entails.
</div>

<br>
<br>

###### What is Initialization?

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<ins style="font-weight: 700;text-underline-offset: 5px;">Initialization refers to the act of assigning an initial value to a variable at the time of its declaration or creation.</ins> Hence, it is called "Initialization" because it sets the variable's starting value. In programming, Initialization is commonly achieved using the equal sign (=) followed by an expression or value. For example, when we declare a variable called "number_1" and initialize it with the value 57, we are performing Initialization. In C++, Initialization can also be done on two separate lines if desired.
</div>

<br>

```C++
main(int argc, char* argv[])
{
	// The equal sign (=) can be used to initialize a variable.
	int number_1 = 57;
	
	// Declaring the variable first, and initializing it on another line.
	int number_2;
	number_2 = 100;
	
	return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Now we can have a discussion as to why information is important. Initialization is important because it ensures that variables have a known value when they are first used in the program. Some languages, like C++, require variables to be initialized before they can be used, which helps enforce good programming practices. The side effects and drawbacks of not initializing variables in C++ can be significant, and can lead to unexpected behavior or even security vulnerabilities in the program. Here are some important notes:
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;If a variable is not initialized, it will contain whatever value happens to be in memory at that location. This can result in unpredictable behavior, as the program may assume the variable has a certain value when in fact it has a completely different value. This can lead to logic errors, crashes, or other unexpected behavior.
</div>

<br>

```C++
#include <iostream>

int main(int argc, char* argv[])
{
    int input = 0;
	
	// Notify the user that they need to input a number.
    std::cout << "Please enter a number: ";
	
	// Obtain input from user.
    std::cin >> input;
    
	// Depending on the input do something.
    if (input > 0)
    {
        // Perform some code.
    }
	
    else
    {
        // Perform some other code.
    }
    
    return (0);
}

```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In the example above, we declare an integer variable called "input", but we do not initialize it with a value. Then, we prompt the user to enter a number using std::cin. Depending on whether the number is positive or negative, we perform different operations. The problem is that since the input variable is not initialized, its value is undefined, which can lead to unpredictable behavior. For example, if the user enters a non-integer value or a value that cannot be read by std::cin, the value of input will remain undefined, and the conditional statement will behave unpredictably. What is even worse is that if some other segment of our code later on decides to use the content of this variable, then it will not only not work, but it may also cause problems on the next run of the program, because the value from the previous operation will remain in this memory location.
</div>

<br>
<br>

###### Try printing without Initialization

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;We might ask ourselves what happens if we attempt to print the content of a variable that has not been Initialized yet. In C++, if you try to print a variable that is only declared but not initialized, the behavior is undefined. This means that the outcome cannot be predicted and can vary depending on the compiler, the optimization settings, and other factors. Let's explore a few possible scenarios that could occur:
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<ins style="font-weight: 700;text-decoration: none;">1-</ins> In some cases, the uninitialized variable may contain a random value from the memory location where it is stored. This value could be leftover from a previous operation or simply an arbitrary value. If you print such a variable, you will see whatever value happens to be stored in that memory location at the time. This is commonly refered to as <ins style="font-weight: 700;text-underline-offset: 5px;">"Garbage value"</ins>.
</div>


Compiler Warning: Many modern compilers will generate a warning when you attempt to use an uninitialized variable. The warning serves as a reminder that you are accessing a variable that may not have a meaningful value. However, the code will still compile and run.

Initialization by Chance: In rare cases, an uninitialized variable may coincidentally have a value that appears to be meaningful. This can mislead you into thinking that the variable is correctly initialized. However, relying on this behavior is highly discouraged, as it is unreliable and can lead to bugs and unexpected behavior in your code.

Program Crash or Unpredictable Behavior: In other cases, attempting to use an uninitialized variable can lead to program crashes or undefined behavior. The variable may cause memory access violations, segmentation faults, or other runtime errors that can terminate the program abruptly.

<br>
<br>

###### A word about memory management

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Wheather a location in memory contains the value from previous programs/operations or is cleared and restored to the defualt value depends on a number of factors. Some of these factors include the way that the operating system handles the momery and the standards set in the programming language and its environmental IDEs/compilers. Some operating systems do not clear the value in the memory after the program/operation is finished as it will probably be overwritten by a later program/operation that uses the same memory location anyways. Some other opertaing systems enforce the need for memory to be cleared and defaulted after the end of each program/operation.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;On the other hand, some programming languages may do the task of Initializating the variables automatically for the programmer. These languages and their respective complier environments insure that all variables are Initialized even if the progarmmer forgets to do it. However, all these conditions/rules may change at any time by the decisions of the maintainers of that programming language/complier environments and it is hard to keep up with all the latest updates. It is generally recommended to always do Initialization by ourselves and do not rely on external processes to do it for us.
</div>

<br>
<br>

### Identifiers and naming conventions

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;The names that we associate to our variables are commonly refered to as <b>identifiers</b>. This is because they ironically, identify what we are trynig to refer to. It almost acts like an identification (ID) that can be used to search and find and use a specific piece of information. When you create an identifier, you should try to make the name both meaningful and easy to remember. To make a name meaningful, you should use as many characters as you need, There are many different methods/patterns in computing science to name your identifiers. camel case, pascal case, snake case. While languages do not enforce any of these patterns it is a good idea to choose one and stick to it.

C++ in particular is case-sensitive, you need to be careful when you create and use identifiers. If, for example, you define an identifier named subtotal, you can’t refer to it later as Subtotal. That’s a common coding error
</div>

<br>
<br>

### Assigning new values

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Initialization is not the only scenario in which we want to assign a value to a variable. Throughout the life time of a program it is very common to change the content of an existing variable multiple times. This is known as an <b>assignment statement</b>, in which the programmer attempts to tell the compiler to change the contents of a variable. This can be done in the following way:
</div>

<br>

```C++
#include <iostream>

int main(int argc, char* argv[])
{
    int number = 0;
	
	// Assigning a new value to "number".
	number = 20;
	
	// Display content of "number" variable.
    std::cout << "The \"number\" variable contains: " << number;
    
    return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;It is important to remember that in a assignment statement (except for when Initializating) we do not specify the data type of the variable again (as it would mean that we want to declare a variable with the same name again, which is not allowed). Instead we only use the identifier of the variable followed by a equal sign (=) and the value that we want it to contain.
</div>

<br>

```C++
[name of variable] = [value];
```


You should research and see what naming conventions are used for variables.
You need to talk about lvalues and rvalues.