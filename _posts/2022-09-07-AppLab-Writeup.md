---
toc: true
layout: post
description: Includes planning and execution of scripts in Javascript using Applab
categories: [markdown, Comp Sci]
title: Week 3 Javascript Quiz Blog
permalink: /notes/javascript_quiz
comments: true
---

Below I describe the procedures that I and Abdullah took to make the quiz. We began with planning a topic, then made the actual questions. The questions are given with correct answers in **bold**. 

# Quiz Questions

1) What is the capital of Iceland?
    a) **Reykjavik**
    b) Kopavogur
    c) Hafnarfjoerdur
    d) Akureyri
2) What is the capital of Brazil?
    a) Rio de Janerio
    b) **Brasilia**
    c) Sao Paulo
    d) Lisbon
3) What is the capital of Pakistan?
    a) Lahore
    b) Karachi
    c) **Islamabad**
    d) Mumbai

## Coding


<details>
<summary>Full Code</summary>
```
var correct = 0;
onEvent("StartButton", "click", function( ) {
  setScreen("Question1");
});
onEvent("reykjavik", "click", function __() {
  console.log("reykjavik clicked!");
  correct ++;
  console.log(correct);
  setScreen("Question2");});
onEvent("kopavogur", "click", function __() {
  console.log("kopavogur clicked!");
  setScreen("Question2");});
onEvent("akureyri", "click", function __() {
  console.log("akureyri clicked!");
  setScreen("Question2");});
onEvent("hafnarfjoedur", "click", function __() {
  console.log("hafnarfjoedur clicked!");
  setScreen("Question2");});
onEvent("brasilia", "click", function __() {
  console.log("brasilia clicked!");
  correct ++;
  console.log(correct);
  setScreen("Question3");});
onEvent("lisbon", "click", function __() {
  console.log("lisbon clicked!");
  setScreen("Question3");});
onEvent("SaoPaulo", "click", function __() {
  console.log("SaoPaulo clicked!");
  setScreen("Question3");});
onEvent("rio", "click", function __() {
  console.log("rio clicked!");
  setScreen("Question3");});
onEvent("islamabad", "click", function __() {
  console.log("islamabad clicked!");
  correct ++;
  console.log(correct);
  setScreen("Results");});
onEvent("karachi", "click", function __() {
  console.log("karachi clicked!");
  setScreen("Results");});
onEvent("lahore", "click", function __() {
  console.log("lahore clicked!");
  setScreen("Results");});
onEvent("mumbai", "click", function __() {
  console.log("mumbai clicked!");
  setScreen("Results");});
console.log(correct);
onEvent("Results", "mouseover", function( ) {
  setText("scorereport", "Congratulations!!! You got " + ((correct + "/3") + " correct!!!"));
});
```
</details>



We started coding the designs. code.org uses Javascript. We first defined a variable.

```
var correct = 0;
```

This command sets a variable **correct** to 0

We then used the onEvent command to configure what happens when buttons or textboxes were clicked. A sample is visible below.

```
onEvent("StartButton", "click", function( ) {
  setScreen("Question1");
});
```

Similar to if statements, loops, and other commands, **onEvent** has associated commands.

- The first criteria of **onEvent**, **StartButton**, defines what object the command applies to. This is an app, so there are objects such as buttons, textboxes, and images.
- The second criteria, **click**, determines the action which triggers the command. 
- The associated command is setScreen, which as implies sets the screen to the named screen (in this case **Question1**)

There were many onEvent commands which were highly similar.

```
onEvent("reykjavik", "click", function __() {
  console.log("reykjavik clicked!");
  correct ++;
  console.log(correct);
  setScreen("Question2");});
```

This does a few more things. **console.log**  prints the text inside the parenthesis and quotes to console. It can also print the value of a variable (in this case **correct**). This was extremely useful for debugging purposes, as I will elaborate on shortly.

correct ++ simply increases the value of the correct variable by 1.

I will now discuss the primary issue we encountered in the project.

```
setText("scorereport", ("Congratulations!!! You got " + correct) + "/3" + " correct!!!");
```

This command was placed at the very end of our code. It essentially put the text into the textbox named **scorereport** Whenever we ran the code, we found that at the end the score was either 0 or undefined.

In order to figure out the issues, we used a command which was seen in the second **onEvent** command

`console.log(correct);`

Using this, we found that the variable **correct** was indeed increasing if the correct answers to the questions were selected. Therefore, the issue was that the last line of code was run before the quiz was even taken (when the variable correct was 0). To solve this issue, we made the **setText** command to be executed as part of an **onEvent** command. Here was the final version of the command.

```onEvent("Results", "mouseover", function( ) {
  setText("scorereport", "Congratulations!!! You got " + ((correct + "/3") + " correct!!!"));
});
```

The **Results** page was the final page where the score was displayed. The event was **mouseover**, which is essentially if the mouse is over the page. This made it so the command was executed only when the quiz taker entered the page, ensuring that the correct value for the number of correct answers was outputted.