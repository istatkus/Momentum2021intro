### title: Momemtum Snowflake with Data Robot Country Analysis
#### date: March 22, 2021
### Project Description
Clean and prepare a data set to learn Snowflake with Data Robot

##### Subject area and questions
Select a simple subject area: country Gini Index and country characteristics. The Gini Index is a measure of wealth inequality. The Gini Index and Gini Gain are also formulas used in decision trees and chosen to build greater understanding of the algorithm.
Gini is 0 to 1, the CIA gini is 0 to 100 where 0 is perfect equality and 1 or 100 is perfect inequality. 
  
  ![image](https://user-images.githubusercontent.com/12059492/112504210-f368ae00-8d61-11eb-8424-0cd45b6be691.png
  from https://www.researchgate.net/figure/Lorenz-curve-and-Gini-coefficient-G_fig1_319861192
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


#### Exploratory using Snowflake Snowsight, minimal charts available
##### Gov Spending on Education
![image](https://user-images.githubusercontent.com/12059492/112052644-bca85300-8b29-11eb-8ffa-ddd0f746a065.png)

##### Median Age
![image](https://user-images.githubusercontent.com/12059492/112053207-71db0b00-8b2a-11eb-965a-e3204092d1c1.png)

##### GDP Growth
![image](https://user-images.githubusercontent.com/12059492/112053396-b1095c00-8b2a-11eb-96d4-3a56c832e0f4.png)

##### Labor Participation
![image](https://user-images.githubusercontent.com/12059492/112053716-0cd3e500-8b2b-11eb-919d-f32da828c4d9.png)

##### Highest Income Tax - higher doesnt promote equality
![image](https://user-images.githubusercontent.com/12059492/112053949-5c1a1580-8b2b-11eb-82fe-0c6d231646d5.png)

##### Personal Freedom Index
![image](https://user-images.githubusercontent.com/12059492/112054268-bca95280-8b2b-11eb-9497-69b399478edb.png)

##### Median Gini by Income Group 
![image](https://user-images.githubusercontent.com/12059492/112054987-a9e34d80-8b2c-11eb-8264-f5bf7b4a6f53.png)

##### Average by Income Group
![image](https://user-images.githubusercontent.com/12059492/112055129-d8612880-8b2c-11eb-94cf-afa3162442f9.png)

##### Economic Freedom and Income Group
![image](https://user-images.githubusercontent.com/12059492/112055327-14948900-8b2d-11eb-8f64-10a5304bc1a1.png)
##### Correlations
![image](https://user-images.githubusercontent.com/12059492/112058713-50c9e880-8b31-11eb-9a8c-1e1a0315adb6.png)  
![image](https://user-images.githubusercontent.com/12059492/112058910-8f5fa300-8b31-11eb-8c84-efe0c709f6e1.png)

#### Exploratory with SAS
![image](https://user-images.githubusercontent.com/12059492/112068712-e1f48b80-8b40-11eb-831b-dbfa199b0f6a.png)  

![image](https://user-images.githubusercontent.com/12059492/112069753-c25e6280-8b42-11eb-93ce-5832a292af34.png)

![image](https://user-images.githubusercontent.com/12059492/112071112-942e5200-8b45-11eb-83c1-b3b2270b7517.png)


#### Descriptive
![image](https://user-images.githubusercontent.com/12059492/112069500-524fdc80-8b42-11eb-980f-1ec80688feec.png)  
![image](https://user-images.githubusercontent.com/12059492/112070020-47e21280-8b43-11eb-8ebd-3344813c4f24.png)  
##### Removed 0 Gini countries
![image](https://user-images.githubusercontent.com/12059492/112070134-7cee6500-8b43-11eb-9b83-be5a49848e09.png)


### Data Robot
![image](https://user-images.githubusercontent.com/12059492/112495751-8e5d8a00-8d5a-11eb-91a4-e6fafd8f9685.png)  
![image](https://user-images.githubusercontent.com/12059492/112496165-e4cac880-8d5a-11eb-8e39-4c2267f3b12e.png)  
![image](https://user-images.githubusercontent.com/12059492/112498041-8acb0280-8d5c-11eb-885a-f04df88dd056.png)
![image](https://user-images.githubusercontent.com/12059492/112498579-0b89fe80-8d5d-11eb-88a0-52f07abbf666.png)  
![image](https://user-images.githubusercontent.com/12059492/112499103-87844680-8d5d-11eb-9c43-6b209dd6aee9.png)
![image](https://user-images.githubusercontent.com/12059492/112499161-9834bc80-8d5d-11eb-88e4-5aa7c54b4c9f.png)
![image](https://user-images.githubusercontent.com/12059492/112499231-a71b6f00-8d5d-11eb-9105-dc847f75c400.png)
![image](https://user-images.githubusercontent.com/12059492/112499455-dcc05800-8d5d-11eb-9037-d84e51b33eaf.png)
![image](https://user-images.githubusercontent.com/12059492/112499512-ecd83780-8d5d-11eb-8e80-f2721cbb3b28.png)
![image](https://user-images.githubusercontent.com/12059492/112500391-b5b65600-8d5e-11eb-94c4-19e3d09d0ea6.png)
![image](https://user-images.githubusercontent.com/12059492/112500458-c961bc80-8d5e-11eb-8ca5-eb487726f0ae.png)
![image](https://user-images.githubusercontent.com/12059492/112500565-e0081380-8d5e-11eb-8a5d-0827ea4cde5c.png)
![image](https://user-images.githubusercontent.com/12059492/112500625-eeeec600-8d5e-11eb-921d-0ebb7968c3af.png)
![image](https://user-images.githubusercontent.com/12059492/112500722-0168ff80-8d5f-11eb-9139-bbcb7a1b4c5f.png)
![image](https://user-images.githubusercontent.com/12059492/112500786-0f1e8500-8d5f-11eb-8482-6a5c252c1368.png)
![image](https://user-images.githubusercontent.com/12059492/112500948-370de880-8d5f-11eb-9156-45d231d6db78.png)

![image](https://user-images.githubusercontent.com/12059492/112500884-26f60900-8d5f-11eb-841b-929682f50424.png)



#### Prescriptive


