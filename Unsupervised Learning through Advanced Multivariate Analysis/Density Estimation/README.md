# Density Estimation
**Bandwidht choice by leave-one-out maximum likelihood**
***
This repository contains the project work on density estimation methods, specifically focusing on histogram and kernel density estimation with bandwidth selection using leave-one-out maximum likelihood.

## Histogram Estimation
The exercises stated below are the primary objectives of the current solution. The detailed explanation of the exercises is included in the [Project Statement file](./docs/Density%20estimation.pdf).

1. **Exercise 1: Relationship Between Histogram Estimators**  
   Establish the relationship between the histogram estimator and its leave-one-out version when both are evaluated at an observed data point.

2. **Exercise 2: Histogram Plotting**  
   Read the [CD rate](./cdrate.dat) dataset, define parameters, and plot the histogram of the data. Convert the histogram to a function for evaluation at any point in R.

3. **Exercise 3: Leave-One-Out Histogram Estimation**  
   Compute the leave-one-out histogram estimates and add these to the previous histogram plot.

4. **Exercise 4: Leave-One-Out Log-Likelihood Calculation**  
   Calculate the leave-one-out log-likelihood function for the histogram with a specified number of bins.

5. **Exercise 5: Optimal Number of Bins Using LooCV**  
   Iterate over a range of bin numbers to find the optimal number using leave-one-out cross-validation and plot the corresponding histogram.

6. **Exercise 6: Optimal Bin Width Using LooCV**  
   Determine the optimal bin width that maximizes the leave-one-out log-likelihood function and plot the histogram.

7. **Exercise 7: Comparison with Scott’s Formula**  
   Generate data from a mixture of Gaussians, select the optimal bin width, and compare the results with Scott’s formula.

8. **Exercise 8: Kernel Density Estimation**  
   Use the generated data to find the optimal bandwidth for the kernel density estimator using leave-one-out log-likelihood and plot the resulting density.
