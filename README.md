# Cheatsheets
## For ML

* Estimator
> Binary Classifier : Logistic regression

* Missing data
> plot  :
>>sns.heatmap(df.isnull())  -   To look for missing values<br>
>>sns.boxplot()             -   To look for central tendency in order to impute<br>

> remove column if >40% is missing

* Plots : 
> categorical vs label : countplot(x=categorical, hue=label)<br>
> numerical vs label : histplot(x=numerical,hue=label)<br>
> categorical vs numerical vs label : barplot(categorical,numerical,hue=label)<br>
> numerical vs numerical vs label : scatterplot(numerical,numerical,hue=label)<br>

* EDA Plots:
> ```
> import seaborn as sns
> import matplotlib.pyplot as plt
> %matplotllib inline
> plt.figure(figsize=(10,8))
> plt.subplot(211) # 1st row plot#1
> sns.plot...
> plt.subplot(212) # 2nd row plot#2
> sns.plot... 
> ```

* Classification Metrics : 
> Confusion matrix<br>
> accuracy<br>
> precision, recall<br>
> classification report<br>

**Pipelines**
```
from sklearn.compose import make_column_transformer
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import FunctionTransformer


* model = Pipeline([ ("name",Transformer), 
                     ("name",Estimator) ])
* multiple_transform = make_column_transformer((Transformer,[columns]),
                                               (Transformer,[columns]),
                                                 ....
                                               )
  model = Pipeline([ ("name",multiple_transform) , 
                     ("name",Estimator) ])
* Multiple transform involving custom transformers :

  # Eg: add 1 to each value in the column(s)
  def custom_transformer(X): 
    return X+1
    
  custom_trans = FunctionTransformer(custom_transformer)
  multiple_transform = make_column_transformer((Transformer,[columns]),
                                               (Transformer,[columns]),
                                               (custom_trans,[columns]), 
                                                 ....
                                               )
  model = Pipeline([ ("name",multiple_transform) , 
                     ("name",Estimator) ])
  
    


Eg: 

1. inp1, target
   inp1 -> transformer1()

   model = Pipeline( [ ("tr", transformer1()), ("est",Estimator()) ] )
   model.fit(data['inp1'],data['target'])

2. inp1,inp2,inp3,inp4,target

   def custom_divide_by_1000(X):
        return X/1000
   
   inp1      -> transformer1()
   inp2      -> transformer2()
   inp3,inp4 -> custom_divide_by_1000()
       
    trans_custom=FunctionTransformer(custom_divide_by_1000)
    multiple_transform = make_column_transformer( (transformer1(),['inp1']),
                                                  (transformer2(),['inp2']),
                                                  (trans_custom,['inp3','inp4']) )

    model = Pipeline( [ ("multi", multiple_transform),
                        ("est",Estimator()) ])
    model.fit(data[['inp1','inp2','inp3','inp4']],data['target'])
```
                          
