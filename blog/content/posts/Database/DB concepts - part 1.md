---
title: "DB Concepts   Part 1"
date: 2023-05-17T12:33:58-07:00
draft: true
---

<br>
<br>

### Intro

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;It is widely recognized that volatile memory like RAM (Random Access Memory) is not suitable for storing and maintaining data due to its tendency to lose information upon each reboot. While programmers are familiar with various methods of storing data, such as files and databases on different storage devices, they may not fully comprehend the factors influencing the choice between these options. This raises the question: Why should we use databases when files can serve the same purpose of storing data? To gain a deeper understanding, this section delves into the past of electronic computers, providing a concise overview of the historical evolution of data storage and explaining the rationale behind selecting one approach over another.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;While I acknowledge that comprehensive historical overviews may not be appealing to everyone, it is crucial to grasp the unique advantages and limitations of different data storage strategies that have been utilized over time. Therefore, it becomes essential to explore the historical evolution of various data storage methods before we can fully appreciate the role of databases and SQL within this context.
</div>

<br>
<br>

### History of data storage

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;During the early stages of computer development, the concept of a database was still emerging, and practical implementation was limited. The focus during this time was on exploring the theoretical aspects and conceptual frameworks of organizing data in a structured manner. During that period, storage costs were significantly high, which led system designers to prioritize minimizing the usage of storage resources for their tasks. In addition, the relatively slower computing speeds necessitated the emphasis on achieving optimal performance. As a result, data was predominantly stored in files, which served as discrete containers for specific information.
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;These files were typically stored on storage media like hard drives or magnetic tapes, but they differed from the everyday files we are accustomed to. To function as well-defined containers, these files required a structured format that allowed users to efficiently work with and manipulate information to the best of the capabilities available at that time. These files acquired the designation of flat files. Despite lacking the complex structure and relationships of a database, they emerged as the preferred architectural solution due to their ability to achieve two crucial objectives: conserving expensive storage and facilitating efficient processing. Put simply, during that period, there were no other viable alternatives available.
</div>

<br>
<br>

### Structure of a flat file

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In a flat file, data is typically organized in a sequential manner, with each record having a consistent length comprising a fixed number of characters. The structure of a flat file revolves around two essential elements: fields and delimiters.
</div>

<br>
<br>

###### Fields

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Fields in a flat file represent the distinct pieces of data within a record. Each field corresponds to a specific attribute or characteristic of the data being stored. For instance, in a flat file containing employee records, fields could include employee ID, name, age, department, and salary. These fields are arranged in a predetermined order within each record.
</div>

<br>
<br>

###### Delimiters

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;Delimiters in a flat file are special characters or symbols used to separate the fields within a record. They serve as markers, indicating the boundaries between different data elements and enabling accurate extraction of specific fields. 
</div>

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;The choice of delimiter depends on the specific requirements and conventions of the flat file. It is crucial for delimiters to possess distinctiveness, ensuring that they are easily distinguishable and do not conflict with the data itself. For instance, the semicolon (;) may not be a suitable delimiter as it is commonly used in languages and regular text, making it less unique and prone to misplacement with other characters. On the other hand, the tilde character (~) could be a suitable option as it is less commonly used and possesses sufficient uniqueness. Additionally, delimiters can even be a combination of symbols that represent a unique distinguisher, such as the symbol ~#@$.
</div>

You can potentially write an example like the one below that demonstrates why it is bad.

OrderID,CustomerName,Product,Quantity,Price
1,John Doe,Widget A,5,10.99
2,Jane Smith,Widget B,3,7.99
3,Adam Johnson,Widget C,2,14.99

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;For example, consider the following flat file representing customer orders:
</div>

```C++ {linenos=false}
OrderID ~#@$ CustomerName ~#@$ Product ~#@$ Quantity ~#@$ Price

@3375 ~#@$ John Doe     ~#@$ Widget A ~#@$ 65 ~#@$ 10.99
@2566 ~#@$ Jane Smith   ~#@$ Widget B ~#@$ 32 ~#@$ 7.99
@5576 ~#@$ Adam Johnson ~#@$ Widget C ~#@$ 5  ~#@$ 14.99
```

<br>

<div align="justify">
&emsp;&emsp;&emsp;&emsp;In this case, the delimiter is ~#@$, and each line represents a record. The fields within each record (OrderID, CustomerName, Product, Quantity, Price) are separated by the delimiter. By parsing the file using the delimiter, the system can extract and process the individual fields.
</div>