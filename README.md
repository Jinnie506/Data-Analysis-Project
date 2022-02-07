
# ANALYZE SUPERMARKET DATA ACROSS THE COUNTRY FOR COMPANY XYZ

Company XYZ owns a supermarket chain across the country. Each major branch located in 3 cities across the country recorded sales information for 3 months, to help the company understand sales trends and determine its growth, as the rise of supermarkets competition is seen to increase. 

# Project Steps

### Step 1: Loading the dataset.
The datasets from the three branches is first combined together using the glob library.
The combined data is saved in my directory as Combined Data.csv and it is loaded to pandas using the pd.read_csv() method. It is then saved as "data" in pandas

### Step 2: Data Exploration
Several libraries are imported to help with data exploration and they are: pandas, numpy, matplotlib, seaborn and warnings. 
1.	The head() function is used to read the first few rows of the dataset
2.	The number of rows and columns are checked using the shape attribute
3.	Also, the names of the columns in the datasets are checked using the columns method
4.	The general statistical summary is checked using the describe function
5.	A more detailed summary is accessed using the info function
6.	The data is checked for the presence of missing values using the isnull() function and is found to be free of missing values.

### Step 3: Dealing with Date and Time Features
The dataset has 2 columns, Date and Time which had the Object data type. The data type has to be changed using the  pandas .to_datetime() feature to enable them become datetime data types. This  is done using pd.to_datetime().
Similarly, new columns are created from date and time. These columns are day, month and year, containing the day month and year found in the data column. Also, a new column, hour is created from the time column and named hour.
The unique method is used to find the number of unique hours in the Hour column.

### Step 4: Unique Values in Columns
Categorical Columns (Columns that have the Object data type) are gotten and their unique values are also derived using the unique(), nunique() and value_counts() functions. 

### Step 5: Group by Aggregations
The Group By function is also explored and they following were obtained:
•	The City Column was grouped and aggregated by Mean and Sum
•	The City with the highest total gross income, highest unit price and highest quantity were obtained.

### Step 6: Data Visualization
Seaborn Visualization Library is used to graphically explore the dataset. The Branch, City and Payment Columns are explored using Seaborn’s countplot to determine the most frequent.  The Product Line is also explored to determine the Highest and Lowest Sold product line.
Similarly, a countplot of the product line grouped by the Payment method using Hue is visualized, as well as the Payment method grouped by the Branch. Other columns were also visualized using Bar plot, Catplot, Bar Chart and Seaborn’s distplot to check the distribution of the Unit Price column.

# Insights

* There are 1000 sales in the company (1000 Unique Invoiced). 
* All 3 branches acquire an average total of 116268 naira and the maximum total sales obtained was 375354 naira.
* Lagos recorded the highest number of sales followed by Abuja and then PortHarcourt. Upon further analysis, it was realized that although Port Harcourt had the least number of sales, it had the highest amount of gross income. 
* Amongst the three main branches, the branch in Port Harcourt generates the most revenue for Electronic accessories, Fashion accessories, Food and beverages, while the branch in Abuja generates the most revenue for Health and beauty, Sports and travel, and the branch in Lagos generates the most revenue for Home and lifestyle products.
* Port Harcourt also has the highest Gross income, while Abuja has the lowest leaving Lagos In between.
* Port Harcourt generated the highest overall revenue out of the three cities.
* Most Customers buying Food and beverages prefer to use their cards as a means of payment, while most customers buying Fashion accessories, Home and lifestyle, Health and beauty products prefer to pay for the products electronically, most customers buying Electronic accessories, Sports and travel products come to the supermarket with their money.
* Out of the three main branches, branch B which is located in Abuja received the lowest rating from customers.


# Future Work

Predictive Analysis could be included by building a machine learning model that would be able to predict the product that would generate the most revenue in each of the three branches at a particular point in time in company XYZ.


# Standout Section

Additional plots were generated to shows the relationship between the continuos variables in the data set. from the plots, it was clear that variables such as Total and Quantity are positively correlated while variables such as Total and ratings have no correlation to each other

# Executive Summary.

An Executive Summary has been included in this repository for futher insights
