---
layout: post
mathjax: true
comments: true
title: Diffusion Maps
image: /img/disk_model.png
---

In this post I will explain and summarize [this](https://www.sciencedirect.com/science/article/pii/S1063520306000546) awesome paper.  The idea behind diffusion maps is dimensionality reduction.  Some datasets (i.e. images) contains useful geometric shapes, and these images often have too many factors (features) and most of the time these features are redundant. Diffusion maps is an efficient representations of these features because it provides a framework where these features are reduced into a smaller number, hence dimensionality reduction.  Mathematically, diffusion maps are coordinates constructed from the eigenvectors of the Markov matrices. Thus, eigenvectors of Markov matrices can be thought of as coordinates on the dataset.  The goal is to change the representation of the dataset in order to understand the phenomenon that generated the data.  

Let X be the data set and <a><img src="https://latex.codecogs.com/gif.latex?\mu" title="\mu" /></a> is the distribution of the points on X and let k(x,y) be a kernal that is 
symmetric k(x,y) = k(y,x) and 
positivity preserving k(x,y) >= 0

In N-dimensional simplex noise, the squared kernel summation radius $r^2$ is $\frac 1 2$
for all values of N. This is because the edge length of the N-simplex $s = \sqrt {\frac {N} {N + 1}}$
divides out of the N-simplex height $h = s \sqrt {\frac {N + 1} {2N}}$.
The kerel summation radius $r$ is equal to the N-simplex height $h$.

$$ r = h = \sqrt{\frac {1} {2}} = \sqrt{\frac {N} {N+1}} \sqrt{\frac {N+1} {2N}} $$




