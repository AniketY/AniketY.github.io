---
author: Aniket
comments: true
date: 2014-06-29 14:46:29+00:00
layout: post
slug: rules-for-constructing-integer-constants-in-c
title: Rules for constructing Integer constants in C
wordpress_id: 54
categories:
- Let us C !
tags:
- Aniket
- compiler rule
- Integer
- LET US C
- rules to use integer in C
---

1. An integer constant must have at least one digit.  

2. It must not be in decimal form.  

3. It can be either negative or positive.  

4. If there is no sign in prefix, then it assumed as positive.  

5. No commas, special symbols, alphabets, or blanks are allowed in an integer constants.  

6. The allowable range for integer constants is –2147483648 to +2147483648. 

NOTE: frankly speaking integer constants depends upon compiler. For visual studio, gcc, it is as mentioned above but for compilers like Turbo C its range varies from - 32768 to +32768.
