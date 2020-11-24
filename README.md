# CS-401 - P3 - ADA

## Signed Networks in Social Media

**`Team`:** BJR

**`Team Members`:** Balz Marty, Jimmy Wilde, Romain Gros

## Title - Analysis of social signed networks

## Abstract
A 150 word description of the project idea, goals, datasets used. What's the motivation behind your project? How do you propose to extend the analysis from the paper? What story would you like to tell, and why?

We would like to go beyond the different theories of social networks and work with unsupervised machine learning techniques for prediction purpose.

## Research Questions
A list of research questions you would like to address during the project.

1. Can we retrieve the balance and status signed networks theories, like in the given paper? Can we predict the sign of an edge using this theories, like in the given paper?
2. Is it possible to train the datasets to predict the sign of an edge by reducing it to a low rank matrix completion problem?
3. What information can we extract from the clusters of these signed networks? 


## Proposed dataset
List the dataset(s) you want to use, and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you've read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible given the datasets at hand.

On top of the datasets used in the paper, we will add a similar dataset downloaded from the same web site (https://snap.stanford.edu/data/#signnets) which represents the links between subreddits on Reddit. A subreddit is a community on the social media Reddit. Links are represented by a sentiment of the source community post towards the target community post, taking value +1 or -1. The signed network can easily be computed from this dataset.
This dataset has a number of nodes and edges of a similar order than the other datasets used in the paper. Its format is equivalent to the Slashdot and Epinions datasets.

## Methods

Matrix factorization and low rank approach on sparse adjacency matrix.

## Proposed timeline

1. Reproduce P2 with the Reddit dataset.
2. Reproduce all the other figures in the paper with all datasets.
3. Report results on prediction using matrix factorization.
4. Work on the information given by clusters in the networks.


## Organization within the team
A list of internal milestones up until project milestone P4. Add here a sketch of your planning for the next project milestone.

Task 2 will have to be separated between each member of the team while Task 1-3-4 can each be done individually by a member of the team.

## Questions for TAs (optional)
Add here any questions you have for us related to the proposed project.

Do we need to replicate all the figures of the paper or only the ones we find to be significant?

## Ressources

CHIANG, Kai-Yang, HSIEH, Cho-Jui, NATARAJAN, Nagarajan, et al. Prediction and clustering in signed networks: a local to global perspective. The Journal of Machine Learning Research, 2014, vol. 15, no 1, p. 1177-1213.
