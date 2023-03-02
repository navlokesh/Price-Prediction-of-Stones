# Price-Prediction-of-Stones
A cubic zirconia manufacturer has a dataset containing the prices and other attributes of almost 27,000 cubic zirconia (which is an inexpensive diamond alternative with many of the same qualities as a diamond). The company is earning different profits on different prize slots. Our task is to predict the price for the stone on the bases of the details given in the dataset so it can distinguish between higher profitable stones and lower profitable stones so as to have better profit share. Also, to provide the best 5 attributes that are most important.

## Univariate, Bivariate Analysis and Exploratory Data Analysis.
Exploratory data analysis was done to understand the spread of the data using various univariate (Histrograms, skewness checkes, boxplots, variance, etc) and bivariate (pairplots, heatmap, covariance, correlation, etc) analysis.

### Null value imputation was done using median of the variable.

### Checking for zero values in the columns:
There are 9 rows containing value of '0'
All these zeroes are seen in the columns x, y, z
Since x, y and z are the length, width and height of cubic zirconia, it doesn't make any sence to have the value as zero
Considering that there are only 9 rows with zero values, we can go ahead and drop them.

### Encoding categorical variables:

Since only numerical variables can be fed to a Machine Learning model, we need to convert out catergorical variables into numerical values using one-hot encoding or label encoding.

### Data scaling:
The indpendent attributes have different units and scales of measurement
It is always a good practice to scale all the dimensions using z scores or someother method to address the problem of different scales
Data was scaled using ZScore slacing method.

## Model Building:

The data was split into training and test sets and training data set was used to build a Linear Regression model.

### Checking feature importance based on magnitude of co-efficients:

Based on the trained model, co-efficients were checked. Below are the co-efficients of out linear regression model:

The coefficient for carat is 1.3246892181912295
The coefficient for cut is 0.013093459981448966
The coefficient for color is -0.11889912715564042
The coefficient for clarity is 0.1269400057424199
The coefficient for depth is -0.05500369475854898
The coefficient for table is -0.052472462400946544
The coefficient for x is -0.33171719200557825
The coefficient for y is 0.0017697139195367488
The coefficient for z is -0.007403794992948854

## Model Evaluation:
Model evaluation was done using R-squared and Root Mean Squared Error (RMSE) metrics.

## Inference:
Below are the most importance variables for the prediction of price for cubic Zirconia as these have higher weights in the prediction equation:
• carat
• X
• Clarity
• Color
• Depth
From the correlations between the different attributes, we can see that the price is highly correlated with the dimensions and the Carat of the Cubic Zirconia.

The stones with higher dimensions and Carat will give us better profits and these are highly correlated with Price of the stones.
