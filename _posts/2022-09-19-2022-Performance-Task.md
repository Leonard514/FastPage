---
toc: true
layout: post
description: Includes planning of the Create Performance Task
categories: [markdown, Comp Sci]
title: Week 3 Create Performance Task
permalink: /notes/performance_plan
comments: true
---

# The Project Idea:

My sister and I had this idea a while back of creating an app to monitor mental health. We didn't make any progress, but the concept was fair. So I'll have a go at it with the Create Performance Task. Here are a few ideas. 

- Providing a list of emergency numbers (I don't know how a calling function would be able to work, especially since this is meant to be a PC program; the previous concept was a mobile program)
- Log daily hours of sleep and display graphically (sleep is important for mental health!)
- Log time/activities spent with family or friends

Of course I need to check all the boxes, so I'll do that real quick. All of this will be based on only one part of the program (the sleep data part), but the other parts will be in the final product as well.

### Row 1: Program Purpose and Function

Take for example the log of the daily hours of sleep.

- I would theoretically make a textbox for user input. This would have two pieces of information to input: the date and how much sleep (hours) was taken.

- This information would be outputted graphically. A possibility would have time represented on an x-axis and hours of sleep represented on the y-axis. Each day would be represented by a dot, and the dots will be connected with straight lines.

- The functionality is essentially that a user enters sleep data every day, and the program **organizes the data** so the user could more easily understand trends of sleep and get appropriate sleep accordingly.

### Rows 2 and 3: Data Abstraction and Managing Complexity

Rows 2 and 3 will be answered with the same response (3b) on the exam, and they both have to do with lists... so I think it's appropriate to group them here. The way this will play out (according to the present plan) will be very similar to the [Python Lists and Dictionaries activity](https://leonard514.github.io/FastPage/scripts/loop_scripts).

- I will make a list of dictionaries named SleepData = []

- Then using the user input, I will store the input into a list using append commands, with the date being stored in the **Date** portion of the entry and the number of sleep hours being stored in the **Sleep_Hours** portion of the entry. In order to append the data, the input would likely be stored in variables before they are used in append commands.

- I will then use a loop to iterate through each item in the list to display all of the days in which data is collected.

- Without a list of dictionaries, it would be very difficult to associate each day with the number of hours of sleep each day. Separate variables could *possibly* be made for each day and each number of hours of sleep, but the number of variables which would eventually build up would make the solution impractical... possibly unless the variables were stored in some separate file and then imported. Even then, a loop must be used to iterate through the variables, raising the question of whether this would be functionally equivalent to using a list but with greater complexity.

Therefore, use of a list is optimal in making output.

### Rows 4, 5, and 6: Procedural Abstraction, Algorithm Implementation, and Testing

- To output the results of the list graphically, a function would be required. This function would likely involve a for loop and commands required to graphically display the data.

- In order to pass the "two calls with different arguments" check in Row 6, I will make variations for how the data is displayed. There will be two forms of variations:

1. The way the data is displayed (by line graphs, bar graphs, by tables, etc.)
1. The amount of days for which data is displayed (for past week, for past month, for past 3 months, for past year, or all-time)

I don't know what graphical displays would look like in terms of code, but in terms of tables I expect to see something functionally similar to the [liquid syntax](https://leonard514.github.io/FastPage/_pages/02_notes.html#tables-in-liquid) from Week 2.