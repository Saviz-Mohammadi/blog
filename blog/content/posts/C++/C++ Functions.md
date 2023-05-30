---
title: "C++ Functions"
date: 2023-05-26T10:31:00-07:00
draft: true
---

<style>

  .line-divider-top {
	
	display: flex;
	align-items: center;
	text-align: center;
	
	margin: 0px 0px 2.5rem 0px;
  }

  .line-divider-top .left-div {
  
	flex-grow: 1;
	background: currentColor;
	height: 1px;
  }
  
  .line-divider-top .right-div {
  
	flex-grow: 1;
	background: currentColor;
	height: 1px;
  }

  .line-divider-top .middle {
  
	margin: 0px 0px;
  }
  
  
  
  
  .line-divider-bottom:not(:last-child) {
	
    display: flex;
    align-items: center;
    text-align: center;
	
	margin: 2.5rem 0 15rem 0;
  }
  
  .line-divider-bottom:last-child {
	
    display: flex;
    align-items: center;
    text-align: center;
	
	margin: 2.5rem 0 0 0;
  }

  .line-divider-bottom .left-div {
  
	flex-grow: 1;
	background: currentColor;
    height: 1px;
  }
  
  .line-divider-bottom .right-div {
  
	flex-grow: 1;
	background: currentColor;
    height: 1px;
  }

  .line-divider-bottom .middle {
  
	margin: 0px 20px;
  }
  
  
  p {
  
	text-indent: 3rem;
	text-align: justify;
  }
  
  ins {
  
	font-weight: 500;text-underline-offset: 5px;
  }
  
  strong {
	
	font-weight: 700;
  }
  
  
  
  .justified-list {
    list-style-type: disc;
  }

  .justified-list li {
    text-align: justify;
  }
  
  
  .justified-ordered-list {
    list-style-type: decimal;
  }

  .justified-ordered-list li {
    text-align: justify;
  }

</style>

<br>
<br>

### Intro

<!-- ##################### Separator - Top ##################### -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Top ##################### -->

<p>
I firmly believe that in order to understand the purpose of something, we must consider the consequences of its absence. Therfore, let's examine a typical scenario that illustrates the implications of not utilizing functions in our code. We begin by analyzing an example that illustrates the impact on program flexibility when functions are not used.
</p>

<br>

<p>
In game development, it is occasionally necessary to print out the information of a player character or any other object for clarification and debugging purposes. This allows us to confirm whether the actual position of that entity, as perceived from a matrix perspective, aligns with its representation in the code. This method is employed to verify if the logic and code of a game engine responsible for visually rendering entities are functioning correctly. Although we won't delve deeply into the inner workings of how engines calculate and perform their tasks, since this is ultimately a simple blog explaining the purpose of functions, we will still attempt to replicate the portion related to printing information. The following is an example showcasing a code snippet aimed at printing information about the position of an imaginary player character in a game engine:
</p>

<br>

```C++ {linenos=false}
// Write some code about printing the position of a player.
```

<br>

<p>
Although the current code may appear relatively easy to comprehend, it harbors several hidden issues that need to be addressed. Let's analyze each of these problems in detail and discuss potential solutions:
</p>

<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->

<li><strong>Difficulty of adapting to changes</strong></li>

<p>
Suppose we decided to modify any aspect of the code, such as changing the output format. In that case, we must ensure that all instances are updated accordingly, which can be a tedious and error-prone process. This challenge becomes even more significant if we have numerous sections and hundreds of changes to apply.
</p>

<!-- ##################### List element ##################### -->


<br>
<br>


<!-- ##################### List element ##################### -->

<li><strong>Code readability</strong></li>

<p>
While we may currently be able to make sense of the functionality, what about one week, two weeks, or three weeks later? Will we still remember the purpose of each part and be able to navigate through all the duplicates? Will it be easy to try and understand the hundreds if not tousands of lines of code that look very similar to each other?
</p>

<!-- ##################### List element ##################### -->


<br>
<br>


<!-- ##################### List element ##################### -->

<li><strong>Difficulty in handling bugs and issues</strong></li>

<p>
What happens if we attempt to fix an issue that we encountered in our code? Identifying the specific section causing the problem becomes challenging, and fixing it becomes a taxing task as we need to address the issue in every instance.
</p>

<!-- ##################### List element ##################### -->


<br>
<br>


<!-- ##################### List element ##################### -->

<li><strong>Bad abstraction hinders logic</strong></li>

<p>
The program's overall reasoning becomes difficult due to the overwhelming number of code lines in front of us. This distracts us from focusing on the program's logic and abstraction, hindering our ability to effectively understand and reason about the code.
</p>

<!-- ##################### List element ##################### -->

</ul>

<br>

<p>
All of the aforementioned reasons contribute to the potential failure and cumbersome nature of large programs that do not take advantage of functions in their code base. Furthermore, these issues serve as the primary motivation behind the existence of functions.
</p>

<!-- ##################### Separator - Bottom ##################### -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Intro</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Bottom ##################### -->

### Function definition & syntax

<!-- ##################### Separator - Top ##################### -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Top ##################### -->

<p>
A function is a named segment of code that carries out a specific task or a series of related tasks. It serves as a fundamental concept in most programming languages, aiding in code organization and modularization. Functions offer a comprehensive overview by concealing the technical complexity and providing a descriptive name that indicates the purpose of that segment of code.
</p>

<br>

<p>
Although the syntax of a function may vary depending on the situation, we can generally demonstrate the typical structure and appearance of a function as shown below:
</p>

<br>

```C++ {linenos=false}
return_type function_name(parameter_list)
{

}
```

<br>

<p>
Functions enable programmers to concentrate on the overall logic being executed, rather than becoming overwhelmed by an excessive number of lines and convoluted details that may distract them from their original objectives. This situation is more common than programmers might realize, where they often find themselves diverted from understanding the program's actual flow to unraveling the technical specifics of why certain implementations are chosen. To illustrate this, let's look at the following code:
</p>

<br>

```C++
#include <iostream>

int main(int argc, char* argv[])
{	
    int digit = 5;
    int power = 7;
	
    int result = 1;

    for (int index = 1; index <= power; index++)
	{
        result *= digit;
    }

    std::cout << "The result is: " << result << std::endl;

    return (0);
}

```

<br>

<p>
Upon initial inspection, it may require several minutes to decipher the purpose of this code. The provided code aims to compute the exponentiation of a given number. While this example may not be exceedingly difficult, consider the scenario where it is. Envision yourself joining a company and being assigned to a project. On your very first day, you are confronted with an extensive codebase comprising hundreds, if not thousands, of lines of code. How would you decipher the functionality of each component?
</p>

<br>

<p>
If you were presented with the following code base instead of the previously mentioned one, how efficiently would you be able to deduce the functionality of the following code? (Please don't concern yourself with the technical details of the syntax. Instead, try to concentrate on the main point being conveyed.)
</p>

<br>

```C++
#include <iostream>

int main(int argc, char* argv[])
{	
    int digit = 5;
    int power = 7;
	
    int result = calculate_power(digit, power); // Function is defined somewhere else in the code.

    std::cout << "The result is: " << result << std::endl;

    return (0);
}

```

<br>

<p>
Although this is a straightforward and arbitrary example, it should hopefully illustrate how functions can contribute to code flexibility and comprehensibility. In the subsequent sections, we will delve further into the definition of each component of the function syntax and enrich our comprehension of them.
</p>

<!-- ##################### Separator - Bottom ##################### -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Intro</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Bottom ##################### -->

### Function Header & Body

<!-- ##################### Separator - Top ##################### -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Top ##################### -->

<p>
A function can be divided into two main components of <strong>Header</strong> and <strong>Body</strong>. While in many other languages, it may not be essential to understand the exact differentiation between these parts, in C++, having a clear understanding of their distinction is crucial. Let's delve deeper into what each of these components entails.
</p>

<br>
<br>
<br>
<br>
<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->
<li><strong>Header</strong></li>

</ul>

<p>
The header of a function is meant to specify the most improtant characteristics of a function. This entails the function's name (identifier), return type, and parameters. It acts as a blueprint for the function, providing essential details on how the function should be called (invoked). The header is alternatively referred to as the function <strong>prototype</strong> or <strong>signature</strong>. Typically, it is the initial line used when creating functions, informing the compiler that we intend to define a block of code that accomplishes some task.
</p>

<br>

```C++
#include <iostream>

int calculate_power(int digit, int power) // Function header
{
	// Function body
}

int main(int argc, char* argv[])
{	
    int digit = 5;
    int power = 7;
	
    // Function must be called here. 

    std::cout << "The result is: " << std::endl;

    return (0);
}

```

<br>

<p>
In the given example, line 15 showcases the header of a function named "calculate_power" as a demonstration. The header is comprised of three essential elements: the return type (in this case, "int"), the name or identifier (in this case, "calculate_power"), and the parameters (named "digit" and "power" in this instance). Now, let's analyze each of these components for a more comprehensive understanding.
</p>

<br>
<br>
<br>
<br>
<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->
<li><strong>Return type</strong></li>

</ul>

<p>
The return type determines the type of data that the function will return upon completion of its execution or what is expected to be returned. It can be any valid data type in C++, including integers, doubles, void, or even a user-defined type. The void type holds a distinct significance in C++. It implies that the function is not obligated to provide a return value once its computation is finished. Another frequently utilized type is "bool," which indicates whether the function has successfully executed its operation or not. In the following section, we will delve into a detailed explanation of how one can specify the return value from a function.
</p>

<br>
<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->
<li><strong>Name</strong></li>

</ul>

<p>
When attempting to call a function to execute its task, we use the function's name, also known as the identifier. It is crucial to uphold to specific naming conventions and guidelines while selecting an identifier for a function. The function name should be descriptive and meaningful, accurately representing the purpose or action performed by the function. Moreover, the function name must be unique within the scope where the function is declared. This ensures that there is no ambiguity when referencing or calling the function in the program. If two functions within the same scope share the same name, it will result in a compilation error.
</p>

<br>
<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->
<li><strong>Parameter List</strong></li>

</ul>

<p>
Parameters serve as a collection of variables that the function anticipates receiving to execute its task correctly or even to function at all. These parameters are enclosed within parentheses (), and if there are multiple parameters, they are separated by commas. Each parameter defines the type and identifier of the data that can be supplied to the function when it is called. The specific values passed during the invocation or calling of the function are referred to as "arguments."Parameters are essentially a list of variables that the function expcets to recieve in order to perform its task correctly (or at all even). The parameters are enclosed within parentheses (), separated by commas if there are multiple of them. Each parameter specifies the type and identifier of the data that can be passed into the function when it is called. The actual value that is passed during the invokation (calling) of the function is called "Arguments".
</p>

<br>
<br>
<br>
<br>
<br>

<p>
Function headers also play a crucial role in type checking. By explicitly defining the return type and parameter types in the header, the compiler can verify if the function is used in a correct way. It can check for type mismatches or missing arguments, ensuring that the function is used appropriately. The following example illustrates how type checking can be utilized to validate the proper usage of a function:
</p>

<br>

```C++
#include <iostream>

void print_number(int number)
{
    std::cout << "The number is: " << number << std::endl;
}

int main(int argc, char* argv[])
{
    print_number(42);
	
    print_number(3.14159);  // Incorrect argument type

    return (0);
}
```

<br>

<p>
The code snippet provided features a function called "print_number" which takes an integer parameter and is responsible for displaying the given number on the console. In C++, due to its strong typing nature, the compiler identifies a type mismatch on line 12, where we are trying to pass a double value. Consequently, the compiler generates a compile-time error indicating that there is no corresponding function for "print_number(double)". This error message serves as a reminder to verify that the argument types align with the expected types when calling functions. By doing so, potential bugs can be caught early, and type safety within the code is ensured.
</p>

<br>
<br>
<br>
<br>
<br>

<p>
If you have followed along until now, then you may have noticed that in nearly every instance of code snipet examples until now the functions that were created are place in some location before the location we intend to call or invoke them. This is not a accident. The reason for this is that C++ compiles the source code in a top-down manner, line by line. When the compiler encounters a function call, it needs to know the function's signature (return type, name, and parameter types) in order to verify that the function call is correct.

By placing function declarations or definitions before the points where they are called, you provide the necessary information to the compiler about the functions' signatures. This allows the compiler to verify the correctness of the function calls during the compilation process.

If a function is called before it is declared or defined, the compiler will generate an error because it doesn't have the required information to verify the call. Placing the function definition before its usage ensures that the compiler has the necessary details to correctly compile the code. this brings us to yet another important ability of headers. As we discussed earlier, headers contain the essential information that a compiler needs in order to compare the correctness of our calls. Since headers contain all the neccessary information for this correct checking, they are the only thing that the complire requires in order to actually make a call statemnt work temporarily (beside from the actual functionality of the function of course). This brings us to prototypes.
</p>

<br>

<p>
headers (prototypes)that provide a way to use a function before its actual implementation. Prototypes allow functions to be declared and referenced in any order, facilitating modular programming and reducing dependencies between code modules. Prototypes are usually ended with a semicolon as their whole porpuse is to just inform the complier of the existance of a function. But, when used in conjunction with a body they do not end with a semicolon.
</p>

```C++ {linenos=false}
// Example of a function header as prototype

void print(std::string);
```

One of the reasnos as to why headers are also called signatures is because just like signing an agreement a function promisses to uphold to what it promisses to recieve and return in this being the header.

<p>
Another reason why headers are important is because Function headers provide type information for the compiler or interpreter to perform static type checking. With the return type and parameter types explicitly defined in the header, the compiler can verify if the function is used correctly, such as checking for type mismatches or missing arguments. This early validation helps catch errors before runtime and ensures program stability.
</p>

<p>
The function body, also known as the function definition or implementation, is the block of code that contains the actual instructions and statements executed when the function is called. It is the part of the function that specifies what the function does. Function bodies provide the implementation details and logic that define what a function does when it is called.
</p>

<!-- ##################### Separator - Bottom ##################### -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Intro</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Bottom ##################### -->

### Function Declaration & Definition

<!-- ##################### Separator - Top ##################### -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Top ##################### -->

<p>
The format of a typical function in C++ shares a similarity with variables, although there are notable differences. The process of creating a function can be divided into two essential steps:
</p>

<br>

<p>
<strong>Declaration</strong> and <strong>Definition</strong>
</p>

<br>

<p>
The source of confusion for many programmers is that other resources often present these steps as a single simultaneous operation, making it challenging to perceive them as distinct actions. Therefore, it becomes nearly impossible to recognize that declaration and definition are in reality two separate operations. While these terms are frequently used interchangeably, it is important to understand their distinctions and the implications they carry.
</p>

<br>

<ul class="justified-list">

<!-- ##################### List element ##################### -->

<li><strong>Declaration</strong></li>

<p>
It acts as a blueprint for the function, providing information about how the function should be called and what it returns. Function declaration is important because it gives teh complire a general idea towards what the function does (in terms of what arguments it takes and what it returns) in one very short and decriptive line without the need to get into the details of what the functions does percisely in its body.
</p>

</ul>