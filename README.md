# Measures of Dispersion Explained 

## Variance

If you have been working with data for a while, you (probably and hopefully) know what variance is. However, since it is easy to calculate it with one line of code in python or R, it is likely for the actual meaning to slip away. In this repo, I will visually breakdown the formula of variance, which doesn't usually make sense for beginners in statistics. 

The variance can be calculated as 

<img src="https://render.githubusercontent.com/render/math?math={\begin{align}
\text{Var}(X) &= \frac{1}{n}\left((x_1-\bar{x})^2+(x_2-\bar{x})^2+\ldots+(x_n-\bar{x})^2\right) \\
&= \frac{1}{n}\sum_{i=1}^n (x_i-\bar{x})^2
\end{align}}">

$\begin{align}
\text{Var}(X) &= \frac{1}{n}\left((x_1-\bar{x})^2+(x_2-\bar{x})^2+\ldots+(x_n-\bar{x})^2\right) \\
&= \frac{1}{n}\sum_{i=1}^n (x_i-\bar{x})^2
\end{align}$

Variance is a numerical value that explains how far away data points are from the mean, and hence from each other. 
- A variance of zero means all data is similar (we have only one data point)
- The higher the variance, the more disperse our data is (the data points are far away from the mean and from each other)
- The lower the variance, the less disperse the data is (data points close to the mean and to each other)
- Variance cannot be negative!

As discussed above, variance is a distance. So it is calculated as the mean of the squared distances from the mean. 

Let's consider the figure below. 

## Population Variance versus Sample Variance

