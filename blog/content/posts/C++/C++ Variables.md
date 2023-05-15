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
&emsp;&emsp;&emsp;&emsp;One of the most important abilites of a computer is to manipulate and work with data (information). Every operation (process) utilizes data in some way, shape, or form. For the computer to be able to use data, it needs to store it in a location called the RAM (Random Access Memory). The RAM is a temporary data storage unit that gets emptied every time the computer shuts down or restarts. The RAM is a contiues block consisting of many units, each having the ability to store and reference a piece of data. In order for other processes and programs to access and manipulate these cells of data, each cell is given a unique address which can be used to reference that cell. The addresses given to these cells look something similar to the following:
</div>

<br>

```C++ {linenos=false}
Example of an address: 0x7fff5fbff6c8
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;If a programmer wants to modify the contents of that particular cell, then they need to refer to the hard to memorize address shown above. The worst thing is that this is just one cell address! Imagine if we need to keep track of a lot of data and cells. The human brain was built for these kind of tasks. This can be quite hard and tidious to do. For this specific reason a much more convinient way needed to be created for accessing and manipulating data.
</div>

<br>
<br>

### Variables

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<b>A variable is a way for the programmer to store, maniputlae, and reference a piece of data from the memory.</b> Variables are critical because they allow us to interact with our data in a convinient and easy way. Variables accomplish this by giving meaningful names and labels to the location which the data is stored. The content of a variable can be modified and changed, hince for the name "Variable".
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;An example of how to use variables for storing and referencing data is a Player character in a game. A player can have X, Y, and Z coordinates. These coordinates indicate where the player is located in our world. The following is an example of how one can go about storing these values and accessing them in C++:
</div>

<br>

```C++
main(int argc, char* argv[])
{
	// Declaring and initializing our Variables
	
	int coordinate_x = 100;
	int coordinate_y = 0;
	int coordinate_z = 50;
	
	// Printing out the content and address of each variable
	
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
<br>

### Declaring & Initializing

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Now that we have obtained some basic understading about variables, it is time to talk about the different phases that we go through to make and work with them. The creation and usage of a variable can be divided into two general steps:
</div>

<br>

- Declaration
- Initialization

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In programming, declaration and initialization are two different concepts with distinct meanings and purposes. Many programmers use these two terms interchangabely which is not acceptable and we need to know the differences between the two.
</div>

<br>
<br>

###### What is Declaration?

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<b>Declaration is the process in which we as the programmer specify to the compiler that a location in memory needs to be reserved for a piece of data and be labeled with the name that we define for it.</b> In other words, declaration can be considered the act of telling the compiler to set aside memory space for creating a variable without any value specfied for it, so that it can be used later in the program. At a fundemental level, declaration is all we need to actually create and interact with variables. The following is the syntax structure for declaring variables in C++:
</div>

<br>

```C++ {linenos=false}
General syntax for creating variables:

[access modifier] [data type] [label/name];
```

<br>

```C++
main(int argc, char* argv[])
{	
	int name;
	
	return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In the above example, we don't use any access modifiers (access modifiers will be explained in later posts). We spcify the data type of the variable, which explains to the complire what type of information it can expect to be stored in this location. In this case, we are specifying that we want to store an "int", which can contain whole numbers (More information about data types will come in later posts). In addtion, we also specify the label/name of our variable by giving it an identifier of "name". Last but not least, we need to end the declaration with a semi-colon [;], indicating the end of the statement in our code line.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;At this point, you may ask what is Initialization? Furthermore, if declaration is all that we need for creating and interacting with variables, then why is it important to know about Initialization? Before we can answer these questions, we first need to know what Initialization is.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;At this point, you may ask what is Initialization? Furthermore, if declaration is all that we need for creating and interacting with variables, then why is it important to know about Initialization? Before we can answer these questions, we first need to know what Initialization is.
</div>

<br>
<br>

###### What is Initialization?

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;<b>Initialization refers to the act of assigning an initial value to a variable at the time it is declared or created, hince for the name "Initialization".</b> Initialization can be performed using an equal sign (=) followed by an expression or value. For example, the following statement declares and initializes a variable called "number_1" with a value of 57. Initialization can also be done on two separate lines in C++.
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

###### A word about memory management

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Wheather a location in memory contains the value from previous programs/operations or is cleared and restored to the defualt value depends on a number of factors. Some of these factors include the way that the operating system handles the momery and the standards set in the programming language and its environmental IDEs/compilers. Some operating systems do not clear the value in the memory after the program/operation is finished as it will probably be overwritten by a later program/operation that uses the same memory location anyways. Some other opertaing systems enforce the need for memory to be cleared and defaulted after the end of each program/operation.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;On the other hand, some programming languages may do the task of Initializating the variables automatically for the programmer. These languages and their respective complier environments insure that all variables are Initialized even if the progarmmer forgets to do it. However, all these conditions/rules may change at any time by the decisions of the maintainers of that programming language/complier environments and it is hard to keep up with all the latest updates. It is generally recommended to always do Initialization by ourselves and do not rely on external processes to do it for us.
</div>