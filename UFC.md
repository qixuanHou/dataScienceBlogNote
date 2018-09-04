### UFC
#### Introduction
Mixed martial art(MMA) is a full-contact combat sport. The Utimate Fighting Championship(UFC) is an American MMA.
#### Missing values
use median or mean to replace NaN
```Python
df['B_Age'] = df['B_Age'].fillna(np.mean(df['B_Age']))
```
### Data visualization 
```Python
import matplotlib.pyplot as plt
import seaborn as sns
from plotly.offline  import download_plotlyjs,init_notebook_mode,plot, iplot
import cufflinks as cf

from plotly import tools
import plotly.plotly as py
from plotly.offline import init_notebook_mode, iplot
import plotly.graph_objs as go
import plotly.figure_factory as ff
import plotly.offline as offline
```
![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/ufc_pie.png)
```Python
temp = df["winner"].value_counts()
fig = {
  "data": [
    {
      "values": temp.values,
      "labels": temp.index,
      "domain": {"x": [0, 1]},
      "hole": .6,
      "type": "pie"
    },
    
    ],
  "layout": {
        "title":"Winner",
        "annotations": [
            {
                "font": {
                    "size": 17
                },
                "showarrow": False,
                "text": "Whos winning more",
                "x": 0.5,
                "y": 0.5
            }
            
        ]
    }
}
iplot(fig, filename='donut')
```

![Alt Text](https://github.com/qixuanHou/dataScienceBlogNote/blob/master/img/ufc_bar.png)
```
fig, ax = plt.subplots(1,2, figsize=(15, 5))
sns.distplot(df.B_Age, ax=ax[0])
sns.distplot(df.R_Age, ax=ax[1])
```

<small>https://www.kaggle.com/rishpande/ufc-data-analysis-visualization-beginner</small>
