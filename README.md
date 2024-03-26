# Who appointed the judges?
This project aims to find out the presidential influence on U.S. courts by looking at current judgeship apppointment at U.S. Court of Appeals.

## Data collection 
The data was collected from [Biographical Directory of Federal Judges](https://www.fjc.gov/node/7946), a database maintained by the Federal Judicial Center. 

So usually scraping starts with `requests` and `BeautifulSoup` but since it is a website that requires clicking around to get to our data, we'll have to start with `Playwright` to get things started. However, unfortunately, this website block bots like `Playwright`, so we'll have to try other ways to get access to their data.

After a good while of struggling, I realized I am never gonna be able to figure this out on my own so I went to my professor Soma to get help with scraping this website. Turns out, he already made a [video](https://www.youtube.com/watch?v=tMj9r7NKVQQ&list=PLewNEVDy7gq1eMYCkL8Q3WuktkUcmvUhE) about it when classmates of mine asked him about it earlier. Here are a few ways to avoid bot detection scraping this website:
* cURL
* change `header`

One would think scraping from here onwards would be smooth and easy. But no. The information I needed was written in paragraphs and there is no better ways to deal with paragraphs than using `regex` (*I think*). So, figuring out the pattern of the paragraphs and then dealing with a few that were formatted in slightly different ways gave me a lot of headaches. It is only much later that I learned we could use `try except` that would have alleviated the difficulties scraping these irregular paragraphs. 

## Data analysis
Once I got all the presidents' name and court of appeals each judge belongs to, the rest became much easier. I simply used conditions and `value_counts` by president to see how many of the judges in a court were appointed by each president.

## What to improve
My end goal is to make a map and put it onto a webpage to make the findings more reader-friendly.
