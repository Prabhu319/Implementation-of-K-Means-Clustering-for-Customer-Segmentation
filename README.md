# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: prabanjan.m
RegisterNumber:24900428
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
print("data.head()")
data.head()
print("data.info()")
data.info()
print("data.isnull()")
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
KMeans(n_clusters=5)
y_pred=km.predict(data.iloc[:,3:])
print("Prediction")
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="green",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="pink",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="yellow",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="blue",label="cluster4")
plt.legend()
plt.title("Customer Segments")

*/
```

## Output:
## data.head()
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/59901714-73e0-48e1-9854-4b76959abca0)

## data.info()
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/a2f116f1-7057-4d7e-bd91-c4a73866f277)
## data.isnull.sum
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/22768e51-9d3c-4432-ae8d-59ac86f29f16)
## Elbow method Graph
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/f58a3789-52af-4f02-982d-c5db15e6d1d1)
## Kmeans cluster
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/6e9d7e61-007c-4ab6-8f4d-fb21fe8cc3b0)
## Customer segments Graphs
![image](https://github.com/Samuelmariappan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119393030/fa9b9ca5-eb84-4148-a733-d83d24ccea71)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
