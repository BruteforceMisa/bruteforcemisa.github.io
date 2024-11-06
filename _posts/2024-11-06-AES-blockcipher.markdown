---
layout: post
title:  "AES - Block Cipher"
date:   2024-11-06 12:27:02 +0200
categories: hardware security AES 
---

AES (Advanced Encryption Standard) is the national standard for encrypting data and is widely used. AES is what we call a blockcipher, which means that the data is encrypted per block. For example, AES-128 denotes that each plaintext is split into blocks of 128 bits and uses a 128-bit key for encryption.
Let’s have a look at the example below. Suppose we want to encrypt the plaintext “Hello world, how are you?”. For now, we will consider each character to be represented in 1 byte (= 8 bits). To correctly encrypt our plaintext, it will be split into the following sets:

[hello world, how are you?]
[hello world, how] + [ are you?]
The first block is exactly 16 bytes, but the second block is 7 bytes short. In AES, 7 bytes of padding will be added to match the block size. For now, we will denote padding as “p”. The schematic for encrypting looks as follows:
[hello world, how] + [ are you?ppppppp]

Each AES block has as input the plaintext and the key. The key is derived from the password chosen by the user. A schematic of AES encryption is shown below.

![image](/assets/images/AESBlockcipher.png) 

<b>Keywords</b>
