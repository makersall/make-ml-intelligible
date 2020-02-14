---
layout: content
title: Loss Rate and Loss Function
image: 'chalk-many-818111-pxh.jpg'

---

{ Here is where my notes will go }
   

What is a loss function?  
It’s whichever function or means of calculating loss you decided to use.  It’s a tool, and different loss functions are good for different types of problems.  

> how do we create a model? We create a CNN. We're going to be learning a lot about loss functions in the next few lessons, but basically the loss function is that number that says how good is the model. For classification, we use this loss function called cross-entropy loss which says basically "Did you predict the correct class and were you confident of that prediction?" We can't use that for regression, so instead we use something called mean squared error.  L3

 If you draw a line on that data, 
> The loss is, on average (mean), how far is each of the actual data points vs the point from our  y=mx+b line prediction?  Or in other words, on average how far off are we?  Loss boils down How off we are, because we don’t want to know how well we did for just one point, it’s how far off are we in general
(This is why edge cases that matter can f you up, cause the model is looking at overall how we doing)
