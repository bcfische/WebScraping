Mission to Mars

Here, we build a web application that scrapes various websites for data related to the Mission to Mars and displays the information
in a single HTML page.

Step 1 is scraping the following information / image data:
~NASA Mars News (BeautifulSoup)
~JPL Mars Space Images Featured Image (Splinter)
~Twitter Mars Weather (BeautifulSoup)
~Mars Facts (Pandas)
~Mars Hemispheres Images (Splinter)

Step 2 is using MongoDB with Flask templating to create a new HTML page that displays all of the information that was obtained
from Step 1. We start by converting the Jupyter notebook into a Python script called scrape_mars.py with a function called scrape
that executes all of the scraping code and returns one Python dictionary containing all of the scraped data. Next, we create a route
called /scrape that imports the scrape_mars.py script and calls the scrape function. The return value is stored in Mongo as a Python
dictionary. We then create a root route (/) that queries the Mongo database and passes the mars data into an HTML template to display
the data. Finally, we create a template HTML file called index.html that takes the mars data dictionary and displays all of the data
in the appropriate HTML elements.
