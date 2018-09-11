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
Deep learning is being used with increasing frequency to solve prob- lems in the domain of computational sustainability and urban plan- ning. Convolutional neural networks have been used to predict the spatial distribution of poverty in developing countries by using night- time lights as a data rich target for a transfer learning task [17, 34]. Pre- trained CNNs have recently been shown to be effective at the problem of remote sensing image scenes classification through the tuning a small number of layers [16, 24]. Similarly, deep learning has been shown to be effective in the task of classifying land cover type, with recent work that has achieved high classification accuracy on new large land cover datasets using mixed CNN based approaches [1, 3].
The most similar work to ours also uses CNNs to estimate popula- tion from satellite imagery [9]. The motivation of this paper is similar to ours, as we both attempt to create high-resolution gridded popu- lation counts for use in planning applications. This paper estimates population in Kenya at a 8km resolution with a CNN trained on data from Tanzania at a 250m satellite pixel resolution. The author’s propose a way to use their CNN’s output as a weighted surface for population disaggregation, and compare this method to others for dis- aggregating population counts in Kenya. Our work differs in several important ways. First, we focus on validating our model’s predictions as raw population projections and do not consider using our model’s prediction as a weighted surface for distributing population counts. If the population (or projected population) of an area is known a priori, then any population assignment method can degrade into a weight- ing scheme. Secondly, we focus on interpreting our model’s results as a way of validating its generalizability. Thirdly, we apply our method to the entire US using census block derived training and testing data.
Other related work is divided between the two problems we aim to address jointly with our method: population projection and popu- lation disaggregation. In the following paragraphs we address each of these problems to give context to our methodology.
On average, county population can be reliably extrapolated over short time horizons with simple linear models, however if some coun- ties experience disproportionally higher or lower growth rates, more complicated models are needed [29]. The US Census has led research into population and demographic projections, and uses a variety of different population and demographic projection methods to create sub-national projections broken down by age, sex, and race [21, 22]. Census postcensal projections, projections done in between census years, are created with a method known as the ratio-correlation method [21, 25, 32]. This method uses the current year’s estimated population, number of live births, registered vehicles, public school enrollment, registered voters, deaths, and other information to de- termine the estimated population change at the next census date. More recently, the American Community Survey has been used as annual supplemental surveys to update the demographics profiles of a variety of sub-national areas in between census years [23, 33].
Population disaggregation methods, and the creation of high res- olution population grids have been studied for decades [7, 15]. The most basic method in this class is areal interpolation, whereby the known population of an administrative zone is distributed uniformly across its area [14]. This process acts on a discretized grid over an ad- ministrative zone, where each cell in the grid is assigned a population value equal to the total population over the total number of cells that cover an administrative zone. Dasymetric weighting schemes extend this idea of distributing the known population of an area by creating a weighted surface to distribute the known population, instead of doing so uniformly. The weighting schemes are determined by combining different spatial layers (e.g., slope, average rainfall, land/water masks) according to some set of rules. While some weighting schemes are completely ad-hoc, recently, machine learning methods have been used to improve upon this approach [13, 30, 31]. These methodologies are similar to traditional supervised machine learning problems [20], but since actual ground truth data does not exist to compare against, validating dasymetric model results is challenging. Finally, there are many existing gridded population datasets created using a variety of the previously mentioned disaggregation techniques. Briefly, these include: Gridded Population of the World [10], GRUMP [26], Land- scan [4, 8], as well as the AfriPop, AsiaPop, and AmeriPop databases.




Caleb Robinson, Fred Hohman, and Bistra Dilkina. 2017. A Deep Learning Approach for Population Estimation from Satellite Imagery. In GeoHuman- ities’17: GeoHumanities’17:1st ACM SIGSPATIAL Workshop on Geospatial Hu- manities , November 7–10, 2017, Los Angeles Area, CA, USA. ACM, New York, NY, USA, 8 pages. https://doi.org/10.1145/3149858.3149863
