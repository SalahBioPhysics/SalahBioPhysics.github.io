---
layout: post
mathjax: true
comments: true
title: The Computational Molecule
image: /img/mol_2.png
---
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:0px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:0px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>

The computatinal molecule; also called stencil, is the key concept to the theory and the implementation of finite difference methods. 
Finite difference methods seek to find numerical solutions to partial diffferential equations. The computational molecule is a geometric arrangement of a nodal group that relate to the point of interest.  For example if we want to calculate the temperature in the middel (green points) of a slab knowing the temperature of the slab on the sides (red points).

<table class="tg">
  <tr>
    <img src="/img/mol_1.png" alt="p1">
  </tr>
 </table>

Let $$u(x,y)$$ be the temperature $$f$$ at the point $$(x,y)$$ and let $$f$$ be zero on three sides, that is, $$f(0,0) = f(0,1) = f(0,2) = f(0,3) = f(1,3) = f(2,3) = f(3,3)
= f(3,2) = f(3,1) = f(3,0) = 0$$ and let, $$f(1,0) = 1$$ and $$f(2,0) = 2$$.  Now we want to estimate the temperature $$u(1,1), u(1,2), u(2,1)$$, and $$u(2,2)$$

We can illustrate this by the following simple value problem,


$$\Delta u = 0 & \text{in} \Omega \\
    u = f & \text{on} \partial{\Omega}$$
 

We can use the finite difference ferences method by replacing the partial derivatives by thier approximating the difference quotiets as follow:

$$\frac{\partial{u{(x,y)}}}{\partial{x}} \approx \frac{u(x+h,y)-u(x,y)}{h}$$

$$\frac{\partial^2{u(x,y)}}{\partial{x^2}} \approx \frac{\frac{u(x+h,y)-u(x,y)}{h}\frac{u(x,y)-u(x-h,y)}{h}}{h}$$

Taking a single forward difference and the second derivative, we have:

$$\frac{\partial^2{u(x,y)}}{\partial{y^2}} \approx \frac{u(x,y+k) -2u(x,y) + u(x,y-k)}{k^2}$$

Setting $$k=h$$ and solving the equation, we have:

$$0 = \Delta{u} \approx = u(x+h,y) + u(x-h,y) + u(x,y+k) + u(x,y-k) - 4u(x,y)$$

Now the boundray value problem has reduced to a problem in the matrix form:

$$\begin{pmatrix}
4 & -1 & -1 & 0\\
-1 & 4 & 0 & -1 \\
-1 & 0 & 4 & -1 \\
0 & -1 & -1 & 4
\end{pmatrix}
\begin{pmatrix} 
u(1,1) \\ u(1,2) \\ u(2,1) \\ u(2,2)
\end{pmatrix} = 
\end{pmatrix}
\begin{pmatrix} 
1 \\ 0 \\ 2 \\ 0
\end{pmatrix}$$




** APPENDICE B (Introduction to Partial Differential Equations and Hilbert Space Methods, 3nd Edition. Karl E. Gustafson)

















