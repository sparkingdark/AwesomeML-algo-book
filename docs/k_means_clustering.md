# K means Clustering 

The other algorithm we will cover is the k-means algorithm. Unlike hierarchical clustering, we know beforehand the number of clusters that we want (k).

The basic algorithm for k-means clustering is as follows:
Choose a k-value for the number of clusters we want to end up with.
Select k number of starting points that we want to initialize to start our clusters. 
For each data point, find the closest mean vector and assign the object to the corresponding cluster.

For each cluster, update its mean vector according to the current assignments.

![A iteration](./images/k_means/graph.png)

We keep repeating the last two steps until a stopping criteria is met. Unlike the hierarchical clustering algorithm, the k-means clustering algorithm isn't always guaranteed to terminate. It can stop during convergence, when the algorithm no longer reassigns points, or it can run indefinitely until it stops at a user-defined number of iterations.
This contrasts with hierarchical clustering which has a more finite and predictable termination step (when everything is inside of one cluster). Additionally, the k-means algorithm may produce different outcomes based on how we initialize our initial k points.
Here is an animation that shows how k-means clustering behaves.

![Graph](./images/k_means/graph.png)


## Reference Used

https://zhonglab.gitbook.io/3dgenome/appendix-homework/students-note/a-brief-introduction-to-machine-learning#k-means-clustering