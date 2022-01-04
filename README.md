# Lab4 - NFL clustering

## Goal

The goal of this lab is to become familiar with a clustering workflow. In the process, you will reuse and re-factor code we have seen in the lectures.

Based on National Football League (NFL) statistics, we will try and find clusters (groups) of receivers. We will try and describe the type of receiver in each cluster based on the cluster means. To be able to do clustering, we need to acquire some domain knowledge.

The role of a receiver is described on this [wide receiver](https://en.wikipedia.org/wiki/Wide_receiver) wikipedia page.

In short:
>The wide receiver's principal role is to catch passes from the quarterback. On passing plays, the receiver attempts to avoid, outmaneuver, or simply outrun defenders (typically cornerbacks or safeties) in the area of his pass route. ... Once a pass is thrown in his direction, the receiver's goal is to first catch the ball and then attempt to run downfield. 

We will use the following features:
- 'Rec': Number of receptions. Total number of times a receiver has caught the ball.
- 'Yds': Receiving yards. The number of yards gained by a receiver on a passing play, including the distance the ball was passed and any additional yardage the player gained after the reception.
- 'TD': Receiving touchdowns. A touchdown scored after a pass has been caught and the receiver makes it into the end-zone.
- 'Fmb': Number of times fumbled (a ball carrier loses the football during a play.)
- 'Ctch_Rate': Catch percentage = receptions / targets

for players with at least 20 pass targets (Tgt).

I found explanations to these features [here](https://www.sportingcharts.com/NFL/dictionary/).


## What to do

### Datasets
yellowbrick NFL: NFL Receiver statistics 
https://www.scikit-yb.org/en/latest/api/datasets/nfl.html

According to the yellowbrick documentation, the dataset comes from [here](https://www.pro-football-reference.com/years/2018/receiving.htm)


### Cluster algorithm
- `KMeans(random_state=54)`


### Steps

1. Load data.
2. Scale the dataset with StandardScaler
3. Find the number of clusters with the Elbow method
4. KMeans clustering with 5 clusters
5. Visualize clusters
6. Interpret clusters

### Specifications
Write the following functions: 
- `add_column_to_dataframe()`
- `plot_cluster_proportions()`
- `plot_cluster_centers()`

Function headers and documentation are included in `lab4.ipynb`. Implement the function body accordingly.

Use these functions to implement the tasks as directed.


## What to hand in
- In the Jupyter notebook `lab4.ipynb` implement the steps above as indicated. 
- Keep code clean and remove any unnecessary cells. 
- Use the results obtained to answer questions throughout the notebook.
- In a section *Reflection*, include a sentence or two about what you liked/disliked, found interesting/confusing/challangeing/motivating while working on this assignment.

During development, checkin progress with git and use descriptive commit messages.

