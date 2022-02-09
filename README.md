# Intelligent-House-Price-Prediction <br/>

![House_Price_pred_snap](https://user-images.githubusercontent.com/82858787/153093693-a7098bd6-da2d-444c-a156-5eadc56e6038.png)


A sneak peek into the Airbnb activity in Seattle, WA, USA <br/>

## Context 

In this project I will be developing a deep learning model to predict the prices of houses to give insight for future hosts at Seattle Airbnb. I have described my own experience in building this model and shared the source code along with libraries and functions used. For having a hands-on experience in building this project, it is necessary to know python and the basics of machine learning. I have kept the model simple and easy to understand for beginners to have a great coding experience 

## Problem Statement and Motivation of the Project
The Dataset I have used here is Seattle Airbnb Open Data. As part of the Airbnb Inside initiative, this dataset describes the listing activity of homestays in Seattle, WA.

The desire of this work is to answer these questions: <br/>
Can you describe the vibe of each Seattle neighborhood using listing descriptions? <br/>
What are the busiest times of the year to visit Seattle? By how much do prices spike?<br/>
Is there a general upward trend of both new Airbnb listings and total Airbnb visitors to Seattle?<br/>

## Dataset
In this project, we use the Seattle Airbnb Open Data [link to the dataset] (https://www.kaggle.com/airbnb/seattle)

## Breakdown of this Project: <br/>
• Exploratory Data Analysis <br/>
• Sentiment Analysis of Reviews <br/>
• Data Preparation <br/>
• Feature Extraction <br/>
• Feature Scaling <br/>
• Encoding Categorical Features <br/>
• Reading the images <br/>
• Employing the model <br/>

##  Exploratory Data Analysis: <br/>
* The following features were analyzed categorically with their respective prices using boxplot:  <br/>
Room type, Property type, Bed type, Host_is_superhost  <br/>

* Count Plot is used to analyze: <br/>
Host_response_time, Neighbourhood_group_cleansed, review_scores_rating  <br/>

##  Sentiment Analysis of Reviews: <br/>
* The reviews.csv file is used for sentiment analysis.<br/>
* The polarity and the Sentiment type is generated using the textblob module. <br/>
* The average polarity of a listing is generated to understand the customers’ views.<br/>

##  Data Preparation: <br/>
* Cleaned our target variable - price by casting the data type of price column from string to float.<br/>
* Filled Null values of categorical variables with NULL and numerical variables with mean value. <br/>
* Applied Log transformation of variable price to reduce skewness of the data. <br/>

##  Feature Extraction: <br/>
![image](https://user-images.githubusercontent.com/82858787/153087031-16987dc4-540d-4073-8075-aabfbf4fae12.png)


* A new dataframe with the features of our interest is created with the help of our Exploratory Data Analysis. <br/>
* The selected features are: <br/>
'property_type', 'room_type', 'bathrooms', 'bedrooms', 'bed_type',  'accommodates', 'guests_included','review_scores_rating', 'neighbourhood_group_cleansed', 'log_price'<br/>


##  Feature Scaling: <br/>
* StandardScaler() from the sklearn module is used to transform the data such that its distribution will have a mean value 0 and standard deviation of 1.<br/>
* Features are scaled so that every variable contributes to the model equally.<br/>

##  Encoding Categorical Features: <br/>
* ML models and Neural Networks require all input and output variables to be numeric. <br/>
Hence, the categorical variables should be encoded before fitting and training.<br/>
Hence, the categorical variables should be encoded before fitting and training.<br/>
* We use the OrdinalEncoding() from the sklearn module for this process. <br/>
   The following features are encoded:'property_type', 'room_type', 'bed_type', 'neighbourhood_group_cleansed' <br/>


##  Reading Images: <br/>
* The column ‘picture_url’ contains the url for corresponding pictures of listing posted by the host. <br/>
* Using the urllib and skimage module the images from the web pages are read and stored in an array ‘images’. <br/>

##  Employing the model: <br/>
![Price_pred_model_image](https://user-images.githubusercontent.com/82858787/153095664-a12426a1-67b4-4b7f-816b-47fa19a17783.png)


* For Numerical data, we employ ANN to train the model 
* For images, we employ CNN to extract features 
* We concatenate the individual outputs and utilise ANN for final prediction of price.

##  Conclusion: <br/>

• We learnt how to learn/extract infromation from raw, unstructured data.<br/>
• We have developed a deep learning model to predict house prices given numerical data as well as images <br/>

