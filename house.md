### House price analysis
```python
dt_train.corr()
f,ax = plt.subplots(figsize=(20,20))
sns.heatmap(dt_train.corr(), annot = True,linewidths=.4, fmt='.1f', ax=ax)
plt.show()
```
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/house_cor.png)
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/house_cor_heat.png)



https://www.kaggle.com/leventizci/house-prices-data-analysis
