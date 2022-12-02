---
toc: true
layout: post
description: Includes all grades and key takeaways
categories: [markdown, Comp Sci, 3 Week Sprint]
title: 3 weeks sprint grades blog
permalink: /sprint/grades
comments: true
---

I'll start with a highly informative table.

| Topics | Relevant Files | Grade |
|-|-|-|
| 3.1-3.2 | [Hacks Markdown](https://leonard514.github.io/FastPage/sprint/hacks1), [Python .ipynb](https://leonard514.github.io/FastPage/jupyter/3%20week%20sprint/2022/11/28/3.2hack.html) | 1/1 |
| 3.3-3.4 | [Hacks Markdown](https://leonard514.github.io/FastPage/sprint/hacks2) | 1/1 |


Now I'll talk about some key takeaways

# Topics 3.1-3.2

- Variable names should be concise yet sufficiently describe the purpose of the variable. For example, the variable name **priceApples** is descriptive enough to show its purpose: storing the price of apples
- There are variable types which can be appropriately applied to different situations
 - Boolean variables are applied to binary, true and false situations (such as whether someone is hungry)
 - Integer/float variables are applied to situations involving numbers, especially those that can be altered by mathematical operations (addition, subtraction, etc.)
 - String variables are appropriate for storage of data (in words) or identification numbers where math is not typically applied. They are enclosed in quotation marks.
- Variables can be assigned different ways in different programming languages. Here are some examples:

CollegeBoard pseudocode
```
numApples ← 10
```

Python
```python
numApples = 10
```
- It is possible to assign the value of a variable to another variable. If the variable a value is assigned to already has a value, that value is typically overwritten. Here's an example in pseudocode:

```
data1 ← 10
data2 ← 25
data1 ← data2
```

In this case, the final value of **data1** would be 25 since the value of **data2** overwrites that of **data1** in the third line.


- The last takeaway is that lists can be assigned as variables. These are often put in square brackets ([]) and the entries are separated by commas. The parts of the list are called **elements** and can exhibit the same data types as variables.
- Each element in a list is assigned an index, a nonnegative integer which is associated with the element in future commands.
 - It is very important to note that different forms of indexing can exist between programming languages. CollegeBoard pseudocode assigns the first element in a list the index **1**, while other languages (including Python) assign the first element the index **0**.

# Topics 3.3-3.4

- Lines of code in a program are executed in a specific order. This pattern is known as sequencing.
- Programs often incorporate selection, where associated lines of code are executed if a condition is satisfied. Often, a different set of commands will be executed if a condition is *not* satisfied. These most commonly take the form of **if statements** in python.
- Sometimes, programs need to execute lines of code on multiple elements in a list. Instead of writing similar lines of code repetitively, an iteration strategy is used. This often consists of a loop (including for loops, while loops, and recursive functions) which executes associated commands on all items in a list or repeatedly until a certain condition is fulfilled (or is not fulfilled).

- There are various operators which can apply mathematical operations on integer/float variables.
 - Addition (+), Subtraction (-), multiplication (*), and division (/) are identical to the operations learned in arithmetic.
 - The modulus operator (seen as a **%** in Python) performs a division operation but outputs the remainder instead of the quotient.

- There are certain string-related commands in pseudocode that *are not on the [exam reference sheet](https://apcentral.collegeboard.org/media/pdf/ap-computer-science-principles-exam-reference-sheet.pdf)*. Their validity and syntax quirks are therefore uncertain.
 - `substring(string, n, m)` reads a given **string** (or string variable) and starts at the **nth** character of that string. It reads **m** characters from that point.
 - `concat(string1, string2)` essentially results in an output of **string1string2** (in other words, the strings mashed together without any spaces). This output can be assigned to a variable.