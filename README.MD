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
![Screenshot_2020-06-01 privacy - Jupyter Notebook(5)](https://user-images.githubusercontent.com/5400662/83519210-dd8cb280-a4db-11ea-926d-c40220f8c2c9.png)

start to anonymize the columns we want, Based on what and where data is going to be used.
for example in some app we need to have name,surname and in other we have to use an id.

+ anonymize the birht date to the age ( it can be age 20-25 or exact 20, again based on purpose we want to use data for).
![Screenshot_2020-06-01 privacy - Jupyter Notebook(3)](https://user-images.githubusercontent.com/5400662/83519532-74f20580-a4dc-11ea-8bac-b3dd4753814b.png)
+ so I added a new column "Age" and convert the Birth Date to Age , then I Dropped the Birthdate and Save it as a newdataset.
![Screenshot_2020-06-01 privacy - Jupyter Notebook(7)](https://user-images.githubusercontent.com/5400662/83519659-ad91df00-a4dc-11ea-9cf9-29927cdf43e3.png)
+ in this project we dont need an emails or address , so they are dropped from secondary saved dataset
