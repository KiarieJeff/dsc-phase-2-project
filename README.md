## Analyzing House Sales in a Northwestern County Using Multiple Linear Regression Modeling

![](Data/img1.jpg)

Photo by <a href="https://unsplash.com/@jimmy_conover?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Jimmy Conover</a> on <a href="https://unsplash.com/s/photos/neighborhood?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

#### Overview

In this project, we will apply statistical analytic methods to comprehend the variables affecting home sales in a certain county in the northwest.  Statistical analyses take into account the inherent uncertainty in data. They provide measures of uncertainty, such as p-values, confidence intervals, and standard errors, which allow us to assess the reliability and robustness of our findings.This study intends to investigate the links between numerous independent variables and the dependent variable of home sales by using multiple linear regression modeling.We will be using regression coefficients because they provide specific numerical values that quantify the relationship between the independent variables and the dependent variable.

Overall, this analysis aims to advance knowledge and comprehension of the northwest county's housing market by illuminating the variables that have a significant impact on sales and possibly assisting various stakeholders in streamlining their strategies and decision-making procedures.

#### Business Understanding

The primary objective of a real estate company that specializes in helping homeowners buy and sell homes is to offer beneficial services that aid homeowners in maximizing the value of their properties. A significant business problem to address is to be able to advise clients on house modifications and their potential impact on the assessed worth of their homes.

#### Data Understanding

 The dataset contains 21 columns and 21,597 entries (rows).
 The columns in the dataset are as follows:
  - `id`: Unique identifier for each entry (21597 non-null integer values).
  - `date`: Date of the house sale (21597 non-null object values).
  - `price`: Sale price of the house (21597 non-null float values).
  - `bedrooms`: Number of bedrooms in the house (21597 non-null integer values).
  - `bathrooms`: Number of bathrooms in the house (21597 non-null float values).
  - `sqft_living`: Square footage of living space in the home (21597 non-null integer values).
  - `sqft_lot`: Total lot area in square feet (21597 non-null integer values).
  - `floors`: Number of floors in the house (21597 non-null float values).
  - `waterfront`: Indicates if the house has a waterfront view (19221 non-null object values).
  - `view`: Quality of view from house (21534 non-null object values).
  - `condition`: Condition of the house (21597 non-null object values).
  - `grade`: Grade given to the house (21597 non-null object values).
  - `sqft_above`: Square footage of house apart from basement (21597 non-null integer values).
  - `sqft_basement`: Square footage of the basement (21597 non-null object values).
  - `yr_built`: Year the house was built (21597 non-null integer values).
  - `yr_renovated`: Year the house was last renovated (17755 non-null float values).
  - `zipcode`: Zip code of the house location (21597 non-null integer values).
  - `lat`: Latitude of the house location (21597 non-null float values).
  - `long`: Longitude of the house location (21597 non-null float values).
  - `sqft_living15`: Living area of the 15 nearest neighbors in square feet (21597 non-null integer values).
  - `sqft_lot15`: Lot area of the 15 nearest neighbors in square feet (21597 non-null integer values).

 The presence of `non-null` values indicates the number of valid (non-missing) entries in each column. Some columns, such as `waterfront`, `view`, and `yr_renovated`, have missing values denoted by the difference between the non-null count and the total count (21597).

 Here we can see some of the categorical data are in form of strings denoted by object Dtype and the numerical are in form of int64 or float64. But not all int64/float64 Dtype are numerical because we have for instance yr_built which is a categorical Dtype but it is expressed in int64/float64.We can also see that sqft_basement is expressed as strings (categorical variable) instead of numeric which we will fix later on.

 Some of the categorical data we have include: id,date,waterfront,view,condition,grade,yr_built,   yr_renovated,zipcode