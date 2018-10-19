## Difference between classification and anomaly detection
* You have labeled training data
* Anomalous and normal classes are balanced ( say at least 1:5)
* Data is not autocorrelated. ( That one data point does not depend on earlier data points. This often breaks in time series data).
If all of above is true, we do not need an anomaly detection techniques and we can use an algorithm like Random Forests or Support Vector Machines (SVM).

Another aspect is that the false positives are a major concern as we will discuss under acting on decisions. Hence, the precision ( given model predicted an anomaly, how likely it is to be true)  and recall (how much anomalies the model will catch) trade-offs are different from normal classification use cases. We will discuss this in detail later.

## what is anomaly detection?
* Point Anomalies. If an individual data instance can be considered as anomalous with respect to the rest of the data (e.g. purchase with large transaction value)
* Contextual Anomalies, If a data instance is anomalous in a specific context, but not otherwise ( anomaly if occur at a certain time or a certain region. e.g. large spike at the middle of the night)
* Collective Anomalies. If a collection of related data instances is anomalous with respect to the entire dataset, but not individual values. They have two variations.
  * Events in unexpected order ( ordered. e.g. breaking rhythm in ECG)
  * Unexpected value combinations ( unordered. e.g. buying a large number of expensive items)

## Anomaly detection techniques

https://iwringer.wordpress.com/2015/11/17/anomaly-detection-concepts-and-techniques/
https://www.kaggle.com/victorambonati/unsupervised-anomaly-detection
