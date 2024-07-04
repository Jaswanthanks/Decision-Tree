# Decision-Tree

# Decision Tree Parameters
This document provides an overview of key parameters used in decision tree algorithms. These parameters are essential for controlling the behavior and performance of decision trees in machine learning tasks.

# Depth and Sample Requirements

1. max_depth
Defines the maximum depth of the tree.
Limits how deep the tree can grow, controlling the potential overfitting.

2. min_samples_split
The minimum number of samples required to split an internal node.
Controls the size of the population of leaf nodes.

3. min_samples_leaf
The minimum number of samples required to be at a leaf node.
Ensures that leaf nodes contain a sufficient number of samples to make reliable predictions.

4. min_weight_fraction_leaf
The minimum weighted fraction of the sum total of weights required to be at a leaf node.
Similar to min_samples_leaf but takes sample weights into account.

# Node and Split Control

1. max_leaf_nodes
Limits the number of leaf nodes in the tree.
Helps in creating a simpler model by reducing overfitting.
Produces the best nodes by maximizing the reduction in impurity.

2. min_impurity_decrease
A node will be split if this split induces a decrease in impurity greater than or equal to this value.
Controls the trade-off between the depth of the tree and the impurity of the splits.

# Splitting Criteria

1. criterion

Defines the function to measure the quality of a split.
Common options include "gini" for the Gini impurity and "entropy" for information gain.

2. splitter

Defines the strategy used to choose the split at each node.
Options include "best" for the best split and "random" for a random split.

# Feature and Randomness Control

1. max_features
The number of features to consider when looking for the best split.
Options include:
int: Consider max_features features at each split.
float: max_features is a fraction 
"sqrt": max_features=sqrt(n_features).
"log2": max_features=log2(n_features).
None: max_features=n_features.

2. random_state
Controls the random number generator used to shuffle the data.
Ensures reproducibility of the model by setting a seed for the random number generator.

# Classification Specific Parameter

1. class_weight
Adjusts the importance of different classes in classification tasks.
Useful when dealing with imbalanced datasets where some classes are more important than others.
Helps improve the performance of the classifier on the minority class by increasing its weight.
