# CS-401 - P3 - ADA

## Signed Networks in Social Media

**`Team`:** BJR

**`Team Members`:** Balz Marty, Jimmy Wilde, Romain Gros

## Title - Analysis of social signed networks

## Abstract
A 150 word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why?

*I think that we should decide what exactly it is that we try to achieve. The task sheet seems to spell out what we need to do quite precisely:
- we could perform a similar analysis as was done in the paper on another dataset. I guess that would be possible with the Reddit data.
- we can propose additional research questions. For instance, we could ask how efficient the networks are. In this case it might be interesting to look into the average shortest path length, small-world properties, ect. Ideally, we could compare that to other networks. Alternatively, we could also ask if we can predict links accurately. With a logistic regression we could try to disentangle the effects of embeddedness, local clustering, triadic type etc. on the missing link. We could also une a matrix factorization. This technique has the advantage that its results are to some degree interpretable. In a sense, it gives an estimate of how similar different users are with respect to the people they like and also which other people tend to like them. This would be yet another model next to status and balance. We would implicitly create a "psychological" profile of users, which could be predictive of the signs edges based on **similarity**.
- we could try to improve the methods. E.g. it would be possible to dig a little deeper when it comes to this theory of positive clusters and negative bridges between them. We could try to use the "graph laplacian" to get the sparsest cut... This is easy to implement with networkx.

*I do not think we should do all the above at once.

We would like to go beyond the different theories of social networks and work with unsupervised machine learning techniques for prediction purpose.

## Research Questions
1. Can we retrieve the balance and status signed networks theories, like in the given paper? Can we predict the sign of an edge using this theories, like in the given paper?
2. Is it possible to train the datasets to predict the sign of an edge by reducing it to a low rank matrix completion problem?
3. What information can we extract from the clusters of these signed networks? 


## Proposed dataset
On top of the datasets used in the paper, we will add a similar dataset downloaded from the same web site (https://snap.stanford.edu/data/#signnets) which represents the links between subreddits on Reddit. A subreddit is a community on the social media Reddit. Links are represented by a sentiment of the source community post towards the target community post, taking value +1 or -1. The signed network can easily be computed from this dataset.
This dataset has a number of nodes and edges of a similar order than the other datasets used in the paper. Its format is equivalent to the Slashdot and Epinions datasets.

## Methods
Matrix factorization and low rank approach on sparse adjacency matrix.

## Proposed timeline

1. Reproduce P2 and the individual part of P4 with the Reddit dataset.
2. Report results on prediction using matrix factorization.
3. Work on the information given by clusters in the networks (can be done in parallel with task 2.)


## Organization within the team
Task 1 will be relatively fast to be done (few hours). One of us will do this first task, and then help the others on the realization of the tasks 2 and 2 bis. We had a flexible organization during the homeworks, each one of us doing the next step that needed to be done when we had time to work on it. It worked pretty well and we will therefore continue with the same organization

## Questions for TAs (optional)


## Ressources

CHIANG, Kai-Yang, HSIEH, Cho-Jui, NATARAJAN, Nagarajan, et al. Prediction and clustering in signed networks: a local to global perspective. The Journal of Machine Learning Research, 2014, vol. 15, no 1, p. 1177-1213.
