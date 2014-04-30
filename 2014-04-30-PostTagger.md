---
layout: post
author: laura
title: Post
---

##Post 3:

__Program:__ PostTagger
__Purpose and description:__ A simple program that will parse sentences and show the parts of speech.
	
__Program capabilites:__
* Have a variable that holds any sentence the user inputs
* Tokenize the sentence
* Attach parts of speech to each word in the sentence
* Output the grammatically parsed sentence

__Code for WebpageFrequency:__

```

import nltk
text = nltk.word_tokenize("And now for something completely different")
print nltk.pos_tag(text)

```						

__Output:__

```

[('And', 'CC'), ('now', 'RB'), ('for', 'IN'), ('something', 'NN'), ('completely', 'RB'), ('different', 'JJ')]

```

_Note: 
* CC = coordinating conjunction
* RB = adverb
* IN = preposition/subordinating conjunction
* NN = noun
* JJ = adjective
* These tags and others can be found <a href="http://www.monlp.com/2011/11/08/part-of-speech-tags/"> here </a>._
