---
layout: post
mathjax: true
comments: true
title: Riemannian Geometry
image: /img/standard.jpg
---

The need for riemannian geometry arises from the fact that there does not always exist a system of coordinates in 
terms of which the distance between any two neighboring points in the space is given by the sum of the squares of the 
coordinate differentials.  The first example comes to mind is a particle moving on the surface of a sphere. 

This mathematical framework is useful for finding meaningful geometric descriptions in data sets. 
If we let $q^m$ where $m=1 ... f$ be a set of coordinates which define a point in configuration space and another set of coordinates $\bar{\mathbb{q}}^n$ where $n=1 ... f$ which are functions of $q^m$:

\begin{equation}
{\bar{\mathbb{q}}}^n = {\bar{\mathbb{q}}}^n(q^1 ... q^f)
\end{equation}


Infinitesimal changes $dq^m$ in the $q^m$ define infinitesimal changes $d\bar{\mathbb{q}}^n$ in the $\bar{\mathbb{q}}^n$ by 

$$d\bar{\mathbb{q}}^n = \frac{\partial{\bar{\mathbb{q^n}}}}{\partial{q^m}}\partial{q^m}\qquad(m,n = 1 ... f)$$

Quantities $\lambda^m$ which transfor according to the law 

$$\bar{\mathbb{\lambda}}^n = \frac{\partial{\bar{\mathbb{q}^n}}}{\partial{q^m}}\lambda^m$$

are called the contravariant components of a vector.Let us consider the quantity $(dr)^2$, in cartesian coordinates this is given by 

$$(dr)^2 \equiv ds^2 = (dx^1)^2 + (dx^2)^2 +(dx^3)^2$$

If generalized coordinates $q^m$ are used, we get

$$ds^2 = (\frac{\partial{x^1}}{\partial{q^m}}dq^m)^2 + (\frac{\partial{x^2}}{\partial{q^m}}dq^m)^2 + (\frac{\partial{x^3}}{\partial{q^m}}dq^m)^2$$

If we define the metric tensor 

$$g_{mn} = \frac{\partial{x^1}}{\partial{q^m}}\frac{\partial{x^1}}{\partial{q^n}} + \frac{\partial{x^2}}{\partial{q^m}}\frac{\partial{x^2}}{\partial{q^n}} + \frac{\partial{x^3}}{\partial{q^m}}\frac{\partial{x^3}}{\partial{q^n}}$$

Then we can rewrite the generalized coordinates $q^m$ as 

$$ds^2 = g_{mn}dq^m dq^n$$












