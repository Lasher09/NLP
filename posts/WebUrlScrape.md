---
layout: post
author: jacobthill
title: Scraping url's from a webpage
---

#Scraping url's from a webpage

This is a simple script for scraping url's from a webpage. To get this to work, cut and paste the script into a text file, save it as name.py and run it from your terminal (python name.py). Before getting started, make sure you have Beautiful Soup installed on your system. 



```
# Simple script for extracting url's from webpages, modified from www.pythonforbeginners.com/python-on-the-web/web-scraping-with-beautifulsoup/

from bs4 import BeautifulSoup

import requests

url=raw_input("Enter a url:")

r = requests.get("http://" +url)

data=r.text

soup = BeautifulSoup(data)

for link in soup.find_all('a'):
	print(link.get('href'))
```