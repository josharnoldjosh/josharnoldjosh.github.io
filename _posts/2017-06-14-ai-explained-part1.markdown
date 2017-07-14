---
layout: default
title:  "Artificial Intelligence Explained Part 1: Introduction"
date:   2017-06-14 16:30:00
categories: deep-learning
---

# Artificial Intelligence Explained Part 1: Introduction

## Introduction

I wanted to make a few posts explaining the 'magic' behind artificial intelligence for people who like me aren't math or programming geniuses. 

This is the first post in the series that will start from the begining assuming little-to-no knowledge of what A.I is. 

### What is Artificial Intelligence or A.I?

Google has a pretty good definition of what A.I is:

>The theory and development of computer systems able to perform tasks normally requiring human intelligence, such as visual perception, speech recognition, decision-making, and translation between languages.

However, one misconception people often have is that all A.I is *artificial general intelligence*. 

### Artificial General Intelligence

What is Artificial General Intelligence? Again, Google has a pretty solid definition:

> Artificial general intelligence (AGI) is the intelligence of a machine that could successfully perform any intellectual task that a human being can.

Essentially, AGI is the A.I you see in the movies, A.K.A fully sentient beings that are usually hostile towards the human race 🔫 🔪 🔥. 

For better or worse, AGI is far from existance 😱. From the time of writing this post, there is no such thing as artificial intelligence that is sentient in the sense of being human-like. 

However, what has excelled in current years is *Weak AI* or *Narrow AI*, which is as the name suggests, weak and narrow (to a degree). 

### Weak AI / Narrow AI

I like to define Narrow AI (I prefer this term over Weak AI) as artificial intelligence that can perform one single (or narrow) task, such as recognizing the difference between cat and dog images or convert sound to text. 

Unlike AGI, Narrow AI is a reality today. Siri on the iPhone is an example of the combination of multiple Narrow AI's, such as speech to text among others, that is connected to a database in the cloud. However, Siri is in no way aware of her surroundings, or has any senses or feelings. Narrow AI like Siri can often [easily be tricked](https://www.youtube.com/watch?v=ijRPlOF2KQE).

Much of Narrow AI fits under the category of *Machine Learning*, which we will explore in the rest of this post. 

## Machine Learning 

Machine Learning is a subset of A.I that can be defined broadly as machines (or computers) learning to analyse specific sets of data. The best way to explain what machine learning does is to give an example. 

Imagine a dataset of house auctions that contains the following information per sale:

* The sale price of the house
* The size of the entire property 

Machine learning in this case could be used to develop an algorithm that can predict the sale price of a house based on the size of the property. But how would this work intuitively? We can find out by first visualizing our dataset.

Because our dataset contains two variables per house sale, we can visualize the information by plotting it on a graph.

![](https://i.imgur.com/mV6YrvG.png)

In highschool, you may have learned about linear regression, or in simple terms, *a line of best fit*. Just by looking at this data, we can see that it follows a trend where the house price is (to an extent) directly proportional to the property size, or in other words, the larger the property size, the higher the cost of the house. 

Intuitively, what a machine learning algorithm does is attempt to find the line of best fit in a given dataset and then make predictions using that line of best fit. 

So, our algorithm would first make an effort to find the line of best fit:

![](https://i.imgur.com/2HCFj5P.png)

And then, if we gave it an input of 0.55 Acres, the machine learning algorithm would draw a line starting from the input value of 0.55 on x axis until it intersects with the line of best fit, and then it would trace a line until it intersects with the y axis to yield a predection of **$13.5 million** for a property size of 0.55 Acres.:

![](https://i.imgur.com/Ku7NSM8.png)

Notice once the algorithm has found a line of best fit, it can make a prediction given any acre size. 

This is in essence how a machine learning algorithm learns to make predictions. Intuitively, it seems pretty simple right? 🎉

Except there are a few caveats...

### Machine Learning Challenges

Although the previous example seemed simple, Machine learning faces the following challenges:

* Dataset size
* The dimension problem 
* Nonlinearity
* Computational power

Let's dissect each of them one by one 😎

**Dataset size**

As we saw in the previous example, before a machine learning algorithm can make predictions it needs a line of best fit. Well, unfortunately, discovering that line of best fit can be quite a challenge. 

We will get into how exactly a line of best fit can be calculated in machine learning, but in general, *to find a quality line of best fit that can be used requires large amounts of data.* [An algorithm Google developed used a dataset that contained roughly 1.2 million images](https://cacm.acm.org/magazines/2017/6/217745-imagenet-classification-with-deep-convolutional-neural-networks/fulltext).

Of course, not every machine learning algorithm requires datasets that are that large, however, depending on the situation, if limited data is available it can be impossible to create a decent model. 

**The Dimension Problem**

The Dimension problem is one of the most challenging aspects of machine learning in my opinion. The easiest way I can think to explain it is like so:

Whenever we plot data on graph, imagine each axis is a dimension. Recall in our previous example we have both a x and y axis, thus, our previous example can be considered two dimensional. 

However, if we were to add another variable to our previous dataset we could no longer use a two dimensional graph to plot our data. 

If you remember, our data set contained the following information per house sale:

* The sale price of the house
* The size of the entire property 

Now, if we add another variable, in this case *the number of rooms in each house*, we would then have three variables per house sale in our dataset: 

* The sale price of the house
* The size of the entire property 
* The number of rooms in the house

Because we represent each variable on an axis and we have three variables, we would naturally have three axes (x, y & z) if we were to plot our data on a graph. 

Our dataset plotted on a graph would look something like this:

![](https://i.imgur.com/lYGbzkU.png)

Suddenly, our machine learning algorithm is no longer dealing with a two dimensional graph but **a three dimensional graph.** I'm sure you would agree just by looking at this graph there is no clear, easy to see relationship between the data. 

This is in essence the dimension problem. Often in machine learning we deal with multiple variables and the number of dimensions doesn't stop at three. We can easily have four, five, six or even twenty variables which results in a lot of dimensions which are difficult to visualize.  



