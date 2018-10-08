* the way to display three dimonsion information by multiple bar charts
![Alt_Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/multiDimensionBarChart.png)

* logisticRegression
```Python
logr = LogisticRegression()
logr.fit(features, target)
logr.score(features, target)
// 0.80808080808080807
coeff_df = pd.DataFrame(train[cols].columns.delete(0))
coeff_df.columns = ['Feature']
coeff_df["Correlation"] = pd.Series(logr.coef_[0])
coeff_df.sort_values(by='Correlation', ascending=False)
```
![Alt_Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/titanicLogistic.png)

```python
rfr = RandomForestClassifier(n_estimators=1000, random_state=10, verbose=0)
rfmod = rfr.fit(features, target)
rfmod.score(features, target)
// 0.97979797979797978
etc = ExtraTreesClassifier(n_estimators=1000, max_depth=4, n_jobs=-1, random_state=1, verbose=0)
etcmod = etc.fit(features, target)

fi = etcmod.feature_importances_
importances = pd.DataFrame(fi, columns = ['importance'])
importances['feature'] = cols
importances.sort_values(by='importance', ascending=False)
```
![Alt_Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/titanicRandomF.png)

https://www.kaggle.com/rcasellas/titanic-kernel-random-forest-classifier
