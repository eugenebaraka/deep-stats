# Measures of Dispersion Explained 

## Variance

If you have been working with data for a while, you (probably and hopefully) know what variance is. However, since it is easy to calculate it with one line of code in python or R, it is likely for the actual meaning to slip away. In this repo, I will visually breakdown the formula of variance, which doesn't usually make sense for beginners in statistics. 

The variance can be calculated as 


[INSERER LA FORMULE]

Let's use a python's built in dataset to break down this formula:



Variance is a numerical value that explains how far away data points are from the mean, and hence from each other. 
- A variance of zero means all data is similar (we have only one data point)
- The higher the variance, the more disperse our data is (the data points are far away from the mean and from each other)
- The lower the variance, the less disperse the data is (data points close to the mean and to each other)
- Variance cannot be negative!

As discussed above, variance is a distance. So it is calculated as the mean of the squared distances from the mean. 

Let's consider the figure below. 

## Population Variance versus Sample Variance

