# abandoned-oil-wells

This repo includes the following:

  1. Python code for scraping web data on abandoned oil wells in Texas
  2. A web app written in R that presents an analysis of the scraped data on a
     static web page

The app is hosted at

https://markcbutler.shinyapps.io/abandoned-oil-wells/

The choice to scrape and analyze data on abandoned oil wells was motivated by
news reports in July, 2020 predicting a surge in the number of abandoned wells
due to the sudden drop in demand for oil and gas associated with the COVID-19
pandemic.  Will abandonment of wells by bankrupt operators do major harm to
the environment?  The web app aims to shed light on that question by exploring
the situation in Texas.

The web-scraping module *scrape.py* was run in August 2020, and the resulting
log, which is in the Scrape_data directory together with the module *scrape.py*,
gives a quick view of the module's operation.  Web scraping is done using the
Beautiful Soup library together with the requests package.  Text is extracted
from downloaded pdf files using the tika package, and pandas is used to
convert an html table to csv.

Note that a follow-up test of *scrape.py* in December 2020 found that an html
error in in one of the scraped web pages had broken the scraping process.
Although the fix would not have been difficult, it was not implemented, and so
*scrape.py* can be viewed as a frozen example of web-scraping code.
