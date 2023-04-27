---
toc: true
layout: post
description: Includes Important Notes about difficult questions and clarifications
categories: [markdown, Comp Sci]
title: MCQ 2020 and 2021 Reflection
permalink: /notes/MCQ2020reflection
comments: true
---

# Integrity Disclaimer

The author does not permit copying of any of the reflections contained within this post. Cheating has severe consequences, among them a stain on the academic record and a lack of understanding about the relevant contents of the course. Do your own work please!

# Statement of Intention

This blog post is for reflection on multiple choice questions that I found to be particularly difficult. These include questions that I got wrong as well as questions that I found to be particularly difficult. I will not go over all of the questions to reduce vulnerabilities in the integrity system.

# Reflection

Here are a few of the questions that were of interest.

## 2020 Question 4: Floating Points

Floating point has nothing to do with overflow errors, but let's look up what they are since I don't know too much about them.

[Wikipedia](https://en.wikipedia.org/wiki/Floating-point_arithmetic)

Apparently sig figs are back. Last time I interacted with them was the beginning of this school year.

That actually makes sense based on what floating points are. It's essentially the way computers do scientific notations with a limited capacity for digits.


## 2020 Question 54: Insert vs Append

According to the [College Board Pseudocode Guide](https://apcentral.collegeboard.org/media/pdf/ap-computer-science-principles-exam-reference-sheet.pdf):

- INSERT(aList, i, value) will insert the **value** at index **i** in the **aList**. All values at that index and the right are moved one index to the right. *This operation does not overwrite elements**.
- APPEND(aList, value) will append the **value** to the end (right) of the **aList**.

## 2021 Question 48: Rogue Access Points

I've never heard of the term **rogue access point**. That's a bit embarrassing. Regardless, here's a primer from [Khan Academy](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:cyber-attacks/a/rogue-access-points-mitm-attacks).

I'll start by navigating to a term I'm more familiar with, which is called the **man in the middle attack**. In this attack, a malicious individual somehow gains access to the connection between the client (you) and the servers. The attackers can read and possibly modify any data sent between the client and the server. This is a big reason why encrypted connections are important (if a connection is encrypted, this increases the difficulty of data readability to third parties, including attackers). If a connection is unencrypted, attackers can read anything you send the servers - including sensitive information like passwords and payment info.

Now we go to the access points. I am more familiar with the **routers**, intermediary networking devices that receive network packets from the client and forward them to other routers in such a manner that the packets reach the server. I've seen lots of networking simulation software where the routers are connected to each other via wired connections, and in like manner to the clients. But as we know, wireless connections have become ubiquitous at this point. Khan Academy then introduces the less-familiar **access points**. These are what allow for wireless connections, and a lot of these are incorporated into networking devices (like routers).

With a **rogue access point**, the attacker manages to install his own access point. This is therefore a special type of man-in-the-middle attack where clients  must use infrastructure installed by the attacker to connect to the Internet, and data can be read and modified at any time. In the Khan Academy article, this showed up as a duplicate Wi-Fi network. In terms of College Board, this most resembles an option where the attacker hijacks a badly-protected router.
