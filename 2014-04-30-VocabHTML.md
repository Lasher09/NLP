---
layout: post
author: laura
title: Post
---

##Post 6:

__Program:__ VocabularyHTML

__Purpose and description:__  This program takes out selecte words from a webpage and outputs those words into a list format for easier copy and pasting with no need to format further. 

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
