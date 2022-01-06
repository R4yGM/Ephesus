---
layout: post
title:  "TryHackMe Pre-Security : the introduction to cybersecurity"
author: R4yan
permalink: /2021-07-11-tryhackme-pre-security-the-introduction-to-cybersecurity/
date: 2020-07-11 13:03:36 +0530
tags: [CTF Guide Reviews]
categories: Genel
---


But first of all what is TryHackMe? well, [TryHackMe](https://tryhackme.com) is a platform that delivers cyber-security training through gamified real-world labs.

don’t concern yourself if you’re a complete beginer on the field or you think that this stuff is too much hard for you because TryHackMe has you covered, it has a ton of **walktroughts** and **challanges** that make you struggle and learn, and they even teach you a wide variety of things, it has over **193** rooms where most of them are completely free!

![](https://miro.medium.com/max/1024/1*LIDqxzIPCiqbK-G9aayx_A.png)

**Now what is the Pre-Security path?**
======================================

As i said before THM has  walktroughts and challanges but it also have **Paths** that are basically a pack of walktroughts with a similiar topic.

The [**Pre-Security**](https://tryhackme.com/path/outline/presecurity) is a path that teaches you the foundamentals to get started on cyber security, that gives you the technical knowledge to learn more difficult topics.

this path contains 4 main topics that i’m going to discuss later which are :

*   **Network Fundamentals**
*   **How The Web Works**
*   **Linux Fundamentals**
*   **Windows Fundamentals**

and also a short room that simply explains the basics and concepts of cyber security.


![](https://i.imgur.com/ixzahMG.png)

the topics

**Cyber Security Introduction**
-------------------------------

this rooms explains why knowing how a website works is important and a few techniques all guided with instructions, and in the end it also explains why learning networking is important showing the danger that can cause ff the network hasn’t been properly segmented

**Network Fundamentals**
------------------------

This category contains 5 rooms all explaining some concepts of how computers communicate with each other which are :

*   **What is Networking?**
*   **Intro to LAN**
*   **OSI Model**
*   **Packet and Frames**
*   **Extending your network**

[**What is Networking?**](https://tryhackme.com/room/whatisnetworking)
----------------------------------------------------------------------

here you can learn the fundamentals of computer networking and how they are used nearly everywhere, it also explains **IP Addresses**, **MAC Addresses** and **ICMP** packets.

[Intro to LAN](https://tryhackme.com/room/introtolan)
-----------------------------------------------------

this room teaches you about some of the technologies and designs that power private networks which are :

1.  Types of LAN
2.  Subnetting
3.  ARP
4.  DHCP

[OSI Model](https://tryhackme.com/room/osimodelzi)
--------------------------------------------------

this room will teach you about the fundamental networking framework that determines the various stages in which data is handled across a network, it teaches you :

1.  What is a OSI Model
2.  The 7 different layers
3.  How it works!

[Packets and Frames](https://tryhackme.com/room/packetsframes)
--------------------------------------------------------------

This room explains how information is sent across a network from one device from another. It does this using both TCP and UDP protocols and in the end it introduces the operations of each protocol and how connections are made.

1.  **What are packets and frames**
2.  **TCP protocol**
3.  **UDP protocol**
4.  **Handshake**
5.  **Ports 101**

[Extending your network](https://tryhackme.com/room/extendingyournetwork)
-------------------------------------------------------------------------

This is the last module of the network fundamentals, explains various ways and techniques which are used to extend and secure networks, such as port forwarding, firewalls, and VPNs.

Overview :

1.  **Port Forwarding**
2.  **Firewalls**
3.  **Practical firewall**
4.  **VPNs**
5.  **LAN devices**
6.  **Simulating a network**

How The Web Works
-----------------

This category contains 4 rooms explaining some concepts and understanding of the underlying functions of the world wide web and what makes it work. which are :

*   **DNS in detail**
*   **HTTP in detail**
*   **How websites work**
*   **Putting it all together**

[**DNS in detail**](https://tryhackme.com/room/dnsindetail)
-----------------------------------------------------------

this room teaches you how DNS works and how it helps you access internet services.

1.  Introduction to the DNS
2.  Record types
3.  Domain hierarchy
4.  Making a request to the DNS
5.  Pratical

[HTTP in detail](https://tryhackme.com/room/httpindetail)
---------------------------------------------------------

provides an overview of the HTTP protocol and how to request content to a web server. It also goes through HTTP methods, status codes and a lot more.

Overview :

1.  What is HTTP and the difference from HTTPS
2.  Requests
3.  Methods
4.  Status codes
5.  Headers and Cookies
6.  How to make a request

[**How websites work**](https://tryhackme.com/room/howwebsiteswork)
-------------------------------------------------------------------

This room essencially teaches how websites works and how you can you attack an interactive website using JavaScript with code injection.

Overview :

1.  How websites works
2.  HTML
3.  JavaScript
4.  Sensitive data exposure
5.  HTML Injection

[**Putting it all together**](https://tryhackme.com/room/puttingitalltogether)
------------------------------------------------------------------------------

This is the last room of the category that basically let’s you combine the knowledge you learned on the previous rooms by explaining the process of how requests are made to web servers through DNS servers, WAF, and load balancers.

**Linux Fundamentals**
----------------------

![](https://i.imgur.com/bSaOOPT.png)


This category is extremely useful if you want to learn further cyber security and you are a complete novice to it, it covers all the basics of linux and a lot of useful commands, it contains 3 rooms all teaching different stuff

*   **Linux Fundamentals part 1**
*   **Linux Fundamentals part 2**
*   **Linux Fundamentals part 3**

[**Linux Fundamentals part 1**](https://tryhackme.com/room/linuxfundamentalspart1)
----------------------------------------------------------------------------------

this room introduces the Linux operating system with some interestic facts about it, Firstly it provides a bit of background and history on Linux before getting you to interact with an in-browser virtual linux machine

you will learn basic commands like `echo` to print strings, how to interact with the file system using `ls`,`pwd`and `cd` , It also shows how to search for files using the `find` command and how to filter the contents of files using `grep`

and in the end you will also learn about shell operators and how you can use them to simplify some tasks

Overview :

1.  **Linux background**
2.  **Deploying and interacting with your Linux machine**
3.  **Running basic commands**
4.  **Interacting with the file system**
5.  **Searching and filtring the content of files**
6.  **Shell operators**

[**Linux Fundamentals part 2**](https://tryhackme.com/room/linuxfundamentalspart2)
----------------------------------------------------------------------------------

this room is basically the continue of the previous linux rooms it introduces **SSH** and the conncetion between other linux devices, it takes a deep dive into flags and switches for various commands. It also covers how to interact with the file system using the `touch` , `mkdir` , `cp` , `mv` , `rm` , and `file` commands

also this room explains the common directories on a Linux file system like `/etc` , `/var` , `/tmp` and `/root`, and in the end the basics of permissions.

Overview :

1.  Connecting to the machine using **SSH**
2.  Introduction to flags and switches
3.  File system interaction
4.  Permissions
5.  Common directories

[**Linux Fundamentals part 3**](https://tryhackme.com/room/linuxfundamentalspart3)
----------------------------------------------------------------------------------

The final part in this category explains how to use some common terminal text editors like `vim` and `nano` to create and edit files. It also shows how to view running processes using commands like `ps` , it also explains how to use `wget` which is useful for downloading files across the internet, and also how to use the package manager `apt` to install programs and tools and in the end it also show where some common logs files are stored

Overview :

1.  **Terminal editors**
2.  **Utilities**
3.  **Processes**
4.  **System automation**
5.  **package manager**
6.  **File logs**

**Windows fundamentals**
------------------------

![](https://i.imgur.com/LzzJrmx.png)

This category is similar to the **Linux Fundamentals**,  this section takes a deep dive into the Windows operating system and provides you with a great foundation which will help you in identifying, exploiting and defending Windows systems, it has 2 rooms :

*   **Windows fundamentals 1**
*   **Windows fundamentals 2**

[**Windows fundamentals 1**](https://tryhackme.com/room/windowsfundamentals1xbx)
--------------------------------------------------------------------------------

This room is nearly a complete introduction for the Windows operating system. In particular, it gives an overview of the Windows file system, user accounts and permissions, and how to effectively use the Task Manager and Control Panel to manage your system and in the end they even show some special folders

1.  **Windows editions**
2.  **GUI**
3.  **File system**
4.  **windows\\system32 folder**
5.  **User accounts , Profiles and Permissions**
6.  **User account control**
7.  **Settings and control panel**
8.  **Task manager**

[**Windows fundamentals 2**](https://tryhackme.com/room/windowsfundamentals2x0x)
--------------------------------------------------------------------------------

In the last room of the Windows Fundamentals module you will discover more about System Configuration, UAC Settings, Resource Monitoring, the Windows Registry and more..

1.  **System configurations**
2.  **UAC settings**
3.  **Computer management**
4.  **System information**
5.  **Resource monitor**
6.  **Command prompt**
7.  **Registry editor**

Review
======

In my opinion, [TryHackMe](https://tryhackme.com) is a great way to get started and expand your knowledge on cybersecurity, i personally just found out about this platform nearly a year ago and then i got seriously interested, i begun spending most of the days doing walktrought and challanges which was very fun, i’ld say this platform is great because it let’s you learn in a gamified way wich is more enjoyable than studying

I found this Pre-Security path interesting to fulfill some holes or features that i forgot, but in my opinion to be honest this path is perfect and complete for a beginner, it nearly covers all of the fundamentals necessary to get better on the field, i would recommend it to a friend or anyone that started getting into the field

Conclusion
==========

And yeah that is Pre-Security path, I hope you enjoyed this blog post and found it useful.

also if you want to register on tryhackme and earn some more special rewards you can signup [here](https://tryhackme.com/signup?referrer=9e5fdb48bae5555e1d90574068b96c0349621a98) using my referral :)

![](https://i.imgur.com/N7wEjaY.png)
