[Official Documentation](https://playwright.dev/python/docs/intro)

### For further automation
- Use classes such as [locator](https://playwright.dev/python/docs/api/class-locator) to find elements (highly beneficial as it includes auto-wait).
- Then, use methods such as click and fill to interact with the page.

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    # Launch the webkit (Safari) browser (can also use firefox or chromium)

    # Turn off the default headless browser with keyword arguments:
    # `headless=False` and `slow_mo=50`
    browser = p.webkit.launch()

    # Open a new page
    page = browser.new_page()

    # Go to a url
    url = "https://google.com"
    page.goto(url)

    # Get the html of the page
    html = page.content()

    # Close the browser
    browser.close()
```
