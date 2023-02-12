Acquisition and Preprocessing of Book Data
-- Project Status: [Completed]
Introduction

This project utilizes web scraping to collect data from amazon.com on best selling books.  The web_scraper.py script cycles through books and creates two directories- one directory containing a parent table that has book information and another directory hosting child tables with review data for each book in the parent table. The parent table  has the following features:

•	 ID - The book ID 
•	Title -  The title of the book
•	Authors - The author of the book
•	Price - The selling cost of the book on amazon.com
•	Ratings - The total star rating (out of 5)  of the book
•	Num_reviews - The number of ratings that contributed to the final rating of the book

The child tables have the following features:
•	ID - number of review in queue
•	Book_ID - ID corresponding to the book ID in the parent table
•	Title - title given to review by the reviewer
•	Location - location of the reviewer
•	Reviewed_on - date the review was written
•	Rating - number of stars (out of 5) the reviewer assigned to the book
•	Body - content of the review
•	Num_helpful_votes - the number of people who found the review helpful 

The final dataset hosts a parent table limited to 200 books and review tables with a max of 500 reviews for each book. 

How To Use It

The script can be run in the command line by calling web_scraper.py in the command line or from any IDE that runs python3.  The variables max_num_books and max_num_reviews (currently set to 200 and 500 respectively) can be adjusted to collect a larger sample of books and reviews than the script currently allows.  

Requirements

The script is run using Python3 and requires the installation of the selenium and webdriver_manager python packages. Both packages can be installed using pip install in the command line.  


Challenges/Limitations

Captchas:  The speed at which the scraper cycles through page links could trigger amazon to issue a captcha to test if a bot is on the page.  
 
Time: The script currently takes 4 hours to run, collecting 200 books and 500 reviews for each book. Any increase in the numbers collected will result in an increase in the runtime of the code.
  
Inconsistent HTML: HTML tags representing similar elements change across pages 

Future Improvements

The efficiency of the script can be improved. Calculations can be done to minimize the total runtime of the script by adjusting the sleep periods between requests.  


Documentation

The documentation for selenium used in this project can be found here:
https://selenium-python.readthedocs.io/

The documentation for webdriver_manager can be found here:
https://pypi.org/project/webdriver-manager/


