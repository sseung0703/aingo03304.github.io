---
layout: post
title: "Gaussian Mixture Model Explained."
date: 2019-10-13 03:48:00 +0900
mathjax: true
---

# What Is Mixture Model?
Before getting into Gaussian Mixture Model, we should look into what `Mixture Model` is. According to [Wikipedia][mixture-model], a mixture model is a probabilistic model for representing the presence of subpopulations within an overall population, without requiring that an observed data set should identify the sub-population to which an individual observation belongs.

A typical finite-dimensional mixture model is a hierarchical model consisting of the following components:
 - _N_ random variables that are observed, each distributed according to a mixture of _K_ components, with the components belonging to the smae parametric family of distributions but with different parameters.
 - _N_ random latent variables specifying the identity of the mixture component of each observation, each distrubuted according to a _K_-dimensional categorical distribution.
 - A set of _K_ mixture weights, which are probabilities that sum to 1.
 - A set of _K_ parameters, each specifying the parameter of the corresponding mixture component. In many cases, each "parameter" is actually a set of parameters. For example, if the mixture components are Gaussian distributions, there will be a mean and variance for each component. If the mixture components are categorical distributions (e.g., when each observation is a token from a finite alphabet of size _V_), there will be a vector of _V_ probabilities summing to 1.

# Gaussian Mixture Model
A Gaussian Mixture Model is a function that is comprised of several Gaussian distributions, each identified by $k \in \\{1, ..., K\\}\$, where _K_ is the number of clusters of our dateset. Each Gaussian _K_ in the mixture is comprised of the following parameters:
 - A mean $\mu$ that defines its center.
 - A covariance $\Sigma$ that defines its width. This would be equivalent to the dimensions of an ellipsoid in a multivariate scenario.
 - A mixing probability $\pi$ that defines how big or small the Gaussian function will be.

[mixture-model]: https://en.wikipedia.org/wiki/Mixture_model
