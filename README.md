## Who appointed the judges?
This project aims to find out the presidential influence on U.S. courts by looking at current judgeship apppointment at U.S. Court of Appeals.

### Data collection 
The data was collected from [Biographical Directory of Federal Judges](https://www.fjc.gov/node/7946), a database maintained by the Federal Judicial Center. 

So usually scraping starts with `requests` and `BeautifulSoup` but since it is a website that requires clicking around to get to our data, we'll have to start with `Playwright` to get things started. However, unfortunately, this website block bots like `Playwright`, so we'll have to try other ways to get access to their data.

After a good while of struggling, I realized I am never gonna be able to figure this out on my own so I went to my professor Soma to get help with scraping this website. Turns out, he already made a [video](https://www.youtube.com/watch?v=tMj9r7NKVQQ&list=PLewNEVDy7gq1eMYCkL8Q3WuktkUcmvUhE) about it when classmates of mine asked him about it earlier. Here are a few ways to avoid bot detection scraping this website:
* cURL
* change header (could refer to my 
