## Who appointed the judges?
This project aims to find out the presidential influence on U.S. courts by looking at current judgeship apppointment at U.S. Court of Appeals.

### Data collection 
The data was collected from [Biographical Directory of Federal Judges](https://www.fjc.gov/node/7946), a database maintained by the Federal Judicial Center. 

So usually scraping starts with `requests` and `BeautifulSoup` but since it is a website that requires clicking around to get our data, we'll have to start with `Playwright` to get around it. Unfortunately, this website block bots like `Playwright`, so we'll have to try other ways to avoid being blocked.
