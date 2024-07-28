# Analyzing the Impact of Sales Reasons and Location Preferences on Sales in AdventureWorks
## Introduction 
In the business environment, understanding the factors that influence sales performance is essential for strategic decision-making. Businesses consistently strive to enhance sales through various methods such as promotions, discounts, and catering to customer preferences. This project aims to deliver a comprehensive analysis of two key aspects that can significantly affect sales outcomes: sales reasons, and location preferences.
## Objective
The primary objectives of this project are to:
* Determine the influence of sales reasons on the quantity of products purchased.
* Analyze how location affects the preference for certain products.
## Data Source
We will utilise the AdventureWorks Database.
## Methodology 
The methodology involves;
1. Data Extraction: Using SQL queries to extract relevant data from the database.
2. Data cleaning and processing:Prepare the extracted data for analysis
3. Data Aggregation: Summarizing data to compute total sales, quantities, and other metrics.
4. Data Analysis: Using Python libraries (such as pandas, matplotlib, and seaborn) to perform detailed analysis and create visualizations.
5. Reporting: Compiling results into comprehensive reports with visualizations to highlight key findings.
### Data Extraction
Retrieved relevant data from SQL for our objective.
Below is the SQL Statement:

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Discounts-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/SQL.PNG)
The key output sales order information,customerdetails,salesreason and territory details.
## Data cleaning and Processing
Load the extract data into a pandas dataframe in python.

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Connection.PNG)

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/SQL%20Query.PNG)

#### Handling Missing Values

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Missing%20Values.PNG)

Since the analysis focuses on the impact of sales reasons, it is crucial to retain only those rows where SalesReasonID and SalesReason are not null. Dropping rows with missing values in these columns ensures the integrity of your analysis.

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Dropping%20nulls.PNG)

The dataset doesnot contain null values.
#### Encoding Variables 
using the Label Encoder to cover both SalesReason1D and TerritoryName to numeric since most machine learning algorithms require numeric input.








