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
Risk prediction models have been widely used in many do- mains, including health care [15], student performance eval- uation [16], and accounting fraud detection [18]. However, urban fire risk prediction has received relatively less atten- tion, despite its obvious importance.
Forest fire prediction. Much of the prior work on data- driven fire risk prediction has targeted woodland and forest fires, such as in Italy [17], Greece [14], and Portugal [9]. They used different methods, such as neural networks [9], fuzzy algebra [14], and decision trees [17] to support the al- location of firefighting, fire prevention, and foliage recuper- ation resources to the areas of highest fire risk. The features they used, such as soil type and topography, are very differ- ent from the ones typically used in urban fire prediction like construction material and property usage type.
Community-level urban fire prediction. Prior work in data-driven urban fire risk prediction tends to work at the region or community level [5, 8], rather than the property- or building-level, which is the unit that the Atlanta fire in- spectors are assigned to inspect. For instance, [5] undertook a randomized controlled trial of community fire risk edu- cation efforts, targeting high-risk residential communities. However, their method for identifying the high-risk areas was to create a point-distribution map of residential struc- ture fires and draw ellipses to capture the areas of densest concentration of fire incidents. A more methodologically rig- orous approach, as seen in [8]’s work on optimizing smoke- alarm inspections, joins data from the American Community Survey and American Housing Survey to predict municipal blocks most likely to have homes without functioning smoke alarms, using a Random Forest. Our work similarly uses publicly available datasets to predict properties most likely to be in need of inspection, but differs in that we offer a fire risk prediction score for individual commercial properties, rather than municipal residential blocks.
Property-level urban fire prediction. There is lim- ited work on predicting fire risk at the property or build-ing level. In British Columbia, [12] developed a risk-based model for determining the frequency of commercial prop- erty fire inspections, using static and dynamic building-level characteristics. They scored each property by its level of compliance on prior inspections and by a set of risk metric components such as building classification, age, and presence of sprinklers. However, as they acknowledge, the weights and selection of those components were based on their fire code, and not on historical data on features that were highly predictive of fire, such as we utilize in our work.
The nearest precedent for our research with AFRD is the recent work from the New York Mayor’s Office of Data An- alytics (MODA) with the Fire Department of New York (FDNY) to build a “Risk-Based Inspection System” (RBIS) [6]. They built a data-driven model to identify structures at greatest fire risk, to better prioritize FDNY’s inspection process, using a set of structural and behavioral information about those properties. However, due to a lack of detailed information on their technical approach, it is unclear how it may apply to AFRD’s scenario.
In both the FDNY RBIS initiative and our work with AFRD, a key challenge emerged: the difficulty of joining dis- parate datasets about commercial properties, gathered from various city departments without a shared convention for building ID numbers, consistent address formats, or strict internal quality control practices to ensure the datasets are accurate and up-to-date. We differ from [6] and [12] by pro- viding a clear method for identifying new inspectable com- mercial properties that the fire department is not already aware of. Further, our work goes beyond [6] by presenting a detailed comparison of the performance of several machine learning algorithms for predicting the fire risk of commercial properties, and by incorporating them into an interactive GIS visualization for use by the AFRD fire inspectors and Community Risk Reduction Section, following





http://firebird.gatech.edu/KDD16_Firebird.pdf
