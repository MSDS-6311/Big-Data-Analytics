# Assignment 3: Regular Expressions, Git, and a Business Case

Due Feb 10, 2021

Skills: 
* Learn to use regular expressions for finding patterns in text 
* Learn to use `scp` for copying files 
* Learn to use git for sharing files with others and version control
* Analyze a Big Data  business case 
* Learn Markdown for formatted text
 

## Regular expressions
Learn to use *regular expressions* in Python, `grep`, etc. Resources:
* https://regexone.com/lesson/introduction_abcs
* https://www.kaggle.com/sohier/introduction-to-regular-expressions
* https://www.guru99.com/python-regular-expressions-complete-tutorial.html
* https://docs.python.org/3/library/re.html

## Git 
Learn the principles of `git` and its usage from the command line. 
* Git in data science [`git`](https://towardsdatascience.com/why-git-and-how-to-use-git-as-a-data-scientist-4fa2d3bdc197).
* Git Handbook https://guides.github.com/introduction/git-handbook/
* Learning Git: https://learngitbranching.js.org/
* Columbia University GitHub Desktop tutorial https://zuckermanbrain.github.io/git-novice/

## Example of Big Data: SiteZeus 
* [Video 1](https://www.youtube.com/watch?v=c4m4HH19m5Q) -- Model basics and adding data 
* [Video 2](https://www.youtube.com/watch?v=CuihDgBtApI) -- Predictive model 
* [Video 3](https://www.youtube.com/watch?v=OHGxfjNzIHY) -- SiteZeus + Uber Media on cell phone data

# Assignment

## Problem 1: Regular expressions 1.
Review the program `list_tags.py` included with this assignment.  It reads the file `/home/shared/Tweets.csv` and prints hashtags from it. 

* Modify it so that it will only print unique tags, skipping duplicates.
* Notice that the program misses some hashtags because it does not match tags containing digits. Modify the program so that it will match all valid Twitter hashtags.


## Problem 2. Regular expressions 2.
Write a new program, `list_love_tags.py` that lists all unique hasthags containing the word "love", ignoring case. To verify, I got 44 matches.

 
## Problem 3: SiteZeus business model
In the same folder, create the file `BusinessModel.md`. Using the [markdown syntax](https://guides.github.com/features/mastering-markdown/), write a 1000-1500 word description of how SiteZeus uses big data to create value for their customers.

1. What problem does SiteZeus address?  What did customers do before solutions like SiteZeus existed?
2. What data sources does the platform use?
3. How does the platform transform the data to make it useful for its subscribers?
4. What technical challenges does the company need to solve to make their service effective?

# Submit the assignment.

Create these files and programs on the cloud linux server in folder `~/homework/a03/` and I will review it there for the grade. 
