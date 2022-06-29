## Primary project objective

- The spatial context of crime statistics is typically derived from individual crime occurences aggregated to areal units, i.e., zip codes, neighborhoods, or beats.  Suppose, however, that finer spatial resolution is desired; the objective is the expected criminal activity at a particular point in space like a street corner.  This project pursues that objective by utilizing a Generalized Additive Model (GAM) with a continuous but non-Gaussian response to model the expected annual crime count as a continuous 2d surface.  Spatial autocorrelation is accounted for by smooth functions (splines) which have the flexibility to model non-linear relationships.

## Primary language

- R

## Highlighted visualizations

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/Observed_violent_crimes.gif" width=675>

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_qq.png" width=675>

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_resids_hist.png" width=675>

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/family_diagnostics_smoothing.png" width=675>

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/predicted_violent_crimes.gif" width=675>

<img src="https://raw.githubusercontent.com/Jon-Does-Stats/project-spatial-poisson-crime/main/figures/residual_spatial_patterning.gif" width=675>
