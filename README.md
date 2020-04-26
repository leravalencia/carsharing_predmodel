SUMMARY:
Car sharing is a growing industry along with the trending sharing economy.
Many factors can affect the profitability of this venture for individual car owners. While pricing is obviously a major factor, there are other variables that may affect profitability including car type, location, descriptions, reviews, and availability settings.
The goal of this research is to build a model that will allow owners to predict what cars will be the most profitable in their area, to regulate the prices and understand other factors that will allow them to earn more.
This project will be essential for everyone who owns a car that can be rented or everyone who is thinking to start car sharing as a side business.
DATA:
The data has been gathered from Turo.com (the leading car sharing web-site/app) and includes information about bookings for the last 12 months). It was gathered through the mix of scraping (BeautifulSoap and Scrapy) and API techniques. Every listing has unique set of parameters (https://turo.com/us/en/car-rental/united-states/los-angeles-ca/toyota/yaris/634022) that we put into a dataframe. It is a structured data frame with the rows as separate listing and columns as variables and outcome value. There are about 70 different variables and around 300,000 listings exist.
Data types:
1)	Numerical: price, year of the car, miles included per booking, delivery prices, prices of the extras, days that car was booked in the previous period during the last 12 months, days unavailable, number of seats, trip count, etc.
2)	Categorical: type of the car, type of the fuel, convertible or not, is it a frequently booked or not, any age restrictions, availability, color, etc.
3)	Text: listing description, FAQ
4)	Geographical: Latitude and Longitude for every listing, State, City, Zip Code
 
PROJECT STAGES:
1.	EDA
We are going to clean all numerical variables, windsorize and normalize them. For the categorical variables we will use one hot encoding encoding and for the location we will do unsupervised clustering with k-means and hierarchical clustering to see what will work better. We’re going to check the quality of the clusters with the silhouette score.
For the text variables we’re going to work with natural language processing algorithms such as parsing, tokenization, bag of words, TD-IDF  and to build nlp model.  
We will do feature engineering with psa and umap.
2.	MODELING
The prediction will be made with supervised learning model such as OLS, Random forest and support vector machine. 
Outcome variable will be the potential earning per month, in $. We will check the prediction accuracy with cv score through different models.
3.	DELIVERABLES
Ideally, we would like to develop a dashboard where you can put your car model, location (or zip code) and get information of how much income per month you can get with your car in your area.
Also, we would like to make an additional output with TOP 5 competitors and their listings details.
 
CHALLENGE:
The primary challenge for this project is to include NLP processing of descriptions and reviews. These variables will be added to the categorical and numerical variables with the goal of providing additional guidance for car owners to consider supporting owners in maximizing their profitability. Our expectation is to define an impact which might be hard to reveal. We’re going to overcome this by trying different approaches and use different bag of words sets and techniques from NLP section in order to find out the most efficient set of words or amount of words that helps to earn more money on renting the car.

