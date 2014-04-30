Program: LoadMyCorpus
Purpose and description the program: User would like to load their own corpus. They must: make directory /usr/share/dict. Whatever the location, set this to be the value of corpus_root . The second parameter of the PlaintextCor pusReaderinitializer canbealistoffileids,like['a.txt', 'test/b.txt'],orapattern that matches all fileids, like '[abc]/.*\.txt'

Program capabilities:
    • Identify a given corpus from a local directory
    • Allow for the user’s corpus to be processed
    
Code for LoadMyCorpus:

```

>>> from nltk.corpus import PlaintextCorpusReader
>>> corpus_root = '/usr/share/dict'
>>> wordlists = PlaintextCorpusReader(corpus_root, '.*')
>>> wordlists.fileids()


```
Output:

```

['README', 'connectives', 'propernames', 'web2', 'web2a', 'words'] >>> wordlists.words('connectives')
['the', 'of', 'and', 'to', 'a', 'in', 'that', 'is', ...]

```
