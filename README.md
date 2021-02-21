# Aconex Mail Data Query

This is a google colab notebook that simplifies the process of querying Aconex web services to retrieve project mail data across a portfolio of projects for a single user. Specifically, it retrieves all projects for a user using the Projects API and passes these to the Mail API to retrieve up to 250 projects mails per day per project and stores them either locally in a csv file or to a user specified google drive account. By default up to 11 mail field/value pairs will be retrieved. Users can set the data range for the search window to limit the size of the data request / runtime, for larger projects / portfolios a shorter search window is suggested.  

## Getting Started:

### Prerequisites:
Please note that you’ll need Organisation Admin rights in Aconex and an API Authorisation Code for your organisation from Aconex to run this query. 

### Set up Aconex: 
First log into Aconex as Organisation Admin and go to ‘User Role Configuration’ under setup and grant ‘Web Services API’ access for the appropriate user group within your organisation. 

Then create an API User account on Aconex and add this user to all of the projects in the portfolio of interest. Finally, go into ‘User Role Assignment’ and ensure that the API User is added to the user group with ‘Web Services API’ access. 

### Setting up and Running the Query: 
Start at Section 2 and enter the search date range for the query using the date fields. For the initial query its recommended that you run a single day to make sure that everything is working correctly.

Then go to Section 4 and enter the API Credentials for the API User and the API Authorisation Code from Aconex. 

### Running the query
Go to 'Runtime' and select 'Run all'. 

Please note that when you first execute the notebook you'll need to complete the google authorisation process in Section 3 before the code will progress. If you don’t want to do this and want to just save the temporary file to a local disk then you can delete or hash out the relevant bits of code in Section 1,3 and 7 and execute the code without this functionality. 

Also, please note that the API queries in Section 7 can take a while to run depending on the search window selected. If this times out while using google colab, please consider reducing the search window range or importing the code in to Jupyter Labs. 

Once completed save a local copy of the temporary csv file or open your drive account to access the retrieved data. 

## Authors:
AddVennture - http://addvennture.co.uk
