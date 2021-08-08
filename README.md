# Statistical-Analysis-on-factors-influencing-Life-Expectancy (WHO)
**Data Source:**  
The dataset is related to life expectancy, health factors for 193 countries has been collected from the **WHO data repository website** and its corresponding economic data was collected from **United Nation website**. It has been observed that in the past 15 years , there has been a huge development in health sector resulting in improvement of human mortality rates especially in the developing nations in comparison to the past 30 years. Therefore, **in this project data from year 2000-2015 for 193 countries** have been considered for further analysis.

#### Approach:
- **Data Cleaning**
  - Ckecking for relevant variable type 
  - Renaming columns
  - Detecting and dealing with missing values in variables - **Imputation**
  - Detecting and dealing with Outliers in variables - **Winsorization**
- **Data Visualization**
  - data description
  - Correlation Matrix Heatmap

![image](https://user-images.githubusercontent.com/81185267/128643468-db966863-75bc-496a-b726-3c78e2973d5a.png)
![image](https://user-images.githubusercontent.com/81185267/128643531-a64a9989-d931-4c8b-a434-59242084dc4b.png)

- **Feature Engineering**
  - creating dummies for categorical values
  - dropping highly correlated independent variables. In those cases, the variable which is most highly correlated to Life Expectancy (target variable) will be kept while the others will be dismissed.
  - also dropping variables which are not very correlated with any of the other variables

- **Model Building**
  - Linear Regression
  - Ridge
  - Lasso

- **Evaluation Metrics**
  - R-squared value
  - RMSE value


                                                                                      

                                                                                                          
--------------------------
#### Variable Description:
Format: variable (type) - description

country (Nominal) - the country in which the indicators are from (i.e. United States of America or Congo)                       
year (Ordinal) - the calendar year the indicators are from (ranging from 2000 to 2015)                              
status (Nominal) - whether a country is considered to be 'Developing' or 'Developed' by WHO standards                                               
life_expectancy (Ratio) - the life expectancy of people in years for a particular country and year                                              
adult_mortality (Ratio) - the adult mortality rate per 1000 population (i.e. number of people dying between 15 and 60 years per 1000 population); if the rate is 263 then that means 263 people will die out of 1000 between the ages of 15 and 60; another way to think of this is that the chance an individual will die between 15 and 60 is 26.3%         
infant_deaths (Ratio) - number of infant deaths per 1000 population; similar to above, but for infants                            
alcohol (Ratio) - a country's alcohol consumption rate measured as liters of pure alcohol consumption per capita                                
percentage_expenditure (Ratio) - expenditure on health as a percentage of Gross Domestic Product (gdp)                                                      
hepatitis_b (Ratio) - number of 1 year olds with Hepatitis B immunization over all 1 year olds in population                                                                   
measles (Ratio) - number of reported Measles cases per 1000 population                                                      
bmi (Interval/Ordinal) - average Body Mass Index (BMI) of a country's total population                    
under-five_deaths (Ratio) - number of people under the age of five deaths per 1000 population                             
polio (Ratio) - number of 1 year olds with Polio immunization over the number of all 1 year olds in population                                  
total_expenditure (Ratio) - government expenditure on health as a percentage of total government expenditure                    
diphtheria (Ratio) - Diphtheria tetanus toxoid and pertussis (DTP3) immunization rate of 1 year olds                                  
hiv/aids (Ratio) - deaths per 1000 live births caused by HIV/AIDS for people under 5; number of people under 5 who die due to HIV/AIDS per 1000 births                        
gdp (Ratio) - Gross Domestic Product per capita                         
population (Ratio) - population of a country                              
thinness_1-19_years (Ratio) - rate of thinness among people aged 10-19 (Note: variable should be renamed to thinness_10-19_years to more accurately represent the variable)   
thinness_5-9_years (Ratio) - rate of thinness among people aged 5-9                             
income_composition_of_resources (Ratio) - Human Development Index in terms of income composition of resources (index ranging from 0 to 1)                                     
schooling (Ratio) - average number of years of schooling of a population                          
