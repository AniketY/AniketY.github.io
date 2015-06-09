---
author: Saurabh
comments: true
date: 2014-10-20 10:26:00+00:00
excerpt: An Introduction to Cryptography and developing a very basic algorithm for
  the Caesar Cipher - A precursor to the Vigenère Square and ROT13 Encryption methods.
layout: post
slug: an-introduction-to-cryptography-the-caesar-cipher
title: An Introduction to Cryptography - The Caesar Cipher
wordpress_id: 127
categories:
- Cryptography
- Python
tags:
- Ciphers
- cryptography
- decryption
- encryption
- functions
- Juilus Caesar
- math
- python
---

An Introduction to Cryptography and developing a very basic algorithm for the Caesar Cipher - A precursor to the Vigenère Square and ROT13 Encryption methods.





<!-- more -->





## 0. Prerequisites





Basic knowledge of Python syntax and constructs.





## 1. Cryptography





Cryptography is the science of writing in secret code. It comprises of Encryption (that is, changing data so that it is unrecognisable and useless to an unauthorised person) and Decryption (that is, changing it back to its original form.)





[![crypto](https://Aniket.files.wordpress.com/2014/10/crypto.gif?w=300)](https://Aniket.files.wordpress.com/2014/10/crypto.gif)





(source:http://www.cryptographyworld.com/ )





## 2. The need for Cryptography





<blockquote>

> 
> _ For thousands of years kings, queens and generals have relied on efficient communication in order to govern their countries and command their armies. At the same time, they have all been aware of the consequences of their messages falling into the wrong hands, revealing precious secrets to rival nations and betraying vital information to opposing forces._
> 
> 

> 
> _It was the threat of enemy interception motivated the development of codes and ciphers: techniques for disguising a message so that only the intended recipient can read it._"
> 
> 

> 
> Simon Singh
> 
> 

> 
> "The Code Book
> 
> 
</blockquote>





These few lines accurately sum up the necessity of codes and ciphers.





In modern context, the ability to protect and secure information is vital to the growth of electronic commerce and to the growth of the Internet itself. Many people need or want to use communications and data security in different areas.






    
  * Banks use encryption methods all around the world to process financial transactions. These involve transfer of huge amount of money from one bank to another.

    
  * The average internet user relies on cryptography not only to protect his passwords and other private data but also to verify his identity ( The RSA Encryption ).

    
  * Multinational firms may use it to protect their trade secrets.





## 3. Types of Cryptography





There are mainly three ways of encryption (that is scrambling up a message so that it may only be read by its intended recipient) :





[![crypto_types](https://Aniket.files.wordpress.com/2014/10/crypto_types.gif?w=300)](https://Aniket.files.wordpress.com/2014/10/crypto_types.gif)(source: http://www.garykessler.net/library/crypto.htm)





## 4. The Caesar Cipher





Caesar Cipher is a simple case of the Symmetric Key Cryptography. It is a substitution cipher(that is, each letter is replaced by another letter or symbol) named after Julius Caesar.





Although easily crackable with modern technology, it is still used in the form of ROT13 ( a caesar shift of 13 places ) in certain forums to hide offensive text or answers to a quiz.





Each letter in the plaintext message is replaced by the letter k places along in the alphabet (where k is between 0 and 25 inclusive) wrapping around to the beginning of the alphabet if necessary.





If k be 3, then A is replaced by D, B is replaced by E, C is replaced by F and so on.





[![caesar-cipher](https://Aniket.files.wordpress.com/2014/10/caesar-cipher.png?w=300)](https://Aniket.files.wordpress.com/2014/10/caesar-cipher.png)





The Caesar Cipher using a shift of k=3.





To decrypt (or, decode) such a coded message, each letter is replaced by the letter k places before it in the alphabet, wrapping around to the end if necessary.





That is, for our example of wrapping around to thek=3, A is replaced by X, B is replaced by Y, C is replaced by Z, D is replaced by A and so on.





## 5. A Math Primer





Because cryptography is basically an application of math and, ( more recently ) programming, there are certain mathematical concepts that I would like you to be familiar with ( Don't worry - it won't be like a boring math class and I'll keep it as simple as possible )





5.1 The Modulo Operator





In Python, the '%' is the modulo operator. It finds the remainder of division of one number by another. For example, 9 % 5 means, divide 10 by 5 and return the remainder of the division ( as opposed to the '/' which returns the quotient of the division ). So 9 % 5 will be 4.





Go ahead and try this out in the python interpreter ( simply type 9%5 and press enter )





Remember I said we'll have to wrap around the alphabet ? The modulo operator can be used for just that ( the value of a%b will always be less than b )





5.2 ASCII Values





Not exactly math but the American Standard Code for Information Exchange encodes 128 characters into 7-bit integers.





The ASCII Table [http://ascii.cl/](http://ascii.cl/)





5.3 Functions





A function simply relates an input to an output.





Each function has three main parts:





1.The Input





2.The Relationship





3.The Output





[![Screenshot from 2014-10-20 14:15:28](https://Aniket.files.wordpress.com/2014/10/screenshot-from-2014-10-20-141528.png?w=300)](https://Aniket.files.wordpress.com/2014/10/screenshot-from-2014-10-20-141528.png)





(source: [http://www.mathsisfun.com/sets/function.html](http://www.mathsisfun.com/sets/function.html))





If we write it a bit more formally, the function will be




    
    f(x) = x*2
    





In programming, functions are "self-contained" modules of instructions that accomplish a specific task. Functions usually "take in" data, process it, and "return" a result.





Python has many functions in its standard library ( that is, they are built-in ). So, for time being, we don't need to care about how the relationship is established ( or, how a task is done ). For example if we want to get the user's name, we'll use the raw_input function -




    
    name = raw_input('What is your name? ')



You may try this out in the python interpreter.



name is a variable that stores the return value or output of the raw_input function





'What is your name? ' is a string that is displayed on the screen to prompt the user. It is a parameter or the input to the function.





Some more useful functions are as follows :






    
  * ord(c) : returns the ASCII value of a character c ( that is, a string of length one in python like 'a' and 'b' )





[https://docs.python.org/2/library/functions.html#ord](https://docs.python.org/2/library/functions.html#ord)






    
  * chr(i) : returns the character corresponding to the ASCII value





[https://docs.python.org/2/library/functions.html#chr](https://docs.python.org/2/library/functions.html#chr)






    
  * int(s) : returns an integer constructed from the string/int/float value s





[https://docs.python.org/2/library/functions.html#int](https://docs.python.org/2/library/functions.html#int)






    
  * range(start,stop[,step]) : returns a list of integers from start to stop-1 at a gap of step. Only stop is mandatory, rest are optional. For example,




    
    range(5)
    





will return




    
    [0, 1, 2, 3, 4]
    





[https://docs.python.org/2/library/functions.html#range](https://docs.python.org/2/library/functions.html#range)





## 6. A To-Do list





When you get down to it, programming is all about algorithms. That's a big fancy word for 'a list of instructions.' Every program is simply a big to-do list of instructions for the computer to follow. So, we'll first try to write down the steps involved in encrypting a single uppercase letter with the caesar cipher.






    
  * Let the letter be 'plain_letter', its ASCII value be 'asc_letter', and the shift be 'k'

    
  *  Calculate its position in the alphabet ( A=0, B=1, C=2 and so on )

    
    pos_letter = asc_letter – ASCII_Value_of_A
    




    
  * Shift it by k places wrapping around the alphabet.

    
    shifted_position_of_letter = ( pos_letter + k ) % 26
    




    
  * Get the ASCII value from the shifted position value and then get the ciphered character corresponding to the ASCII value

    
    asc_ciphered_letter = shifted_position_of_letter + ASCII_Value_of_A
    




 For example, let's shift 'C' by 5 places




    
    * ASCII Value of C = 67

    
    * ASCII Value of A = 65

    
    * Position of C = 67- 65 = 2

    
    * Shifted position of C = (2+5) %26 = 7%26 = 7

    
    * ASCII Value of Shifted C = 7 + 65 = 72

    
    * Character corresponding to ASCII Code (72) = 'H'








**C** D E F G **H**





Hence, C has been shifted 5 places.





## 7. Implementation in python





You may now fire up your interpreter and use the functions to implement the algorithm on your own. A more detailed implementation and cracking the Caesar Cipher will be in the next post.
