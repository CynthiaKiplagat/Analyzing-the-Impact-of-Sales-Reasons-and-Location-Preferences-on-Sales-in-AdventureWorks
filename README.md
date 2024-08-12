# Analyzing the Impact of Sales Reasons and Location Preferences on Sales in AdventureWorks
## Introduction 
In the business environment, understanding the factors that influence sales performance is essential for strategic decision-making. Businesses consistently strive to enhance sales through various methods such as promotions, discounts, and catering to customer preferences. This project aims to deliver a comprehensive analysis of two key aspects that can significantly affect sales outcomes: sales reasons, and location preferences.
## Objective
The primary objectives of this project are to:
* Determine the relationship between sales reasons and sales amounts
* Evaluate how different locations (cities, states, regions) affect sales performance
## Data Source
We will utilise the AdventureWorks Database.
## Methodology 
The methodology involves;
1. Data Extraction: Using SQL queries to extract relevant data from the database.
2. Data cleaning and processing:Prepare the extracted data for analysis
3. Exploratory Data Analysis: Summarizing data to compute total sales, quantities, and other metrics.
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
using the Label Encoder to cover both SalesReason1D and TerritoryName to numeric since most machine learning algorithms require numeric input.I performed mapping to be able to understand the encode.

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Encode%20Variables.PNG)'

### Exploratory Data Analysis
#### Sales by Sales Reason 
![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Sales%20by%20Sales%20Reason.PNG)

The leading sales reason is Pricing, generating over $40 million, followed by Promotion with $13 million, Manufacturer with $6.7 million, and Quality with $6.1 million. Reviews, Other, and Television Advertisement contribute significantly less, at $2 million, $900,000, and $31,000 respectively. Prioritizing pricing strategies, promotional activities, and strong manufacturer partnerships will optimize sales performance.

#### Sales per Territory 
![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Sales%20per%20Territory.PNG)

Australia leads with $18M in sales, followed by SouthWest with $15M, Northwest with $9M, and the UK with $8M. Germany, France, and Canada contribute $7M, $6M, and $5M, respectively. South East, North East, and Central have the least sales at $54K, $17K, and $8K, respectively.
#### Sales Trend by Territory Over Time.

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Sales%20Trend%20Over%20Time.PNG)

Sales showed no significant change during the first period but faced a downturn in the next phase, indicating a possible market or operational issue. However, starting June 2013, sales experienced a positive trend, suggesting a recovery or improvement in factors influencing sales, which likely correlated with the subsequent rise in performance.
### Data Analysis
ANOVA used to test if there are significant differences in sales amounts across various sales reasons.
![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Anova.PNG)
A higher F-Statistic and  P-Value is below the normal threshold suggesting that there is a statistically significant difference in sales amounts across different sales reasons.Different sales reasons have a meaningful impact on the sales amounts, and the differences between them are not likely due to random chance.
Since there are more than two sales reasons, we consider conducting post-hoc tests the Tukey's HSD to identify which specific groups differ from each other.

![Alt Text](https://github.com/CynthiaKiplagat/Analyzing-the-Impact-of-Sales-Reasons-and-Location-Preferences-on-Sales-in-AdventureWorks/blob/main/Turkey%20HSD.PNG)

Price is a key competitive strategy that can significantly attract customers. However, to maximize its effectiveness, it should be complemented with high-quality products, strategic promotions, and positive customer reviews. Integrating these elements will enhance the overall value proposition and improve customer engagement.














