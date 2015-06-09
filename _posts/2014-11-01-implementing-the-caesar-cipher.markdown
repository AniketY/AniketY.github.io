---
author: Saurabh
comments: true
date: 2014-11-01 17:17:07+00:00
layout: post
slug: implementing-the-caesar-cipher
title: Implementing the Caesar Cipher
wordpress_id: 164
categories:
- Python
tags:
- caesar-cipher
- Ciphers
- encryption
- for loop
- functions
- python
- rot13
---

Implementing the caesar cipher in python and in turn, the ROT13 cipher.





<!-- more -->





**0. Prerequisites**





Caesar Cipher





Basic Python





**1. A Recap**





In the last post we devloped a method to encipher a single character with the caesar cipher. Now we'll implement a full program that enciphers a whole block of text.





Remember functions from the last post ? This time we'll create our own function. So lets get started.





**2. The def keyword**





In python, function are defined using the def keyword.





{% highlight ruby %}

def <func-name> (<params>) :
  <body-of-function>
  [return <value>]
{% endhighlight  %}
    






for example if we want to define a function add that takes two values and returns their sum the we would say




    
 {% highlight ruby %}

def add(a,b):
  c = a+b
  return c
print 'sum of 1 and 2 is ' + sum(1,2)
{% endhighlight  %}





This will print sum of 1 and 2 is 3





Note how change in indentation(spaces, that is) is used to denote the start and end of the function. You can indent with any number of space or tabs but you should be consistent with it. **Never** mix tabs and spaces.





**3. Making modules**





Most of the work we did was on the python interpreter. While it is really useful to test new features, it has a serious drawback : If you quit from the Python interpreter and enter it again, the definitions you have made (functions and variables) are lost. That is terribly inconvenient. So python provides a way for you to store the definitions and commands in a file and load that file when required. Such a file is called a script or a Python Module.





Now you can reuse your code !





To make a module simple open up your favourite code-editor ( not a text-editor like notepad but like sublime-text or emacs ) , type your commands and save it as file with suffix .py.



You can now execute it in the terminal as many times as you like.



**4. The first function**





Now, simply type all the code from the last post to a function named encipher(c, shift)





Your file should look something like this :




    
  {% highlight ruby %}
def encipher(letter,shift):
  letter = letter.upper() # just to make sure the letter is uppercase
  ascii_letter = ord(letter)
  ascii_A = ord('A')
  pos_letter = ascii_letter - ascii_A
  shifted_pos_letter = ( pos_letter + shift )%26
  asc_ciphered_letter = shifted_pos_letter + ascii_A
  return chr(asc_ciphered_letter)

{% endhighlight  %}




Go ahead and save the file in your home directory ( or, [C:\python27](/python27) for windows users) as cipher.py.





Now open a terminal and type




    
    {% highlight ruby %}

>>> import cipher
>>> cipher.encipher('A',2)
{% endhighlight  %}




In the next line you will get




    
   {% highlight ruby %}
'C'


{% endhighlight  %}
    





To get back your original text you will have to shift back


    





That is




    
   {% highlight ruby %}
>>> cipher.encipher('C',-2)
'A'

{% endhighlight  %}





Here, in the first line you are loading the file into the interpreter and in the second, you are calling the function named encipher from the module cipher with parameters 'A' and 2. That is, 'A' will be shifted by 2 places.





**5. Enciphering a block of text**





So we can encrypt and decrypt single characters but what if we have to encrypt a whole block of text or a sentences. To avoid writing all the calls to the function or to repeat anything python provides the _**for loop**_ which simply means repeat a particular task certain number of times. Basically this




    
   {% highlight ruby %}
for i in range(100):
  print 'I will follow the rules.'

{% endhighlight  %}




instead of this





[![images](https://saurabhmathur96.files.wordpress.com/2014/11/images.jpeg)](https://saurabhmathur96.files.wordpress.com/2014/11/images.jpeg)





So this is what our second function looks like now




    
    {% highlight ruby %}
def encipher_text(text,shift):
  ciphertext = ''
  for c in text:
    ciphertext += encipher(c,shift)
  return ciphertext

{% endhighlight  %}





It calls the encipher function for **each **of the characters of text. But not all characters are letters of the alphabet. They may be white-space like a tab or a space or the may be special characters or numbers. We don't want to shift them. So we'll check each character if it belongs to the alphabet before calling the encipher function




    
   {% highlight ruby %}
def encipher_text(text,shift):
  ciphertext = ''
  for c in text:
      if c.isalpha():
          ciphertext += encipher(c,shift)
      else :
          ciphertext += c
  return ciphertext

{% endhighlight  %}
    





Now just like in section 4 you can try to encipher a sentence or a block of text.




   {% highlight ruby %}

>>> cipher.encipher_text("This is how you encrypt a sentence.",10)
'DRSC SC RYG IYE OXMBIZD K COXDOXMO.'
{% endhighlight  %}





**6. ROT13**





ROT13 is a special case of the caesar shift. As the name implies it shifts the text by 13 places so if we encrypt it again we get the original text.





This type of encryption is used in online forums as a means of hiding spoilers, punchlines, puzzle solutions, and offensive materials from the casual glance. It has been described as the "Usenet equivalent of a magazine printing the answer to a quiz upside down".





We can write rot13 as a special case of out encipher_text function




    
   {% highlight ruby %}
def rot13(text):
    return encipher_text(text,13)

{% endhighlight  %}





**7. The code**





[View the whole code(Hosted by github)](https://gist.github.com/saurabhmathur96/75bdcfa08edeb9b7336a)
