# Sales Predictions Project 

This project analyzes the prediction of sales for food items sold at various stores. The goal is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.

Objectives:  
1. Exploratory Data Analysis 
   
   -Data Cleaning 
   
   -Data Visualizations 
   
2. Build Machine Learning Models 
  
   -Random Forests 
  
3. Provide Recommendations 


Data Cleaning
>Using python I loaded the data set and imported libraries, Pandas, and Numpy to start exploring the data. The first few steps required validating data types and checking syntax errors. While all data types were consistent, there were missing values in two columns. Before moving forward, the syntax in the Item_Fat_Content column had several inconsistencies that needed to be changed. For example, the strings were 'LF', 'reg', low fat' that needed to be mapped into a dictionary under 'Low Fat' or 'Regular'. 

>Now we can move on to handling the missing values.  There were missing values in 'Outlet_Size' and 'Outlet_Type'. Before filling in the missing values, I created a No Flag column in case I want to check how my inputted values affected Machine Learning Models. For missing values in the Outlet Size column, I noticed all the missing values for Outlet Size fell under 'Tier 2' or 'Tier 3' in Outlet Location Type. 'Tier 1' had no missing values, only values of 'Small' or 'Medium'. For 'Tier 2' it had values for 'Small' and missing values. Lastly, 'Tier 3' had values for 'Medium' and missing values. With that, I inferred that values missing for 'Tier 3' should be filled in with 'High' Outlet Location Type and values missing for 'Tier 2' should be filled in with 'Medium' Outlet Location Type. For missing values in the Item Weight column, It wouldn't make sense to fill in the missing values with '0'. Decided to take the average Item Weight for each Item Type and fill in the missing values with those numbers.
![DataTypes](https://user-images.githubusercontent.com/77766107/110859263-0a8ea280-8270-11eb-9863-19c03a8fa765.png)

Data Visaluizations
>I came up with a few graphs that helped me better understand the data. 
