---
toc: true
layout: post
description: Includes python for loops and web development notes
categories: [markdown, Comp Sci, Review Tickets]
title: Week 2 Review Ticket
permalink: /submissions/Week_2_Submission
comments: true
---

## Hi!

This is part of the Week 2 Review Ticket. If you came here, I hope you came here from the github issue. If not, please take a look right [here](https://github.com/Leonard514/FastPage/issues/5). That being said, if you missed where the python is, it's [here](https://leonard514.github.io/FastPage/scripts/loop_scripts)!

Anyways, if you came from the github issue, you are probably here for the fastpages/web development part of the submission. That part of the submission is too complex to just stick a single link in the title without a dedicated post, so here's to the changes!

## Changes!!!

There are quite a few things in the HTML hacks that I have had previously for a while. In case you missed the tags and search pages:

- [Tags](https://leonard514.github.io/FastPage/categories/)
- [Search](https://leonard514.github.io/FastPage/search/)

My website has plenty of "time box fragments" (otherwise known as tables), including the one below. If you want to see a lot of tables, you should see my [notes page.](https://leonard514.github.io/FastPage/_pages/02_notes.html#week-1-python-vocab)

Also, you probably noticed that my website has a different color scheme. Specifically, my top bar is black while the rest of the background is navy blue. I had to make quite a few customizations to an example dark mode file (as well as the default `fastpages-styles.scss` file) to change the colors of the background and the text to ensure a dark background and text with sufficient contrast.

I also had an adventure modifying the theme of my website. For notes about that adventure, click [here.](https://leonard514.github.io/FastPage/_pages/02_notes.html#week-2-html-notes). I decided to remove the theme since it removed the top bar, making it harder to access the tags page.

## Now, here's a table of my daily progress

| Date | Activities completed |
|-|-|
| August 29 | First attempt at theme integration using _config.yml. The theme was not inputted correctly, breaking the CI task in fastpages and making it impossible to update the website. |
| August 30 | Learned about dictionaries in a list in python. Added new information into the given list of dictionaries InfoDB, and demonstrated how to output list items backwards and in a random order. |
| August 31 |  Attempted to make a python quiz using a new list of dictionaries QuizDB, but got stuck due to various issues within the for loop and since I was appending my question/answer pairs to InfoDb instead of QuizDB. Also tried to append to a list using input and had trouble due to quotation issues. I eventually fixed the issue using f"{var_name}", which allowed printing of any variable value inside the quotation marks. Also learned about how I inputted my website theme wrong in a lesson, and revised that. Had trouble customizing dark mode example code. |
| September 1 | Was able to customize dark mode, making all parts of the website except the top bar navy blue (the top bar is the default dark-mode color) |
| September 2 | Customized the text color to contrast sufficiently with the background. |

## Remaining tasks
- Figure out how to control site status (when it's up and down) 
