---
layout: post
mathjax: true
comments: true
title: Diffusion Maps
image: /img/disk_model.png
---
<style>
div_1 {
  background-color: lightgrey;
  width: 100px;
  border: 10px solid lightgreen;
  padding: 10px;
  margin: 5px;
}
</style>

In this post I will explain and summarize [this](https://www.sciencedirect.com/science/article/pii/S1063520306000546) awesome paper.  
Diffusion maps are coordinates. More precisely, they are the eigenfunctions of Markov matrices.  Diffusion maps generate efficient
data representations of complex geometric structures that allow us to extract relevant features out of the data in order to gain insight and understanding of the phenomenon that generated the data.  

<div_1>An $n x n$ matrix is called a Markov matrix if all entries are nonnegative and the
sum of each column vector is equal to 1.</div_1>







