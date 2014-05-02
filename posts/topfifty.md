---
layout: post
author: ethan
title: Top 50
---

This code has been based off of code found here: http://nltk.googlecode.com/svn/trunk/doc/book/ch01.html#fig-inaugural
Packages needed to run this program can be found here: http://matplotlib.org/

*Program Name:* Top 50

*Program Purpose:* The user wants to generate a graph that shows a distribution of the top 50 words in the selected text. 

*Code and Output*

First we want to establish a variable 
```
import nltk # this should be done once at the start of every session
fdist1 = FreqDist(text2)
fdist1
```
This will give you some output
```
<FreqDist with 6833 samples and 141576 outcomes>
```
Continue with this:
```
vocabulary1 = fdist1.keys()
vocabulary1[:50]
```
This gives you the output of the top 50 words in a text
```
[',', 'to', '.', 'the', 'of', 'and', 'her', 'a', 'I', 'in', 'was', 'it', '"', ';', 'she', 'be', 'that', 'for', 'not', 'as', 'you', 'with', 'had', 'his', 'he', "'", 'have', 'at', 'by', 'is', '."', 's', 'Elinor', 'on', 'all', 'him', 'so', 'but', 'which', 'could', 'Marianne', 'my', 'Mrs', 'from', 'would', 'very', 'no', 'their', 'them', '--']
```
After that output is produced, continue with this:
```
fdist1[‘have’]
```
This will produce some output as well. It tells you the exact number of times that the word “have” shows up in the text. 
```
807
```
Now to the good part, the distribution graph. Input this:
```
fdist1.plot(50, cumulative=True)
```
You will get a beautiful graph that looks something like this:  

![Distribution] (http://i.imgur.com/JLGVhQq.jpg)