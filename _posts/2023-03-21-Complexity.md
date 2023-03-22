---
toc: true
layout: post
description: Includes Important Notes about Algorithm Complexity and managing high volumes of complexity
categories: [markdown, Comp Sci]
title: Time/Space Complexity Notes
permalink: /notes/complexity
comments: true
---


### Prompt 1: Why do programmers care about time and space complexity?

Programmers care about space complexity because they want to make sure that their computer programs consume a reasonable amount of resources to function. If programs consume too much memory to function, they may crash the computers they run on (especially if this is a product intended to be installed on consumer machines; these machines will have limited memory). Programmers care about time complexity because they want to ensure their programs run in a reasonable amount of time. If programs run too slowly (ex: a search engine taking a minute to pull up results), this decreases ease of use. From a corporate perspective, slow programs are not that competitive and will not make profits.


Notes
- Loading time for 5000 pixels in width took between 0.1 and 0.5 seconds.
- Loading time for 2500 pixels in width took less time
- Loading time for greater image resolution has slowed down performance and in some cases has crashed the kernel. The maximum width of 40000 pixels took 30-60 seconds to load (if it did)

Loading large images is both a space complexity and a time complexity problem. The space complexity is through managing

Big O notation

- Constant O(1)
- Linear On
- Quadratic On^2
- Logarithmic Olog(n)
- Exponential O2^n


Constant
- Finding number in a list with a known index
- Dictionary (keys and values)
  - An example of time complexity (will take the same time to fetch the object)
- Space complexity: returning a sum of two numbers (no matter how large those numbers are)

Linear
- Iterating through list (not as efficient as constant) - Time
  - Searching for a value in a list with unknown index
- Space: Reversing the order of a list

Quadratic
- Nested for loop operation (time)
- Space complexity - Matrix - this may take a while

Logarithm - shorter than 0(n)
- Binary Search - elements in order, do number in center, adjust search based on if element is above or below that part

Exponential (2^n)
- Fibonacci sequence, series of numbers and each number is sum of two preceding numbers. Do recursion with CRUD menu...
- As numbers increase, the function will take a while to execute.
- Generate subset will print every possible combination of a list of numbers. This will make many additional combinations very quickly. 
