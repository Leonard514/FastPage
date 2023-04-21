---
toc: true
comments: true
layout: post
title: April 21 Binary Lesson
description: Application of Binary Math
categories: []
---

## Lesson Prompts

Prompt 1: Record 5 things you already knew about binary before this lecture
1. Binary is a base 2 numeric system with digits 0 and 1
2. An IPv4 address uses 8 binary bits for each octet ranging from 0 to 255
3. Other characters in computers are represented by binary bits
4. Boolean variables have a binary behavior (only two possible values of true and false)
5. 

Prompt 2: Think of three applications that rely on binary

Now the funny thing is, all things related to computers rely on binary. So I can essentially list three programs of my choice here.

1. Cisco Packet Tracer
2. Github
3. Discord

Why is binary effective for storing information?

Binary is effective since having no/little electrical signal can be 0 and having electrical signal is 1.
Having a base-2 number system reduces time complexity of operations

Bitwise Operations (table!)

| Operator | Name | Action |
|-|-|-|
| & | AND | Returns true (or 1) if both boolean operations are true (or 1) |
| pipe/vertical bar | OR | Returns true (or 1) at least one of two boolean operations return true (or 1) |
| ^ | XOR | Returns true (or 1) if exactly one of two boolean operations return true (or 1) |
| ~ | NOT | Returns true (or 1) for a false operation (or 0), returns false for true |
| << | Left Shift | |
| >> | Right Shift | |
| >>> | Zero-fill Right Shift | |


## Notes on Code Block 1

```python
def binary_operations(num1, num2):
    # Perform the binary operations
    and_result_decimal = num1 & num2
    or_result_decimal = num1 | num2
    xor_result_decimal = num1 ^ num2
    not_result_decimal = ~num1

    # Convert results to binary
    and_result_binary = bin(and_result_decimal)[2:]
    or_result_binary = bin(or_result_decimal)[2:]
    xor_result_binary = bin(xor_result_decimal)[2:]
    not_result_binary = bin(not_result_decimal)[2:]

    # Return the results as a tuple of tuples
    return ((and_result_decimal, and_result_binary),
            (or_result_decimal, or_result_binary),
            (xor_result_decimal, xor_result_binary),
            (not_result_decimal, not_result_binary))

# Ask the user for input
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))

# Call the binary_operations function and print the results
and_result, or_result, xor_result, not_result = binary_operations(num1, num2)
print("AND result: decimal =", and_result[0], ", binary =", and_result[1])
print("OR result: decimal =", or_result[0], ", binary =", or_result[1])
print("XOR result: decimal =", xor_result[0], ", binary =", xor_result[1])
print("NOT result: decimal =", not_result[0], ", binary =", not_result[1])
```

The AND operation seems to execute something similar to what I've seen with my subnetting experience in the school cyber team. It seems to take all the bits and compare left-to-right. When the operation fails the first time, the operation terminates and all the bits to the left will be zeros. OR and XOR seems a bit more flexible with the bits

## Code Block 2 Notes

I modified it so I can run it multiple times in one session

```python
def string_to_binary(string):
    binary = ''
    for char in string:
        binary += format(ord(char), '08b')  # Convert the character to binary and append to the binary string
    return binary

# Example usage
def hrar():
    word = input("Enter a word to convert to binary: ")
    binary_word = string_to_binary(word)
    print(f"The binary representation of '{word}' is {binary_word}")

hrar()
```

It seems the binary conversions of each ASCII character are printed one on top of the other. I would prefer that a space be added between each character's binary conversion for clarity purposes.


## Code Block 3 Notes

This is an example of binary search. Keep splitting the list in half and adjusting guesses based on if the number is higher or lower.

```python
import random 

hid = random.randint(0,100)
gues = 0
def game():
    global gues
    gues += 1
    num = int(input('Pick a number'))
    if num < hid:
        print('higher')
        game()
    if num > hid:
        print('lower')
        game()
    if num == hid:
        print(hid)
        print('You Win !!!')
        print('guesses: ', gues)
game()
```


## Logic Gates

This is NOT, AND, OR gates. They are summarized in the table towards the top. There's a few notes:

NAND Gate is a NOT performed on the AND (outputs false if both inputs are true)

NOR gate - NOT performed on the OR??? (output true if both inputs false) 
