---
layout: post
title:  'Why GPU is Important for training Deeplearning Models'
date:   '2018-10-31'
categories: stories
tags: ['Neural Network', 'Deep Learning' , 'GPU' ]
comments: true
---
Whenever we start with Deeplearning , we are bombarded with the doubts that Deep Learning requires a lot
of hardware. I have seen people training a simple deep learning model for days on
their laptops (typically without GPUs) which leads to an impression that Deep Learning requires
big systems to run execute.

We know that the computationally intensive part of neural network is made up of multiple matrix multiplications. So how can we make it faster?

We can simply do this by doing all the operations at the same time instead of doing it one after the other. This is in a nutshell why we use GPU (graphics processing units) instead of a CPU (central processing unit) for training a neural network.
