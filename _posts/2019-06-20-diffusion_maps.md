---
layout: post
title: Diffusion Maps
image: /img/disk_model.png
---

In this post I will explain and summarize [this](https://www.sciencedirect.com/science/article/pii/S1063520306000546) awesome paper.  The idea behind diffusion maps is dimensionality reduction.  Some datasets (i.e. images) contains useful geometric shapes, and these images often have too many factors (features) and most of the time these features are redundant. Diffusion maps is an efficient representations of these features because it provides a framework where these features are reduced into a smaller number, hence dimensionality reduction.  Mathematically, diffusion maps are coordinates constructed from the eigenvectors of the Markov matrices. Thus, eigenvectors of Markov matrices can be thought of as coordinates on the dataset.  The goal is to change the representation of the dataset in order to understand the phenomenon that generated the data.  

Let X be the data set and <a><img src="https://latex.codecogs.com/gif.latex?\mu" title="\mu" /></a> is the distribution of the points on X and let k(x,y) be a kernal that is 
symmetric k(x,y) = k(y,x) and 
positivity preserving k(x,y) >= 0




