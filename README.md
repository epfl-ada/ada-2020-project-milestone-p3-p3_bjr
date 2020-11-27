# CS-401 - P3 - ADA

## Signed Networks in Social Media

**`Team`:** BJR

**`Team Members`:** Balz Marty, Jimmy Wilde, Romain Gros

## Predicting interactions using signed social networks

### Abstract
First, we are using tools from graph theory to further investigate and compare the networks from the [original paper](https://cs.stanford.edu/people/jure/pubs/triads-chi10.pdf) and a similar one from [Reddit](https://snap.stanford.edu/data/#signnets). We are looking into graph-efficiency and small-world metrics. We are trying to corroborate the hypothesis that the graph consists of positive clusters and negative bridges between them by checking if the [sparsest cut](https://en.wikipedia.org/wiki/Cut_%28graph_theory%29#Sparsest_cut) does disproportionally affect negative edges.
Second, we wish to come up with models that predict edge signs to better understand the psychology of signed interactions on social media. We are using [matrix factorization](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29). The technique has the advantage of being interpretable; latent variables can be seen as modeling the factors that contribute to the esteem for and from other types of users. Matrix factorization thus implicitly generates individual preference profiles for each user. Logistic regression will be applied to disentangle the magnitude of effects suggested by theories on *status*, *balance*, and *embeddedness*.

### Research Questions
1. Are signed networks from different social media platforms alike in terms of additional graph-theoretical properties?
2. Do these networks efficient and do they have small-world properties?
3. Can we validate the claim made by Leskovec *et al.* that negative edges tend to connect dense positive clusters?
4. Is it possible to predict the sign of an edge accurately? What can such a models reveal about the psychology of signed interactions on social media?

### Proposed additional dataset
In addition to the datasets used by Leskovec *et al.*, we are considering a similar dataset from the same [website](https://snap.stanford.edu/data/#signnets) where the other datasets can be obrained. This dataset contains links between subreddits on Reddit. A subreddit is a community on the social media platform Reddit. Links are represented by a sentiment of the source community post towards the target community post, taking value +1 or -1. The signed network can easily be computed from this dataset. This dataset has a number of nodes and edges comparable to the original datasets. Its format is therefore equivalent to the Slashdot and Epinions datasets.

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
