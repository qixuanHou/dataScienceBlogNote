Notes:
* hour_df['month'] = hour_df.month.astype('category')
* ohe = preprocessing.OneHotEncoder()
  http://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html 
* regression
```python
X = train_df_new
y = y.total_count.values.reshape(-1,1)

lin_reg = linear_model.LinearRegression()

# using the k-fold cross validation (specifically 10-fold) to reduce overfitting affects
# cross_val_predict function returns cross validated prediction values as fitted by the model object.

predicted = cross_val_predict(lin_reg, X, y, cv=10)
```


how to understand residuals of regression model
http://docs.statwing.com/interpreting-residual-plots-to-improve-your-regression/

https://www.kaggle.com/marklvl/explanatory-data-analysis-on-bike-sharing-dataset
