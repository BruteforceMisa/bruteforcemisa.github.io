---
layout: post
title:  "Learning the Decision Boundary"
date:   2024-11-06 12:46:02 +0200
categories: ai data labels decision boundary
---

Instead of using regular statistics to detect the decision boundary, we can try to learn the function iteratively. This is where deep neural networks/AI come into play. It is important to note that “AI” is basically “statistics on steroids”, as the decision boundary is decided based on the error.
For example, suppose we have a coffee which is medium butter and is on the lighter side. When the function is learning, it might misclassify this coffee as tea. We have to correct the decision boundary then. This process - called gradient descent - is repeated many times, until the most optimum decision boundary is found, i.e. most datapoints are classified correctly.

![image](/assets/images/Decisionboundary.png) 

Finding a deep neural network with the best decision boundary is therefore an optimisation problem. This can be calculated mathematically (from high school mathematics, you might recall finding global and local minima/maxima using the derivatives). However, it can be the case that there exist multiple minima. Finding the global minimum is one of the challenges in learning such a function.

![image](/assets/images/Optimum.png) 


<b>Keywords</b>
