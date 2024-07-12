# Advanced Multivariate Analysis
Projects of Advanced Multivariate Analysis (AMA) Course for the Master in Data Science Program of Universitat Politècnica de Catalunya (UPC)
***

# Sections and Assignments

## [Unsupervised Learning through Advanced Multivariate Analysis](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/)
### Density Estimation
- **Assignment Description**:
  - **Histogram**:
    - Explore the relationship between the leave-one-out histogram density estimator and the histogram density estimator using all observations.
    - Utilize [CD rate data](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation/cdrate.dat) to plot histograms and evaluate them at observed data points.
    - Apply leave-one-out cross-validation to determine optimal histogram bin number and width.
  - **Kernel Density Estimator**:
    - Generate data from a mixture of two normal distributions.
    - Use the `leave-one-out log-likelihood function` to select the `optimal bandwidth` for kernel density estimation.

### Density Estimation GMM DBSCAN
- **Assignment Description**:
  - **Gaussian Mixture Model (GMM) Clustering**:
    - Use the `mclust` library to perform model-based clustering on [bike-sharing data](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation%20GMM%20DBSCAN/BikeDay.Rdata) (temperature and casual users) for the year 2012.
    - Determine the best number of clusters using `BIC`, and visualize the results.
  - **Kernel Density Estimation**:
    - Compare `GMM` density plots with non-parametric kernel density estimates using bandwidths proportional to standard deviations.
  - **Cluster Analysis**:
    - For each `GMM` cluster, estimate and visualize the joint density of temperature and casual users.
    - Use the `fpc` library to merge clusters and validate the final number of clusters.
  - **DBSCAN Clustering**:
    - Apply `DBSCAN` to identify clusters and outliers in the data.
    - Determine the best combination of tuning parameters and compare results with merged `GMM` clusters.
  - **Cluster Interpretation**:
    - Provide interpretations for the identified clusters using additional variables in the dataset.

### Non-linear Dimensionality Reduction
- **Assignment Description**:
  - **Principal Curves**:
    - Generate a 3D dataset and fit `principal curves` using the `princurve::principal_curve` function.
    - Select the **optimal smoothing parameter** using **leave-one-out cross-validation**.
    - Compare results with different degrees of freedom to identify overfitting.
  - **Local MDS for ZIP Data**:
    - Reduce dimensionality of [ZIP digit data](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Non-linear%20Dimensionality%20Reduction/zip.train) using `Local MDS` with the `stops` package.
    - Visualize the 2D configuration and interpret the results by plotting selected digit images.
    - Optimize tuning parameters using **local continuity meta criteria**.
  - **ISOMAP for ZIP Data**:
    - Apply `ISOMAP` to the ZIP digit data using the `vegan` package.
    - Visualize and interpret the 2D configuration.
    - Optimize the tuning parameter using **local continuity meta criteria**.
  - **t-SNE for ZIP Data**:
    - Apply `t-SNE` to the ZIP digit data using the `Rtsne` package.
    - Visualize and interpret the 2D configuration.
    - Optimize the `perplexity` parameter using **local continuity meta criteria**.
  - **Comparison of Methods**:
    - Compare the 2D configurations obtained by `Local MDS`, `ISOMAP`, and `t-SNE`.
    - Identify which method produces the largest value of the **local continuity meta criteria**.



### Statement Files:
- [Density Estimation.pdf](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation/docs/Density%20estimation.pdf)
- [Density Estimation GMM DBSCAN.html](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation%20GMM%20DBSCAN/docs/Density%20Estimation%20GMM%20DBSCAN.html)
- [Non-linear Dimensionality Reduction.html](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Non-linear%20Dimensionality%20Reduction/docs/Non-linear%20dimensionality%20reduction.html)

### Proposed Solutions:
- [Density Estimation](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation/docs/density_estimation.pdf)
- [Density Estimation GMM DBSCAN](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Density%20Estimation%20GMM%20DBSCAN/clustering.html)
- [Non-linear Dimensionality Reduction](./Unsupervised%20Learning%20through%20Advanced%20Multivariate%20Analysis/Non-linear%20Dimensionality%20Reduction/docs/principalCurves.html)

***

## [Nonparametric Regression Models](./Nonparametric%20Regression%20Models/)
### Local Linear Regression
- **Assignment Description**:
  - Utilize [Aircraft data](https://vincentarelbundock.github.io/Rdatasets/doc/robustbase/aircraft.html) to estimate conditional variance by **local linear regression**.
  - Apply nonparametric regression to estimate the function $\sigma^2(x)$ for transformed aircraft data.
  - Use **leave-one-out cross-validation** and direct plug-in (function `dpill` from library `KernSmooth`) methods to select bandwidth values.

### Local Poisson Regression
- **Assignment Description**:
  - Modify existing functions to create a **bandwidth choice method** for `local Poisson regression` using **leave-one-out cross-validation**.
  - Fit a `local Poisson regression` model to [country development data](./Nonparametric%20Regression%20Models/Local%20Poisson%20Regression/HDI.2017.subset.csv), modeling the rounded development indicator as a function of life expectancy.

### Smoothing and Regression Splines
- **Assignment Description**:
  - Use the [bikes.Washington.Rdata dataset](./Nonparametric%20Regression%20Models/Smoothing%20and%20Regression%20Splines/bikes.Washington.Rdata) which includes daily bike rental counts in Washington D.C. for `2011` and `2012`.
  - Estimate the regression function \(m(\text{instant})\) using a **cubic regression spline**.
    - Determine the **optimal penalty parameter** `λ` using `Generalized Cross Validation`.
    - Provide the value of `λ`, the `equivalent number of degrees of freedom (df)`, the `number of knots` used, and a plot of the scatter plot with the estimated regression function.
  - Fit a `non-parametric binary regression` using the `logistic.IRWLS.splines` function.
    - Define a new variable \( \text{cnt.5000} \) indicating days with bike rentals ≥ 5000.
    - Fit the model as a function of temperature using `df=6` and determine the temperature range where the probability is `higher than 0.5`.
    - Use `k-fold log-likelihood cross-validation` to choose the `optimal df value`.

### Generalized Additive Models
- **Assignment Description**:
  - The [Hirsutism dataset](./Nonparametric%20Regression%20Models/Generalized%20Additive%20Models/hirsutism.dat) includes measurements from a clinical trial evaluating the effectiveness of an anti-androgen combined with an oral contraceptive in reducing hirsutism over `12` months.
  - Fit several **Generalized Additive Models (GAMs)** to explain `FGm12` as a function of baseline variables and treatment.
    - Use summary, plot, vis.gam, and gam.check functions to evaluate the models.
    - Apply the anova function to select the most appropriate model(s).


### Statement Files:
- [Local Linear Regression.pdf](./Nonparametric%20Regression%20Models/Local%20Linear%20Regression/docs/local%20linear%20regression.pdf)
- [Local Poisson Regression.pdf](./Nonparametric%20Regression%20Models/Local%20Poisson%20Regression/docs/Local%20Poisson%20regression.pdf)
- [Smoothing and Regression Splines.pdf](./Nonparametric%20Regression%20Models/Smoothing%20and%20Regression%20Splines/docs/Smoothing%20and%20regression%20splines.pdf)
- [Generalized Additive Models.pdf](./Nonparametric%20Regression%20Models/Generalized%20Additive%20Models/docs/Generalized%20Additive%20Models.pdf)

### Proposed Solutions:
- [Local Linear Regression](./Nonparametric%20Regression%20Models/Local%20Linear%20Regression/docs/local_linear_regres.html)
- [Local Poisson Regression](./Nonparametric%20Regression%20Models/Local%20Poisson%20Regression/docs/Assignment-Local-Poisson-regression.html)
- [Smoothing and Regression Splines](./Nonparametric%20Regression%20Models/Smoothing%20and%20Regression%20Splines/docs/Bikes-in-Washington.html)
- [Generalized Additive Models](./Nonparametric%20Regression%20Models/Generalized%20Additive%20Models/docs/Lab_hirsutism.html)

***

## [Interpretable Machine Learning](./Interpretable%20Machine%20Learning/)
### Interpretability and Explainability in Machine Learning
- **Assignment Description**:
  - Utilize the [Concrete Dataset](./Interpretable%20Machine%20Learning/Concrete_Data.xls) to fit various models including `Random Forest`, `linear`, and `generalized additive models`.
  - Assess **variable importance** using different methods such as `reduction of impurity`, `out-of-bag random permutations`, and `Shapley` values.
  - Compute relevance using `ghost variables`.
  - Employ `global and local importance` measures and plots using the `DALEX` library.
  - Explain predictions for specific instances in the test set using `SHAP`, `break-down` plots, `LIME`, and `ICE` plots.

### Statement Files:
- [Interpretability and Explainability in Machine Learning.pdf](./Interpretable%20Machine%20Learning/docs/Interpretability%20and%20Explainability%20in%20Machine%20Learning.pdf)

### Proposed Solutions:
- [Interpretability and Explainability in Machine Learning](./Interpretable%20Machine%20Learning/docs/Concrete.html)