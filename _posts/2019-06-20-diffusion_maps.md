---
layout: post
title: Diffusion Maps
image: /img/disk_model.png
---

In this post I will explain and summarize [this](https://www.sciencedirect.com/science/article/pii/S1063520306000546) awesome paper.  The idea behind diffusion maps is dimensionality reduction.  Some datasets (i.e. images) contains useful geometric shapes, and these images often have too many factors (features) and most of the time these features are redundant. Diffusion maps is an efficient representations of these features because it provides a framework where these features are reduced into a smaller number, hence dimensionality reduction.  Mathematically, diffusion maps are coordinates constructed from the eigenvectors of the Markov matrices. Thus, eigenvectors of Markov matrices can be thought of as coordinates on the dataset.  The goal is to change the representation of the dataset in order to understand the phenomenon that generated the data.  


<a href="https://www.codecogs.com/eqnedit.php?latex=\left&space;\{&space;{\acute{}}''&space;\right&space;\}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left&space;\{&space;{\acute{}}''&space;\right&space;\}" title="\left \{ {\acute{}}'' \right \}" /></a>


