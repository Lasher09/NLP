---
layout: post
author: laura
title: Post
---

##Post 5:

__Program:__ UnusualWords

__Purpose and description:__ This program  can read a text for the most unusual words in a text. This is great for judging the reading level of a text.

__Program capabilites:__
* Read all the lowercase words in a text
* Compare the words in this text to the words in another text file holding a list of unusual words.
* Output the resulting unusual words
	
	
__Code for UnusualWords:__

This example is going to look through the 1801 Inaugural Speeches, Specifically Jefferson's. What kind of words do you think might be there?

```
import nltk
def unusual_words(text):
    text_vocab = set(w.lower() for w in text if w.isalpha())
    english_vocab = set(w.lower() for w in nltk.corpus.words.words())
    unusual = text_vocab.difference(english_vocab)
    return sorted(unusual)

print unusual_words(nltk.corpus.inaugural.words('1801-Jefferson.txt'))
```						

__Output:__

```
['abuses', 'acknowledging', 'acquisitions', 'actions', 'administrations', 'adoring', 'affairs', 'agonizing', 'alliances', 'angels', 'announced', 'assembled', 'authorities', 'banished', 'bestowed', 'billows', 'bled', 'blessings', 'bulwarks', 'burthened', 'called', 'cases', 'charged', 'citizens', 'committed', 'concerns', 'convulsions', 'councils', 'debts', 'decisions', 'degradations', 'delights', 'descendants', 'destined', 'destinies', ...]
```

Are you surprised?
