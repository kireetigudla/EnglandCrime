# Analyzing Data with Spark SQL
## Introduction of dataset
### Delving into the crime data from Cambridgeshire, Leicestershire, and North Wales, our report analyses incidents from March 2021 to March 2023, sourced from the Police Open-Source Data.

We focus on these specific areas to identify:

Temporal Trends: We track the evolution of crime rates, pinpointing trends, and seasonal shifts in criminal activity over the two years.
Geographical and Demographic Insights: By examining the distinct geographic and demographic traits of the regions, we shed light on unique crime patterns.
Category-Specific Analysis: We scrutinize various crime types, like burglary or violent crimes, assessing their frequency and regional spread.

Our analysis aims to reveal crime trends, evaluate regional crime dynamics, and offer insights for enhancing public safety measures and informing policy in these locales. The objective is to deepen the understanding of crime in these regions, contributing to safer 

## Methodology
### Utilizing PySpark's robust data handling, our analysis of crime data from Cambridgeshire, Leicestershire, and North Wales proceeded through structured phases:

1. Data Loading and Preparation: Quick data importation into PySpark DataFrames, with meticulous correction of missing values and data type verification for analysis readiness.

2. Exploratory Data Analysis (EDA): Initial EDA provided a statistical overview and identified preliminary patterns, setting the stage for deeper analysis.

3. In-Depth Data Analysis:
	Temporal Analysis: Scrutinized crime trends over time, highlighting monthly and annual patterns.
	Comparative Analysis: Compared crime rates and types across regions.
	Crime Categorization: Examined crime type prevalence to understand their spread.

4. Visualization and Reporting: Visuals translated complex data into understandable findings, balancing quantitative data with qualitative insights.

## Data Analysis 
### For analyzing my dataset, I utilized SQL queries. Let's start by loading the dataset with Pyspark and importing the required libraries:
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/e85bc8ee-a952-4b5a-a738-033e266fa967)

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/ab98df27-1359-40f4-bdb0-942d752cd150)

### My dataset has many string-type columns, some of which may have missing values. Since the existing column names contain spaces between them and sql commands do not function correctly with spaces in column names, I am renaming the columns.
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/b05d2cef-10e3-4fdc-b7b7-0e6eb64aa970)

###  report more crimes than Cambridge and north Wales.
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/6cde08db-6d7d-4f3e-8b15-da4565f45177)

### Here we can see in 2022 most crimes of 275417 were reported and decreased drastically in 2023. It’s can great work to reduce crimes by police department.

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/42ccb4a9-f77a-415d-a4cd-40979cbc167c)



### Listed Crime count by location.

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/424441cb-ecda-4d98-abbe-0bed5acf5093)


### In this crime dataset, 'Violence and sexual offences' top the list with 212,749 incidents, indicative of significant safety concerns. 'Anti-social behavior' follows with 79,713 cases, highlighting challenges in maintaining public order. 'Public order' offences are also substantial at 60,234, suggesting widespread disturbances. Additionally, 'Criminal damage and arson' have a notable count of 50,789, pointing to prevalent property-related crimes. Lower down, but still significant, 'Vehicle crime' and 'Shoplifting' are recorded at 25,245 and 24,243 incidents respectively, reflecting concerns in personal property security. These figures underscore the areas that may need targeted policing and community engagement strategies.
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/b18c7d2c-3b88-43f3-ba78-a5dec2d0c4d2)


### Creating a new data frame with month and averages. Preparing for visualization.

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/03165849-f9cb-47d6-a4e5-3f4c776d71b6)

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/521a25e9-6f4d-413f-ad73-a7f1da5d79c2)

![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/da2f8dc0-4a96-4a2c-9d77-34147221a18b)
### The analysis of the monthly crime data indicates a variable trend throughout the year. The total reported crimes peaked significantly in March with 67,024 incidents, followed by a noticeable drop in April. The average crime rate per month also peaked in March at approximately 22,341, suggesting a seasonal pattern that could warrant further investigation. The graphical visualizations further underscore these fluctuations, with the highest spike in the cumulative monthly chart aligning with the March peak. A sharp decrease in average monthly crime rates is observed towards the end of the year, with December recording the lowest at roughly 20,005, potentially signaling effective year-end crime reduction strategies.




## Type of crime Offenses breakdown.
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/b0c9f59d-8ab0-43c3-af95-dd5c1508112a)
### The bar chart illustrates the breakdown of criminal offenses, showing a predominant occurrence of 'Violence and sexual offences', which far exceed other categories with over 200,000 cases. 'Anti-social behavior' and 'Public order' crimes also feature prominently, indicating significant issues with personal and public safety. Lesser frequent crimes like 'Bicycle theft', 'Possession of weapons', 'Theft from the person', and 'Robbery' appear at the lower end of the scale. The visual representation emphasizes the disparities among crime types, with a steep decline in frequency from the most to least common offenses.

## Geographical Distribution of Crime 
![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/4f7e78e6-b905-408d-ba84-6d55e0ea2076)


![image](https://github.com/kireetigudla/EnglandCrime/assets/122108823/e8b8ec0e-0c7e-41e9-9737-0c7b02d37fd0)
### The map depicting the geographical distribution of crimes indicates pronounced hotspots in Leicester and Cambridge shire, with a notable number of incidents clustered within these areas, suggesting higher crime rates in these regions. In contrast, North Wales shows a much more dispersed pattern, indicating either lower crime rates or less dense reporting of incidents. The concentration in Leicester and Cambridge shire might reflect urban-related crime trends, which could be due to various socio-economic factors. These areas might benefit from targeted policing and community initiatives to address and mitigate the higher crime prevalence. The sparse distribution in North Wales may point towards different policing needs, possibly focusing on rural crime and community engagement.


##Discussion/Findings

###Geographical Trends: Our findings highlight Leicester and Cambridgeshire as primary crime hotspots, contrasting with North Wiles’ more scattered criminal activity. This disparity suggests socio-economic factors in urban locales could influence crime prevalence, necessitating robust community and policing responses.

Temporal Patterns: The year 2022 marked a peak in crime reports, with a subsequent decline in 2023. This shift might reflect the success of law enforcement or broader societal changes. Seasonal crime spikes also emerged, hinting at complex underlying causes.

Crime Types: Predominant crimes include violence, sexual offenses, and anti-social behaviour, underscoring key focus areas for law enforcement. Lower-frequency crimes like bicycle theft and robbery, while less common, significantly impact community safety.

Policing Effectiveness: The 2023 crime reduction across all regions, especially noticeable at the year's end, suggests effective policing strategies, possibly enhanced by year-end crime prevention efforts.

##Conclusion

###This report has revealed valuable insights into the crime dynamics of Cambridgeshire, Leicestershire, and North Wales. The in-depth analysis underscores the importance of understanding geographical and temporal patterns in crime to devise targeted strategies that address the unique challenges of each region.

The findings point towards a need for sustained efforts in combating violence and sexual offenses, which pose the greatest threat to public safety. Additionally, the role of socio-economic factors in influencing crime rates cannot be understated, as evidenced by the urban concentration of crimes in specific areas.

The observed reduction in crime rates in 2023 is encouraging and suggests that strategies implemented in recent years are yielding positive results. It is imperative that these strategies are continually reviewed and adapted to maintain the downward trend in criminal activity.

In summary, while challenges remain, the overall direction is one of improvement. It is crucial that law enforcement agencies continue to leverage data-driven approaches to enhance public safety, reduce crime, and foster safer communities across Cambridgeshire, Leicestershire, and North Wales.











































