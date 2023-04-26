---
toc: true
comments: true
layout: post
title: April 26 Big Idea 3 Lesson
description: Includes all the important Big Idea 3 Stuffs
---

Lists
- Ordered sequence elements
- Index has integers (not string keys)
- Starts at 1 for AP exam (usually 0 for Python)
- Helpful for data storage in one list (rather than lots of variables)
  - Can perform iterative functions on each list (for loops, etc.)
  
  #### Code Block 1
  
  ```python
  # variable of type string
name = "Sri Kotturi"
print("name", name, type(name))

# variable of type integer
age = 16
print("age", age, type(age))

# variable of type float
score = 90.0
print("score", score, type(score))

print()

# variable of type list (many values in one variable)
langs = ["Python", "JavaScript", "Java", "Bash", "html"]
print("langs", langs, type(langs))
print("- langs[2]", langs[2], type(langs[2]))

print()

# variable of type dictionary (a group of keys and values)
person = {
    "name": name,
    "age": age,
    "score": score,
    "langs": langs
}
print("person", person, type(person))
print('- person["name"]', person["name"], type(person["name"]))
```

#### Mathematical Expressions

- + addition
- - subtraction
- * multiplication
- / division
- % modulo
- ** raise to power

#### Code Block 2

```python3
num1 = 2
num2 = 4
num3 = 6
num1 = num2 ** num3
num3 = num1 % 5
num2 = (num1 + num3) // 9

print(num1)
print(num2)
print(num3)
```


num1 is 4^6 or 4096
num3 is 




#### Selection

- Execute code based on conditional statements
   - Conditional allows code to execute if a condition true/false
   - If, Elif, Else
   
If: If a condition is true or not (any boolean expression)
   - If true, executes the block
Else: Executes code block if the condition is false
Elif: Checks multiple conditions in sequence, executes if any is true
- Nested Conditional: Conditional statement inside another conditional statement. For more complex conditions that depend on each other.

Indentation is important for conditionals in Python to allow Python to tell which code is conditionally executed

#### Binary Search

- Efficient Search algorithm to find and select element in sorted list
- Divides search interval in half for the middle element, compares to target. Continues to lower/upper half based on greater than/less than
- Has O(log(N)) time complexity (max iterations is # of times list can be divided into half)


#### HACK: Write program using conditionals or nested conditionals

```python3
```

#### algorithms and data structures

Algorithms rely on sequential steps with input and output
- Algorithms rely on data structures (ex: sorting algorithm needs lists, arrays, etc)


- Algorithm: Finite set instructions to accomplish task
- Sequencing: Order to task completion (lines code)
- Selection: Choose from two outcomes based on decisions
- Iteration: Repeat until condition met
- Procedure: Sequence of instructions to perform tasks

- Call procedure with arguments. Parameters passed to function, can perform tasks/calculations.
- Can store results in variables, print, etc.
- Can be defined in external files (libraries)

Avoid errors:
- Use proper syntax

Algorithmic Efficiency
- Time/resources required for execution
  - Time complexity: Time to complete tasks
  - Space Complexity: Memory needed to complete task
  - Use Big O notation
  
  
```python3
a = 0
for i in range(N):
  for j in reversed(range(i, N)):
    a = a + i + j
```

Time complexity: likely polynomial O(N*N) because for each number in a range, an operation must be performed for each number once again... this results in a number of operations totalling around N squared.

```python3
value = 0
for i in range(n): #iterates "n" times, with "i" taking on values from 0 to n-1.
  for j in range(i): # iterates "i" times, with "j" taking on values from 0 to i-1.
    value=value+1
```

Time Complexity: For each i in a range: the second line runs n times while the third line runs n+1 times. This makes for n(n+1) complexity.


Efficiency is required to make sure the algorithms run in a reasonable amount of time


#### Simulations and Iterations


Simulations needed to model complex phenomena while efficiently using resources

```python3
numlist = [3, 5, 68, 203]

for key, num in enumerate(numlist):
    print(f"This entry's index is {str(key)}, but its value is {str(num)}.")
    print(f"The difference between the value and the index is {num - key}.")
```

Note: this prints indexes. **Key, num** is similar to a dictionary since a dictionary uses **key, value**. The key gives access to the items/numbers. The index of the list in this case is similar to the key in the dictionary.


#### List Comprehensions

```python3
player_hand = [] # the player's hand is represented as a list
# because lists are mutable (can change), they can be added to, like drawing a card

# assume the deck below is a a deck of shuffled cards
deck = [Card("Hearts", 3), Card("Spades", 12), Card("Diamonds", 11)]
def draw_card(hand, deck):
    hand.append(deck.pop())

#try it out
draw_card(player_hand, deck)
print([card.show() for card in player_hand])
```

#### Recursive Loops

```python3
def fibonacci(terms):
    if terms <= 1:
        return terms
    return fibonacci(terms-1) + fibonacci(terms-2)

fibonacci(5)
```

Recursive loops are good for functions that call themselves with diff arguments

#### Nesting Loops (increase time complexity)

```python3
def build(deck):
        for suit in ["Spades", "Clubs", "Diamonds", "Hearts"]:
            for val in range(2, 15): #HINT: try replacing this function
                deck.append(Card(suit, val))
```

#### While Loop

```python3
def build(deck):
        for suit in ["Spades", "Clubs", "Diamonds", "Hearts"]:
            for val in range(2, 15):
                deck.append(Card(suit, val))

#HINT: you may want to make an incrementing i variable
```

Can occur to make functions execute until something happens

```python3
import random
i = 0

while True:
    i += 1
    ch = random.randint(1, 11)
    if ch == 10:
        print(f"It took {str(i)} random generations to get 10.")
        break
```


#### Randomization

```python3
def shuffle(deck):
    random.shuffle(deck)
```


#### Databases

Contains columns and rows. Do SQLite stuff... ok.

Model file: Make new databases + standardizes database formatting. Objects are made.


Init function initializes the attributes

Setters: Set/change values of attributes in class
Getter: Access attributes in a class
API File: Messenger to allow programs to access the databases

Important for Flask repositories. Do initUsers()

#### Hacks DB

Class with at least 4 attributes (if no cursor)
Setters/getters
CRUD functions
init function with 4 entries
Screenshot of SQLite file
