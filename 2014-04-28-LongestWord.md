---
layout: post
author: laura
title: Post
---

---------------------
##Post 1:

__Program:__ LongestWord
__Purpose and description the program:__ This program will find the longest word in the given text:  Milton's Paradise Lost.
	
__Program capabilites:__
* Read the given file
* Calculate the average word length in a given text
* Output the longest word/s
	
__Code for LongestWord:__

```

import nltk
text = nltk.corpus.gutenberg.words('milton-paradise.txt')					
longest = ' '				
for word in text:				
    if len(word) > len(longest):
	longest = word			
								
print longest

```						

__Output:__

```

unextinguishable

```

