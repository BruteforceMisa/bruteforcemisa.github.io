---
layout: post
title:  "Side-channels"
date:   2024-11-06 11:08:02 +0200
categories: hardware security side-channels 
---

Side channels are channels on which information is leaked through the physical properties of the device. One example of a side channel is power consumption. It is possible to measure the current through the CPU and link that to an instruction. Consequently, it is possible to deduct what the CPU is executing without direct access to the program. This attack is based on leaking information, rather than a mistake in the program or algorithm. It is possible to attack secure algorithms using side channels.

Other examples of side channels are optical emissions, timing delays and electromagnetic emanation. There are also non-technical side-channels, such as the sound of your keyboard when you are typing in your password, or the muscles in your hand when you are typing in your pincode when paying.

Side channels are only as interesting as the program being executed. One of the assumptions of a side- channel attack is that you have physical access to the device. On this basis, you are correlating the side-channel data to the program being executed to obtain sensitive information.

![image](/assets/images/sidechannel.png) 

<b>Keywords</b>
