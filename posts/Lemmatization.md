---
layout: post
author: jacobthill
title: Lemmatizing a Text
---

*Program:* Text Lemmatizing

*Purpose and Description:* Lemmatization is the process of grouping the various inflections of a given word for the purpose of analysis. In english, it most often involves removing the affixes from the word. For example, if you want to determine the frequency words from the same root as 'apply', you would need to idenify words such as 'application', 'applied'. 'applies', etc. This nltk function will help with this process.

*Program Capabilities:* Becuase English grammar rules are often inconsistent, it can be difficult to write a program that works on all cases. The lemmatization funtion in nltk deals with this by listing each word along with its inflections in a dictionary. Consequently, the function will only lemmatize words found in its dictionary.

*Code:* 
```
import nltk # this should be done once at the start of every session

raw = open('document.txt').read() # opens, reads content of 'document.txt' and stores in variable 'raw'

tokens = nltk.word_tokenize(raw) # stores the tokenize method in 'tokens' variable

wnl = nltk.WordNetLemmatizer()  # stores the WordNetLemmatizer method in 'wnl' variable
[wnl.lemmatize(t) for t in tokens] # calls lemmatizer method  for t in 'tokens' variable
```

*Output:* Output will vary depending on the ocntent of the 'document.txt' file. 