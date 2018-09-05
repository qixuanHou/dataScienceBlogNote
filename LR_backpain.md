### Normalization

we need to make the ranges between min and max values of each column equally. This can be done by fitting all values between 0 and 1. This is called Normalization.
```
#Normalize values to fit between 0 and 1. 
x = (new_data-np.min(new_data))/(np.max(new_data)-np.min(new_data)).values
```

### Assigning x and y Values

We need to split our data into two dimension as x and y values. y value is our class name, which gives if the row is Abnormal or Normal. So, we assign Class_att column as y values then drop the column from data set. The rest of the data ; all Col1, Col2..., Col12 columns will be our x value. Add .values function to convert both x and y values to numpy arrays.

### Implementation of Logistic Regression
```
z = b + w_0 * x_0 + w_1 * x_1 + w_2 * x_2 + w_3 * x_3 + ...
```
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/tree/master/img/sigmoid_graph.png)

![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/tree/master/img/sigmoid.png)

x value would be our x_train matrix. w means weights, and b means bias. But we haven't known what is b values, yet. We need to find weight values for each Col1, Col2,...,Col12 and a single bias value. For this dataset, our w matrix will have 12 values. Then we will multiply x_train matrix with transpose of w matrix and then add bias value. The result would have no meaning at this point, so we apply <strong>sigmoid function</strong> to find a y_head value. Sigmoid function gives the result a probabilistic value between 0 and 1. At first try, the result would be so wrong because we don't know what should be optimal w and b values.
Then, according to y_head and y_train values, we will calculate the loss and cost of this iteration. At first iteration, cost would be so high because the result is wrong. We need to minimize the cost in order to find the optimal w and b values.



https://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html#cost-function 

<small>https://www.kaggle.com/meldadede/logistic-regression-for-lower-back-pain-symptoms</small>
