# Food Sale Predictions
The creation of a model to help with predicting food sales at a grocery store based on almost 10 features.

### Author:
Clint Atterberry

### Business Problem:
Trying understand sales at a store depending on factors like the location and the type of item sold.

### Data:
A CSV file of the data has been uploaded [here](https://docs.google.com/spreadsheets/d/e/2PACX-1vQ9hM0TmmxdZ3whTnYlhnTpQR0bVvUFganKildu6gE-u4P5hMtFyr0VXkgZ6b8IfBvC148lRAvmgAXU/pub?output=csv).

## Data Dictionary
| Variable Name | Description |
| ------------- | ----------- |
| Item_Identifier | Unique product ID |
| Item_Weight | Weight of product |
| Item_Fat_Content | Whether the product is low fat or regular |
| Item_Visibility | The percentage of total display area of all products in a store allocated to the particular product |
| Item_Type | The category to which the product belongs |
| Item_MRP | Maximum Retail Price (list price) of the product |
| Outlet_Identifier | Unique store ID |
| Outlet_Establishment_Year | The year in which store was established |
| Outlet_Size | The size of the store in terms of ground area covered |
| Outlet_Location_Type | The type of area in which the store is located |
| Outlet_Type | Whether the outlet is a grocery store or some sort of supermarket |
| Item_Outlet_Sales | Sales of the product in the particular store. This is the target variable to be predicted. |

## Overview of Project
The project explored a Linear Regression Model and a Regression Tree Model. The data was first cleaned by removing the identifier variables, filling in missing weight values with the mean value, and lastly the column of the outlet size was dropped due to it being ordinal and missing so many (about 1/4th) of the data. Afterwards the data was explored looking for trends or standout bad statistics to deal with. The models were then created and compared with one another.

## Insights
### 1. The maximum retail price, or list price, of items has a very interesting histogram. I believe in further, more indepth studies, could conclude more detailed information based on splitting this information up into smaller groups.
![Insight Pic #1](https://docs.google.com/drawings/d/e/2PACX-1vRpXqKmF44iseKc0QFxDWqcNYZdqoYMmlLAjAZzdQqZCSSIHxPVZwEop7l6h7ly-VvLoa1PePXiOT1e/pub?w=480&h=360)

### 2. The sales data is skewed to the right, which would be expected. The mean sale price, however, is almost $400 more than the median.
![Insight Pic #2](https://docs.google.com/drawings/d/e/2PACX-1vQL43Zjh4Ri7uSkopj4oQ-dkeTyvDjD56zZWj6RC4bQSCndtnj8PX0grHizRYARrq07Jw70WDPSz1EK/pub?w=480&h=360)

## Summary of the Model Used
The Regression Tree Model was the final model used. Numerical, OneHot encoded categorical, and ordinal data were all used to complete the model. The max depth of the regression tree was 30 and there were 4,531 tree nodes. The optimized model, however, used only a depth of 5. Fitting the cleaned data to the model, a R-Squared value of 0.599 and a Root Mean Squared Error of 1093.013 were calculated.

## Recommendations
My recommendation is that the trained Regression Tree could very well be used, however, the R-Squared value of about 60% means that there is still more to the data to explain the sales price than the features we were able to explore. More data is needed in order to find a more accurate model.
