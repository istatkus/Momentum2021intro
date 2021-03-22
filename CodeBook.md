### title: Momemtum Snowflake with Data Robot Country Analysis
#### date: March 22, 2021
### Project Description
Clean and prepare a data set to learn Snowflake with Data Robot

##### Subject area and questions
Select a simple subject area: country Gini Index and country characteristics. The Gini Index is a measure of wealth inequality. The Gini Index and Gini Gain are also formulas used in decision trees and chosen to build greater understanding of the algorithm.
  
Downloaded data sets from: 

https://worldpopulationreview.com/country-rankings/gini-coefficient-by-country

https://datacatalog.worldbank.org/dataset/environment-social-and-governance-data

#### The First Step is to analyze and understand the data.

These are very small data sets without any column descriptions. Initial analyis will occur in Excel. Some data cleansing will also be done manually. The data will be loaded to Snowflake IRENE_DB. 

countrycodes 
![image](https://user-images.githubusercontent.com/12059492/112009929-36761780-8afd-11eb-92e4-c88e540a8c0d.png)

countryfreedom  
![image](https://user-images.githubusercontent.com/12059492/112015270-0bda8d80-8b02-11eb-9cdb-1d6421fd6595.png)

ESGCountrylabor participation  This data set is from a different source and has many challenges. Isolated one indicator, removed commas and special characters  
![image](https://user-images.githubusercontent.com/12059492/112023300-7d6a0a00-8b09-11eb-9743-5ab026e13c5f.png)

country indicators from https://datacatalog.worldbank.org/dataset/environment-social-and-governance-data
![image](https://user-images.githubusercontent.com/12059492/112052192-3986fd00-8b29-11eb-9991-30a6f2554c26.png)

giniindex  This source does not appear to be accurate. World Population Review
![image](https://user-images.githubusercontent.com/12059492/112011594-c799be00-8afe-11eb-82ff-1b4297d74f46.png)

ESGcountryincomegroup  Due to UTF8 encoding issues, replaced special characters  
![image](https://user-images.githubusercontent.com/12059492/112023165-5dd2e180-8b09-11eb-8cb0-2e83eca2861c.png)

countrytax  The tax data is incomplete. Removed all occurances of -1, -, N/A and stripped notes away form percent, percents were not in consistent decimal and were converted to decimal.
![image](https://user-images.githubusercontent.com/12059492/112015326-1a28a980-8b02-11eb-9ac1-53ee7ba8fb10.png)


#### Import the data into snowflake  
![image](https://user-images.githubusercontent.com/12059492/112023547-be621e80-8b09-11eb-87d0-2b033ab4bab0.png)


#### Exploratory using Snowflake Snowsight
Gov Spending on Education
![image](https://user-images.githubusercontent.com/12059492/112052644-bca85300-8b29-11eb-8ffa-ddd0f746a065.png)

Median Age
![image](https://user-images.githubusercontent.com/12059492/112053207-71db0b00-8b2a-11eb-965a-e3204092d1c1.png)

GDP Growth
![image](https://user-images.githubusercontent.com/12059492/112053396-b1095c00-8b2a-11eb-96d4-3a56c832e0f4.png)

Labor Participation
![image](https://user-images.githubusercontent.com/12059492/112053716-0cd3e500-8b2b-11eb-919d-f32da828c4d9.png)

Highest Income Tax - higher doesnt promote equality
![image](https://user-images.githubusercontent.com/12059492/112053949-5c1a1580-8b2b-11eb-82fe-0c6d231646d5.png)

Personal Freedom Index
![image](https://user-images.githubusercontent.com/12059492/112054268-bca95280-8b2b-11eb-9497-69b399478edb.png)

Median Gini by Income Group 
![image](https://user-images.githubusercontent.com/12059492/112054987-a9e34d80-8b2c-11eb-8264-f5bf7b4a6f53.png)


#### Descriptive

#### Inferential / Predictive

#### Prescriptive


