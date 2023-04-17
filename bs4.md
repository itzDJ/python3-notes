[Official Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
#### Ways to get the html file
- local file
- requests.get()
- page.content() from [playwright](playwright.md)
#### Html parsers
Commonly used html parser: "html.parser"
Faster than html parser but requires pip install: "lxml"
## Example code
Program to scrape and print the title of a Wikipedia page

```python
from bs4 import BeautifulSoup  # pip install bs4
from requests import get

url = "https://en.wikipedia.org/wiki/Python_(programming_language)"
html = get(url).text

soup = BeautifulSoup(html, "html.parser")

# find_all method can take an html tag as a parameter and returns a list
h1s = soup.find_all("h1")
for h1 in h1s:
    # text accesses the text within the line of html code
    print(h1.text)  # output: Python (programming language)
```
