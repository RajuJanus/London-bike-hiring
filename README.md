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

# Web-App based on this analysis and prediction:

https://share.streamlit.io/rajujanus/bicycle_hiring_app_deployed/webapp.py

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

### Modeling, training and testing with Facebook prophet
#### Iteration 1: Prepare the data for facebook prophet, it needs two columns, y and ds.
#### Iteration 2: Adding holiday feature to the model:
#### Iteration 3: Try the same with a larger dataset Now we look at a dataset that is larger and which contains bike hiring stats from 2010 to present.
#### Iteration 4: Tune the model with on and off season
#### Iteration 5: Validate the model (Cross validation): Create Train and Test dataset from available data based on years, look at the change points of the trend and then perform cross validation
#### Iteration 5, second part: check Performance by using Mean Absolute Error (Cross validation)
#### Iteration 6: Multivariate time series prediction. We import temperature column and also consider it for the modeling and predictions
#### Iteration 7: Sum everything up and train the model again. Also test how the model performance without temperature modifications
But it seems no improvement. Though the model already performs pretty well with MAPE ranging from 0.2 to 0.4 -->


# Data

The first dataset was downloaded from publicly available dataset 'London Bicycle Hire' in Bigquery.

(https://console.cloud.google.com/marketplace/product/greater-london-authority/london-bicycles?project=fit-shift-332509)
This data contains the number of hires of London's Santander Cycle Hire Scheme from 01/2015 to 06/2017. Data includes start and stop timestamps, geographical location of the station names and ride duration.
This is a big dataset and it was downloaded by chunks and added together. Also the start and end dates are already converted to date-time datatype  and added as new columns before importing here.

The second dataset was downloaded from London data store (https://data.london.gov.uk/dataset/number-bicycle-hires) which contains the daily number of bicycle hire from 2010 to present.

I have compiled all the data in a google drive folder and can be downloaded here
(https://drive.google.com/drive/folders/1gtCTDjOvfX77ZIA7uIUHybrTY78GRHzn?usp=sharing)


