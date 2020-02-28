# HW 3
# Reading:
Instead of a traditional reading assignment, read this bogpost which will help you do the HW assignment. 
However, make sure you read it all, not only the functions I ask you to use. If you see any improvements that can be made on the homweork model based on this by changing or tuning any of the model parameters, please note that in the notebook!

[Implementing Facebook Prophet efficiently](https://towardsdatascience.com/implementing-facebook-prophet-efficiently-c241305405a3)
https://towardsdatascience.com/implementing-facebook-prophet-efficiently-c241305405a3

# Assignment: 

This homework will guide you through a complete additive model analysis of a time series and familiarize you with the (fairly new) Facebook Prophet package for time series analysis.

Prophet simplifies the implementation of analysis like "Structural Time Series modeling" and/or "Bayesian dynamic linear model": similarly to the ARMA family of models, these models attempt to recreate (and predict) a time series by linearly combining variouos components: trends, seasonalities, but also regression on exogenous variables. In this case, we will see if Uber rides area affected by weather, in additional to trends and seasonality.

Under the hood, the model will implement an optimization to find the best fit parameters for each component (mostly the relative amplitude of each component) in a Bayesian framework, either as a direct optimization which is possible since the model is linear, or by MCMC (https://github.com/facebook/prophet/issues/669)

Follow the [instructions](https://github.com/fedhere/MLTSA_FBianco/blob/master/HW3/uberprophet_instructions.ipynb)
