## Very simple web scraper

### To run
```
> python scraper.py 'http://www.example.com/' outfile.json
```

### Shortcomings of this program
* Will not attempt to parse URLs shortened by a URL service (which in theory can point back to the original site).
* Only parses the raw html it finds. ie the program will not find any links or images inserted by javascript.
* Similarly, some methods of javascript file loading use javascript code, which isn't detected.
* No cookie state is kept; in theory this could mean the discovered links differ to those shown to what the host site considers a repeat visitor.
* No 'logging in' capabilities; therefore the scraper can't access any areas of the site that are given over to known users (for instance, account pages).
* Doesn't handle a few cases, like id linking and mailtos.
* Will only find images included in img elements, ie will not discover images loaded by css background
* Won't find css files linked to from within css files
* Won't find pages that are only discoverable via a form submission
