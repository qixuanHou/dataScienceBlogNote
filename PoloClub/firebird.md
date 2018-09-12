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
* 2,543 historical fire incidents
* fire inspection
* structural information about commercial properties 
* parcel data from Atlanta’s Office of Buildings provides parcel-level in-formation, 
* The business license dataset 
* Google Places API 
* State of Georgia Government
* socioeconomic and demographic data from the U.S. Census Bureau
* liquor license and 2014 crime data from the Atlanta Police Depart- ment, and Certificate of Occupancy (CO) data from the At- lanta Office of Buildings. All of these data sources con- tributed to discovering new inspections and developing our predictive model for commercial fire risk estimation.



http://firebird.gatech.edu/KDD16_Firebird.pdf
