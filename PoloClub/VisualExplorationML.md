## Visual Exploration of Machine Learning Results using Data Cube Analysis
### ABSTRACT
We present our ongoing work on developing interactive and visual approaches for exploring and understanding machine learning results using data cube analysis. 

### INTRODUCTION
**Introducing MLCube Explorer.** 
**Drilling down model results.**
**Interactive visualization.** 

### BACKGROUND: A TYPICAL MACHINE LEARNING PIPELINE

### MLCUBE: DATA CUBES FOR MACHINE LEARNING
For the measure attributes of the cube (i.e., values to be aggregated), we find the following measures particularly use- ful for analyzing model results:
• Accuracy (or any evaluation measure, such as AUC) for a model
• Accuracy difference between two models
• Number of instances(model-independent).
• Proportion of positive instances(model-independent)

### VISUAL EXPLORATION OF MLCUBE
This section presents MLCube Explorer, an interactive vi- sualization tool for exploring machine learning results us- ing MLCube. Interactive visualizations has been proven to be very effective for finding interesting patterns and spot- ting anomalies from large, multidimensional data by effec- tively representing data and allowing users to interact with them [22, 23, 1, 15]. We first introduce the interface of our visualization tool and describe operations for users to inter- act with the interface. Then we present a usage scenario of how the tool can help a machine learning engineer under- stand models.
#### User Interface
* (1) the subset summary view which shows summary statistics for each subset and 
* (2) the correlation matrix view which visualizes its pairwise cor- relations to other subsets. 
#### Interactive Operations
Users can interact with the interface to further explore MLCube using the following operations.
1. Drill-down/Roll-up into a subset
2. Adding user-defined subsets
3. Using different measures
4. Sorting subsets
#### Usage Scenario
* Recognizing data encoding issue.
* Analyzing the performance improvement. 

https://www.cc.gatech.edu/~dchau/papers/16-sigmod-mlcube.pdf
