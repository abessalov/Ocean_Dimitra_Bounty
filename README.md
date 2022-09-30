# Ocean Protocol :: Dimitra Bounty Phase 2

## Files description

- 1_Feature_Selection.ipynb - code with the analysis and models for the first part. 
- 2_Time_Series.ipynb - code with the analysis and models for the second part.
- Ocean_Presentation.pdf - final solution presentation.
- startup.py - initial script that run in every notebook when started.

## Task description

### Challenge Dataset
The dataset provided for this challenge can be downloaded at no cost on the Ocean Market ( Polygon Network) by accessing the following link: https://bit.ly/dimitra-p2.

It provides crop yield data for soybean in the 46 districts of the Madhya Pradesh State, India for a period of 10 years, between 2010-2019.

It also provides MODIS satellite data for the same 10 year period, for the months June - November, for the following features:
- NDVI: Normalized Difference Vegetation Index
- LAI: Leaf Area Index
- ET: Evapotranspiration
- LST: Land Surface Temperature
- RF: Rainfall
    
Note: The soybean crop duration in Madhya Pradesh is from June to November hence the data extracted for the variables is from June to November month.


### Challenge
Given the (target) soybean yields and the satellite data (features), we ask you to:
- Rank the factors that affect yields and build a simple model to predict yields based on the features.
- Identify and explain any trends in the yields over the 10 year period.

<b>Recommended Procedures</b>

You MUST AT LEAST perform the graphical methods described below in order to be considered for the competition.

<b>Understand the data</b>

Learn the meaning of the satellite data features.
Understand that the satellite data features not only include information about soybean crops but also about any other vegetation, soil and/or land-cover/land-use present in the districts.

<b>Feature Selection Analysis</b>

Graphical Method: Based on graphs of the features (NDVI, LAI, ET, LST, RF) values versus time and of the target (yield) values versus time, can you rank (from most positive to most negative) the correlation between each feature and the yield? Can you rank the features correlations between each other?

Potential Advanced Methods**: Filter Methods (Univariate selection (ANOVA), Chi Square, based on correlation, based on variance); 
Wrapper Methods (Forward Selection, Backward Selection, Exhaustive Search); Embedded Methods (Lasso/Ridge (using ElasticNet), 
Tree based selection, Regression coefficients), Hybrid Methods (Feature shuffling, Recursive feature elimination, Recursive feature addition), PCA.

<b>Time Series Analysis</b>

Graphical Method: In the above graphs, can you identify any seasonal (intra-year), cyclical and/or secular (long-term) trends? Do the 
intra-year shapes of the curves change from year to year?(compare the slopes and curvatures of curves for the various years). What 
are the reasons and consequences of the variations and trends?

Potential Advanced Methods**: To develop a model to predict future yields consider ARIMA, Prophet, Vector Autoregression, 
Catboost Regressor, any regressor.
** Feel free to augment the challenge dataset (see below) with any open source real-data dataset of your choice. If you do so, please 
reference the data and provide a link to it. Bonus points will be awarded for publishing the referenced data on the Ocean Market!!!


### Evaluation
A panel of evaluators from Ocean and Dimitra will independently review and rank submission entries selecting 1st, 2nd and 3rd place winners. The selection will be announced publicly and the community will be invited to vote for the Community Choice Award winner.

<b>Evaluation Criteria & Scoring</b>
Minimum requirement: Plotting all the features (NDVI, LAI, ET, LST, RF) and the yearly yields versus time (10 years range).

<b>Feature Selection Analysis:</b>
- 15% - Performing the Graphical Method for the Feature Selection Analysis and interpreting the results (textual - no code required).
- 10% - Augmenting the data, specifically, finding and using additional open source datasets of relevant real data to complement the given data (performing any valuable data preprocessing, if necessary).
- 10% - Deriving a simple empirical formula to predict yields as a function of the features, if possible from your above Graphical Method analyses or otherwise.
- 15% - Training a machine learning model to calculate/predict yields based on features data. Providing a file with your code with comments explaining your pipeline’s flow. Explaining your criteria for dealing with any of the following items, whenever applicable: selected algorithm(s), hyperparameter values, ensemble method, cross validation, method for determining your model’s accuracy, and others.

<b>Time Series Analysis:</b>
- 15% - Performing the Graphical Method for the Time Series Analysis and interpreting the results (textual - no code required).
- 10% - Augmenting the data, specifically, finding and using additional open source datasets of relevant real data to complement the given data (performing any valuable data preprocessing, if necessary).
- 10% - Deriving a simple empirical formula to predict future seasons yields as a function of features and yields data, if possible from your above Graphical Method analyses or otherwise.
- 15% - Training a machine learning model to predict future seasons yields based on features and yields data. Providing a file with your code with comments explaining your pipeline’s flow. For unfinished work partial credit will apply.
