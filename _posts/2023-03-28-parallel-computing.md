---
toc: true
layout: post
description: Includes Important Notes about Algorithm Complexity and managing high volumes of complexity
categories: [markdown, Comp Sci]
title: Parallel Computing + Hashmaps Notes
permalink: /notes/parallel
comments: true
---

# Class Notes - Parallel Computing

top -H gives a list of processes! I've run this on Linux machines before. You want to run this on a terminal. There is a #TH in Mac and/or the total number of threads at the top. I think number of threads is also available via Windows Task Manager.

When the code affecting the images is run, there is a img.putdata([grey_pixel(pixel) for pixel in image['numpy']]). This is a for loop in one line, with brackets for the list. There is a list comprehension hacks exercise (I'll have to use the W3Schools Python interpreter for that). You put the list of the for loop into the list.

**Sequential Processing** example: Each image is processed **one at a time**. In order to see this more clearly, the class increased the baseWidth to 2000 pixels. Since it took half a minute for each set of images to render on Lily's computer, it was more obvious that sequential processing was occurring.

**Parallel Processing**: Each of the images are processed simultaneously. Mr. Yeung's execution took 43.9 seconds rather than 48 seconds. This was largely dependent on the threads. Mr. Yeung observed 110 threads initially/during sequential processing, but 113 threads while the parallel processing was occurring. Mr. Yeung also noted that computers can max out their threads and parallel processing would not be too different. In my opinion, parallel computing should be faster if computing resources are not being strained by other processes

Chinmay asked if it was possible to apply multiple threads to the same loop (iteration operation). Mr. Yeung responded that it is not possible to run multiple threads on one loop, but it is possible to run multiple threads on multiple loops. However, setting up multiple loops would be impractical/inefficient 

# College Board Notes

I was instructed to provide answers + thoughts about the question form of the college board video. I'll provide my general notes on the video contents first.


- Sequential/parallel/distributed computing

- Computers handle many tasks
   - System: Managing hardware, working with network, etc.
   - User: Executing user programs (google chrome, MS Excel)
- Computer needs to balance + schedule all the tasks


Sequential Computing
- Do tasks one at a time.
   - Applies to computers with one Core Processor Unit
   - Tasks with dependencies (Task C depends on Task B, Task B depends on Task A, etc.)
- Time to execute is the sum of execution times of individual tasks


Parallel Computing
- Program is segregated into smaller computing operations
  - Done on same computer. Usually has sequential/parallel portions
- Why?
  - Hardware-driven (1 CPU/GPU has many cores), faster
    - Ex: Having all students grade their papers is faster
  - Lots of data can be processed in same way - [Single Instruction, Multiple Data (Wikipedia)](https://en.wikipedia.org/wiki/Single_instruction,_multiple_data) (SIMD - processors perform the same operation on multiple pieces of data)
  - More scalable than sequential computing
  - Time taken is longest time of any processor
    - Works if there aren't dependencies in tasks
    - Takes as long as all sequential tasks + longest parallel task

Speedup time
 - Sequential processing time / Parallel Time (proportional comparison)
 - Parallel computing restricted by sequential portions (dependencies). At a point, adding parallel portions won't increase efficiency


Distributed Computing
- Uses other computers to run a program (uses more than one computer). Needs network access.
 - Mixes sequential and parallel computing. Allows for execution of programs that would otherwise be impossible with a single computer
- Ex: Google Search, Beowolf Clusters, executing tasks over the web
- If the network is not down or if responses take a long time, time efficiency may decrease.


### Example 1

- Computer has 2 identical processors. Each process must be executed on single processor, each processor can do one at a time. No dependencies. Find the minimum time to execute.

| Process | Execution time |
|-|-|
| X | 50 seconds |
| Y | 10 seconds | 
| Z | 30 seconds |

Assign these processes as follows
- Processor 1: X (50 sec)
- Processor 2: Y and Z (10 + 30 = 40 sec)

Minimum time of **50 seconds* detected.

### Example 2

- Computer has two identical processors that can run parallely. No dependencies.

| Process | Execution Time |
|-|-|
| A | 25 Seconds |
| B | 45 Seconds | 

Find difference in execution time between parallel processing and sequential processing.

In parallel processing, assign the processes as follows:

Processor 1: Process A (25 sec)
Processor 2: Process B (45 sec)

This will take a total of 45 seconds.

In sequential processing, these processes will be run one after another for a total of (45 sec + 25 sec) 70 sec. 

The time difference is 70 sec - 45 sec = **25 seconds**.

### Example 2

Computer has two processors. No dependencies. Assign the 4 processes to optimize execution time.

| Process | Execution Time |
|-|-|
| A | 25 seconds |
| B | 25 seconds |
| C | 10 seconds |
| D | 40 seconds |

To optimize the execution time, the execution time for each of the parallel processors should theoretically be as close as possible. Here are assignments that would fulfill this aim:

Processor 1: Processes A and B (25 sec + 25 sec = 50 seconds)
Processor 2: Processes C and D (10 sec + 40 sec = 50 seconds)

The execution will take 50 seconds and will have the maximum efficiency possible. Execution time will be optimized.


# Hack 3: Example of List Comprehension

Here is a [URL](https://www.w3schools.com/python/trypython.asp?filename=demo_list) that is particularly important since I need it to execute Python on a chromebook. Anyways, I'll paste in my code and current results for now. I'll be sure to expand on this later.

```python
# This W3Schools lesson was very helpful. https://www.w3schools.com/python/python_lists_comprehension.asp


#Let's start simple. All the numbers from 0 to 99.

numbers = [i for i in range(100)]

print(numbers)

# List comprehension can be used to filter lists!!!

evenNumbers = [i for i in numbers if i % 2 == 0]

print(evenNumbers)
```

![image](https://user-images.githubusercontent.com/92343899/228383636-f13843fa-1a22-40a3-897e-beffc31d9e05.png)
