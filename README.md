# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries such as pandas, matplotlib, and KMeans clustering from sklearn.
2. Load the customer dataset (Mall_Customer.csv) and select the features Annual Income and Spending Score for clustering.
3. Create the K-Means model with 5 clusters, train the model using fit_predict(), and group the customers into different clusters.
4. Plot the clustered customer data and centroids using a scatter plot, then display the graph with labels and title.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Danaseelan G
RegisterNumber:  212225040053
*/
```


```
# Simple K-Means Clustering Program for Customer Segmentation

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customer.csv")

X = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(X)

plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')

# Labels
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()

```
## Output:
<img width="838" height="566" alt="WhatsApp Image 2026-05-15 at 2 38 22 PM" src="https://github.com/user-attachments/assets/34ff5023-b8ba-47fb-ab4a-6f3783650f91" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
