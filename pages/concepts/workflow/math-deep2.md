---
layout: content
title: 'In My Own Words: The Math behind Deep Learning'
image: 'colorful-art-supplies-1445895-pxh.jpg'
---





> You want to find **parameters** (weights) `a` such that you minimize the *error* between the points and the line `x@a`. Note that here `a` is unknown. For a regression problem the most common *error function* or *loss function* is the **mean squared error**.

Translation: if you have Y = MX + B,
a.k.a. 
y = a[0]*x + a[1]

Parameters is what pie torch calls them, also known as weights; in stats they call it coefficients

The parameters/weights are the values in a.

Only that version won't let you use matrix multiplication, which is wicked fast.
So, you kludge it by turning x from a row of numbers into a matrix,
where x[row, 0] is what x used to be
and x[row, 1] is 1, because 1*B = B

As a result, you can describe the formula as 2 tensors, a and x:
y[row] = a[0] * x[row, 0]  +  x[row, 1]
And now you can do matrix multiplication!


And now we play the equivalent of computer 20 questions.

Basically, you start off with a guess. Only instead of guessing, "is it a person?", The computer guesses:
m = -1
b = 1
Or to put it in tensor format:
a =  [1.0, 1.0]

You might ask, why that guess?
It all goes back to, what are computers really good at and really bad at?
- They are really bad at asking sophisticated questions that require a lot of knowledge about the world (at least for now :-) ).
- But if you give them a bunch of data with the right answers, they are really good at making lots and lots of guesses and figuring out if they are right or wrong really quickly

Or to put it another way, this is the equivalent of computer 20 questions, the solitaire edition.

> So far we have specified the *model* (linear regression) and the *evaluation criteria* (or *loss function*). Now we need to handle *optimization*; that is, how do we find the best values for `a`? How do we find the best *fitting* linear regression. [Lesson 2]

"Optimization" is just a fancy name for playing computer 20 questions, the solitaire edition.
Or maybe it's the other way around:
computer 20 questions, the solitaire edition is one hack that computers use for "optimization"
Optimization is how do you get as close as you can to weights/parameters, a.k.a. a that accurately predict the answers?

So the way computers 20 questions the solitaire edition works,
if the computer starts with a number it knows is way, way off,
then keeps calculating in what direction is it off,
and then moves towards the right answer by the learning rate.

That's the problem with a higher learning rate:
if the correct answer is 3
and your starting guess is -1
and your learning rate is 3,

Your guesses will go like this:
-1
2
5
7
..

So in 2 guesses, you will have overshot the answer

right,
the computer makes a guess,
it does a calculation using mean squared error
and that basically tells it, hot, cold, too hot, too cold, way way too hot, etc.
And with gradient descent, you are only guessing in one direction, so if you overshoot and go from too cold to too hot, you are SOL.

So why couldn't you just work your way back?
I'm not sure, but I think it's because this is a super simplified example. We've got only 2 parameters/weights/coefficients we are worrying about. In the real world, we are probably looking at lots, lots more. And at that point, I'm not sure "back" would make sense -- and they may also be reasons that have to do with again, what computers are good at versus bad at so this tactic wouldn't work.


Rather than moving it up or down or left or right, you can calculate the derivative, which gets you the same thing -- only a lot faster. In other words, another hack.

lost.backward(): that calculates the gradient for you
that's because pie torch keeps track of how the mean squared error was calculated, and then uses it or lets us to use it to calculate the derivative.
So backward gets you derivative, at which it stores inside the attribute .grad


> if you think back to the gradient descent tutorial last week is we have to have a few images/items at a time so that our GPU can work in parallel… Mini-batch is a few items that we present to the model at a time that we can train from in parallel. [Lesson 3]