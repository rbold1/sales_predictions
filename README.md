# sales_predictions
Project goal was to predict food item outlet sales:

Here is an overview of the data columns, as well as a definition of each column (to help define what the column represents).

![image](https://user-images.githubusercontent.com/89427707/136724213-7245ae6d-0788-4d4b-a616-4d675cf1f1a7.png)

![image](https://user-images.githubusercontent.com/89427707/136724161-ab7a5dea-af41-4fb4-bc57-82d041176d1a.png)

Once data was loaded, it was cleaned of duplicates, missing data, and inconsistent column headers.

With clean data, it was time to analyze the data looking for trends (using correlation) with a goal of understanding which data fields would have an impact on sales.

![image](https://user-images.githubusercontent.com/89427707/136724997-004e7c78-d906-49c3-8611-b6da8659bfc6.png)

Figure:  Heat map shows best correlation between Item_Outlet_Sales and Item_MRP



Given the correlation between Item_Outlet_Sales and Item_MRP, I wanted to dig deeper into the various items within the Item_MRP data.  

![image](https://user-images.githubusercontent.com/89427707/136727206-795b8afd-0e65-4fe8-b44f-3e1945000c1b.png)

Figure:  The mean sales by item type did not provide any insights that stood out, although there were considerable outliers.

![image](https://user-images.githubusercontent.com/89427707/136725652-55874c97-34a1-4cb5-a96e-c01a4b357e80.png)

Figure:  There were 16 different items within the Item_MRP data, although the mean max retail (list) price did provide any visual insights that would help predict sales.

Given that the data visualizations did not offer any obvious insights into sales predictions, we turned to ML regression models to look for insights, including:

1) Linear Regression Model
2) Simple Decision Tree Model
3) Bagged Tree Model
4) Random Forest Model

After further manipulating the data so that the computer could perform ML models (one hot encoding), data was run through the above supervised learning models.  The Random Forest Model, despite being overfit, yielded the best fit of the four models (see correlation and RMSE values below).

R^2 train:  Suggests that the model could account for 90% of the variation on the training data.

0.9370377920925759

R^2 test:  Suggests that the model could only account for 55% of the variation on the test data.

0.551683795847306

RMSE:  Suggests that the range of mean predicted values have a variance of $670 vs. actuals.

670.0781825468398




