---
toc: true
layout: post
description: Includes Important Notes about difficult questions and clarifications
categories: [markdown, Comp Sci]
title: MCQ #4 Reflection
permalink: /notes/MCQ5reflection
comments: true
---

# Integrity Disclaimer

The author does not permit copying of any of the reflections contained within this post. Cheating has severe consequences, among them a stain on the academic record and a lack of understanding about the relevant contents of the course. Do your own work please!

# Statement of Intention

This blog post is for reflection on multiple choice questions that I found to be particularly difficult. These include questions that I got wrong as well as questions that I found to be particularly difficult. I will not go over all of the questions to reduce vulnerabilities in the integrity system.

# Reflection

Here are a few of the questions that were of interest.

## Question 7: What is assigned to a new computer after connecting to the Internet?

There was an option here that I had never heard of despite previous experience with computer networking, and that is called a packet number. I am familiar with the idea of data transmissions via packets through networks from servers to clients. According to this [source](https://www.liveaction.com/resources/blog/network-packet/#:~:text=The%20packet%20number%20%E2%80%93%20each%20packet,part%20of%20the%20complete%20information.), packet numbers are identifiers within a packet saying where within a set of data the packet fits and how many packets comprise the set of data. The debate about what packet numbers are assigned to is therefore closed.

I am familiar with computers being assigned IP addresses through a process known as [Dynamic Host Configuration Protocol](https://www.spiceworks.com/tech/networking/articles/what-is-dhcp/). Essentially, a DHCP server (which could be a standalone server or a router) assigns a computer an IP address for a finite period of time. This address comes from a pool of available addresses. It is actually possible to manually configure your computer IP address, but DHCP is more scalable for larger networks (ex: the school network) and is less susceptible to IP address conflicts (computers must have unique IP addresses to properly receive network packets).

## Question 23: What is not an example of searching for patterns in large datasets to produce useful information?

I answered this one incorrectly. The wrong answer I chose had to do with online companies looking through viewing habits to suggest products based on other customers' purchases. I selected this one on the basis that the behavior of other customers may not be representative of the behavior of one specific customer. However, it seems that similarities are enough in this case.

The correct answer in this case had to do with finding the top 10 students in class rank at a local high school. Sorting through the highest GPAs is not pattern matching according to college Board. I can see that looking for the highest values in a dataset is a relatively simple operation here. There is also some context that is obscured by the conditions of this school, where we have around 2500 students. That's actually 5 times higher than the [national average](https://www.publicschoolreview.com/average-school-size-stats/national-data), but that's not to say we're close to the biggest school in the United States. Regardless, 500 students and their GPAs is a small scale operation compared to analyzing millions of customer data points in an online system.
