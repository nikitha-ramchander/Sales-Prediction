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

Data Visaluizations
>I came up with a few graphs that helped me better understand the data. 
![Picture1](https://user-images.githubusercontent.com/77766107/110861673-542cbc80-8273-11eb-81a6-c3dfbe2f7bf3.png)
>This graphs shows the price range for the amount of outlet sales being done. There are higher bars in the really low price range meaning that most items are sold under $200.

![Picture2](https://user-images.githubusercontent.com/77766107/110861687-5bec6100-8273-11eb-9306-87e4dc7dd7aa.png)
>Fruits and Vegetables has the most sales coming in at over 2.5 million. Seafood has the least amount of sales at around one hundred thousand.

![Picture3](https://user-images.githubusercontent.com/77766107/110861700-5ee75180-8273-11eb-8502-d4d5be39ff7c.png)
>On average each Supermarket Type3 makes a total sale of over 3500 which is the most of the 4 outlet types. Grocery Outlet Type makes less than 500 for each outlet.

![Picture4](https://user-images.githubusercontent.com/77766107/110861715-63136f00-8273-11eb-8f2e-1f66ae6404b9.png)
>The year 1985 had the most sales and the year 1998 had the lowest sales. From this graph you can also tell the years between 1987 and 1997 has no data, as well as years 2000, 2001, 2005, and 2006. I'm assuming data wasn't gathered for those years.

![Picture5](https://user-images.githubusercontent.com/77766107/110861729-673f8c80-8273-11eb-9358-b9b34977b012.png)
>Overall all Item Types are fairly consistent around the 2,000 mark which back up our finding in the previous graph. The lower 25% has a short distance meaning that the data is tightly packed and a lot of our data has low sale amounts. The top 25% has varying degrees and is more spread out showing us higher ranges of sales. For Item Types of 'Fruits and Vegetables' and 'Household' they have the most spread out outliers which means that there were sales in the $12,000 range.

![Picture6](https://user-images.githubusercontent.com/77766107/110861741-6c044080-8273-11eb-9bfd-8d05621f4abe.png)
>This heatmap shows the correlation of all features. The darker blue shows a perfect positive correlation, all-white show a perfect negative correlation, and light blue would show no correlation. The darkest blue or '1' correlation is the correlation of the feature in itself and that is why it is a perfect positive correlation. The next strongest positive correlation is between 'Item Outlet Sales' and 'Item MRP'. This might be the case because if we know the maximum retail price (list price) of the product then we can predict how many total sales there will be of each product. 'No Weight Flag' and 'Outlet Establishment Year' columns have a fairly strong negative correlation, meaning when one increases, the other decreases. A reason for that could be the year 1985 had no record of Item Weight for any of the Item Types.

![Picture7](https://user-images.githubusercontent.com/77766107/110861750-6f97c780-8273-11eb-9a88-ad165c030c1c.png)
>The top 3 highest sales of item types in Supermarket Type 3 are Breakfast, Fruits/Vegetables, and Dairy.







