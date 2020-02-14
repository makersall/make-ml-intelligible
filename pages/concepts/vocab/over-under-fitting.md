---
layout: content
title: Underfitting and Overfitting
image: 'chalk-many-818111-pxh.jpg'

---

## Overview

Babies:

- Underfitting: "dog" = dogs and any other pets
- Overfitting: "dog" = only our family's dog

Or:

- Overfitting: the model only learns to recognize blenders in these particular photos and not pictures in general of blenders

## Overfitting

The only way to get an idea of whether your overfitting is to use a validation set -- a set of data that the model doesn't train on

##  Overfitting, Validation Set

 > Wait a minute, how do you know it can actually recognize pictures of people playing cricket versus baseball in general? Maybe it just learnt to recognize those 30. Maybe it's just cheating. That's called "overfitting". We'll be talking a lot about that during this course. But overfitting is where you don't learn to recognize pictures of say cricket versus baseball, but just these particular cricketers in these particular photos and these particular baseball players in these particular photos. We have to make sure that we don't overfit. The way to do that is using something called a validation set. A validation set is a set of images that your model does not get to look at. So these metrics (e.g. error_rate) get printed out automatically using the validation set - a set of images that our model never got to see. When we created our data bunch, it automatically created a validation set for us. We'll learn lots of ways of creating and using validation sets, but because we're trying to bake in all of the best practices, we actually make it nearly impossible for you not to use a validation set. Because if you're not using a validation set, you don't know if you're overfitting. So we always print out the metrics on a validation, we've always hold it out, we always make sure that the model doesn't touch it.
   