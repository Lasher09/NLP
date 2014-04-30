---
layout: post
author: laura
title: Post
---


##Post 4:

__Program:__ GenderNames

__Purpose and description:__ A program that reads a list of names and will predict whether a name is a male or a female name. This program will also produce a graph to illustrate the frequency of names ending in certain letters and their predicted gender.
	
__Program capabilites:__
* Read two files
* Read the words in both files
* Output the names
* Plot: be able to compare the last letter and  output a plot that shows the results of names in by their last letters

	
__Code for GenderNames:__

```
import nltk
names = nltk.corpus.names
names.fileids()
male_names = names.words('male.txt')
female_names = names.words('female.txt')
[w for w in male_names if w in female_names]
	
cfd = nltk.ConditionalFreqDist((file, name[-1])
	for file in names.fileids()
	for name in names.words(file))
	cfd.plot()    		# see  a neat plot
```						

__Output:__
![Alt GenderMap](http://puu.sh/8rBAw.png)

Here you can see the frequeuncy of the last letter of a name and how often they occur in male or female names. This graph is showing that names that end in 'a' are usually female names. Pretty neat!
