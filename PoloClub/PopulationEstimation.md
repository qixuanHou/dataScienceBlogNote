## A Deep Learning Approach for Population Estimation from Satellite Imagery
### Abstract
* The goal
  estimate population, and where do they live 
* Why the topic is important
  urban development, infectious disease containment, evacuation planning, risk management, conservation planning, and more
* The gap
  bottom-up. survey drivern censuses is expensive to realize in a frequent manner, and can only provide popluation counts over broad areas
* The method
  a deep learning modal for creating high resolution population estimations from satellite imagery 
  * train CNN to predict population in the USA at a 0.01°×0.01° resolution grid from 1-year composite Landsat imagery. 
  * validate with two ways
    * quantitatively, comparing the results to several US census county-level population projections
    * qualitatively, interpreting the model's predictions in terms of the satellite image inputs
* Generally
  the modal presents how machine learning techniques can be an effective tool for extracting information from inherently unstructured, remotely sensed data to provide effective solutions to social problems.

### Introduction
* why it is important to know population estimation - examples and citations about the importance of population estimation
* Gap - "Unfortunately, censuses in many other countries are non-representative due to limited civil registration systems"
* two main questions in this paper 
  * population projection: estimate the number of people that live in a particular administrative area based on historical data. 
  * population disaggregation: distribute a population estimate for a given administrative area within that area
* The proposed method

### Related Work
* Deep learning is being used with increasing frequency to solve problems in the domain of computational sustainability and urban planning. #### Data
* the Center For International Earth Science Infomration network US Census Summary Grids for 2000 and 2010
  * one similar work [9], estimates population in Kenya at a 8km resolution with a CNN trained on data from Tanzania at a 250m satellite pixel resolution. The paper differs in the following ways
    * focus on validating our model's predictions as raw population projections and do not consider using the models predictions as a weigthed surface for distributing popluation counts
    * focus on interpreting our model’s results as a way of validating its generalizability. 
    * apply our method to the entire US using census block derived training and testing data.
* population projection research 
* population disaggregation research

### Method
* P_t - grid of target population values covering the continental US
* C_t - grid of target poplution class values
* O_t - grid of satellite images
* regression format f(O_t_ij) = P_t_ij
* classification format g(O_t_ij) = C_t_ij
#### Data
* US Census Summary Grids for 2000 and 2010
* Landsat 7 1-year composite images for 2000 and 2010
* county level population data for 2000 and 2010
#### model architecture
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/satellite.png)
#### Experimental Setup 
* POSTCENSAL - comparing our model’s aggregate population estimates at the county level with US Census Postcensal county level estimates for 2010
* ACS5YR - comparing with American Community Survey 5-year estimates for 2006-2010 
* CONVRAW - converting the class values directly into population values
* CONVAUG - using the values from the softmax activations in the last layer of each CNN as “features” into a secondary machine learning model
### Results and Discussion
#### county level estimates
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/mapEval.png)
#### Prediction Interpretability 
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/top8.png)
* we show, for each class, the top 8 satellite image inputs from the testing set, that maximize the softmax output for that class. These images give us an insight into what types of features our model is learning. 
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/mapPeople.png)
* we show maps for several of the output population classes that show the estimated probability of each pixel belonging to the respective class. From these we observe that our model makes confident predictions about the 0 population class (Layer 0), and the higher population classes. The lack of confidence in the lower population classes (Layers 2 and 4) makes sense as we do not expect the visual difference between 1km2 areas in which 4 and 16 people live to be large. 
#### Prediction errors

### Future work and conclusion 



Caleb Robinson, Fred Hohman, and Bistra Dilkina. 2017. A Deep Learning Approach for Population Estimation from Satellite Imagery. In GeoHuman- ities’17: GeoHumanities’17:1st ACM SIGSPATIAL Workshop on Geospatial Hu- manities , November 7–10, 2017, Los Angeles Area, CA, USA. ACM, New York, NY, USA, 8 pages. https://doi.org/10.1145/3149858.3149863

[9] Patrick Doupe, Emilie Bruzelius, James Faghmous, and Samuel G Ruchman. 2016. Equitable development through deep learning: The case of sub-national population density estimation. In Proceedings of the 7th Annual Symposium on Computing for Development. ACM, 6.









