## Primary project objective

- The spatial context of crime statistics is typically derived from individual crime occurences aggregated to areal units, i.e., zip codes, neighborhoods, or beats.  Suppose, however, that finer spatial resolution is desired; the objective is the expected criminal activity at a particular point in space like a street corner.  This project pursues that objective by utilizing a Generalized Additive Model (GAM) with a continuous but non-Gaussian response to model the expected annual crime count as a continuous 2d surface.  Spatial autocorrelation is accounted for by smooth functions (splines) which have the flexibility to model non-linear relationships.

## Primary language

- R

## Highlighted visualizations
- (below) Annual violent crimes recorded in Boston by year from 2015 to 2021.  Aggregated and binned to a hexagonal grid with each cell having a quarter-mile centroid-to-edge distance.  

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/Observed_violent_crimes.gif" width=675>

- (below) Diagnostic QQ plos to help determine which family of distributions best models the observed crime count. Feathered lines represent the quantiles from several empirical distributions of residuals calculated by simulating data from each fitted model, 25 times.  The negative binomial family fits the observed data much better.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_qq.png" width=675>

- (below) Comparing histograms of deviance residuals between two potential model families. Compared to the poisson model, the negative binomial model results in deviance residuals of a far lesser magnitude. When it comes to GLMs (of which GAMs can be considered an extension), an important validation check is the assumed mean variance relationship. For example, if a Poisson model is employed, then the variance of the residuals should increase in direct proportion to the size of the ﬁtted values. This behavior can be difficult to confirm by inspecting simple raw residuals.  Thus, we standardize GLM residuals so that, if the model assumptions are correct, the standardized residuals should have approximately equal variance and behave, as far as possible, like residuals from an ordinary linear model. Deviance residuals (shown here), and pearson residuals, are two common alternatives to raw residuals.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_resids_hist.png" width=675>

- (below) image plots and overlaid contour plots of the resulting smooth term for each model family, on the scale of the linear predictor. 

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_smoothing.png" width=675>

- (below) The annual number of predicted violent crimes expected within a quarter-mile radius, by year, from 2015 to 2021. The final model used for the analysis is a negative binomial GAM model with cubic regression smoothers for longitude and latitude coordinates, and a tensor spline for their interaction.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/predicted_violent_crimes.gif" width=675>

- (below) Pearson residuals by year from 2015 to 2021. Residuals appear random in nature and void of spatial patterning indicating spatial autocorrelation is being modeled successfully.

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/residual_spatial_patterning.gif" width=675>
