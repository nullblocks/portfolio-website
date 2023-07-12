---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Fing search"
subtitle: ""
summary: "Fing Search is a project that leverages a Python web framework, to create a highly efficient search engine. By indexing and organizing web content, users can enter queries and receive relevant search results through a user-friendly interface. This project aims to demonstrate the implementation of a functional search engine"
authors: []
tags: [python, search-engine , nlp , flask]
categories: []
date: 2023-07-11T17:38:58+05:30
lastmod: 2023-07-11T17:38:58+05:30
featured: false
draft: false

# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "HomePage"
  focal_point: ""
  preview_only: false

url_code: 'https://github.com/nullblocks/FingSearch'
url_pdf: 'https://github.com/nullblocks/FingSearch/blob/main/Report/Report .pdf'
# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
# projects : ["nlp"]
#   Otherwise, set `projec
---
Fing Search is a fully functional search engine made using Python Programming Language. It displays search results based on a textual search query. MongoDB is used as database in the project. Several python libraries including BeautifulSoup, Pymongo and Requests are utilized and the web application is created using Flask.


## Aim:

- Crawling the web and indexing data in the database.
- Find results based on a search query.
- Display search results in a systematic and efficent manner by applying ranking algorithms.


APPROACH TO BUILD THE CRAWLER
* We are going to use the following python libraries to achieve the task .

1. `requests` library to fetch the pages.
2. `beautifulsoup4` to parse the response received from the response
object.
3. `pymongo` to connect to mongodb where we are going to store the data.
* Yes that’s it, that’s all we need.

* We will build a python class named `Crawler` inside the `crawler.py` file.
* The first thing we want to do is to make a connection with our database using
“ `pymongo`” library.
```pyhton
client = pymongo.MongoClient(connect_url_to_mongodb)
db = client.name_of_database
```
* After the connection is made we are going to define two methods inside the
class “`Crawler`” named `start_crawling` and `crawl`.
* Both of the methods mentioned above are going to take two arguments:
* url (string containing the url to the page we want to parse)
* depth(integer parameter to control the number of pages your program crawls)

Project Architecture:
![Architecture](https://user-images.githubusercontent.com/110848103/252709166-2adf8b27-6565-40d0-9191-39a35fe86d1d.png)

### Ranking Mechanism
Once the search results are fetched from the database, next comes sorting them in order of relevance. To achieve this, first, the search query is separated into different keywords, after which, each search result is checked for the number of keywords present in it, and ranked according to it.
#### Algorithm
* Get the search query after the preprocessing and store them in an array keywords. Preprocessing of data is done with `NLP / NLTK` . 
* Get the search results from the database and store them in an object results.
* Check for the number of keywords present in each result in the object results.
* For each keyword in the title of the result, it is given score +2, and for each
keyword in the description of the result, it is given score +1.
* Sort the results object in the descending order of score of each result.

### Output
Homepage
![Homepage](https://user-images.githubusercontent.com/110848103/240235176-1a2ce2ce-731e-4bce-9551-e0b9bdf887b6.png)
Search Results
![Search results](https://user-images.githubusercontent.com/110848103/240235191-22b1e621-a4a4-4c1d-9980-b111af325108.png)
History
![History](https://user-images.githubusercontent.com/110848103/252709747-03cf9c98-3e1b-4e7b-9cf6-f86980f2cedd.png)

### Tech stacks used:

- Python 
- MongoDB
- Flask

