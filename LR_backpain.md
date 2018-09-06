### Normalization

we need to make the ranges between min and max values of each column equally. This can be done by fitting all values between 0 and 1. This is called Normalization.
```
#Normalize values to fit between 0 and 1. 
x = (new_data-np.min(new_data))/(np.max(new_data)-np.min(new_data)).values
```

### Assigning x and y Values

We need to split our data into two dimension as x and y values. y value is our class name, which gives if the row is Abnormal or Normal. So, we assign Class_att column as y values then drop the column from data set. The rest of the data ; all Col1, Col2..., Col12 columns will be our x value. Add .values function to convert both x and y values to numpy arrays.

### Implementation of Logistic Regression
#### Predictions
```
z = b + w_0 * x_0 + w_1 * x_1 + w_2 * x_2 + w_3 * x_3 + ...
```
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/sigmoid.png)
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/sigmoid_graph.png)

x value would be our x_train matrix. w means weights, and b means bias. But we haven't known what is b values, yet. We need to find weight values for each Col1, Col2,...,Col12 and a single bias value. For this dataset, our w matrix will have 12 values. Then we will multiply x_train matrix with transpose of w matrix and then add bias value. The result would have no meaning at this point, so we apply <strong>sigmoid function</strong> to find a y_head value. Sigmoid function gives the result a probabilistic value between 0 and 1. At first try, the result would be so wrong because we don't know what should be optimal w and b values.

```python
def predict(features, weights):
  '''
  Returns 1D array of probabilities
  that the class label == 1
  '''
  z = np.dot(features, weights)
  return sigmoid(z)
  ```
  
#### Cost & Loss
Then, according to y_head and y_train values, we will calculate the loss and cost of this iteration. At first iteration, cost would be so high because the result is wrong. We need to minimize the cost in order to find the optimal w and b values.
We use cross-entropy, which is divided into two separate cost functions,
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/lr_cost_2.png)
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/lr_cost.png)
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/lg_cost_vector.png)

![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/lg_cost_img.png)


```python
def cost_function(features, labels, weights):
    observations = len(labels)
    predictions = predict(features, weights)
    #Take the error when label=1
    class1_cost = -labels*np.log(predictions)
    #Take the error when label=0
    class2_cost = (1-labels)*np.log(1-predictions)
    #Take the sum of both costs
    cost = class1_cost - class2_cost
    #Take the average cost
    cost = cost.sum()/observations
    return cost
 ```
 
 #### Gradient Descent
Steps
  * 1. Calculate gradient average
  * 2. Multiply by learning rate
  * 3. Subtract from weights
```python
def update_weights(features, labels, weights, lr):
    N = len(features)
    #1 - Get Predictions
    predictions = predict(features, weights)
    #2 Transpose features from (200, 3) to (3, 200)
    # So we can multiply w the (200,1)  cost matrix.
    # Returns a (3,1) matrix holding 3 partial derivatives --
    # one for each feature -- representing the aggregate
    # slope of the cost function across all observations
    gradient = np.dot(features.T,  predictions - labels)
    #3 Take the average cost derivative for each feature
    gradient /= N
    #4 - Multiply the gradient by our learning rate
    gradient *= lr
    #5 - Subtract from our weights to minimize cost
    weights -= gradient
    return weights
```

training

 ```python
 def train(features, labels, weights, lr, iters):
    cost_history = []
    for i in range(iters):
        weights = update_weights(features, labels, weights, lr)
        #Calculate error for auditing purposes
        cost = cost_function(features, labels, weights)
        cost_history.append(cost)
        # Log Progress
        if i % 1000 == 0:
            print "iter: "+str(i) + " cost: "+str(cost)
    return weights, cost_history
 ```

<small>https://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html#cost-function</small>
<small>https://www.kaggle.com/meldadede/logistic-regression-for-lower-back-pain-symptoms</small>
