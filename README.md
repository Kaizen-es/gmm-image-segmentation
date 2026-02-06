# Gmm-Image-Segmentation
Unsupervised image segmentation using Gaussian Mixture Models with automatic model order selection via cross-validation

## Overview
Segments natural images into distinct regions by modeling pixel features as samples from a Gaussian Mixture Model. The optimal number of segments is selected automatically using 10-fold cross-validation.

## Method
Extract 5D feature vector per pixel: (row, column, R, G, B), normalized to [0,1]
Fit GMMs with M = 2 to 10 components using EM algorithm
Select M* via cross-validation (maximum average validation log-likelihood)
Assign each pixel to the component with highest posterior probability

## Results
Image: 321 × 481 pixels (Berkeley Segmentation Dataset)
Selected model: M* = 10 components

## Dataset
Berkeley Segmentation Dataset
