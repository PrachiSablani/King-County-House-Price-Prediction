# King-County-House-Price-Prediction
Supervised Machine Leraning | Regression | Predictive Analytics |Python

The objective of this project is to predict house prices in the King County, Washington from the transaction details of houses sold previously.

The data has 11000 records with 24 features like number of bathrooms, number of bedrooms, location information, zone code, block group, view type, transaction date, build date, etc.

To approach this project, I followed all the Data Science pipelines right from Exploratory Data Analysis, Feature Engineering, Feature Selection, and Model building and finally prediction of house prices for unseen data.

STEP 1 : Exploratory Data Analysis(EDA)

I started the project with Exploratory Data Analysis where I checked data types, missing values, numerical features, distribution of numerical features, categorical features, cardinality of categorical features, outliers, relationship between dependent and independent variable, distribution of independent feature

STEP 2: Feature Engineering

Firstly, I handed missing values where I imputed different values suitable for that particular feature.
Then I converted continuous numerical features to log normal form and standardized the data and took values up to 3 std deviation to deal with outliers. I did the one-hot encoding to convert categorical features to numerical form and applied feature scaling.
Also, I removed some unnecessary features like the property id which was not adding any useful value to the house price.
I also came up with new features, for example I subtracted the year in which the houses were sold to the year they were built and created a new feature. Also, I fetched out the month from transaction dates to check month-wise transactions.

STEP 3: Feature Selection

I applied Pearson’s Correlation matrix and Random Forest for checking the feature importance and selecting useful features.
Finally, out of 24 I was left with 7 useful features to predict the house prices.

STEP 4 : Model Building

I split this data into training and validation set to track the performance of my model using cross-validation technique.

First, I started with linear regression as a baseline model, which gave me a R-squared value of 0.73. Then I moved towards more sophisticated models like random forest and XGBoost. And finally, after 5-fold cross validation I got the best mean R-squared value of 0.83 for house price prediction with XGBoost model.

For more details, follow the comments, results and next steps in the House_Price_Prediction.ipynb file.



