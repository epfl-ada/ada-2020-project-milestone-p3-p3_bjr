# CS-401 - P3 - ADA

## Signed Networks in Social Media

**`Team`:** BJR

**`Team Members`:** Balz Marty, Jimmy Wilde, Romain Gros

## Predicting interactions using signed social networks

### Abstract
First, we are using tools from [graph theory](https://en.wikipedia.org/wiki/Graph_theory) to further investigate and compare networks from the [original paper](https://cs.stanford.edu/people/jure/pubs/triads-chi10.pdf) and a [similar one](https://snap.stanford.edu/data/#signnets) from the social media Reddit. We are looking into graph-efficiency and small-world metrics. We are then trying to corroborate the hypothesis that the graph consists mainly of positive clusters and negative bridges between them by checking if the [sparsest cut](https://en.wikipedia.org/wiki/Cut_%28graph_theory%29#Sparsest_cut) does disproportionally affect negative edges.
Second, we wish to come up with models that predict edge signs to better understand the psychology of signed interactions on social media. We are using [matrix factorization](https://en.wikipedia.org/wiki/Matrix_factorization_%28recommender_systems%29) and logistic regression. The former is handily interpretable; latent variables can be seen as modeling the factors that contribute to the esteem for and from other types of users. Matrix factorization thus implicitly generates individual preference profiles for each user. The latter is applied to disentangle the magnitude of effects suggested by theories on *status*, *balance*, and *embeddedness*.

### Research Questions
1. Are signed networks from different social media platforms alike in terms of additional graph-theoretical properties?
2. Are these networks efficient and do they have small-world properties?
3. Can we validate the claim made by Leskovec *et al.* that negative edges tend to connect dense positive clusters?
4. Is it possible to predict the sign of an edge accurately? What can such a models reveal about the psychology of signed interactions on social media?

### Proposed additional dataset
In addition to the datasets used by Leskovec *et al.*, we are considering a similar dataset from [this website](https://snap.stanford.edu/data/#signnets) where the other datasets can be obtained as well. This dataset contains links between subreddits on Reddit. A subreddit is a community on the social media platform Reddit. Links are represented by a sentiment of the source community post towards the target community post, taking value +1 or -1. The signed network can easily be computed from this dataset. This dataset has a number of nodes and edges comparable to the original datasets. Its format is therefore equivalent to the Slashdot and Epinions datasets.

### Methods
For the first part, we will be using [NetworkX](https://networkx.org/) to compare [clustering coefficients](https://en.wikipedia.org/wiki/Clustering_coefficient) and [average path lengths](https://en.wikipedia.org/wiki/Shortest_path_problem). We are also computing the [graph laplacian](https://en.wikipedia.org/wiki/Laplacian_matrix) to obtain the sparsest cut.
In the second part, we will use [singular value decomposition](https://en.wikipedia.org/wiki/Singular_value_decomposition) (SVD) to perform the matrix factorization. To visualize the "preference profiles" of users, we could be using clustering and dimensionality reduction techniques such as PCA or t-SNE. For the logistic regression part, we are going to generate features which are expected to have more or less predictive power depending on the different theoretical considerations (e.g. the number of common neighbors, a balance and a status score based on the triads that the edge is involved in, etc.).

### Proposed timeline

#### Week 1
1. Reproduce P2 and the individual part of P4 with the Reddit dataset in order to see whether this dataset is similar to the others.
2..
#### Week 2
3. Perform matrix factorization, subsequent clustering and logistic regression.
4. Discuss and visualize the findings.
#### Week 3
5. Prepare the data story and the short video.

### Organization within the team

Up until now, the collaboration in the team went smoothly. We had a flexible organization for the homework; each one of us was just doing the next step that needed to be done whenever he had time to work on it. We communicated frequently and when a task was not straight-forward, we helped each other out right away. Overall, each of us invested roughly the same amount of time. Because this laissez-faire approach worked so well, we plan to continue in the same manner. Should we not be able to stick to the proposed timeline or if we notice that the workload gets unequally distributed, we can always fall back on a stricter regime.

### Contributions of group member

**Balz Marty**: replication of P3 with the Reddit dataset, analyzing properties of the network

**Jimmy Wilde**: feature matrix used for the regression

**Romain Gros**: training the model, reporting result of prediction, visualization of the preferences profiles of users

We have worked conjointly on the report.

#### Resources
CHIANG, Kai-Yang, HSIEH, Cho-Jui, NATARAJAN, Nagarajan, et al. Prediction and clustering in signed networks: a local to global perspective. The Journal of Machine Learning Research, 2014, vol. 15, no 1, p. 1177-1213.
