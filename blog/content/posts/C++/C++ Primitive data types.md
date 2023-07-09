---
title: "C++ Primitive data types"
date: 2023-05-01T17:13:09-07:00
draft: true
---



<br>
<br>
<br>



### Introduction



<!-- ############################################# Separator - Top ############################################# -->

<hr>

<br>

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
  <hr class="left-line">
  <span>|</span>
  <span class="middle">Introduction</span>
  <span>|</span>
  <hr class="right-line">
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










### Primitive types



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
In programming languages, including C++, a primitive data type, also known as a built-in or fundamental type, represents a basic information type provided by the language itself. These types are commonly used to represent simple data values like numbers and characters. Primitive types are directly supported by the language implementation. They have fixed sizes and predefined behaviors, enabling efficient storage and optimized operations. Primitive types often have built-in operations for arithmetic, logical operations, and comparisons, and they are typically supported by the underlying hardware. In C++, some examples of primitive data types include the following:
</p>



<br>
<br>



| Type    | Description                                           |
|---------|-------------------------------------------------------|
| `int`   | Short for "integer". Used to represent whole numbers without decimal points. |
| `float`| Short for "floating-point". Used to represent decimal numbers with precision points.|
| `char`  | Short for "character". Used to represent a single character. |
| `bool`  | Short for "boolean". Used to represent a logical value that can be either `true` or `false` |



<br>
<br>



<p>
Each of these primitive data types provides a specific meaning to our data. They not only suggest their potential usage but also define their capacity in terms of the size of data they can store and the set of operations they can perform on that data. These characteristics enable the compiler to accurately determine the memory requirements for each type and apply optimization techniques to enhance the efficiency of logical operations associated with that data type. To demonstrate this concept, let's examine the following code snippet and see how the data type helps us to understand the purpose of the variable in completing the functionality:
</p>



<br>
<br>



```C++
main(int argc, char* argv[])
{
	bool isConnected = true;
	
	if(isConnected)
	{
		// ...
		// Perform task.
		// ...
	}
	
	return (0);
}
```



<br>
<br>



<p>
The provided code indicates that the variable "isConnected" is intended to hold a boolean value. This implies that the variable will be utilized as a condition to determine whether a specific code segment will be executed or not based on its stored value. As a boolean type only requires a minimal amount of memory, the compiler can allocate a small memory space to store the "true" or "false" value. In this particular case, since the boolean variable holds the value "true," it signifies that the associated code segment is permitted to execute given the specified conditions.
</p>



<br>
<br>



<code><h3>IMPORTANT NOTE:</h3></code>

<P>
There are specific reasons why types have shorter names like "int" instead of "integer." The adoption of the term "int" in C++ rather than its complete form "integer" can be attributed to historical factors. C++ originated from the C programming language, which was created in the early 1970s. C was developed with a primary emphasis on efficiency and performance. During that era of computing, memory and storage were scarce resources, and every byte counted. Therefore, the creators of C made deliberate design decisions to optimize for efficiency.
</p>



<br>



<p>
One of the design choices made in the C programming language was to introduce concise and hardware-compatible basic data types. These types were specifically implemented to closely align with the capabilities of the underlying hardware. The objective was to provide a minimal set of types that efficiently represented the most commonly used data in programs. By opting for abbreviated forms like "int" instead of the full word "integer," the intention was to save space and reduce the amount of typing required. This decision required striking a balance between brevity and expressiveness. As C++ evolved, it maintained compatibility with its predecessor, C, and inherited many of its design decisions.
</p>



<br>
<br>


| Type    | Description                                           |
|---------|-------------------------------------------------------|
| `int`   | Used to represent whole numbers without decimal points |
| `float`| Used to represent decimal numbers with precision points |
| `char`  | Used to represent a single character                   |
| `bool`  | Used to represent a boolean value, which can be either `true` or `false` |



<br>
<br>


<p>
In addition to primitive types, programming languages often offer composite types or user-defined types, which are constructed by combining multiple primitive or composite types. Composite types encompass a variety of constructs such as arrays, structures, classes, or objects. They enable developers to create intricate data structures and represent entities with multiple properties or behaviors. While these concepts are currently quite complex, they will be explored in detail in subsequent sections.
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










### Bits and Bytes



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
All though this section is typically ignored and not covered by most tutorials, I feel the need to explain these concepts as they can help us understand later parts. Remmeber that it is the change in voltage that gives it a meaninng not the individual by themselves. Let's imagine for a moment that we are trapped in a room and the only way out is by trying to communicate to a friend that is in a room next door. The rooms are completely isolated, meaning that sound cannot go through them, what is worse is that the rooms have no windows. So, there is no way for the person to hear or see us. However, there does appear to be a light bolb in the room and the other person has the switch for it (I know, very wierd scenario). So, how do we establish communication to the other person? Since a light bolb can be at only two states at a time, which is either on or off, it can be quite tricky to come up with a solution to communicate. One might say let's filck the light on and off and create codes between each other. If I switch it on and off very quickly two times that would mean a yes, and if I do it just once that means a no. Now we are getting somewhere. Yay! I got out.

You can imagine the room problem as a game of 2 players.

We can imagine the on state of a light as saying yes. and teh off state as no. THis way we have the ability to to answer a lot of questions such as am I on teh right track or not. But, the issue with this approach is that it is very tidious as we have to ask a lot of questions and break them down into yes or no qusetions. If we want to do anything slightly more complicated we probably need to come up with combinitions that can represent more complex answers. Me and my team mate can agree on a set of rules and contracts that we can use to create more complex answers and questions, such as turn on and off quickly 2 times to say "what does that mean". or one long on and off to say "let me see".



The binary language is limited in teh number of resources (digits) it can provide to us for representing different entities. You can use as many zeros and ones as you like the only qeustion is at what cost?


THis type of communication is actually refered to as Morse code and was used in the military for communication.

if you look at a character it is not exactly useful as it has no meannig, it is rather the combination of letters together that give the text some meaning.


How does this translate into the computer language? Computers are made of millions of chipsets called "transistors" that can have two different voltage values at a time. This can be either 0.5 or 1. each of these respond to the on and off state. A common source of confusion when it comes to this topic is that most peopel imagine that a computer has a voltage of 0 when it is off, but this is not true after all a computer needs a current and electrcity to function. Saying a voltage of zero means that the computer is literally off! If each of these states represent a yes and no, then the change of these states over time can represent a more complex message.

Another question that we get asskeedd all teh time is why binary? why not base 10 or something else? it is because of the fact that binary system and the two states on and off are very compatible with a chipset that can be only switched on and off as that is the nature of electronic devices. A voltage can only be flowing or not flowing in a wire.

The word binary actually means being composed of 2 things (like a switch)


One of the reasons as to why hexidecimal is so important when dealing with computers and why they are used to represent memory instead of binary is because they are much easier to work with in comparison to long and huge binary numbers.


Now let's talk about how to interact with information that is not a numebr such as text.
</p>



<br>
<br>



```C++
main(int argc, char* argv[])
{
	signed   int number1 = -100;
	unsigned int number2 = 100;
	
	std::cout << "This is the signed number: "   << "number1 = " << number1 << "/n";
	std::cout << "This is the unsigned number: " << "number2 = " << number2 << std::endl;
	
	std::cin; // To insure that the command prompt does not close immediately in some IDEs.
	
	return (0);
}
```



<br>
<br>



<p>
Due to the way in which a signed number is saved in memory, the maximum number that we are able to store in a unsigned number increases, because we no longer need to accomodate negative numbers and therfore, we can use those bits to hold larger positive numbers.
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










### Signed and unsigned



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
Most of the fundamental numerical primitive types have the ability to store and manipulate both positive and negative numbers. In contrast to other programming languages, where the programmer may have limited or no control over whether a primitive numerical type can accommodate negative and positive numbers or only positive numbers, C++ offers a different approach. C++ provides the programmer with the ability to decide whether to store both negative and positive numbers, referred to as <strong>signed</strong> data types, or solely positive numbers, known as <strong>unsigned</strong> data types. Here's an example of how this can be achieved in C++:
</p>



<br>
<br>



```C++
main(int argc, char* argv[])
{
	signed   int number1 = -100;
	unsigned int number2 = 100;
	
	std::cout << "This is the signed number: "   << "number1 = " << number1 << "/n";
	std::cout << "This is the unsigned number: " << "number2 = " << number2 << std::endl;
	
	std::cin; // To insure that the command prompt does not close immediately in some IDEs.
	
	return (0);
}
```



<br>
<br>



<p>
Due to the way in which a signed number is saved in memory, the maximum number that we are able to store in a unsigned number increases, because we no longer need to accomodate negative numbers and therfore, we can use those bits to hold larger positive numbers.
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










### Primitive sizes are not consistent!



<!-- ############################################# Separator - Top ############################################# -->

<div class="line-divider-top">
  <div class="left-div"></div>
  <span></span>
  <span class="middle"></span>
  <span></span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Top ############################################# -->



<p> There is a difference between saying something is predefined with saying something is consisitent. predefined means that something is known and set from before hand. Consisitent means that there are no changes when switching among different conditions and variations.
&emsp;&emsp;&emsp;&emsp;While working in other languages such as Java, C#, Python, etc. you never have to worry about the size of your primitive types changing. If an int is considered to be 4 bytes, then it will stay consistent throughout other environments. However, in C/C++ world this is a different story. Languages such as C and C++ were made to be used with as many types of hardware as possible. Different types of hardware and CPUs have different types of architectures. Therefore, it is very challenging to accomodate the needs of them all. For this reason, at the time were these languages were envented and used no strict rules were enforced upon sizes and global best practices. If an int is 4 bytes in one system and environment, then it could be 6 or 8 bytes in others. The size of each primitive type dependends upon the standards that the chipset of each hardware and the operating system of that device enforces. Different operating systems and hardwares have different standards and opinions as what is the correct allocation to be made is. For these reasons the primitive types sizes can change. This can cause a lot of confusion and unindentended behaviour to occur. A program that you made for one device may not function as well or even at all for other devices.
</p>

You need to talk about the different primitive types in the primitive type section and provide code segments with examples.



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

<div align="justify">
&emsp;&emsp;&emsp;&emsp;The amount of space in memory that the compiler needs to allocated to each data type is another important aspect of these primitive data types. As an example, while a `int` primitive type is meant to store whole numbers, but the smallest and largest numbers that it can hold are limited to the size it holds. A regular int in most environments (programming languages, operating systems, etc.) can usually have a size of 4 bytse or 32 bits. This allows the int to have a minimum of "-2147483648" and a maximum of "2147483647". But, what if we need store bigger values? What if we don't want to use as much space and only store smaller ranged values? The answer to these questions are the other similar data types that were created for these purposes. Each one of these major primitive data types have other sibling primitive data types that only vary in thier size capability. As an example, the int has other counter parts such as: `short` and `long`. The short has the ability to store a smaller range of numbers and uses less memeory. The long has the ability to store massive numbers at the cost of more memory usage. A similar situation exists for most other primitive data types. For a complete list of all availabl primitive data types and their sizes one must refer to the official documentation of that language and the underlying system. However, here is a list of most common types:
</div>



(also talk about signed and unsigned and explain how bits can be used to determine the size of a variable as well as sizeof method)



<!-- ############################################# Separator - Bottom ############################################# -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">Introduction</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ############################################# Separator - Bottom ############################################# -->