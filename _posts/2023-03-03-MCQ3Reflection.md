---
toc: true
layout: post
description: Includes Important Notes about missed questions and other misconceptions
categories: [markdown, Comp Sci]
title: Final Exam 2 Reflection
permalink: /notes/MCQ3reflection
comments: true
---

# Integrity Disclaimer

The author does not permit copying of any of the reflections contained within this post. Cheating has severe consequences, among them a stain on the academic record and a lack of understanding about the relevant contents of the course. Do your own work please!

# Statement of Intention

This blog post is for reflection on multiple choice questions that I found to be particularly difficult. These include questions that I got wrong as well as questions where I utilized a search engine. Mr. Yeung has permitted use of search engines orally on the condition that students are transparent about their methods. Unlike previous posts where I have used a tabular format, I will format each question with a subheading to give me more space to write longer reflections.


##### Question 2: Which has the greatest potential for compromising user privacy?

This question is difficult in that all options presented represent significant threats to privacy.

A) [Cookies stored by Web Browsers](https://support.mozilla.org/en-US/kb/cookies-information-websites-store-on-your-computer#:~:text=This%20allows%20you%20to%20stay,address%2C%20or%20telephone%20number).)

According to this article on Internet cookies by Mozilla (developers of FIrefox), cookies have information relevant to websites a user visits. They may store PID (phone numbers, emails, etc.) if the user entered this information into a website. This could reasonably happen if the user entered information into an online form (ex: applying for membership within a certain group, or even something as simple as sharing contact information with other members of a team). Here are some potential ways this could be a threat to privacy:
- An attacker compromises a user's computer system. After establishing control, the attacker goes to the web browser files where the cookies are cached. The attacker extracts information about the user and uses it for his/her ends.
- As part of a phishing scam, an attacker sets up a fake website that is a convincing mock-up of a legitimate corporate website. The user enters information as is expected. The catch is that the information is actually extracted using Internet cookies. This is known as [session hijacking](https://www.mcafee.com/blogs/privacy-identity-protection/what-are-browser-cookies-and-how-do-i-manage-them/).

B) The IP address of the user's computer

This question is quite vague in my opinion, because it fails to specify if it's talking about the private IP address (which is often somewhere in the 192.168.0.0 to 192.168.0.255 range) or the public IP address (which is used to communicate with other machines). When I've learned about cybersecurity, I've heard that public IPs should be kept a secret at all costs, so I took a look around and found [this stack exchange](https://security.stackexchange.com/questions/35160/is-publishing-your-public-ip-address-a-security-threat), where someone from a large corporation encountered something similar. The accepted answer said that if attackers knew which IP addresses were being used, then they could conduct reconnaissance of their targets without an obvious trail. If the attackers aim to do a data breach, this could be a significant threat to privacy.

C) User email addresses

The email address is somewhat a piece of identifiable information, though if anyone is running their own website or applying for a job with a resume and the like, it's probably already out there. There are a few ways malicious individuals can use this information to gain private information:
- Phishing/social engineering emails (as I've said before)
- The attacker may try to crack the password to the email. Many users use insecure passwords, and if that fails, there's always the security questions used to reset the passwords (with attackers hoping that the users put in true information so a search engine would suffice for information gathering). After the email account is compromised, attackers will have access to private correspondence.

D) Public keys for encryption

This one is difficult because it is not specified if symmetric encryption or asymmetric encryption is used. If the secret key for symmetric encryption is obtained by attackers, the connection is essentially compromised. Attackers can use software to monitor the connection (and extract any data sent over the connection, such as passwords and credit card numbers). They may also be able to get into the connection as part of a man-in-the-middle attack. However, if this is asymmetric, there is no cause for worry since [the *private* key is required to decrypt the connection](https://www.google.com/search?surl=1&q=assymetric+encryption+public+key&rlz=1CADTIH_enUS1045&oq=assymetric+encryption+public+key&aqs=chrome..69i57.4263j0j7&sourceid=chrome&ie=UTF-8&safe=active&ssui=on). Given my Google search called asymmetric cryptogrpahy "Public-Key Cryptography," I think this is relatively safe.


Before I move on, I'll say that the [habit of corporations to harvest and sell data](https://itchronicles.com/big-data/how-do-big-companies-collect-customer-data/) is another privacy concern. I believe that cookies are most closely associated with privacy issues.


8) What are true about digital certificates for web browsers?

I probably should have paid more attention to the question. When I started looking stuff up I was somewhat surprised to be greeted by stuff I (should) already know.

i) Verify ownership of encrypted keys

This one's a no-brainer. I helped with a certain deployment process, and yeah there was the whole HTTPS certification part for the website. To top it off, here's the [Britannica article](https://www.britannica.com/topic/digital-certificate) about this topic.

2) Ensure fault tolerance of a network connection

Apparently I forgot what fault tolerance was. According to [this article](https://www.imperva.com/learn/availability/fault-tolerance/) I found, it's the ability of a network to remain up despite certain problems (because keeping downtime to the absolute minimum is basically essential in today's environment). To give a bit more context, let's talk about HSRP (Hot Standby Routing Protocol)

![]({{site.baseurl}}/images/cisco-hsrp.jpg "Image taken from https://www.networkstraining.com/cisco-router-hsrp-configuration/")

Now, this is a network with routers and switches. This might be a bit unfamiliar to some, but I'll say a few basic things here. All the Internet traffic to the computers at the bottom of the network is usually routed through **Router1** (that's how to access Internet, and this is denoted by the label **active**). Now, it is possible that **Router1** is unexpectedly powered off, or perhaps there is a system maintenance. If this should happen, all the traffic will be routed through **Router2** instead (as indicated by the **standby** label). This is a demonstration of fault tolerance.

Now, take a scenario like this and apply this to a corporation that needs to keep its website running at all times. There must be configurations like this so that all of the web servers (hosting the website) may still be online in case a device (like a router) should go down unexpectedly or due to maintenance.



I could go on and on about this, but the key thing here is to notice that I didn't say anything about encrypting the connection between the client and the server or anything about digital certificates. Because that's not what fault tolerance is about. Fault tolerance is about keeping the network running at all times.


13) In which situation would it be better to use creative commons licenses over copyright for an e-book?

i) Make the e-book freely downloadable
ii) Prevent people from sharing copies of the book on P2P networks
iii) Allow people to use and modify the book

The interesting part about creative commons is that [there are multiple licenses](https://creativecommons.org/licenses/). There is a general theme of the following

- Others may distribute and build upon the work
- Users must give credit to original author
- Some licenses may restrict to non-commercial purposes
- Some licenses require remakes/modified works to keep the same license
- One license prohibits modified works entirely; one license prohibits distribution of modified works

