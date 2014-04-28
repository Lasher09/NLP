User would like to get a word count for the text they are examining to compare word length with other texts.

```

>>> from nltk.book import *
>>> len(*)

```

User wants to have a count for the occurrences of the term “begat” in the book of Genesis in the Bible.

```

>>> from nltk.book import *
>>> text1.concordance("begat")

```

User wants to get the plural form of words occurring in a text.

```

def plural(word):
if word.endswith('y'):
return word[:-1] + 'ies'
elif word[-1] in 'sx' or word[-2:] in ['sh', 'ch']:
return word + 'es' elif word.endswith('an'):
return word[:-2] + 'en' else:
return word + 's'
>>> plural('fairy') 'fairies'
>>> plural('woman') 'women'

```

User want to be able to run a search without common words like "the" and "about".

```

>>> from nltk.corpus import stopwords
>>> stopwords.words('english')
['a', "a's", 'able', 'about', 'above', 'according', 'accordingly', 'across', 'actually', 'after', 'afterwards', 'again', 'against', "ain't", 'all', 'allow', 'allows', 'almost', 'alone', 'along', 'already', 'also', 'although', 'always', ...]

```

