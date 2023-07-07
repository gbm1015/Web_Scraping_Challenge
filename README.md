# Web-scraping and Data Analysis Homework Solution: Mars News Articles and Mars Weather Data

## Background

We learned to identify HTML elements on a page, identify and use their id and class attributes to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup.  We learned to scrape various types of information, including HTML tables and recurring elements; such as, multiple news articles on a webpage.
In Part 1 we scraped titles and previewed texts from Mars news articles at https://static.bc-edx.com/data/web/mars_news/index.html.
In Part 2 we scrapeed and analyzed Mars weather data, which existed in a table at https://static.bc-edx.com/data/web/mars_facts/temperature.html.

### Before opening the starter codes in Jupyter Notebook

1. I created a new repository in GitHub for this project called `Web_Scraping_Challenge`. 
2. Inside the new repository I cloned the new repository to my computer.
3. Inside my local Git repository, I created a directory/folder for the two parts of the assignment and named them Mars_News and Mars_Weather, respectively.
4. Then added the Jupter notebooks part_1_mars_news.ipynb and part_2_mars_weather.ipynb with starter scripts, as well as the chromedriver.exe within each folder.
  
### Files including data 

* mars_weather.csv - The Mars Weather HTML table that was extracted into a Pandas DataFrame and exported into a CSV file

## Part 1 - Scraped Titles and Previewed Text from Mars News

1. Used automated browsing to visit the Mars News site at https://static.bc-edx.com/data/web/mars_news/index.html. Inspected the page to identify which elements to scrape.
2. Created a Beautiful Soup object and used it to extract text elements from the website.
3. Extracted the titles and previewed the text of the news articles that were scraped. Stored the scraping results in Python data structures as follows:
   - Stored each title-and-preview pair in a Python dictionary and gave each dictionary two keys: title and preview.
   - Stored all the dictionaries in a Python list.
   - Printed the list in the Jupyter Notebook part_1_mars_news.ipynb.
    
## Part 2 - Scraped and Analyzed Mars Weather Data

1. Used automated browsing to visit the Mars Temperature Data at https://static.bc-edx.com/data/web/mars_facts/temperature.html. Inspected the page to identify which     elements to scrape. 
2. Created a Beautiful Soup object and used it to scrape the data in the HTML table. 
3. Assembled the scraped data into a Pandas DataFrame. The columns had the same headings as the table on the website with the following explanations:
    - id: the identification number of a single transmission from the Curiosity rover
    - terrestrial_date: the date on Earth
    - sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
    - ls: the solar longitude
    - month: the Martian month
    - min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
    - pressure: The atmospheric pressure at Curiosity's location 
4. Examined the data types that were currently associated with each column. If necessary, casted (or converted) the data to the appropriate datetime, integer, or float data types.
5. Analyzed the resulting dataset by using Pandas functions to answer the following questions:
    - How many months exist on Mars?
    - How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    - What are the coldest and the warmest months on Mars (at the location of Curiosity)?
      To answer this question we found the average minimum daily temperature for all of the months, then plotted the results as a bar chart.
    - Which months have the lowest and the highest atmospheric pressure on Mars?
      To answer this question we found the average daily atmospheric pressure of all the months, then plotted the results as a bar chart.
    - About how many terrestrial (Earth) days exist in a Martian year?
      To answer this question we considered how many days elapsed on Earth in the time that Mars circled the Sun once, then visually estimated the result by plotting the          daily minimum temperature.
6. Exported the DataFrame to a CSV file.

   
