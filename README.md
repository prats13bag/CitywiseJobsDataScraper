# Web Data Scraper - Jobs Listed (citywise) on Indeed.com

### _1. Introduction_
A Python (jupyter notebook) script is built and tested to scrape jobs listed in the cities entered by the user as input which are available on the job search website - indeed.com

### _2. Brief description about the implemetation steps_

	1. Input cities from the user and store them in a list with some housekeeping such as conversion to lower case and replacing ' ' with '+'

	2. For each city do the following steps:
	  2.1. Iterate over all indeed.com's page pagewise within this city and do the following:
        a. For each job posted in that page locate, extract and append to a list the following: "job title", "company name", "sponsored post or not", "no. of days posted ago" and "salary" using BeautifulSoup
        b. add this list to result (out_df) pandas dataframe
        
      2.2. if result (out_df) pandas dataframe is not empty then create csv file for jobs posted in city while removing duplicates. This step also helps in filtering out 'inconsistent' city names entered by the user with indeed's website

### _3. Software installations required to run code_
 - Anaconda Python distribution - prefereably Anaconda3 with python 3.6
 - pip packages imported at the top of the notebook file
 
### _4. About the data scraped_

The scraped data is stored in .csv files bearing respective city names with sample information as below:<br>

| `Job Title`                                               | `Company Name`               | `Sponsored`   | `Posted`      | `Salary`       |
| --------------------------------------------------------- | ---------------------------- | ------------- | ------------- |--------------- |
| Dog Walker                                                | Wag!                         | Sponsored     | Not Available | $30 an hour    |
| Apple Genius - Technical Customer Service                 | Apple                        | Sponsored     | Not Available | Not Available  |
| Customer Support Operations - Uber Freight, Inbound Phone | Uber                         | Sponsored     | Not Available | Not Available  |
| HOLIDAY CLERK ASSISTANT                                   | United States Postal Service | Not Sponsored | 4 days ago    | $17.19 an hour |

### _5. References_
 - [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
 - [Pandas](http://pandas.pydata.org/pandas-docs/stable/)