---
layout: content
title: Error Rate
image: 'chalk-many-818111-pxh.jpg'

---
How is error rate calculated?
In the fastai library, they take the results of running the model against your validation set, take the list of answers that will predicted versus the actual answers, where 0 is no match and 1 is match, then average up the results, which gives you the percent of times the model correctly predicting the answer in the validation set.
Then the error rate is: 1 - accuracy
