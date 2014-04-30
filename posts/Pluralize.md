Program: Pluralize
Purpose and description the program: User wants to get the plural form of words occurring in a text.

Program capabilities:
    • identify the plural form of a word 
    • Output plural form
    
Code for Pluralize:

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

        
Output:

```

(“fairies” “women”)

```
