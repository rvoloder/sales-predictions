# sales-predictions
Predict Sales Outcomes
# Identify Key Factors Affecting Sales Outcomes on Items
## Using analytic graphics to find which factors most affect sales outcomes. Then use predictive modeling to make sales predictions for items in the future. 

**Author**: Rija Voloder

### Business problem:

This project attempted to aid a company who sells various food items at various store locations. The goal was to find any major factors that could be affecting item sales and to create a model that would allow for good predictions for future sales on each item. 


### Data:
The project allowed us to find a strong correlation between the Maximum Retail Price of each item and it's corresponding sales. Based on our outliers we were also able to determine that most of the company's "high sales" items were found in the "Household," "Fruits and Vegetables," and "Snack Food" categories. 


## Methods:
- The data was first analyzed for missing data. The missing store sizes were figured out based on analysis and linking different data points that were available.
- The numeric missing data was left alone as to prevent data leakage.
- A variety of visualizations were then performed on the data to derive some more specific insights on various factors affecting item sales. 
- Ordinal data was encoded accordingly.
- The data was then split into training and target data using a train_test_split.
- The data was then processed with two different pipelines. The numeric pipe used a mean imputer to imput missing values that were then scaled down using a standard scaler. The categorical pipe used a frequency imputer to fill in any remaining missing categorical data as well as a OneHotEncoder to convert nominal values into numerical ones.
- Two tuples were than put in place to hold the data and place into a column transformer so the data could be finally processed.
- Two models were then built to predict data. The first, a linear regression model, performed poorly on the data (evaluated based on r2 and rmse scores). 
- The second, a simple regression tree model, performed much better once maximum depth was adjusted. The model provided has a low variance and low bias and can give good predictions for future item sales. 

## Results:
The analysis conducted provided quite a few different observations from the data. I found that Tier 3, Medium Sized stores, and Supermarket Type 3's seem to have items with the highest sales performance. I also found the Maximum Retail Price seemed to be highly correlated with the sales of that item (based on a correlation heatmap).  The graphics also revealed (as stated in the data portion) that the items with the highest sales were in the "fruits and vegetables," "household," and "snack food" items. 
### The images below show evidence of the above results:


#### Outlet Size, Outlet Type, and Location Type vs. Item Sales

Medium Sized Stores seem to be performing the best. 

<img width="402" alt="Outlet Size" src="https://user-images.githubusercontent.com/101893905/165898328-22f7293e-0c91-44de-afe9-d535567223c2.png">

Supermarket Type 3 Stores sales' are outperforming other types. 

<img width="403" alt="Outlet Type" src="https://user-images.githubusercontent.com/101893905/165898972-e04514be-ec19-479d-b001-196d1da96201.png">

Tier 3 Location types seem to have the most high-performing items. 

<img width="403" alt="Outlet Type" src="https://user-images.githubusercontent.com/101893905/165899563-c2d8568d-02eb-4cbb-9ca3-45024c397612.png">


#### Item Category Sales

The categories with the highest performing items are "Household", "Fruits and Vegetables", and "Snack Foods".

<img width="403" alt="Item Type" src="https://user-images.githubusercontent.com/101893905/165899981-f0211047-dece-4d1f-8b9e-9369dff53f09.png">

## Recommendations:

From the analysis provided above and within the file, I would recommend that the company figure out exactly which items are the highest performers. It would then be a good idea to evaluate which components seem to be making those items outperform others. Is it something the company can control (their display, item visibility, etc.) or something that is linked more to the individual product (brand recognition, advertising, etc.). They can then act accordingly. It would also be wise to figure out why certain location types or store types seem to be performing better and try to implement some of those aspects in other stores or for other items (design, location selection, etc.). Any of these factors could lead to improved sales numbers in the future. 

The model is also able to provide predictions based on the current data and can be improved as more data is added. 


## Limitations & Next Steps:

The biggest limitation in this project is the lack of individual product name or description that would have allowed us to make further insights into causation of high or low performance. Missing data was also another challenge but was dealt with appropriately.

In the next steps, the individual items with high sales should be looked at and analyzed more deeply to find links and reasons for their high performance, concepts that can be carried over to other stores and items. The model should also be used to predict the sales of future items added to the store and to compare whether making certain changes do indeed created better performance and higher sales predictions for other "low performers".

### For further information


For any additional questions, please contact **rijavoloder@gmail.com**
