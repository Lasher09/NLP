Program: Specific Book Word Count
Purpose and description the program: User would like to get the word count for the book "Emma" by Jane Austen in the Gutenburg Corpus

Program capabilities:
    • Find and Read the given file from corpus
    • Output total specific word count of book
    
Code for Specific Book Word Count:

```

>>> import nltk
>>> from nltk.corpus import gutenburg
>>> emma = nltk.corpus.gutenberg.words('austen-emma.txt')
>>> len(emma)

        
Output:

```

(wordcount of “Emma”)

```
