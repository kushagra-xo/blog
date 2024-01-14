+++
title = 'Gentoo Goes Binary'
date = 2024-01-14T11:36:32+05:30
+++

![gentoo-logo](https://www.phoronix.net/image.php?id=2023&image=gentoo) 

## The state of current GNU/Linux distributions

- Almost all modern GNU/Linux distributions rely on the model of binary package distribution, or i.e. they make packages for you, so you don't have to, namely Debian, Ubuntu, ArchLinux and many others. That has it's advantages and disadvantages that we shall discuss further.

![waiter](https://images.unsplash.com/photo-1516788875874-c5912cae7b43?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8d2FpdGVyJTIwc2VydmluZ3xlbnwwfHwwfHx8MA%3D%3D) 

## Source based distributions

- Apart from the normal way, some distributions don't make packages for you, i.e. you shall compile them yourself, kinda like DIY
- They provide you with the necessary information about where to retrieve the source-code and how to compile it. With package managers such as `emerge`(for gentoo), it is a breeze leaving that fact that it takes a tad bit of more time heavily depending on your hardware.

![tools](https://images.unsplash.com/photo-1540103711724-ebf833bde8d1?q=80&w=1752&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D) 

## Why should I care?
- Well, for the most part you shouldn't, in most packages it does not matter, but in some larger applications compiling from source on hardware itself can provide noticeable performance benefits. It is also about just general control over what you compile your software with, and to ignore compiling the features that you do not need stripping the software you run to the bare minimum.

## Opinion?
- Gentoo's recent decision about going primarily binary in my opinion is a progressive change and for the good, keeping in the mind the users that do not particularly powerful hardware, while also not forgetting it's roots and the use cases of source-based distribution of packages. This allows for workflows that merge and blend binary and source based packages making a more flexible user-experience.

### References:
- https://www.gentoo.org/news/2023/12/29/Gentoo-binary.html
