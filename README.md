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
