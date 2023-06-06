# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import dataset and print head,info of the dataset

2.check for null values

3.Import kmeans and fit it to the dataset

4.Plot the graph using elbow method

5.Print the predicted array

6.Plot the customer segments

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: logeshwaran s
RegisterNumber:  212220040081
##program##

import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans

wcss=[]

for i in range(1,11):

kmeans=KMeans(n_clusters=i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No.of.clusters")

plt.ylabel("wcss")

plt.title("Elbow Method")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()

plt.title("customer segments")

*/
```

## Output:
# Data Head
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/67937bce-772e-423f-a217-fb3ef3ff2519)
# Data Info
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/4a877d08-f1cc-4ec3-b01f-cb5ee9788a0b)
# Total rows
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/156d1765-5982-4eb1-941e-eb9412a24697)
# Clusters using Elbow method
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/b6371b99-96d7-45f3-8b7d-281aeac17c10)
# k-means clustering
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/3a2510b8-f7ce-4f5b-9322-6653e4997827)
# y_pred data
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/29cb7939-92b0-4eae-bd6d-c4f703b7670a)
# Customer Segments graph
![image](https://github.com/ATHDY005/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/84709944/6078cf6c-f8e2-4989-868d-5aa4a3016f38)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
