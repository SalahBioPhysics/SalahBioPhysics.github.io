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

$$d\bar{\mathbb{q}}^n = \frac{\partial{\bar{\mathbb{q}}^n}}{\partial{q^m}}\partial{q^m}\qquad(m,n = 1 ... f)$$

Quantities $\lambda^m$ which transfor according to the law

$$\bar{\mathbb{\lambda}}^n = \frac{\partial{\bar{\mathbb{q}}}^n}{\partial{q^m}}\lambda^m$$

are called the contravariant components of a vector.Let us consider the quantity $(dr)^2$, in cartesian coordinates this is given by 

$$(dr)^2 \equiv ds^2 = (dx^1)^2 + (dx^2)^2 +(dx^3)^2$$

If generalized coordinates $q^m$ are used, we get

$$ds^2 = (\frac{\partial{x^1}}{\partial{q^m}}dq^m)^2 + (\frac{\partial{x^2}}{\partial{q^m}}dq^m)^2 + (\frac{\partial{x^3}}{\partial{q^m}}dq^m)^2$$

If we define the metric tensor 

$$g_{mn} = \frac{\partial{x^1}}{\partial{q^m}}\frac{\partial{x^1}}{\partial{q^n}} + \frac{\partial{x^2}}{\partial{q^m}}\frac{\partial{x^2}}{\partial{q^n}} + \frac{\partial{x^3}}{\partial{q^m}}\frac{\partial{x^3}}{\partial{q^n}}$$

Then we can rewrite the generalized coordinates $q^m$ as 

$$ds^2 = g_{mn}dq^m dq^n$$

We can use other coordinates $\bar{\mathbb{q}}^r$ to have

$$ds^2 = \bar{\mathbb{g}}_{rs} d\bar{\mathbb{q}}^r d\bar{\mathbb{q}}^s$$

Using the invariance of $ds^2$, we get

$$\bar{\mathbb{g}}_{rs} \frac{\partial{\bar{\mathbb{q}}^r}}{\partial{q^m}} \frac{\partial{\bar{\mathbb{q}}^s}}{\partial{q^n}} dq^m dq^n = g_{mn}dq^mdq^n$$

Identifying coefficients of products of coordinate differentials, we have

$$\bar{\mathbb{g}}_{rs} \frac{\partial{\bar{\mathbb{q}}^r}}{\partial{q^m}} \frac{\partial{\bar{\mathbb{q}}^s}}{\partial{q^n}} = g_{mn}$$

If we use the transformation equation for the metric tensor:

$$g_{mn} = \bar{\mathbb{g}}_{ij} \frac{\partial{\bar{\mathbb{q}}^i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}^j}}{\partial{q}^n}$$

Then, we get

$$\frac{\partial{g}_{mn}}{\partial{q}^r} = \frac{\partial{\bar{\mathbb{g}}}_{ij}}{\partial{\bar{\mathbb{q}}}^k} \frac{\partial{\bar{\mathbb{q}}}^{i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}}^{j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}}^{k}}{\partial{q}^r} + \bar{\mathbb{g}}_{ij} \left( \frac{\partial^2{\bar{\mathbb{q}}^i}}{\partial{q}^r\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}^j}}{\partial{q}^n} + \frac{\partial{\bar{\mathbb{q}}^i}}{\partial{q}^m} \frac{\partial^2{\bar{\mathbb{q}}^j}}{\partial{q}^n\partial{q}^r}\right)$$

Changing the indices syclically:

$$\frac{\partial{g}_{rm}}{\partial{q}^n} = \frac{\partial{\bar{\mathbb{g}}}_{ki}}{\partial{\bar{\mathbb{q}}}^j} \frac{\partial{\bar{\mathbb{q}}}^{i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}}^{j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}}^{k}}{\partial{q}^r} + \bar{\mathbb{g}}_{ij} \left( \frac{\partial^2{\bar{\mathbb{q}}^i}}{\partial{q}^n\partial{q}^r} \frac{\partial{\bar{\mathbb{q}}^j}}{\partial{q}^m} + \frac{\partial{\bar{\mathbb{q}}^i}}{\partial{q}^r} \frac{\partial^2{\bar{\mathbb{q}}^j}}{\partial{q}^m\partial{q}^n}\right)$$

$$\frac{\partial{g}_{nr}}{\partial{q}^m} = \frac{\partial{\bar{\mathbb{g}}}_{jk}}{\partial{\bar{\mathbb{q}}}^i} \frac{\partial{\bar{\mathbb{q}}}^{i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}}^{j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}}^{k}}{\partial{q}^r} + \bar{\mathbb{g}}_{ij} \left( \frac{\partial^2{\bar{\mathbb{q}}^i}}{\partial{q}^m\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}^j}}{\partial{q}^r} + \frac{\partial{\bar{\mathbb{q}}^i}}{\partial{q}^n} \frac{\partial^2{\bar{\mathbb{q}}^j}}{\partial{q}^r\partial{q}^m}\right)$$

Putting the last three equations together, we get:

$$\frac{\partial{g}_{rm}}{\partial{q}^n} + \frac{\partial{g}_{nr}}{\partial{q}^m} - \frac{\partial{g}_{mn}}{\partial{q}^r} = \left( \frac{\partial{\bar{\mathbb{g}}}_{ki}}{\partial{\bar{\mathbb{q}}}^j} + \frac{\partial{\bar{\mathbb{g}}}_{jk}}{\partial{\bar{\mathbb{q}}}^i} - \frac{\partial{\bar{\mathbb{g}}}_{ij}}{\partial{\bar{\mathbb{q}}}^k} \right) \frac{\partial{\bar{\mathbb{q}}}^{i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}}^{j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}}^{k}}{\partial{q}^r} + 2\bar{\mathbb{g}}_{ij} \frac{\partial{\bar{\mathbb{q}}^j}}{\partial{q}^r} \frac{\partial^2{\bar{\mathbb{q}}^i}}{\partial{q}^m\partial{q}^n}$$

We define the Christoffel symbol of the first kind as:

$$\left[mn,r\right] \equiv \frac{1}{2} \Bigg(\frac{\partial{g}_{rm}}{\partial{q}^n} + \frac{\partial{g}_{nr}}{\partial{q}^m} - \frac{\partial{g}_{mn}}{\partial{q}^r}\Bigg)$$

And the Christoffel symbol of the second kind as:

$${s\choose{mn}} = g^{sr}\left[mn,r\right] = \frac{1}{2} g^{sr} \Bigg(\frac{\partial{g}_{rm}}{\partial{q}^n} + \frac{\partial{g}_{nr}}{\partial{q}^m} - \frac{\partial{g}_{mn}}{\partial{q}^r}\Bigg) $$

We can write the above equation as:

$$\left[mn,r\right] = \overline{\left[ij,k\right]} \frac{\partial{\bar{\mathbb{g}}^i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{g}}^j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{g}}^k}}{\partial{q}^r} + \bar{\mathbb{g}}_{ij} \frac{\partial^2{\bar{\mathbb{q}}}^i}{\partial{q}^m\partial{q}^n}$$














