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
big systems to run execute , which is not true ! 

Recently while Working on Chatbot ( My first experience with Deep Learning and it is 💚).I have faced the Problem of memory and GPU! 

<div class="image">
    <a href="/public/img/Killed .png">
        <img alt="Out of Memory" src="/public/img/Killed .png" />
    </a>
   <div class="image-caption">
        "Out Of Memory when training" 
    </div>
</div>

For Solution I used Google Colab 💚 (which apparently saved me in Major Project Submission) 
It is Deep Learning Cloud Provider for training ( Google Colab is free. It’s a Jupyter notebook system with nice UX. It integrates with GitHub and Google Drive.Colab is super fast to get started with for Keras or TensorFlow .Colab has both <strong>GPUs</strong> and <strong>TPUs</strong> available )

<h2> WHY GPU ? </h2>

We know that the computationally intensive part of neural network is made up of multiple matrix multiplications. So how can we make it faster?

We can simply do this by doing all the operations at the same time instead of doing it one after the other. This is in a nutshell why we use GPU (graphics processing units) instead of a CPU (central processing unit) for training a neural network.

The CPU is good at fetching small amounts of memory quickly (5 * 3 * 7) while the GPU is good at fetching large amounts of memory (Matrix multiplication: (A*B)*C). CPUs are <strong>latency optimized</strong> while GPUs are <strong>bandwidth optimized</strong>. The best CPUs have about 50GB/s while the best GPUs have 750GB/s memory bandwidth. So the more memory your computational operations require, the more significant the advantage of GPUs over CPUs.
