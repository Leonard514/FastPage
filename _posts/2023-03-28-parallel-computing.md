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

Here is a [URL](https://www.w3schools.com/python/trypython.asp?filename=demo_list) that is particularly important since I need it to execute Python on a chromebook. Anyways, I'll paste in my code and current results below so you can take a gander.

```python
# This W3Schools lesson was very helpful. 
# https://www.w3schools.com/python/python_lists_comprehension.asp
# I can also do a documentation drop on you if you're more curious about this stuff. 
# The instructors have only skimmed the surface of the available data structures in Python.
# Here you go: https://docs.python.org/3/tutorial/datastructures.html

# Let's start simple. All the numbers from 0 to 99.

numbers = [i for i in range(100)]

print("Numbers:", numbers)

# List comprehension can be used to filter lists!!!

evenNumbers = [i for i in numbers if i % 2 == 0]

print("Evens:", evenNumbers)

# Can also perform operations on each item in a list.
# See example for changing all these numbers back to the integers

convertedNumbers = [ int(i/2) for i in evenNumbers]


print("Back to integers:", convertedNumbers)


# I've created an equivalent to the head function and the tail function using list comprehension.
# These list the first 10 elements in a list and the last 10 elements in the list, respectively.
# You can replace the list name with your desired list and you're off!!!

headNumbers = [i for i in numbers if i < 10]
print("Head:", headNumbers)

tailNumbers = [i for i in numbers if i > (len(numbers) - 11)]
print("Tail:", tailNumbers)
```

![image](https://user-images.githubusercontent.com/92343899/228683565-a3313dc0-cd16-485d-b435-03658d557cf7.png)

![image](https://user-images.githubusercontent.com/92343899/228683592-f0a69e64-27fd-40ff-bbb8-f4527d83c4b0.png)

# Hashmap Notes

In python, the built-in hashtable is a dictionary. Hashtables allow for efficiency in lookup, insertion, deletion. The time complexity for looking up an item in a hashtable is constant O(1) since the known key can be found quickly. Without dictionaries, there are hashing. **There are no duplicates** (can't have multiple values into the same key); collisions can result from different keys mapping to the same hash value.

Set Example: Executing the code results in removal of all duplicate elements within the brackets. The set is printed in curly braces. Sets are in the tech talk along with hash maps likely since they are cleaner versions of hashmaps, which cannot contain duplicate entries associated with a key (this would result in collisions). Dictionaries cannot have duplicate keys.


Dictionary example about lover album: Within here are string variables (ex: the title of the album and the artist), integer variables (release year), list variables (the genre of the music), and a dictionary variable (the tracks).


SAVED WORK BELOW

```python
# Question 1: What do you notice about the set, and why is this in the tech talk?

my_set = set([1, 2, 3, 2, 1])
print(my_set)  


# Question 2 about the lover album. What data structures are there?

lover_album = {
    "title": "Lover",
    "artist": "Taylor Swift",
    "year": 2019,
    "genre": ["Pop", "Synth-pop"],
    "tracks": {
        1: "I Forgot That You Existed",
        2: "Cruel Summer",
        3: "Lover",
        4: "The Man",
        5: "The Archer",
        6: "I Think He Knows",
        7: "Miss Americana & The Heartbreak Prince",
        8: "Paper Rings",
        9: "Cornelia Street",
        10: "Death By A Thousand Cuts",
        11: "London Boy",
        12: "Soon You'll Get Better (feat. Dixie Chicks)",
        13: "False God",
        14: "You Need To Calm Down",
        15: "Afterglow",
        16: "Me! (feat. Brendon Urie of Panic! At The Disco)",
        17: "It's Nice To Have A Friend",
        18: "Daylight"
    }
}

# What data structures do you see?
#
#

# Printing the dictionary
print(lover_album)




# CODE BLOCK 3

print(lover_album.get('tracks'))
# or
print(lover_album['tracks'])


# CODE BLOCK 4

print(lover_album.get('tracks')[4])
# or
print(lover_album['tracks'][4])


# CODE BLOCK 5

lover_album["producer"] = ['Taylor Swift', 'Jack Antonoff', 'Joel Little', 'Taylor Swift', 'Louis Bell', 'Frank Dukes']

# What can you change to make sure there are no duplicate producers?
# Use set notation!!!
#

# Printing the dictionary
print(lover_album)



# CODE BLOCK 6

lover_album["tracks"].update({19: "All Of The Girls You Loved Before"})

# How would add an additional genre to the dictionary, like electropop? 
# 
# 

# Printing the dictionary
print(lover_album)

# CODE BLOCK 7

for k,v in lover_album.items(): # iterate using a for loop for key and value
    print(str(k) + ": " + str(v))

# Write your own code to print tracks in readable format
#
#

# CODE BLOCK 8

def search():
    search = input("What would you like to know about the album?")
    if lover_album.get(search.lower()) == None:
        print("Invalid Search")
    else:
        print(lover_album.get(search.lower()))

search()

# This is a very basic code segment, how can you improve upon this code?
#
#
```
