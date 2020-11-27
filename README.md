# CS-401 - P3 - ADA

## Signed Networks in Social Media

**`Team`:** BJR

**`Team Members`:** Balz Marty, Jimmy Wilde, Romain Gros

## Predicting interactions using signed social networks

### Abstract
In this work, we propose to go beyond the social theories and to work with machine learning techniques for prediction purpose. The first idea would be to look into several properties of the networks (such as the average shortest path length, small-world properties, ect.), using unsupervized ML techniques. We would compare these properties to other networks, if possible. Additionaly, it could be possible to dig a little deeper when it comes to the theory of positive clusters and negative bridges between them. In a second time, we propose to determine if we can predict links accurately. For this, a logistic regression could help to disentangle the effects of embeddedness, local clustering, triadic type etc. on the missing link. Matrix factorization, whose results are to some degree interpretable giving an estimate of how similar different users are, could also be interesting to use. Indeed, we would implicitly create a "psychological" profile of users, which could be predictive of the signs edges based on similarity.

### Research Questions
1. What are similarities and differences of these signed networks compared to other networks? 
2. Is it possible to train the datasets to predict the sign of an edge by reducing it to a low rank matrix completion problem?
3. If possible, what could we learn from the "psychological" profile of users generated?

### Proposed additional dataset
On top of the datasets used in the paper, we will add a similar dataset downloaded from the same [website](https://snap.stanford.edu/data/#signnets). In this dataset, one can find the links between subreddits on Reddit. A subreddit is a community on the social media Reddit. Links are represented by a sentiment of the source community post towards the target community post, taking value +1 or -1. The signed network can easily be computed from this dataset. This dataset has a number of nodes and edges of a similar order than the other datasets used in the paper. Its format is equivalent to the Slashdot and Epinions datasets.

### Methods
For the first part, we will use unsupervized ML methods in order to obtain data from which we could determine several properties of the network. For the prediction part, we would use logistric regression, matrix factorization and low rank approach on sparse adjacency matrix. To learn from the "psychological" profile of users, we would have to find a way to show our data in a representative way, perhaps using dimensionality reduction techniques such as PCA or t-SNE.

### Proposed timeline
1. Reproduce P2 and the individual part of P4 with the Reddit dataset in order to see wether this dataset is different from the others.
2. Analyze several properties of the networks, determine suitable methods to obtain data that could be used for this task.
3. Report results on prediction using matrix factorization and logistic regression.
4. If 3. is successful, work on the information given by clusters in the networks and find ways to represent this information.
5. Prepare the data story and the short video.

### Organization within the team
Task 1 will be relatively fast to be done (few hours). One of us will do this first task, and then help the others on the realization of the tasks 2 and 3 (and 4, if needed). We had a flexible organization during the homeworks, each one of us doing the next step that needed to be done when we had time to work on it. We talked a lot between us, asking for how to do a particular task if it was not straight-forward. It worked very well and we will therefore continue with the same organization. We will also use this flexible organization for the data story and short video preparation.

#### Ressources
CHIANG, Kai-Yang, HSIEH, Cho-Jui, NATARAJAN, Nagarajan, et al. Prediction and clustering in signed networks: a local to global perspective. The Journal of Machine Learning Research, 2014, vol. 15, no 1, p. 1177-1213.


Balz part (faut aussi faire attention pcq l'abstract ne doit faire que environ 150 mots)
- we could perform a similar analysis as was done in the paper on another dataset. I guess that would be possible with the Reddit data.
- we can propose additional research questions. For instance, we could ask how efficient the networks are. In this case it might be interesting to look into the average shortest path length, small-world properties, ect. Ideally, we could compare that to other networks. Alternatively, we could also ask if we can predict links accurately. With a logistic regression we could try to disentangle the effects of embeddedness, local clustering, triadic type etc. on the missing link. We could also une a matrix factorization. This technique has the advantage that its results are to some degree interpretable. In a sense, it gives an estimate of how similar different users are with respect to the people they like and also which other people tend to like them. This would be yet another model next to status and balance. We would implicitly create a "psychological" profile of users, which could be predictive of the signs edges based on **similarity**.
- we could try to improve the methods. E.g. it would be possible to dig a little deeper when it comes to this theory of positive clusters and negative bridges between them. We could try to use the "graph laplacian" to get the sparsest cut... This is easy to implement with networkx.
