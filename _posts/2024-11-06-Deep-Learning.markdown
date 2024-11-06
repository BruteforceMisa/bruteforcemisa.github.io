---
layout: post
title:  "Deep Learning"
date:   2024-11-06 12:47:02 +0200
categories: ai data labels decision boundary
---

By now, you probably have the feeling why the terminology of neural networks and deep learning are used interchangeably. In fact, the neural network is “learning” the decision boundary based on how many datapoints are classified correctly and how many are classified incorrectly. This is always done in two steps: the forward pass and the backpropagation step. In the forward pass, the neural network classifies all datapoints given its features. In the backpropagation step, we check how many datapoints are classified correctly. At one point in time, it is not possible to classify more datapoints correctly than we already have: this is our optimum.
But how do we build such a network? A neural network consists of nodes/neurons which are organised in layers. For this post, we will focus on a fully connected feedforward network. Each node has connections to all other nodes in the next layer.

A neural network consists of one input layer, at least one hidden layer and one output layer. The amount of nodes chosen for the network depends on your dataset. For our coffee & tea dataset, we would define our network as follows:

![image](/assets/images/DNN.png) 

We have three input features, thus we choose three input neurons. Each input neuron is then used to model a feature. The hidden layer we can choose ourselves, depending on how complex the model needs to be. As we want to classify whether our drink is coffee or tea, we have two output classes. Our output layer consists of two nodes. Our output neurons will model our output classes by using probabilities. Thus, the first output node would denote the probability that our drink is tea, and the second output node would denote the probability that our drink is coffee. Thus, the sum of our output neurons should be approximately 1.


![image](/assets/images/DNNtraining.png) 

To train this network, we feed our first datapoint and label to our network. The network will decide which of the features are more important to classify our drink, and which are less important. The weights between the nodes are updated accordingly. Based on the loss - i.e. how many datapoints are classified correctly - the network is adapted. Then, we put our second datapoint and label into the network. This sequence repeats until all datapoints are seen by the network.

It is also possible to show the dataset another time to the network, in case the network has not found an optimum yet. Epoch is the term used in the deep learning community to indicate how many times the whole dataset is passed through the network.



<b>Keywords</b>
