# Socrata Twitterbot v1.1

### Python script application that tweets daily updates of new/modified SOCRATA datasets
#### Initial version created at the Health 2.0 National Day of Civic Hacking, made available for public use.

This python application checks the metadata of a target Socrata Open Data Portal and identifies datasets that have are new or modified.  It then tweets the title and a link to the dataset to Twitter programatically.

### v1.1 IMPROVEMENTS as of 2017-04-26
* Twitterbot now checks for long titles and truncates appropriately to 140 characters to avoid errors.
* Twitterbot now has a memory! Using a local csv file, twitterbot is 'aware' of what it has tweeted in the last x number of days. This threshold can be set and is defaulted at 7 days. This is to avoid 'white noise tweets' of datasets that are updated every day via CRON or task scheduler so our audiences don't tune out the twitterbot.

#### Deployment instructions:
* Clone or download the repository/files
* Run the jupyter notebook version of the script one cell at a time to generate a initial memory file
  * Take care to replace twitter API tokens, 'threshold' days and 'baseline' days
* Update the .py version of the file
  * Take care to replace twitter API tokens, and 'threshold' days
* Schedule the .py version of the script to run once a day in the evening using CRON, launchd, task scheduler, or the automation of your choice

#### Known bugs/features:
* If you change the wording of the tweet, the 'slice' that truncates tweets to make sure it is <= 140 will need to be adjusted

#### Future features:
* Tweet data sets with low view counts over time to build a user base
* Tweet descriptive statistics for a open data portal to demonstrate month over month growth, etc.
* Encapsulate initial memory creation into a function so all code can be contained in a single .py file
* Generate requirements.txt file for dependency management
* Further improved documentation