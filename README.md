# Specification

We would like you to build a simple web crawler script that will fetch and process data from the specified website and all its subpages linked from the main page and subpages of subpages etc.
Build the app as CLI.

# Task 1 
crawl --page <URL> --format <csv/json> --output <path_to_file>
Results should be saved in CSV/JSON file format where each row is representing one page, with the following columns/keys:

link
title
number of internal links
number of external links
number of times url was referenced by other pages*

* if on the page there are multiple references to the one page, count it as a one
Example csv file provided in the repository.

# Task 2

print-tree --page <URL>
There should be an option to print the structure of the page as a tree in the following format

Main page (5)
  subpage1 (2)
    subpage1_1 (0)
    subpage1_2 (0)
  subpage2 (1)
    subpage2_1 (0)


The subpage represents actual urls to pages and the numbers in parentheses represent the number of internal pages at the current level.

# Extra points for:
using asyncio
tests
error handling

# Rules & hints
use Python 3.9
use OOP paradigm
You are free to use any third-party libraries
Link to the website you are crawling should be passed as a parameter to the script
Links are defined using the <a> tag, you can ignore all other types of links
Provide README with examples how to use your script
Write Python code that conforms to PEP 8 standard
Please handle possible exceptions within script in a user-friendly way
