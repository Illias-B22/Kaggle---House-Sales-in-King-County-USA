# Kaggle---House-Sales-in-King-County-USA

The goal of this project is to predict the price of houses based on factors such as the condition of the house, number of floors, bedrooms and bathrooms 


Procedure

1. Checked all columns for missing and null values - quite fortunate as dataset contains neither of these. Removed ID columns as contains a high amount of duplicates. Also, converted Date column into a dtype format from an object 

2. Split Price feature into bands to better visualise the spread of house prices. EDA shows that 67% of houses are sold in band 3-6 (200k - 600k), with the highest number of houses 19.7%, located in price band 4 (300k - 400k)

3. We then move on to modelling. 
LR: We start our modelling off with Linear Regression. This gives us a score of around 58% which is only slightly better then randomly guessing.

KNN: Firstly, we scale the data using a StandardScaler as it is nesscessary to scale the features in order to make sure that one featrure does not outweigh another based on its scale. We obtained a slightly improved score of 59%.

RandomForest: Finally we implemented a RandomForest which performed the best with a score of 63%. Applying a   GridSearchCV to optimise hyperparameters we reached an improved score of 66%. After tweaking the hyperparamters by limiting the n_estimators to 150 and increasing the max_depth, this gave us our higest score yet of 73%. 


Data Understanding
id - unique identified for a house
date - house was sold
price - is prediction target
bedroomsNumber - of Bedrooms/House
bathroomsNumber - of bathrooms/bedrooms
sqft_livingsquare - footage of the home
sqft_lotsquare - footage of the lot
floorsTotal - floors (levels) in house
waterfront - has waterview from the house
view - Has been viewed
condition - How good the condition is ( Overall )
grade - overall grade given to the housing unit, based on King County grading system
sqft_above - square footage of house apart from basement
sqft_basement - square footage of the basement
yr_built - Built Year
yr_renovated - Year when house was renovated
zipcode - zip
lat - Latitude coordinate
long - Longitude coordinate
sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbours
sqft_lot15 - The square footage of the land lots of the nearest 15 neighbours
