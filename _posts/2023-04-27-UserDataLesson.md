---
toc: true
comments: true
layout: post
title: April 26 Big Idea 3 Lesson
description: Includes all the important Big Idea 3 Stuffs
---


Fill in the blanks: Copy-pasted from the lessons. Paragraphs 1 and 3 are duplicate instances that occurred twice in the document. Fill-ins are bolded.

In Python, classes are templates used to create objects, which are instances of those classes. Classes define the data elements (**attributes**) and methods that describe the behavior of the objects. Let's explore how to define a class and create objects in Python.

In the context of backend functionality, this class can be used to **create** , **manipulate**, and **manage** user data. For example, when a new user signs up for an account, you could create a new User object with their username and email. This object can then be used to perform various operations, such as validating the user's input, storing the user's data in a database, or processing user-related requests.

In Python, classes are templates used to create objects, which are instances of those classes. Classes define the data elements (attributes) and methods that describe the behavior of the objects. Let's explore how to define a class and create objects in Python.

Property Decorators allow developers to access and modify instance data more concisely. The @property decorator creates a getter method, while the @attribute.setter decorator creates a setter method.

In the context of backend functionality, this Employee class can be used to model employees within an application. You can create instances of this class to store and manage employee data, and the getter and setter methods can be used to access and modify employee information in a controlled way.

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

In the context of **backend functionality**, this Car class can be used to model cars within an application. You can create instances of this class to store and manage car data, and the getter and setter methods can be used to access and modify car information in a controlled way.

SQLite is a **software** library that provides a relational database management system. Unlike other databases, such as MySQL or PostgreSQL, SQLite is embedded within an application, which means it does not require a separate server process to operate. This makes SQLite a great choice for small-scale applications or for use in situations where you don't want to set up a full database server.

In this lesson, we will be demonstrating how to set up a SQLite database in Flask, which provides an easy-to-use interface for interacting with SQLite databases, and we'll walk through the process of setting up a new database, creating tables, and adding data. We'll also cover some basic SQL commands that you can use to interact with your database, including CREATE TABLE, INSERT, SELECT, UPDATE, and DELETE. By the end of this lesson, you'll have a good understanding of how to work with SQLite databases in Flask and be ready to start building your own **applications**.

One of the key features of **Flask** is its ability to work seamlessly with ~~ , including SQLite. A database is a collection of data stored in an organized manner that can be easily accessed, managed, and updated.

**SQL** is really useful because it helps people do a bunch of things with the data stored in databases. For example, they can use it to create new tables to organize data, add new data to a table, update data that's already there, or delete data that's no longer needed.

This block of code is a menu function that helps with **create** , **read** , **update** , and **delete** (CRUD) tasks and displays the schema. The menu function acts as a control point that directs the program to call different functions based on what the user wants to do. When users enter their preferred action, the input is checked to see which function to use. The menu function is created with no arguments and is called repeatedly, displaying the menu options until the user decides to leave.


The **create()** function allows users to input information about a coding professor and store it in a SQLite database named 'professors.db'. This script prompts the user for the professor's name, field of expertise, rating out of 10, and any reviews or comments about the professor. It then establishes a connection to the SQLite database and creates a cursor object for executing SQL commands.

This code demonstrates how to read data from a SQLite database using Python and the **sqlite3 library**. The first step is to establish a connection to the database and create a cursor object to execute SQL commands. Then, a SELECT query is executed to fetch all records from the "professors" table. If there are any records, the code iterates through each record and prints out the name, field of expertise, rating, and reviews for each coding professor. If there are no records in the table, a message indicating so is printed.

This code is a Python function for **deleting** a record from a SQLite database. The function prompts the user to input the name of the professor they want to delete. It then uses a SQL query to search for the professor in the database. If the professor is found, the user is prompted to confirm the deletion. If the user confirms, the function executes a SQL command to delete the record from the database. The function also prints a message confirming that the professor has been deleted from the list of coding professors. If the professor is not found in the database, the function prints a message indicating that the professor is not in the list.
