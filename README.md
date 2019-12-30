# Parallel-KMeans-using-Map-Reduce
K-Means
To process the learning data, the K-means algorithm in data mining starts with a first
group of randomly selected centroids, which are used as the beginning points for every
cluster, and then performs iterative (repetitive) calculations to optimize the positions of
the centroids.
The way kmeans algorithm works is as follows:
1. Specify number of clusters K .
2. Initialize centroids by first shuffling the dataset and then randomly selecting
K data points for the centroids without replacement.
3. Keep iterating until there is no change to the centroids. i.e assignment of
data points to clusters isn’t changing.
4. Compute the sum of the squared distance between data points and all
centroids.
5. Assign each data point to the closest cluster (centroid).
6. Compute the centroids for the clusters by taking the average of the all data
points that belong to each cluster.

# MapReduce & Hadoop with Python
We chose to implement the code in python as it is the easiest with machine learning and
big data algorithms like this one, with all the different libraries and functionalities.
However, since hadoop is java based, only the later versions of hadoop started to
provide support to implement MapReduce codes in other languages, using the Hadoop
Streaming interface.
## Mapper
### Takes:

● data

● centroids

### Computes:

● the nearest center for each data instance

### Emits:

● nearest centers ( key ) and points ( value ).

## Reducer
### Takes:

● center instance / coordinate ( key ) from mapper

● points ( value )

### Computes:

● the new centers based on clusters

### Emits:
● new centers

