## Firebird: Predicting Fire Risk and Prioritizing Fire Inspections in Atlanta
### ABSTRACT
* what is AFRD? 
  The Atlanta Fire Rescue Department (AFRD) works to reduce fire risk by inspecting commercial properties for potential hazards and fire code violations. 
* what does Firebird do?
  The Firebird framework to help identify and prioritize commercial property fire inspections, using machine learning, geocoding, and information visualization.
* what is the result?
  * Firebird computes fire risk scores for over 5,000 buildings in the city
  * with true positive rates of up to 71% in predicting fires. 
  * It has identified 6,096 new potential commercial properties to inspect
  * Firebird integrates and visualizes fire incidents, property information and risk scores to help AFRD make informed decisions about fire inspections. 
  
### INTRODUCTION
* why the topic is important?
In 2014 alone, there were 494,000 structure fires in the United States, causing 2,800 civilian deaths and $9.8 billion in property damage. 
* challenges
  * Property Identification. they did not have a way to obtain a more complete list of commercial properties that potentially needed inspection. -> Cleaning and merging the datasets to identify which inspectable properties in the city had fallen through the cracks required significant effort. 
  * Fire Risk Prediction. Because 19,397 new commercial property inspections is far greater than the current number of annual commercial property inspections, and far more than AFRD’s current staff of fire inspectors can reasonably inspect, -> we developed a method to prioritize those inspections based on their fire risk. 
    * First, we created a joined dataset of building- and parcel-level information variables, for 8,223 commercial properties.    
    * Then, we built predictive models of fire risk using machine learning approaches, including Support Vector Machine (SVM) and Random Forest. 
* Contributions & Impact. 
  * With Firebird, AFRD can now use data about historical fires to inform their fire inspections and more efficiently utilize their inspection personnel capacity. 
  * Discovering new properties. 
  * Predictive fire risk model. 
  * Impact to Atlanta: Firebird at work.
  * National impact: reusable end-to-end frame- work for inspection prioritization. 
  
### RELATED WORK
-> Risk prediction models.
--> Forest fire prediction. 
---> Community-level urban fire prediction. 
----> Property-level urban fire prediction.
  * The nearest precedent for our research with AFRD is the recent work from the New York Mayor’s Office of Data An- alytics (MODA) with the Fire Department of New York (FDNY) to build a “Risk-Based Inspection System” (RBIS).

### DATA DESCRIPTION
#### Data Sources
* historical fire incidents
* fire inspection
* structural information about commercial properties 
* parcel data from Atlanta’s Office of Buildings provides parcel-level in-formation, 
* The business license dataset 
* Google Places API 
* State of Georgia Government
* socioeconomic and demographic data from the U.S. Census Bureau
* liquor license 
* 2014 crime data  
* Certificate of Occupancy (CO) data 
#### Data Joint
We joined the datasets together based primarily on spatial location information. 

### IDENTIFYING NEW PROPERTIES NEEDING INSPECTION
* we first needed to understand what types of properties currently required fire inspections according to the Fire Code, 
* we then identified other similar properties.
the most challenging part was to determine how buildings with different names (or IDs, or address formats) in various datasets actually refer to the same building. 

### PREDICTIVE MODEL OF FIRE RISK
#### Data Cleaning
* For each property with missing data for a particular feature, we replaced missing values with 0 when appropriate. 
* We also included a binary feature indicating whether each property had missing data for each feature. 
* We used log transformation for variables with a large numerical range, such as the “for sale” price of properties.
#### Feature selection
* We manually examined each variable to de- termine whether it may be relevant to fire prediction, and ex- cluded many obviously non-predictive variables in this initial process (such as the phone number of the property owner, or property ID numbers). 
* We then used <strong>forward and backward feature selection processes</strong> to determine each variable’s contribution to the model, and removed the variables that did not contribute to higher predictive accuracy. 
Our final model includes only 58 variables. We then expanded categorical variables into binary features. For example, the zip code variable was expanded into 37 binary features, and for each property only one zip code was coded as 1 (all zip codes were designated as 0 if a property’s zip code data was missing). After expansion, we had 1127 features in total.
#### evaluation of the models
* Goal - A fire risk model would ideally be tested in practice by predicting which properties would have a fire inci- dent in the following year
* method - We chose to validate our model using a time-partitioned approach. 
Note that training and testing sets include the same set of properties, but different labels correspond to fires in different periods of time. This is a valid approach because we didn’t use information that we would only know after the training period, i.e., fires in 2015.
#### Further Discussion of the Models
* different meaning of labels
* whether the performance of predicting fires is consistent in different testing time peri- ods.
* it is helpful for us and for AFRD to know which features are the most effective predictors.
#### Assignment of Risk Scores

### IMPACT ON AFRD AND ATLANTA
#### Previous Inspection Process
#### Technology Transfer to AFRD
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/firebird.png)
#### Impact on AFRD Processes

### Challenges

### Conclusions
http://firebird.gatech.edu/KDD16_Firebird.pdf

