# Chicago_Restaurant_Risk_Analysis

## File descriptions:

30112finalproject.ipynb--the overall Jupyter notebook that contains all the codes.

slides.pdf-In--class presentation slides

resturant.txt--contains the link of the dataset we downloaded form Chicago.gov. It has the basic resturant information and the food risk level which is a target feature of this project. The orginal file is too big and it exceeds GitHub limitation, so we add a link of the Google Drive.

dedup_yelp.csv--csv we got from wen scrapping

chi_bound.geojson--file downloaded from website containing geographical information for graphing the map using folium library

updated.json--file downloaded from website containing geographical information for graphing the map using folium library

income_household_median_zip1.csv-file downloaded from website containing zipcodes with income household median, we use this file to link the income househould median to the web scrapped dataset

link_df.csv & link_dfn.csv- files generated during the process of data cleaning

zips.csv - a list of zipcodes

final_report_zzzz.pdf - a document with the more detailed project description

.DS_Store - DS_Store is a file that stores custom attributes of its containing folder, such as folder view options, icon positions, and other visual information. The name is an abbreviation of Desktop Services Store, reflecting its purpose.


## Summary:
We are interested in discovering the relationship between restaurants’ food inspection risk levels and various attributes for restaurants in the city of Chicago.
For identifying the food inspection level, we will refer to Chicago Data Portal’s restaurant public data. This database includes a column called “risk”, which is categorized into three levels: low, medium, and high.
For restaurants’ attributes, we would like to consider a restaurant’s location, rating, price level, etc. To obtain corresponding data, we decided to use Yelp’s API(Yelp Fusion), in combination with Google Map’s restaurant rating section, and Chicago Data Portal’s restaurant data.

We believe there will be plenty of conclusions to draw from this project. And we are specifically interested in consumers’ perspectives on restaurants’ risk levels. In addition, we add a geographical constraint of Chicago. Since Chicago is a metropolitan city having both abundant amounts and differentiations of restaurants, plus, restricting to Chicago reduces workload but also ensures the representativeness of our analyzing results.

The significance of researching the relationship between restaurant sanitary conditions and their information on the Yelp platform can be quite significant in a number of ways: improve consumer health and safety, reveal industry standards, improve business practices, make suggestions for public health policy and the advancement of knowledge in relevant fields.


### Research Question:
1. How are  income level segmentation(zip codes) and a restaurant’s risk level(sanitary level) correlated？
2. How are the features of restaurants correlated with their risk level?
(We select these features of restaurants according to the result of our Exploratory Data Analysis. The hypothesis section and Exploratory Data Analysis sections will provide details of “features of restaurants” )

### Hypothesis:
	1. There is a positive correlation between risk level and median household income level.
	2. There is a positive correlation between risk level and price, rating, transactions, and review counts. 

### Main Findings and Conclusions:
1. Restaurants’ rating, review, operation modes and price level all have statistically significant positive correlation with our target variable: restaurants’ risk levels. Whether a restaurant is operated in multi modes (offering pickup and delivery services) is the most important feature to impact its risk level. The result supports our second hypothesis. 
2. Income household median does not have a correlation with restaurants’ risk level. Our first hypothesis is not supported. 

### Implications:
1/It may be because ratings mean more popularity of the restaurant, thus making it more difficult to keep sanitary.
2/Multi-mode operation is more difficult to keep sanitary. (Many restaurants with high risks offer pickup options together with delivery service.)
3/More review count may also mean more popularity of the restaurant, so more difficult to keep sanitary.
4/Reinspection usually means re-assessing a restaurant's risk level. It could be more rigid in procedure, which may correlate with the result of a high-risk level.


### list the data sources with the links to retrieve them
https://data.cityofchicago.org/Health-Human-Services/Restaurant/5udb-dr6f

https://simplemaps.com/city/chicago/zips/income-household-median

https://docs.developer.yelp.com/docs/fusion-intro

https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-ZIP-Codes/gdcf-axmw
### list the required libraries:
pandas-1.5.2

numpy-1.23.5

seaborn-0.12.2

recordlinkage-0.14

matplotlib-3.6.2

scipy-1.9.3

requests-2.28.1

folium-0.14.0

wordcloud-1.8.2.2

regex-2022.7.9
