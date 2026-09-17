# Density Estimation and Applications in Clustering & Segmentation

Parametric and nonparametric probability density estimation, applied to synthetic data, a Gaussian mixture model, and real image segmentation.

![MLE of an exponential distribution](https://raw.githubusercontent.com/MikeFerko/Density_Estimation_and_Basics_of_Segmentation/main/Project%20Pictures/MLE%20Exponential%20pdf.JPG)

- [Notebook](<Density Estimation and Applications in Estimation, Clustering  and Segmentation.ipynb>)
- [Paper](<Density Estimation and Basics of Segmentation by EM Method.pdf>)
- [Dataset](data.csv)

## Approach

**Part 1: Density estimation and the EM algorithm**
- Estimated a nonparametric density with the Parzen window method at multiple bandwidths, and compared it against k-NN density estimation at multiple k values
- Derived and computed the maximum likelihood estimate for an exponential distribution's rate parameter, overlaying the fitted density on the data histogram
- Implemented the Expectation-Maximization algorithm from scratch to fit a K-component Gaussian mixture model, tracking parameter convergence and verifying the log-likelihood increases monotonically across iterations
- Applied the EM-fitted mixture model to segment real grayscale images (lung and kidney scans) by their intensity distributions

**Part 2: Density estimation and Bayesian classification**
- Generated samples from unit normal, uniform, triangular, and mixed densities
- Re-estimated each density from the samples using both Parzen windows and k-NN
- Designed a two-class Bayesian classifier using the estimated densities (Gaussian vs. uniform/triangular/mixed), then tested it and compared the empirical probability of error against the theoretical case
