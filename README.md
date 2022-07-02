# Measures of Dispersion Explained 

## Variance

In my data science learning journey, I set a goal to really understand the fundamental topics before moving on to advanced ones. Instead of striving to learn as many things as I can, I slow down and really understand how things work under the hood. This is because I believe that "you can't fix what you don't understand" and understanding is totally different from knowing. This weekend, I revisited my statistics basics and thought of writing about an easy way to understand variance. 

In this article, I will discuss:
- How to make sense of variance by using visuals
- Why population variance and sample variance have different denominators
- Write a variance function from scratch

First, let do a little refresher on what variance is:

Variance is a statistical measure that explains how far away data points are from the mean, and hence from each other. 
- A variance of zero means all data is similar (we have only one data point)
- The higher the variance, the more disperse our data is (the data points are far away from the mean and from each other)
- The lower the variance, the less disperse the data is (data points close to the mean and to each other)
- Variance cannot be negative!


The variance is calculated as 

![variance](/assets/var.png)

Let's use python's scikit-learn built-in dataset, the Iris dataset, to break down this formula. Please find the full notebook on my [github](/variance.ipynb)

We will import all necessary libraries first:

```
# importing necessary libraries
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
from sklearn.datasets import load_iris
```

Loading and visualizing the first 7 rows of the data

```
iris = load_iris()
df = pd.DataFrame(iris.data, columns=iris.feature_names)
df.head(7)
```

![first 7 rows](/assets/head.png)

For simplicity we will exclusively use the first column of the data, but the process is the same! By visualizing the distribution of sepal length, we see that is pretty much normally distributed with a mean of around 5.8 cm.

![Distribution of sepal length](/assets/output.png)



As discussed above, variance is a distance. So it is calculated as the mean of the squared distances from the mean. 

Let's consider the figure below. 

## Population Variance versus Sample Variance

