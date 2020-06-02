# Privacy in Location-Based Services (LBS):
## using :
+ Python 3.8.2
+ jupyter notebook

 ## Libraries used : 
+ 1-ipyleaflet
+ 2-matplotlib
+ 3-random
+ 4-Pandas
+ 5-Numpy
+ 6-Csv
+ 7-Faker
## DataSet :
+ Faker library used to creat the dataset with #Name , #surname , #Email , #Address , #Latitude , #Longitude , #Zipcode
+ this dataset will be saved as a title "test data.csv" with N number of data. here we create 20 rows of data.


![Screenshot_2020-06-01 privacy - Jupyter Notebook](https://user-images.githubusercontent.com/5400662/83520725-70c6e780-a4de-11ea-9bc6-e783adea0aef.png)
![Screenshot_2020-06-01 privacy - Jupyter Notebook(5)](https://user-images.githubusercontent.com/5400662/83519210-dd8cb280-a4db-11ea-926d-c40220f8c2c9.png)

start to anonymize the columns we want, Based on what and where data is going to be used.
for example in some app we need to have name,surname and in other we have to use an id.

+ anonymize the birth date to the age ( it can be age 20-25 or exact 20, again based on purpose we want to use data for).
![Screenshot_2020-06-01 privacy - Jupyter Notebook(3)](https://user-images.githubusercontent.com/5400662/83519532-74f20580-a4dc-11ea-8bac-b3dd4753814b.png)
+ so I added a new column "Age" and convert the Birth Date to Age , then I Dropped the Birthdate and Save it as a newdataset.
![Screenshot_2020-06-01 privacy - Jupyter Notebook(7)](https://user-images.githubusercontent.com/5400662/83519659-ad91df00-a4dc-11ea-9cf9-29927cdf43e3.png)
+ in this project we dont need an emails or address , so they are dropped from secondary saved dataset.
+ as it is shown, we changed each original zip code to the unique value beacuse we dont want to have any conflict in zip code and longitude and latitude when we anonymize them.
+ converting the zip codes will be execute with function calling "anonymize_df".
+then it is the Name column turn. we dont want to anyone has access to name,surname with sensitive informatoin like location coordations.
+ so we assign a unique uuid to each user and drop the name column.


![Screenshot_2020-06-01 privacy - Jupyter Notebook(6)](https://user-images.githubusercontent.com/5400662/83520409-eed6be80-a4dd-11ea-93f2-b7d38bdba142.png)
+ after this we go to change the most important column here *Location* 
+ we read the longitude and latitude and add a random niose in range of x(we can assign how far we want be our limits).
 
![Screenshot_2020-06-02 privacy1 - Jupyter Notebook](https://user-images.githubusercontent.com/5400662/83520785-8b00c580-a4de-11ea-9eda-e766a632c773.png)
+ this is the dataset we prepared : 
![Screenshot_2020-06-02 privacy1 - Jupyter Notebook(1)](https://user-images.githubusercontent.com/5400662/83520880-ae2b7500-a4de-11ea-8206-ad5a026f49db.png)
+ with use of ipyleaflet and vega dataset, I create the map.html and use the usa airports as a user gps location with radius of 1km for possible locatoin (accurate location + noise).
+ so when you open the map.html you see the default point with zoom 15 on map with blue 1km radius of possible locations with 3 basic sample of random location (east , west , north , south).
 
![Screenshot_2020-06-02 Screenshot](https://user-images.githubusercontent.com/5400662/83521220-36117f00-a4df-11ea-9c63-3c45c7adda50.png)
 
 
![Screenshot_2020-06-02 Screenshot(1)](https://user-images.githubusercontent.com/5400662/83521260-445f9b00-a4df-11ea-8819-41603835d95b.png)
