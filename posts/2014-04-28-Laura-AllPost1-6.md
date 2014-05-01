---
layout: post
author: laura
title: Post
---

---------------------
##Post 1:

__Program:__ LongestWord

__Purpose and description the program:__ To find the longest word in a given text. This program will sift through a given text and find the longest word. This program will find the longest word in Milton's Paradise Lost text.
	
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


---------------------
##Post 2:

__Program:__ WebpageFrequency

__Purpose and description:__ This program allows a user to tokenize a webpage and get the most frequent words used in it.
	
__Program capabilites:__
* read a URL
* tokenize all the words
* calculate the given number for the most used words
* and then give the output of the word

	
__Code for WebpageFrequency:__

```

import nltk
constitution = "http://www.archives.gov/exhibits/charters/constitution_transcript.html"
def freq_words(url):
    freqdist = nltk.FreqDist()
    text = nltk.clean_url(url)
    for word in nltk.word_tokenize(text):
        freqdist.inc(word.lower())
    return freqdist
 	
fd = freq_words(constitution)
print fd.keys()[0:50]

```						

__Output:__

```

['the', ',', 'of', 'and', 'shall', 'be', 'to', 'in', 'or', ';', 'states', 'united', 'a', 'by', 'for', 'state', 'any', 'which', 'all', 'may', 'such', 'president', 'have', 'as', 'on', 'congress', 'no', 'from', 'he', 'other', 'house', 'not', 'but', 'section.', 'law', 'their', 'each', 'one', 'constitution', 'office', 'that', 'two', 'this', ':', 'at', 'person', 'senate', 'time', 'under', 'with']

```

-------------------
##Post 3:

__Program:__ POSTagger

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

--------------------

##Post 4:

__Program:__ GenderNames

__Purpose and description:__ A program that reads a list of names and will predict whether a name is a male or a female name. This program also will produce a graph to illustrate the frequency of names ending in certain letters and their predicted gender.
	
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

![Markdown Logo](http://puu.sh/8rBAw.png)
Format: ![Alt GenderMap](url)

-----------------------

##Post 5:

__Program:__ UnusualWords

__Purpose and description:__ A program that can read a text for the most unusual words so that a user can judge the reading level of that text.

__Program capabilites:__
* Read all the lowercase words in a text
* Compare the words in this text to the words in another text file holding a list of unusual words.
	
	
__Code for UnusualWords:__

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

-----------------------

##Post 6:

__Program:__ VocabularyHTML

__Purpose and description:__ A program that takes out a list of words from a webpage in a list format for easier copy and pasting with no need to format further.

__Program capabilites:__
* Capture a webpage
* Import nltk, urllib, urlopen, pprint
* Target a certain number of words
* Output those words into a list format with no puntucation
	

__Code for VocabularyHTML:__

```
import nltk
from urllib import urlopen
import pprint
url="http://www.worldwidewords.org/weirdwords"
raw=urlopen(url).read()
html=urlopen(url).read()
raw=nltk.clean_html(html)
tokens=nltk.word_tokenize(raw)
tokens=[x.replace(";","") for x in tokens]
tokens = filter(None, tokens)
print '\n'.join(tokens[200:300])

```						

__Output:__

```
Blurb
Bodacious
Bodger
Bombilation
Bonzer
Boondoggle
Bootless
Borborygmus
Boscage
Boustrophedonic
Bowdlerise
Bridewell
Brimborion
Brobdingnagian
Bromopnea
Brosiering
Brummagem
Bruxer
Burgoo

```
