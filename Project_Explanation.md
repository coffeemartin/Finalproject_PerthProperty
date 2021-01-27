### 1 Project Title : Perth Protery Market Analysis

### 2 Project Description : 

2020 has definitely been a strange year for every one around the world. The Covid-19 Pandemic has affected everything, including the property market. The shortage of the property in WA has caused by the growing number of returned local populations. As all the Australians are trying to get home when no one is allowed to travel overseas(yet). Therefore looking for a property to buy is currently on the top of my to-do-list.

As I've been renting since moving out of my parents' place, I've got 0 knowledge on the property market. By having a rough budget is not enough to find an ideal house. Picking a prefered suburb is my priority at moment as it will give me an entry point to know where to look at.


### 3 Data

I have selected & downloaded this dataset from Kaggle. https://www.kaggle.com/syuzai/perth-house-prices
It includes over 35k data entries of houses been sold in Perth, majority between 2010 - 2020. 


### 4 Cleaning & Analysis

At first, I have gained some general info regarding the dataset. such as how many rows/columns. what are the column titles, how many suburbs this dataset includes etc. Then I checked the duplicates, filling the missing values, deciding whether I should disregard the missing value data entries or fill in with the values that might help me with the investigation. I have also re-coded some data info for my visualisation purpose based on the original data info.

### Analysis (Questions):

Question 1: where are the 5 cheapest and the 5 most expensive (mean price) suburb in Perth? and how much are they?

Question 2: Which suburbs has the average price that fits within 840k to 870k?

Question 3: Which suburb sold the most houses in this dataset in these suburbs from Question 2?

Question 4: What is the relationship between Landsize & price for these suburbs?

Question 5: How far these houses are located away from CBD? I'd like to live no further than 15km.

Question 6: Which suburb should be my first entry point to start with? 

Question 7: Where are these houses? Are they close to the Freeway? Parks? Train stations? Can I visualise them on a real map?

### Analysis (Answers & Visualisations):

#### Answer 1: 

By creating 2 Pivot tables we are able to find out the top 5 most expensive average price suburbs are: Dalkeith, Peppermint Grove, City Beach, Nedlands, Cottesloe.

The 5 most affordable average price suburbs are: Medina, Haynes, Armadale, Kwinana Town Centre

##### Visualisation 1 : From two simple scatter plots we can see there are quite a big price differences between suburbs. Dalkeith has an average price of 1.95m where as Cottesloe has an average prices of 1.65m. And the most expensive suburb average price is nearly 100 times more than the most affordable suburb!!!



#### Answer 2: 

Buy creating a mask, there are 7 suburbs' average price fits into a budget of 840k to 870k:
Gwelup, Gooseberry Hill, Leederville, Darling Downs, Fremantle, North Perth, Alfred Cove.



#### Answer 3: 

Gwelup, sold over 175 houses over the years.

##### Visualisation 2 : By creating a count plot, it shows clearly that Gwelup sold most houses over the years.I understand it doesn't mean it is the most popular suburb amongst others, there might just because more houses in Gwelup. However it is always good to pick a suburbs with more information to look at.


#### Answer 4:

##### Visualisation 3 : By creating a relplot, it shows the relationship between landsize & price, however I have realised in the data there are some landsize figurs are way too large than the average, might due to the location. So firstly I had to further clean the data as any house with the landsize over 1000m2 is out of my consideration. 

From the second relplot, I can see the majority of the houses are between 400m2 and 600m2 range with a price range between 600k to 1M. We can also see bigger land size not necessarily mean higher price, it also relates to the house condition, location of the land, etc.


#### Answer 5:

From a simple pivot table we can see on average, Darling Downs & Gooseberry Hill are located more than 15km from the CBD, which are too far for my work and social life.

Suburbs which are less than 15km from CBD: Alfred Cove, Fremantle, Gwelup, Leederville, North perth.

#### Answer 6:

From the above analysis I have pick Gwelup as my entry point. The average of this suburb fit in the budget, it is relatively close to Perth CBD, and it is very active in the property market. 

##### Visualisation 4 : By using CategoricalColorMapper, I can group all the sold houses in Gwelup by nearest train station: Warwick & Stirling. As I wish to catch public transportation as much as I can.



#### Answer 7:

I'd like now to look more closely of the suburb Gwelup, where is it? Is it close to the freeway? Parks? Where are the houses being sold? How much are they?

##### Visualisation 5 : To answer above question, I think the quickest way to do is mapping all the Gwelup sold house data onto a map. In order to achieve so. I chose to use geopy, and using my hometown CHENGDU as a testing location, as this is my first time use this packages not sure if it will work. It will save me lots of time to make sure it is working before apply onto my dataset. 

##### *FYI:It will take a while for the code to run, when it apply geolocator to all the Gwelup house data*

##### By mapping the Gwelup data on to the map, I have re-coded my data, transformed the address format, then convert them into GPS coordinates, then apply geolocator on those coordinates to be shown on the map. by using with Folium.map.  I have now successfully tested my hometown and produced the map. Then I have further successfully mapped all the Gwelup house locations on a real map, with pop ups of each houses showing the price and landsize. 

### 5 Conclusion & Future Work:

By cleaning, understanding, investigating, recoding, and visualising the data, I have now got much better idea regarding the Perth property market. Most importantly I have successfully picked my starting point suburb (Gwelup), to spend time going through more detailed information about this suburb. 

It is also very straight forward and clear to see all these datas by mapping all the address on to a map, which is extremely helpful for knowing where are these houses are, what is around them, rather than by putting each address into google maps. 

However this is just a starting point, there are so much more to explore, I can add more info on the map pop up window as I wish, if it is 4x2 or 3x2 house? How many garages do they have? There are some other suburbs also worth further looking into even their average house price is outside my budget range.
I can also look into these suburbs, what are the relationship between price and build year. There are unlimited resource waiting for me to discover.




