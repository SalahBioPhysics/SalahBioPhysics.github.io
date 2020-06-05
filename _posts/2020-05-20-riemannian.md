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

$$\left[mn,r\right] = \overline{\left[ij,k\right]} \frac{\partial{\bar{\mathbb{g}}^i}}{\partial{q}^m} \frac{\partial{\bar{\mathbb{g}}^j}}{\partial{q}^n} \frac{\partial{\bar{\mathbb{g}}^k}}{\partial{q}^r} + \bar{\mathbb{g}}_{ij} \frac{\partial^2{\bar{\mathbb{q}}}^i}{\partial{q}^m\partial{q}^n} \frac{\partial{\bar{\mathbb{q}}}^j}{\partial{q}^r}$$

Solving for the second derivative give us:

$$\frac{\partial^2{\bar{\mathbb{q}}}^i}{\partial{q}^m\partial{q}^n} = {r\choose{mn}} \frac{\partial{\bar{\mathbb{q}}}^i}{\partial{q}^r} - \overline{i\choose{jk}} \frac{\partial{\bar{\mathbb{q}}}^j}{\partial{q}^m} \frac{\partial{\bar{\mathbb{q}}}^k}{\partial{q}^n}$$

The generalized velocity components are taken to be $\dot{q}^j$, we have

$$\dot{\bar{\mathbb{q}}}^k = \frac{\partial{\bar{\mathbb{q}}}^k}{\partial{q}^l}\dot{q}^l$$

And the generalized acceleration is:

$$\ddot{\bar{\mathbb{q}}}^k = \frac{d}{dt}\Bigg(\frac{\partial{\bar{\mathbb{q}}}^k}{\partial{q}^l}\dot{q}^l\Bigg) \\ = \frac{\partial{\bar{\mathbb{q}}}^k}{\partial{q}^l}\ddot{q}^l + \frac{\partial^2{\bar{\mathbb{q}}}^k}{\partial{q}^m\partial{q}^l} \dot{q}^l\dot{q}^m$$

Using the above equation, we have:

$$\ddot{\bar{\mathbb{q}}}^k + \overline{k\choose{mn}} \dot{\bar{\mathbb{q}}}^m \dot{\bar{\mathbb{q}}}^n = \Bigg(\ddot{q}^l + {l\choose{rs}} \dot{q}^r \dot{q}^s\Bigg) \frac{\partial{\bar{\mathbb{q}}}^k}{\partial{q}^l} $$

Now we can write the contravariant components of a vector as:

$$a^l \equiv \ddot{q}^l + {l\choose{rs}} \dot{q}^r \dot{q}^s$$

In cartesian coordinates all the Christoffel symblos vanish because the $g_{mn}$ are constant. In curvilinear coordonates the terms involving the Christoffel symbols give exactly such terms as the centripetal and Coriolis accelerations.  For example, the transformation  from retangular cartesian coordinates in two dimensions $\left(q^1 = x, q^2 = y\right)$ to polar coordinates $\left(\bar{\mathbb{q}}^1 = r, \bar{\mathbb{q}}^2 = \theta \right)$.

$$ds^2 = g_{mn}dq^mdq^n = \bar{\mathbb{g}}_{mn}d\bar{\mathbb{q}}^md\bar{\mathbb{q}}^n$$

with:

$$g_{mn} = \begin{pmatrix}
1 & 0 \\
0 & 1 
\end{pmatrix} = g^{mn}$$

$$\bar{\mathbb{g}}_{ij} = \begin{pmatrix}
1 & 0 \\
0 & r^2 
\end{pmatrix},\quad \bar{\mathbb{g}}^{ij} = \begin{pmatrix}
1 & 0 \\
0 & r^{-2} 
\end{pmatrix}$$

All the unbarred Christoffel symbols vanish and in the barred set of coordinates:

$$\overline{\left[22,1\right]} = -r, \quad \overline{\left[21,2\right]} = \overline{\left[12,2\right]} = r 
\\ \overline{1\choose{22}} = -r, \quad \overline{2\choose{12}} = \overline{2\choose{21}} = \frac{1}{r}$$

and all other terms vanish.

The components of the acceleration vector are given by:

$$\bar{\mathbb{a}}^1 = \ddot{r} = r\dot{\theta}^2 \\ \bar{\mathbb{a}}^2 = \ddot{\theta} + 2\frac{\dot{r}\dot{\theta}}{r}$$

If spherical coordinates $\bar{\mathbb{q}}^1 = r, \bar{\mathbb{q}}^2 = \theta, \bar{\mathbb{q}}^3 = \phi$ are introduced to describe the motion of a particle in three dimensions:

$$ds^2 = dr^2 + r^2d\theta^2 + r^2\sin^2{\theta}d\phi^2$$

$$\bar{\mathbb{g}}_{mn} = \begin{pmatrix}
1 & 0 & 0\\
0 & r^{2} & 0 \\
0 & 0 & r^2\sin^2{\theta}
\end{pmatrix}, \quad \bar{\mathbb{g}}^{mn} = \begin{pmatrix}
1 & 0 & 0\\
0 & r^{-2} & 0 \\
0 & 0 & r^{-2}\csc^2{\theta}
\end{pmatrix}$$

The only nonvanishing Christoffel symbols are those involving, we have:




$$\overline{\left[22,1\right]} = -r \qquad \overline{1\choose{22}} = -r \\ \overline{\left[12,2\right]} = \overline{\left[21,2\right]} = -r \qquad  \overline{2\choose{12}} = \overline{2\choose{21}} = \frac{1}{r} \\
\overline{\left[33,1\right]} = -r\sin^2{\theta} \qquad \overline{1\choose{33}} = -r\sin^2{\theta}$$

...

















