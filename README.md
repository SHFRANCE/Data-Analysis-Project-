# Data-Analysis-Project

We chose to work on the Zomato dataset, available at https://www.kaggle.com/shrutimehta/zomato-restaurants-data

The goal was to analyze our dataset by first performing exploratory data analysis. We then made model predictions by applying Machine Learning techniques in order to select the best one. With our final model, we created a Flask API to make some fun predictions about restaurants. 

**Description of the dataset**

We are using the Zomato Restaurants dataset and the Country Code dataset.
The first dataset contains information about 9951 restaurants from 15 countries.
Using the information about these 9951 restaurants, the challenge is to build a model to predict the `Average Cost for two` based on the following fields:

- **Restaurant ID** (int64) - ID of the restaurant
- **Restaurant Name** (object) - Name of the restaurant
- **Country Code** (int64) - Country code
- **City** (object) - City where the restaurant is located
- **Address** (object) - Postal address of the restaurant
- **Locality** (object) - Location of the restaurant in the city
- **Locality Verbose** (object) - Detailed description of the location
- **Longitude** (float64t) - Longitude of the location
- **Latitude** (float64) - Latitude of the restaurant
- **Cuisines** (object) - Types of cuisine served in the restaurant
- **Average Cost for two** (int64) - Average cost of a two-persons meal
- **Currency** (object) - Currency of the country
- **Has Table booking** (object) - Possibility of booking a table or not (Yes/No)
- **Has Online delivery** (object) - Possibility of online delivery or not (Yes/No)
- **Is delivering now** (object) - Possibility of delivery at the moment (Yes/No)
- **Switch to order menu** (object) - Possibility of ordering with a switch button (Yes/No)
- **Price range** (int64) - Price range of the restaurant
- **Aggregate rating** (float64) - Average rating of the restaurant
- **Rating color** (object) - Category of 5 colors representing the average rating
- **Rating text** (object) - Category of 5 attributes to qualify the quality of the restaurant
- **Votes** (int64) - Number of votes for the restaurant

The second dataset represents the country names of the first dataset associated to their country codes.

**Exploratory Data Analysis**

We first got to know the dataset by exploring the different columns and all the values they contain. 
After a deep analysis, we decided to make model predictions on _Average Cost for two_ using the following features: `City`, `Has Table booking`, `Has Online delivery`, `Price range`, `Type 0`, `Type 1`, `Type 2`, `Type 3`, `Type 4`, `Type 5`, `Type 6` and `Type 7`.

**Model Predictions**

The first part of making model predictions is to decide what we are going to predict and what features we are going to consider.  Once we did that, we tested different models by changing the features and the parameters and select the best one to make our final predictions.

**Conclusion**

After testing several machine learning models, we obtained a score of approximately 0.85 on the predicition of the _Average Cost for two_. We improved our model performance by 0.2. Our best model was a Random Forest model, when we used the parameters obtained with a Random Search Cross Validation. This the model we used to make our final predictions in the Flask API.

Enjoy !
