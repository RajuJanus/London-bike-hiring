# Time series analysis and predictions on London Bike Hiring Dataset
London is a crowdy city. An analysis and prediction on bike hiring/ bike traffic on daily basis can benifit many industries. 

## Aims: 
   ### Doing an exploratory analyis.
   ### Data storytelling: Finding differnt patterns especially seasonality : (https://public.tableau.com/app/profile/raju.roy#!/)
   ### Predict the number of bike hire on a particular day/month/year in London. For example predict how the bicycle traffic will look like on a month or a particular location.


I have also visualized the data in Tableu (https://public.tableau.com/app/profile/raju.roy#!/). 
If you want to get an overal idea, such as where most crowdy stations located. At which month or day more people hire bikes, you can interactively select features and the dashboard will show you the trends. 

# Example visualization:

https://public.tableau.com/app/profile/raju.roy#!/

# Technologies: 

Pandas, Seaborn, Numpy, Facebook Prophet, Tableau etc.

# Data Cleaning
Correct the Date formats, drop NaNs
Check the duration columns: negative values, problem with start and end dates 
Adding holiday calendar of UK, adding daily temperatures
Remove unused stations

# Data Storytelling:

 Question we might ask to the Data:
Show me the yearly bike hires from 2010
Is there any seasonality pattern? Yeary? Monthly? Weekly? Daily?
How does the weather affects the bike hire?
What are the most popular stations? Where they are located in Street map?
Most popular routes? Visualize!

# Time series forcasting:

### Prepare the data in a format the Facebook Prophet require
### Intitalize Facebook Prophet
### Split the dataset into train and Test
### Train The model
### Tune the hyper parameters
### Find trends. Visualize performance metrics


# Data
The first dataset was downloaded from publicly available dataset 'London Bicycle Hire' in Bigquery.

(https://console.cloud.google.com/marketplace/product/greater-london-authority/london-bicycles?project=fit-shift-332509)
This data contains the number of hires of London's Santander Cycle Hire Scheme from 01/2015 to 06/2017. Data includes start and stop timestamps, geographical location of the station names and ride duration.
This is a big dataset and it was downloaded by chunks and added together. Also the start and end dates are already converted to date-time datatype  and added as new columns before importing here.

The second dataset was downloaded from London data store (https://data.london.gov.uk/dataset/number-bicycle-hires) which contains the daily number of bicycle hire from 2010 to present.



