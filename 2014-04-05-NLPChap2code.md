Gutenberg Corpus
NLTK includes a small selection of texts from the Project Gutenberg electronic text archive, which contains some 25,000 free electronic books, hosted at [Gutenburg](http://www.gutenberg.org/). We begin by getting the Python interpreter to load the NLTK package, then ask to see nltk.corpus.gutenberg.fileids(), the file identifiers in this corpus:

```
>>> import nltk
>>> nltk.corpus.gutenberg.fileids()

```
Anyone could pick out the first of these texts—Emma by Jane Austen—and give it a short name, emma, then find out how many words it contains:

```
>>> emma = nltk.corpus.gutenberg.words('austen-emma.txt') 
>>> len(emma)
```


