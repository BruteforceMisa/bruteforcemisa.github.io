---
layout: post
title:  "AES - Inner workings"
date:   2024-11-06 12:29:02 +0200
categories: hardware security AES  
---

In this post, we are going to zoom in on the inner workings of one AES block. AES operates in rounds, which are usually 10, 12 or 14 rounds (matching with AES-128, AES-192 and AES-256). <!--more--> The output of each round is xor’ed with a subkey, which is derived from the main key using the key scheduler. How the key scheduler exactly works, is out of the scope for this blog.
AES consists of four main operations: AddRoundKey, SubBytes, ShiftRows & MixColumns. These functions are repeated for the number of rounds. A visualisation of these functions is shown below.

![image](/assets/images/AESinners.png) 

AddRoundKey is the function where the subkey is added to our data. SubBytes is a function where each byte of our data is mapped to another value. ShiftRows and Mixcolumns are functions where our data is represented as a 4x4 byte matrix and shuffled toadd dependencies within the encryption for security. In the next post, we will zoom in on the SubBytes function


<b>Keywords</b>
