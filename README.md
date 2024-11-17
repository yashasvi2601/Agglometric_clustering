Agglomerative Hierarchical Clustering Report
1. Dataset Description
The dataset used for this analysis is the Iris dataset, which contains 150 samples of iris flowers. The
features represent four measurements:
1. Sepal length (cm)
2. Sepal width (cm)
3. Petal length (cm)
4. Petal width (cm)
The dataset also includes a target column with three classes, representing the species of the iris
flowers (Iris-setosa, Iris-versicolor, and Iris-virginica). However, for clustering purposes, the target
column was excluded to perform unsupervised learning.
Preprocessing steps:
- Scaling: The feature values were standardized using StandardScaler to ensure all features have a
mean of 0 and a standard deviation of 1. This is crucial since hierarchical clustering is sensitive to
feature magnitudes.


2. Linkage Method and Distance Metric
Linkage Method: Ward's method was chosen because it minimizes the variance within clusters,
producing compact and spherical clusters. This method is effective for datasets like Iris, where
clusters are relatively well-separated.
Distance Metric: Euclidean distance was used, which measures the straight-line distance between
points in the feature space. It is the most commonly used metric for clustering continuous numerical
data.


4. Clustering Results
Using Agglomerative Hierarchical Clustering, we set the number of clusters to 3 based on the
dendrogram analysis.
Observations:
- The clusters corresponded closely to the actual species in the dataset.
- Most data points were assigned to their respective species correctly, as observed in the scatter
plot and cluster labels.
Cluster Characteristics:
- Cluster 1: Consisted primarily of Iris-setosa, which is the most distinct species due to its smaller
petal measurements.
- Cluster 2 and Cluster 3: Divided the samples of Iris-versicolor and Iris-virginica. These two species
had overlapping feature spaces, causing slight misclassifications between them.


4. Strengths and Weaknesses
Strengths:
- Interpretability: The dendrogram provided a clear visual representation of the hierarchical structure.
- No need for predefined cluster count: The dendrogram allowed us to decide the optimal number of
clusters dynamically.
- Effective for small datasets: The algorithm efficiently handled the 150 samples.
Weaknesses:
- Scalability: Hierarchical clustering is computationally expensive for large datasets, as it requires
calculating the distance between all pairs of points.
- Sensitive to scaling: Without proper feature standardization, results can be misleading.
- Cluster shapes: It may struggle with irregularly shaped clusters or datasets with high overlap.


5. Reflection
This exercise provided valuable insights into the workings of Agglomerative Hierarchical Clustering
and its application to real-world datasets. The key learnings include:
- The importance of data preprocessing, particularly scaling.
- How linkage methods and distance metrics impact the clustering results.
- The role of visualization (dendrograms and scatter plots) in interpreting clustering outcomes.
Challenges Faced:
- Choosing the optimal number of clusters required careful analysis of the dendrogram and domain
knowledge.
- Handling the overlapping nature of Iris-versicolor and Iris-virginica clusters was challenging due to
their similar feature distributions.
