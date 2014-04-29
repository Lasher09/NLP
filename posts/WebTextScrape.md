---
layout: post
author: jacobthill
title: Scraping text from a webpage
---

#Scraping text from a webpage

This is a simple python script for extracting text from a webpage. It can be challenging to get all of the text formatted in the way you want, but this does a decent job. You should be able to find other resources on the web to adapt this script to your particular need. To get this to work, cut and paste the script into a text file, save it as name.py and run it from your terminal (python name.py). Before you start, make sure you have Beautiful Soup and urllib2 installed. 



```
# modified from from http://stackoverflow.com/questions/22799990/beatifulsoup4-get-text-still-has-javascript

import urllib2
from bs4 import BeautifulSoup

# get url from user
url = raw_input("Enter a url:")
# open url
html = urllib2.urlopen(url)
# read content from url
page_content = html.read()
soup = BeautifulSoup(page_content)

# kill all script and style elements
for script in soup(["script", "style"]):
    script.extract()    # rip it out

# get text
text = soup.get_text()

# break into lines and remove leading and trailing space on each
lines = (line.strip() for line in text.splitlines())
# break multi-headlines into a line each
chunks = (phrase.strip() for line in lines for phrase in line.split("  "))
# drop blank lines
text = '\n'.join(chunk for chunk in chunks if chunk)

print text
```