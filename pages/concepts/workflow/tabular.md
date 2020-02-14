---
layout: content
title: Working With Tabular Data
image: 'colorful-art-supplies-1445895-pxh.jpg'
---


 For Tabular
 > We have a number of processes in the fastai library. And the ones we're going to use this time are:
> 
> FillMissing: Look for missing values and deal with them some way.
> Categorify: Find categorical variables and turn them into Pandas categories
> Normalize : Do a normalization ahead of time which is to take continuous variables and subtract their mean and divide by their standard deviation so they are zero-one variables.

This is critical— you transform all the number data so they’re between -1 and 1
L4
