---
title: "DB Concepts   Part 1"
date: 2023-05-17T12:33:58-07:00
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
  
	font-weight: 700;text-underline-offset: 5px;
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

  .justified-list li::after {
    content: "";
    display: inline-block;
    width: 100%;
  }
  
  
  .justified-ordered-list {
    list-style-type: decimal;
  }

  .justified-ordered-list li {
    text-align: justify;
  }

  .justified-ordered-list li::after {
    content: "";
    display: inline-block;
    width: 100%;
  }

</style>

<!-- ################################################################################ Content ################################################################################ -->

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
It is widely recognized that volatile memory like RAM (Random Access Memory) is not suitable for storing and maintaining data due to its tendency to lose information upon each reboot. While programmers are familiar with various methods of storing data, such as files and databases on different storage devices, they may not fully comprehend the factors influencing the choice between these options. This raises the question: Why should we use databases when files can serve the same purpose of storing data? To gain a deeper understanding, this section delves into the past of electronic computers, providing a concise overview of the historical evolution of data storage and explaining the rationale behind selecting one approach over another.
</p>

<br>

<p>
While I acknowledge that comprehensive historical overviews may not be appealing to everyone, it is crucial to grasp the unique advantages and limitations of different data storage strategies that have been utilized over time. Therefore, it becomes essential to explore the historical evolution of various data storage methods before we can fully appreciate the role of databases and SQL within this context.
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

### History of storing data

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
During the early stages of computer development, the concept of a database was still emerging, and practical implementation was limited. The focus during this time was on exploring the theoretical aspects and conceptual frameworks of organizing data in a structured manner. During that period, storage costs were significantly high, which led system designers to prioritize minimizing the usage of storage resources for their tasks. In addition, the relatively slower computing speeds necessitated the emphasis on achieving optimal performance. As a result, data was predominantly stored in files, which served as discrete containers for specific information.
</p>

<br>

<p>
These files were typically stored on storage media like hard drives or magnetic tapes, but they differed from the everyday files we are accustomed to. To function as well-defined containers, these files required a structured format that allowed users to efficiently work with and manipulate information to the best of the capabilities available at that time. These files acquired the designation of flat files. Despite lacking the complex structure and relationships of a database, they emerged as the preferred architectural solution due to their ability to achieve two crucial objectives: conserving expensive storage and facilitating efficient processing. Put simply, during that period, there were no other viable alternatives available.
</p>

<!-- ##################### Separator - Bottom ##################### -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">History of storing data</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Bottom ##################### -->

### Structure of a flat file

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
In a flat file, data is typically organized in a sequential manner, with each record having a consistent length comprising a fixed number of characters. The structure of a flat file revolves around two essential elements: <ins>fields</ins> and <ins>delimiters</ins>. Let's delve deeper into each of these concepts and provide a comprehensive breakdown of their respective structures and porpusesses.
</p>

<br>

<ul class="justified-list">
  <li><strong>Fields</strong></li>
</ul>

<p>
Fields in a flat file represent the distinct pieces of data within a record. Each field corresponds to a specific attribute or characteristic of the data being stored. For instance, in a flat file containing employee records, fields could include employee ID, name, age, department, and salary. These fields are arranged in a predetermined order within each record. Fields are also sometimes referred to as attributes.
</p>

<br>

<ul class="justified-list">
  <li><strong>Delimiters</strong></li>
</ul>

<p>
Delimiters in a flat file are special characters or symbols used to separate the fields within a record. They serve as markers, indicating the boundaries between different data elements and enabling accurate extraction of specific fields. 
</p>

<br>

<p>
The choice of delimiter depends on the specific requirements and conventions of the flat file. It is crucial for delimiters to possess distinctiveness, ensuring that they are easily distinguishable and do not conflict with the data itself. For instance, the semicolon (;) may not be a suitable delimiter as it is commonly used in languages and regular text, making it less unique and prone to misplacement with other characters. On the other hand, the tilde character (~) could be a suitable option as it is less commonly used and possesses sufficient uniqueness. Additionally, delimiters can even be a combination of symbols that represent a unique distinguisher, such as the symbol ~#@$.
</p>

<!--
You can potentially write an example like the one below that demonstrates why it is bad.

OrderID,CustomerName,Product,Quantity,Price
1,John Doe,Widget A,5,10.99
2,Jane Smith,Widget B,3,7.99
3,Adam Johnson,Widget C,2,14.99

-->

<br>

```C++ {linenos=false}
// Fields (Attributes)
OrderID ~#@$ CustomerName ~#@$ Product ~#@$ Quantity ~#@$ Price

// Rows (Records)
3375  ~#@$  John Doe      ~#@$  Widget A  ~#@$  65  ~#@$ 10.99
2566  ~#@$  Jane Smith    ~#@$  Widget B  ~#@$  32  ~#@$ 7.99
5576  ~#@$  Adam Johnson  ~#@$  Widget C  ~#@$  5   ~#@$ 14.99
```

<br>

<r>
In this case, the delimiter is ~#@$, and each line represents a record. The fields within each record (OrderID, CustomerName, Product, Quantity, Price) are separated by the delimiter. By parsing the file using the delimiter, the system can extract and process the individual fields.
</r>

<!-- ##################### Separator - Bottom ##################### -->

<div class="line-divider-bottom">
  <div class="left-div"></div>
  <span>|</span>
  <span class="middle">History of storing data</span>
  <span>|</span>
  <div class="right-div"></div>
</div>

<!-- ##################### Separator - Bottom ##################### -->