# Crop_Production_India

# Overview
This dataset provides a huge amount of information on crop production in India ranging from several years. Based on the Information the ultimate goal would be to predict crop production using powerful machine learning techniques.
In this case after a indepth exploratory analysis I applied a random forest on the two most cultivated crops, being Rice and Wheat. On the test dataset I obtained a correlation of
around 98%

# Data Preprocessing
1. drop the nan on production (there were only 2k missing values on more than 200k)
2. check for correaltion between numerical variables (not found)
3. divide according to macrogroups (as suggested by vivekkumarprajapati) both states and crops. The states were divided into 6 macro zones, and the crops in 8 crop types.
4. eliminate the last year (2015) as it was clearly an outlier (the production for most crops dropped to 1/100)
5. formatting the year column to transform it in a regression problem (using the [shift() function](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.shift.html) from Panda) 
![](https://github.com/luigigreselin/Crop_Production_India/blob/main/images/crop_per_region.PNG)

# Analysis
After having noticed that wheat and rice are the two most common crops, I proposed a random forest regressor. On the test dataset the correlation was around 98% for both wheat and rice

![](https://github.com/luigigreselin/Crop_Production_India/blob/main/images/rice_production.PNG)
![](https://github.com/luigigreselin/Crop_Production_India/blob/main/images/wheat_production.PNG)

# Data

Data can be found [here](https://www.kaggle.com/abhinand05/crop-production-in-india) 
