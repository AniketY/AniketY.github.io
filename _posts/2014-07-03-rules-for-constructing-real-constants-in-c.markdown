---
author: Aniket
comments: true
date: 2014-07-03 10:15:02+00:00
layout: post
slug: rules-for-constructing-real-constants-in-c
title: Rules for constructing real constants in C
wordpress_id: 58
categories:
- Let us C !
tags:
- constructing real constants
- exponent
- Exponential form
- fraction form
- mentissa
---

Real constants are also known as floating point constants. Real constants can be expressed in two forms Fraction and Exponential form.

**Rules for constructing real constants in Fractional form:**





  1. It Must have at least one digit. 


  2. It must have a decimal point. 


  3. It could be either positive or negative. 


  4. If no sign is added, then default sign is positive. 


  5. No commas or blanks are allowed in real constants 



For example: +56.5554, - 56.455, - 7, 5655.5557

**Meaning of MANTISSA and EXPONENT **

Before moving on to Exponential form one should understand the meaning of MANTISA and EXPONENT. 
Exponent form is generally used when value of constant is either to small like - 0.00000058 or very large such as +5684455544555.
Now let us understand this with the help of an example : 
1. Take a very small or large number (In my case it is. 0.00000058 ) 
2. We can convert it into 5.8 * 10 ^-7. 
3. If we convert it into Exponential form then it can be written as 5.8e-7.
4. In Exponential form real constant is represented into two parts, part before 'e' is called MANTISSA and part after 'e' is called EXPONENT.

**Rules for constructing a real constant expressed in Exponential form :**





  1. The MANTISSA part am doing the EXPONENT part is separated by a letter 'e' or 'E'. 


  2. The MANTISSA part may be positive or negative 


  3. Default sign of MANTISSA is positive. 


  4. Range of real constants expressed in Exponential form is - 3.4e38 to +3.4e38.



For example : +3.2e25, - 7E56
