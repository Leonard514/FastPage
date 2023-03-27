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

# Hacks Response

I started by testing all the algorithm stuff. I should probably paste this [URL](https://www.w3schools.com/python/trypython.asp?filename=demo_list) here since it'll let me execute python without Jupyter.

Now here's a table

| Algorithm Form | Time | Patterns |
|-|-|-|
| Constant | Negligibly small - took 2.622 * 10^-6 seconds to fetch an item from a list of 1000 elements. Took 9.536 * 10^-7 seconds to add two large numbers | The time is always negligibly small |
| Linear | Printing all values in larger list takes progressively more time. Printing a list with 100 elements takes 3.07 * 10^-5 seconds, but printing lists of 1000 elements takes 2.49 * 10^-4 seconds. | Time increases proportionally to the number of elements to perform operations on. |
| Quadratic | Performing the nested for loop operation took 0.00467 seconds on a list with 100 elements, but 0.0455 seconds on a list with 1000 elements. For a 10-fold increase of elements, the time taken increased by 100-fold | As the number of elements increases by a certain extent, time taken for execution increases by the square of this extent |


I also have some [sorting algorithms](https://www.bigocheatsheet.com/).

| Sorting Algorithm | Functionality | Worst Case Space Complexity| Worst Case Time Complexity |
|-|-|-|-|
| [QuickSort](https://en.wikipedia.org/wiki/Quicksort) | A pivot element is selected in the array, and all the other elements are divided into two subarrays so that all elements of one array have value less than the pivot element and all elements of the other array have value greater than the pivot element; the pivot element is then placed in the middle of the array. This process is repeated for all the subarrays until this is sorted. | Logarithmic | Quadratic |
| [Merge Sort](https://en.wikipedia.org/wiki/Merge_sort) | Make the unsorted list into sublists with one element. The sublists will be merged together with elements in order until a complete list is made | Linear | O(nln(n)) |
| [Timsort](https://en.wikipedia.org/wiki/Timsort) | 
| [Heapsort](https://en.wikipedia.org/wiki/Heapsort) | Divides the data into sorted and unsorted parts (the unsorted part is in a data heap, which is essentially a binary data structure where each object is a parent object with two child objects. This allows a targeted element to be obtained more quickly in a process similar to binary search); the algorithm starts by turning the unsorted part into the mentioned heap. For the unsorted part, the algorithm then gets the 


