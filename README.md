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

* Classification Metrics : 
> Confusion matrix<br>
> accuracy<br>
> precision, recall<br>
> classification report<br>
