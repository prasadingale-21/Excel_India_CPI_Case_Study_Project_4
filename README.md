# Excel_India_CPI_Case_Study_Project_4

## Collect Data  

* The dataset is already provided along with case study in a CSV file format  
* The dataset is imported here in this workbook through Get Data option  
* The provided CPI dataset comprises the CPI values of different broader categories like food and beverages, clothing, housing, fuel and light etc. from the year 2013 to year 2023. These values measured are classified further for rural, urban, combined rural and urban demographic area.  
* Rows: 372 & Columns: 30   
* The data is raw input needed to clean further.  

## Clean Data

* In the month column, March spelling was incorrect. So it is updated with correct spelling.  
* Total Blank values in all columns: 117   Formula used: =COUNTBLANK(All_India_Index_Upto_April23[#All])    
* Count of cells where value is "NA" : 122 Formula used: =COUNTIF(All_India_Index_Upto_April23[#All], "NA")  
* All non-numeric values in numeric colums deleted to blank cell initially. For Example - Housing column has non-numeric values such as "-" & "NA".  
* Blank Values in individual columns are replaced with moving average method. For single blank value the average of previous and next moth is taken while for consecutive blank values, backword fill is taken.  
* Housing column values were appearing as Text, so converted to number using formuls =VALUE()  
* Row 32 - November has extra trailing space - removed  


## EDA
* Calculated Annual Inflation Rate  
* Average CPI  
* Max CPI  
* Min CPI  
* Trends - Monthly CPI yearwise, Monthly Inflation Rate yearwise, Year over Year Inflation Rate, Important Category % contribution in Overall CPI  

##  Define Problem Statement

You are working with the National Statistical Office which is equipped to release inflation numbers in India. As an analyst, you are provided with CPI data and are equipped to find out insights from the data. Your senior wants you to find key trends and deep dive into the data to answer the following questions -  

1. **Based on the latest month’s data, identify the contribution of different broader categories (food, energy, transportation, education, etc.) towards the CPI basket.**   

   Broader categories (buckets) can be created by combining similar categories into one bucket; Ex: Meals, Beverages, Cereals, can be clubbed to create “Food”   category, etc.
* Which broader category has the highest contribution towards CPI calculation 
* Contribution is calculated by evaluating the underlying index values for broader category and should add to 100% when contribution from different broader categories are added. 

**Analysis:**  
*Contribution of Broader Categories Towards CPI Basket (May 2023)*  

* Based on the latest month data (May 2023), the CPI basket shows a relatively balanced distribution across broader consumption categories. The categories Clothing and Footwear, Pan/Tobacco/Intoxicants, Health, and Personal Care & Effects have the highest contribution, each accounting for approximately 9% of the CPI basket.  
* Most of the remaining categories such as Food and Beverages, Housing, Fuel and Light, Household Goods and Services, Transport and Communication, Recreation and Amusement, Education, and Miscellaneous contribute around 8% each.
* The chart indicates that the CPI basket is fairly diversified, as no single category dominates the overall inflation calculation.
* The relatively higher contribution of Clothing and Footwear, Health, Personal Care & Effects, and Pan/Tobacco/Intoxicants suggests that these categories have a slightly greater impact on the overall CPI calculation compared to other categories during the selected period.

<img width="1082" height="615" alt="image" src="https://github.com/user-attachments/assets/d6033fcb-6ef0-48a2-89df-8e767df88576" />



2. **A trend of Y-o-Y increase in CPI (rural + urban) inflation starting 2017 for the entire basket of products combined.**
   Create a graph depicting the growth rate Y-o-Y and identify the year with highest inflation rate.  
   Highlight the reason why the year has the highest inflation (based on research).
   
**Analysis:**  
  *Year-on-Year CPI Inflation Trend Analysis (Rural + Urban)*

* CPI inflation remained stable between 2017 and 2019, ranging from 3.3% to 3.95%.  
* Inflation increased sharply during the COVID-19 period, reaching 6.10% in 2020 due to supply chain disruptions and higher prices of essential goods.  
* Although inflation slightly reduced in 2021, it remained high compared to pre-pandemic years.  
*  2022 recorded the highest inflation rate at 6.62%, mainly because of widespread price increases across major categories.  
* The biggest contributors in 2022 were: 
  - Fuel and Light (10.11%)  
  - Clothing and Footwear (9.57%)  
  - Household Goods and Services (7.44%)  
  - Transport and Communication (7.00%)  
  - Personal Care and Effects (6.80%)
* Rising global crude oil prices, post-COVID recovery, and supply chain issues were the key reasons behind high inflation in 2022.
* Inflation started easing in 2023, indicating gradual stabilization in prices and economic conditions.

<img width="1728" height="406" alt="image" src="https://github.com/user-attachments/assets/9a05ce81-835c-40ff-854e-269629f4ac5f" />



3. **With India’s retail inflation reaching a 3-month high of 5.55% in November 2023, largely due to a sharp rise in food prices. Analyze the following for 12 months ending May’23**  

    Investigate trends in the prices of broader food bucket category and evaluate month-on-month changes. Highlight month with highest and lowest food inflation
Identify the absolute changes in inflation over the same 12 months period and identify the biggest individual category contributor (only within broader food category) towards inflation  

**Analysis:** 

*Trend in Broader Food Inflation (Month-on-Month) for Rural + Urban Sector*

* Food inflation increased steadily from June 2022 to October 2022.  
* The highest food inflation was recorded in October 2022 (+1.8), mainly driven by rising prices of spices, cereals, and milk products.  
* After October 2022, inflation started declining sharply.  
* The lowest food inflation was observed in December 2022 (-2.4), showing a major fall in food prices compared to previous months.  
* From January 2023 onwards, food inflation gradually recovered and remained moderately positive until May 2023.

<img width="1212" height="391" alt="image" src="https://github.com/user-attachments/assets/bdd6a887-009b-48cb-adb9-7132075d30e3" />

  The food inflation trend during the 12-month period showed significant fluctuations, indicating unstable food prices throughout the year.  
  
  **Major Contributors to Food Inflation**
  The following categories contributed the most toward rising food inflation:
  
  1. Spices – 16.52%  
    - Highest contributor to food inflation.
    - Sharp increase likely due to supply shortages and higher transportation costs.
  2. Cereals and Products – 12.06%  
    - Significant rise due to higher wheat and rice prices.
  3. Milk and Products – 8.26%  
    - Increase in dairy input costs contributed to inflation.
  4. Pulses and Products – 6.88%  
    - Continued upward pressure from supply-demand imbalance.
  5. Prepared Meals, Snacks, and Sweets – 5.60%  
    - Processed food prices remained elevated.

<img width="1021" height="522" alt="image" src="https://github.com/user-attachments/assets/f7985757-bf5d-44f8-bf1f-d9a9753460fa" />

**Key Insight**

    Although some categories such as oils, fats, and vegetables experienced falling prices, the sharp increase in essential food categories like spices, cereals, milk, and pulses had a stronger impact on the overall food basket. Among all categories, Spices emerged as the biggest individual contributor to food inflation during the 12-month period ending May 2023.  



4. **Investigate how the onset and progression of the COVID-19 pandemic affected inflation rates in India. Analyze the impact of key pandemic milestone [first lockdown] on the CPI inflation %, specially focus on categories like healthcare, food, and essential services.**    
Hint: You can consider Mar’20 as the onset of covid, and can compare the inflation trend before and after Mar’20 to see if there is a change in inflation % before and after.

**Analysis:**  
*Impact of COVID-19 on CPI Inflation in India*

* The first COVID-19 lockdown in India began in March 2020, which significantly affected inflation trends across essential categories such as food, healthcare, and fuel.  
* Before March 2020, inflation levels across categories were relatively stable with gradual changes.  
* After the lockdown, Food and Beverages inflation increased sharply, rising from around 149–150 before COVID to nearly 161 by Oct 2020.  
* The rise in food inflation was mainly due to:  
    - Supply chain disruptions  
    - Transportation restrictions  
    - Panic buying and shortage of essential goods  
* Healthcare inflation also showed a continuous increase after the onset of COVID-19.  
    - Health index increased steadily from around 149 in Oct 2019 to 156 by Oct 2020.  
    - Increased demand for medicines, medical equipment, and healthcare services contributed to this rise.  
* In contrast, Fuel and Light inflation declined after March 2020.  
    - Fuel index dropped from around 149 in Mar 2020 to nearly 142 by Jun–Jul 2020.  
    - This decline was mainly caused by reduced travel, lower industrial activity, and a fall in global crude oil prices during the pandemic.  
* The graph clearly indicates that the pandemic created uneven inflationary pressure:
    - Essential goods like food and healthcare became more expensive  
    - While fuel-related inflation weakened due to reduced economic activity.  
* Overall, COVID-19 had a significant impact on India’s inflation pattern, especially during the initial lockdown period, causing volatility in essential consumer categories.  

<img width="1166" height="395" alt="image" src="https://github.com/user-attachments/assets/a3299fc9-ff64-4599-9afd-e115ef016d4a" />


5. **Investigate how major global economic events (like imported crude oil price fluctuations) have influenced India's inflation. This can include an analysis of imported goods and their price trends.**  

      For the purpose of this analysis, focus only on the imported oil price fluctuations for years 2021 to 2023 (Month-on-month)
      Identify trends in oil price change with change in inflation prices of all the categories and identify category whose inflation prices strongly changes with fluctuations in imported oil price (Hint: you can use =correl function)

**Analysis:**  

* Fuel & Light has the strongest correlation with General Index (0.987), meaning oil price fluctuations directly drove overall inflation  
* Clothing & Footwear (0.986) is surprisingly the most co-moving category — likely due to rising manufacturing and logistics costs driven by fuel prices  
* Transport & Communication (0.967) shows very strong correlation — directly impacted as fuel is a core input cost  
* Food (0.965) is strongly correlated — higher fuel prices raise transportation and supply chain costs, pushing food prices up  
* All four categories show correlation above 0.96, suggesting oil price is a systemic inflation driver across the entire economy, not just energy-specific categories  

    Imported crude oil price fluctuations between 2021–2023 had a broad-based impact across all major CPI categories. Fuel & Light most directly reflects oil prices, but its ripple effect on transport, food supply chains, and manufacturing makes it a primary upstream driver of India's overall inflation during this period.

<img width="1719" height="384" alt="image" src="https://github.com/user-attachments/assets/2118d496-0cbc-43fb-a21b-596ed8a9a075" />


## Validation and Communication

* India's CPI basket (based on latest month data - May 2023) is broadly diversified with Clothing and Footwear, Pan/Tobacco/Intoxicants, Health, and Personal Care & Effects contributing the highest share (~9%), while most other categories contribute nearly equally at ~8% each, indicating no single category dominates inflation.  
* Inflation peaked at 6.62% in 2022 — the highest over 2017–2023 — driven by Fuel and Light (10.11%), Clothing (9.57%), and Transport (7.00%), largely due to rising global crude oil prices and post-pandemic supply chain disruptions.  
* Within the food basket, Spices (16.52%) were the biggest inflation contributor during June 2022 – May 2023, with food inflation peaking in October 2022 and dropping sharply in December 2022, reflecting significant price volatility.  
* The COVID-19 pandemic (March 2020) caused an asymmetric shock — Food and Healthcare prices surged due to supply disruptions and panic buying, while Fuel and Light deflated temporarily due to reduced economic activity.  
* Imported crude oil prices proved to be a systemic inflation driver, with Fuel & Light (0.987), Clothing (0.986), Transport (0.967), and Food (0.965) all showing near-perfect correlation with oil price fluctuations during 2021–2023.  
* Overall, India's inflation is deeply interconnected across sectors, and managing it effectively requires addressing domestic food supply vulnerabilities alongside reducing exposure to global energy price volatility.  


## Dashboard designed based on provided historical dataset

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3776f404-c548-4bb1-a77e-d07671a1d2c3" />
