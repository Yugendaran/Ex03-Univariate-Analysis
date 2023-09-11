# Ex03-Univariate-Analysis

## AIM:
To read the given data and perform the univariate analysis with different types of plots.

## EXPLAINATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## ALGORITHM:

Step1:Read the given data set  using standard libraries.

Step2:Get the information about the data.

Step3:Remove the null values from the data.

Step4:Mention the datatypes from the data.

Step5:Count the values from the data.

Step6:Do plots like sepallength,species,sepalwidth.

## PROGRAM:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/iris.csv")

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_width","sepal_width").add_legend();
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_length","sepal_length").add_legend();
plt.show()

sns.pairplot(df,hue="species",size=3)

```

## OUPTUT:

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/672760bc-3333-4e18-aace-5d38f7ee37a1)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/2afebd8f-cf6b-4e41-a0bc-5c8c2996c72b)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/174e0739-e2c8-431a-b3e4-43060cee8998)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/62df5ad7-b064-4c54-b018-78de66713e4e)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/5cbb4abe-0150-4b52-84f1-226235291dda)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/424072a8-a1bb-4cd8-9f02-74d55d8ce0e3)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/c38867f6-7b52-49ce-87a3-3e4ef4aaad55)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/300d70ae-343d-420d-9d65-d6747c439539)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/fe5da9c2-5cbe-48b7-ac67-6412b29cc850)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/4fa94823-afa6-4b9c-8db6-d41176359162)

![image](https://github.com/Yugendaran/Ex03-Univariate-Analysis/assets/128135616/8e81c31d-4d44-41c4-a5c1-43ef964a723b)


## RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots are created and verified successfully.








