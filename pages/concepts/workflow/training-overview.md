---
layout: content
title: 'Training A Model: Overview'
image: 'colorful-art-supplies-1445895-pxh.jpg'
---

## Basic Overview

Learner: in fastai, used to train a model
Or: a learner is something that can learn to fit a model

Most basic learner, used by intro example of cats and dogs species:
```
learn = create_cnn(data, models.resnet34, metrics=error_rate)
learn.fit_one_cycle(4)		# Training for 5 epochs (5 cycles through the data)
```

- data: data
- arch: your architecture, in this case, ResNet34

Architectures:

- ResNet34 contains pre-trained weights, which effectively means that the model has already been trained for a particular task.
- Why do you have different types of architectures -- e.g., if you want to create a model that's going to run on a smart phone.
- The advantage of ResNet34 is that it works pretty well across a pretty broad range of problems -- and that's part of their general philosophy: "one of the things we try to show you is stuff which just tends to always work even if you don't quite tune everything perfectly" (Lesson 1)


Learn.fit_one_cycle: fitting the model using "one cycle learning"

NOTE: a lot of what you are doing when you do machine learning or deep learning is not just transforming the data into a form that will work, but using transformations that you can do quickly enough so that you don't want to bang your head against the wall.

Data Augmentation
For example, when you've got pictures of cats and dogs, you will want to do a transformation that randomly flips each image, but only left to right or right to left -- not upside down. Similarly, you might want to do "prospective warping" if your library is fast enough at it, which allows you to modify some of the pictures so that the image looks like you took a photo of a cat or dog from a higher or lower angle. (Wouldn't bother to do that with satellite photos, because there's no such thing when it comes to satellite photos)
The purpose of doing this is that it'll "make your models generalize better"


<hr/>


NOTE: not sure where to put this; need to break out.



> When you create a DataBunch, you're basically giving it a training set data loader and a validation set data loader. And that's now an object that you can send off to a learner and start fitting. [Lesson 3]



fbeta: it's a metric that's useful with Kaggle data, which is a way of weighing the impact of having false positives and false negatives into a single number, one of which is the F score

Thresh: if you have multiple labels, you can't just use the biggest probability
If you are trying to recognize a digit someone wrote, you end up with 10 numbers that are the probability that the image is each of those digits, so then you pick the biggest -- e.g., 8.
So what you do if there are more than one label, not just a digit (or a cat species).

Suppose the image could have up to 17 features, we can say, anything that's higher than a certain threshold of probability, like 0.2, we will assume it has that feature
So for accuracy, you use accuracy_thresh

To make sense of this, go back and look at what Lesson 3 says about partial
it's used for calculating some of the metrics

