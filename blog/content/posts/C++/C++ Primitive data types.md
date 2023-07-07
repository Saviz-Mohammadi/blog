---
title: "C++ Primitive data types"
date: 2023-05-01T17:13:09-07:00
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
	
	margin: 2.5rem 0 20rem 0;
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
<br>



### Introduction



<!-- ############################################# Separator - Top ############################################# -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Top ############################################# -->



<p>
If I present a mathematical question, such as "What is 2x2=?" on a piece of paper to a human being, they will likely respond with the correct answer, which is 4 (or am I hallucinating?). Humans understand that numbers possess specific operations that can be performed on them. However, if I were to ask the question, "What is yellow multiplied by brown?" they would likely find it strange. This is because I am attempting to multiply two sets of characters, which is not a valid operation. We encounter these problems and find solutions in our daily lives without always realizing or caring about it.
</p>



<br>



<p>
The situation differs when it comes to computers. While computers can execute instructions rapidly, they lack the same level of capability and flexibility as humans. We have previously discussed variables and how they allow us to direct the computer to store and manipulate information. Yet, we have not explored how we specify the type of information a variable can hold. Equally important is determining the set of actions that the computer can perform on that information. In this discussion, we will first delve into the reasons for the existence of data types and then explore primitive data types in greater detail in the C++ programming language.
</p>



<!-- ############################################# Separator - Bottom ############################################# -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Introduction</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Bottom ############################################# -->










### Why have data types?



<!-- ############################################# Separator - Top ############################################# -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Top ############################################# -->



<p>
In computer programming, a data type plays a crucial role as it defines and specifies the nature of information that a variable or expression can store and manipulate. However, one might question the reason of having numerous data types. Why not just have a single type called "data" that encompasses everything? At first glance, the idea of having a single data type appears appealing as it simplifies the programming task. Nevertheless, adopting a single type is impractical due to several reasons:
</p>



<br>
<br>
<br>



<ul class="justified-list">
<li><strong>Determine operations</strong></li>
</ul>



<p>
By defining a specific data type, we enable the compiler to identify and understand the range of operations that can be applied to that particular piece of information. For instance, if we designate our data as numeric, the compiler recognizes that arithmetic operations like addition, subtraction, division, and multiplication can be performed on it. This knowledge hepls the compiler in optimizing the execution of these operations as well as ensuring that the data is appropriately tailored for such computations.
</p>



<br>



<ul class="justified-list">
<li><strong>Type safety</strong></li>
</ul>



<p>
Employing a single data type for all values would introduce challenges in maintaining type safety within a program. Type safety is crucial as it safeguards against errors that may arise when data is utilized in unintended ways. Consider the scenario where our information is of type text. In this case, the acceptable set of operations differs from that of numerical data types. Attempting arithmetic operations, such as division, on text would be invalid and can be prevented by the compiler.
</p>



<br>



<ul class="justified-list">
<li><strong>Memory size</strong></li>
</ul>



<p>
Utilizing a single data type would result in excessive memory usage, leading to inefficiency. For instance, if the requirement is to store small number values, it is more efficient to employ a data type that occupies less memory compared to a generic type capable of storing any data. This optimized memory allocation ensures efficient utilization of resources and prevents unnecessary memory consumption. 
</p>



<!-- ############################################# Separator - Bottom ############################################# -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Introduction</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Bottom ############################################# -->










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
