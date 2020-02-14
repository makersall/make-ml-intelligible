---
layout: content
title: Workflow
permalink: /workflow/
image: 'colorful-art-supplies-1445895-pxh.jpg'
---


## Prepping the Data

Before we train, we turn our data into a form the computer can rock out on.

For ex: we want to look at an image and figure out what digit it is, such as an 8
Since computers don't have eyeballs and really like numbers, we turn the image into an 18 x 18 matrix of pixels, where 0 = white, 255 = black, everything in between is a shade of white/black/gray. 

## Training the Model

[Overview](../pages/workflow/training-overview.html)

Things we need to tweak our model about:
- [Overfitting](../pages/vocab/over-under-fitting.html) and [Underfitting](../pages/vocab/over-under-fitting.html)

## The Math behind the Training Model
- [Vectors, Matrixes, and Tensors](../pages/workflow/vector-matrix-tensor.html)
- Notes Dump: The [Math behind Training the Model](../pages/workflow/math-deep-learning.html)
- Notes Dump 2:  [More Math behind Training the Model](../pages/workflow/math-deep2.html)


## Types of Data/Analyses
- [Gradient Descent](../pages/workflow/gradient-descent.html), including Stochastic Gradient Descent
- [Tabular](../pages/workflow/tabular.html)
- [Collaborative Filtering](../pages/workflow/collaborative-filtering.html)

<hr/>

NOTE: not sure where to put this stuff 

### Activations and Parameters
> Activations and parameters, both refer to numbers. They are numbers. But Parameters are numbers that are stored, they are used to make a calculation. Activations are the result of a calculation﹣the numbers that are calculated. So they're the two key things you need to remember.
> -  An activation is the result of either a matrix multiply or an activation function.
> -  Parameters are the numbers inside the matrices that we multiply by.
L4

In other words,  
-  Parameters are the weights/biases inside a matrix, and building a model is about starting w some random guesses for those parameters, then doing gradient decent or whatever until you end up with parameters (weights/biases) that you think are going to get you a pretty good prediction
- An Activation is what you get when you take whatever vector you’ve got (either the initial input, like a vector of pixels, or the latest result of the previous layer of number crunching) and run it though a matrix or an activation function (eg, turn all the negative numbers to 0)

> Every one of these things that does a calculation, all of these things that does a calculation (red arrow), are all called layers. They're the layers of our neural net. So every layer results in a set of activations because there's a calculation that results in a set of results.
> There's a special layer at the start which is called the input layer, and then at the end you just have a set of activations and we can refer to those special numbers (I mean they're not special mathematically but they're semantically special); we can call those the outputs. The important point to realize here is the outputs of a neural net are not actually mathematically special, they're just the activations of a layer.
L4

> It's very common to have an activation function as your last layer... it’s  very often going to be a sigmoid or something similar because it's very likely that actually what you want is something that's between two values and kind of scaled in that way.
 L4

Non-linearity: basically the same as activation function?  
>What are we actually doing? And here's the interesting thing﹣all we're actually doing is we literally do have a matrix multiplication (or a slight variation like a convolution that we'll learn about) but after each one, we do something called a non-linearity or an activation function. An activation function is something that takes the result of that matrix multiplication and sticks it through some function.
L3


> called a rectified linear unit (ReLU). It's very important, when you're doing deep learning, to use big long words that sound impressive. Otherwise normal people might think they can do it too 😆. But just between you and me, a rectified linear unit is defined using the following function:  max(x, 0)
> That's it. And if you want to be really exclusive, of course, you then shorten the long version and you call it a ReLU to show that you're really in the exclusive team. So this is a ReLU activation.

Me: so all the activation in this is doing is replacing any negative number w a 0.

> Here's the crazy thing. If you take your red green blue pixel inputs, and you chuck them through a matrix modification, and then you replace the negatives with zero, and you put it through another matrix modification, replace the negatives at zero, and you keep doing that again and again, you have a deep learning neural network. That's it.
L3

> The reason it's hard to understand intuitively is because we're talking about weight matrices that have (once you add them all up) something like a hundred million parameters. They're very big weight matrices. So your intuition about what multiplying something by a linear model and replacing the negative zeros a bunch of times can do, your intuition doesn't hold. You just have to accept empirically the truth is doing that works really well.


> model. A lot of people think regression means linear regression, it doesn't. Regression just means any kind of model where your output is some continuous number or set of numbers.
L3
