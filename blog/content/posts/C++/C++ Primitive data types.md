---
title: "C++ Primitive data types"
date: 2023-05-01T17:13:09-07:00
draft: true
---

<br>
<br>

### Intro

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;I am sure that many programmers are familiar with the concept of a data type in a programming language. However, it suprises me as to how many people do not know the real reason behind the existance of data types in the first place. We will first try and explain the reason behind the existance of data types and then go in more depth about primitive data types specifically.
</div>

<br>
<br>

### Why have data types?

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Before we can discuss why we have so many different variations of data types, we need to define the meaning of a data type. <b>In computer programming, a data type is a classification that specifies the type of information that a variable or expression can hold and operate upon.</b> But, why do we need so many data types? Why not just have one type and call it "data"? The answer to these questions is hidden within the definition. The idea of having a single data type instead of multiple specific types may seem attractive because it simplifies the programming process. However, it is not practical for several reasons:
</div>

<br>
<br>

<div align="justify">
<code><b>1-</b></code>&emsp;&emsp;Defining a specific type helps the compiler to determine the set of operations that is possible to perform on that piece of information. As an example, imagin if our data is of type numeric, this will hint to the compiler that we are able to perform arithmatic operations such as addition, subtraction, division, and mulitplication on that data. This also helps the compiler to optimise the data for these operations to take place on it.
</div>

<br>

<div align="justify">
<code><b>2-</b></code>&emsp;&emsp;In addition, using a single data type for all values would make it difficult to ensure type safety in a program. Type safety is important because it prevents errors from occurring in a program when data is used in an unintended way. For example, if our information is of type text, then the set of operations that we can perform on that data is different from numerical data types. We cannot perform arithmatic operations such as division on text. 
</div>

<br>

<div align="justify">
<code><b>3-</b></code>&emsp;&emsp;Last but not least, using a single data type would require a lot of memory, which would be inefficient. For example, if you only need to store small integer values, it is more efficient to use a data type that occupies less memory than an integer. 
</div>

<br>
<br>

### About primitive types

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;I am going to give a very brief explanation as to what a data type is. A primitive data type is a data type that is built into the language and is used to represent basic values. Primitive data types are also sometimes called fundamental data types or simple data types. C++ is no exception to this rule. In C++ there are many fundemental data types that can be used to create logic. Some of the primitive data types in C++ include the following:
</div>

<br>

| Type    | Description                                           |
|---------|-------------------------------------------------------|
| `int`   | Used to represent whole numbers without decimal points |
| `float`| Used to represent decimal numbers with precision points |
| `char`  | Used to represent a single character                   |
| `bool`  | Used to represent a boolean value, which can be either `true` or `false` |

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Each of these primitive types apply a certain meannig to our data by not only hinting at their potential usage, but also by defining their capability in terms of the size of data that they can store and the set of operations they can perofrm upon that data. As an example let's take a look at the following code:
</div>

<div>
Why types are made shorter like "int" instead of "integer":


The use of the term "int" in C++ instead of its full version "integer" can indeed be attributed to historical reasons. The C++ programming language evolved from its predecessor, the C programming language, which was developed in the early 1970s.

C was designed to be a low-level language with a strong focus on efficiency and performance. In those early days of computing, memory and storage were limited resources, and every byte mattered. As a result, the designers of C made certain design choices to optimize for efficiency.

One such choice was to introduce a set of basic data types with short, concise names. These types were implemented in a way that closely matched the hardware capabilities of the underlying computer systems. The goal was to provide a minimal set of types that could efficiently represent the most common data used by programs.

The term "int" stands for "integer" and is used to represent whole numbers in C and C++. The decision to use a short, abbreviated form like "int" instead of the full word "integer" was likely made to save space and reduce the amount of typing required. It was a trade-off between brevity and expressiveness.

Over time, as C++ evolved, it maintained compatibility with C and inherited many of its design decisions, including the use of abbreviated type names. This compatibility allowed C++ to leverage the existing C codebase and benefit from its large ecosystem of libraries and tools.

Therefore, the use of "int" as the type name in C++ can be seen as a historical artifact that reflects the language's roots in C and its focus on efficiency and compatibility.
</div>

<div>
Historically, a computer processor can process integer arithmetic quicker than 
it can floating-point arithmetic. Thus, while a processor can add 1 million integer numbers in a given amount of time, the same processor may be able to 
perform only 200,000 floating-point calculations during the same period. (Not 
surprisingly, I couldn’t even get around to reading the first value.) 
Calculation speed is becoming less of a problem as microprocessors increase 
their capabilities. Most modern processors contain special calculation circuitry for performing floating-point calculations almost as fast as integer 
calculations.
</div>

<br>

```C++
main(int argc, char* argv[])
{
	bool isConnected = true;
	
	if(isConnected)
	{
		performFunction();
	}
	
	return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;The above code specifies that our variable is attempting to store a boolean type. This suggests to us that our variable is going to be used as a condition which will determine if some other segment of code will be executed or not depending on the value stored in it. Furthermore, the compiler can store this value in a relatively small memeory sized location as storing a true or false value does not take much effort.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;The amount of space in memory that the compiler needs to allocated to each data type is another important aspect of these primitive data types. As an example, while a `int` primitive type is meant to store whole numbers, but the smallest and largest numbers that it can hold are limited to the size it holds. A regular int in most environments (programming languages, operating systems, etc.) can usually have a size of 4 bytse or 32 bits. This allows the int to have a minimum of "-2147483648" and a maximum of "2147483647". But, what if we need store bigger values? What if we don't want to use as much space and only store smaller ranged values? The answer to these questions are the other similar data types that were created for these purposes. Each one of these major primitive data types have other sibling primitive data types that only vary in thier size capability. As an example, the int has other counter parts such as: `short` and `long`. The short has the ability to store a smaller range of numbers and uses less memeory. The long has the ability to store massive numbers at the cost of more memory usage. A similar situation exists for most other primitive data types. For a complete list of all availabl primitive data types and their sizes one must refer to the official documentation of that language and the underlying system. However, here is a list of most common types:
</div>

<br>
Change this tabel to contain the full list (also talk about signed and unsigned and explain how bits can be used to determine the size of a variable as well as sizeof method)

| Type    | Description                                           |
|---------|-------------------------------------------------------|
| `int`   | Used to represent whole numbers without decimal points |
| `float`| Used to represent decimal numbers with precision points |
| `char`  | Used to represent a single character                   |
| `bool`  | Used to represent a boolean value, which can be either `true` or `false` |


<br>
<br>

### Signed and unsigned

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Every numerical primitive type has the capability to store and manipulate both positive and negative numbers. In other programming languages, the programmer has less to no control over if a primitive numercial type can store both negative and positive numbers or weather it should only contain positive numbers. In C++ this is a different story. C++ gives the programmer the ability to decide weather they want to have the ability to store both negative and positive numbers (signed data type) or just positive numbers (unsigned data type). Here is an example of how one can do this in C++:
</div>

<br>

```C++
main(int argc, char* argv[])
{
	signed int number1 = -100;
	unsigned int number2 = 100;
	
	std::cout << "This is the signed number: " << "number1 = " << number1 << "/n";
	std::cout << "This is the unsigned number: " << "number2 = " << number2 << std::endl;
	
	std::cin; // Just to make sure the command prompt does not close immediately in some IDEs.
	
	return (0);
}
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Due to the way in which a signed number is saved in memory, the maximum number that we are able to store in a unsigned number increases, because we no longer need to accomodate negative numbers and therfore, we can use those bits to hold larger positive numbers.
</div>

<br>
<br>

### Primitive sizes are not consistent!

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;While working in other languages such as Java, C#, Python, etc. you never have to worry about the size of your primitive types changing. If an int is considered to be 4 bytes, then it will stay consistent throughout other environments. However, in C/C++ world this is a different story. Languages such as C and C++ were made to be used with as many types of hardware as possible. Different types of hardware and CPUs have different types of architectures. Therefore, it is very challenging to accomodate the needs of them all. For this reason, at the time were these languages were envented and used no strict rules were enforced upon sizes and global best practices. If an int is 4 bytes in one system and environment, then it could be 6 or 8 bytes in others. The size of each primitive type dependends upon the standards that the chipset of each hardware and the operating system of that device enforces. Different operating systems and hardwares have different standards and opinions as what is the correct allocation to be made is. For these reasons the primitive types sizes can change. This can cause a lot of confusion and unindentended behaviour to occur. A program that you made for one device may not function as well or even at all for other devices.
</div>

You need to talk about the different primitive types in the primitive type section and provide code segments with examples.
