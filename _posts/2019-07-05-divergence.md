---
layout: post
title: Divergence
subtitle: Vector calculus is not horrible.
tags: [divergence, vector calculus, math]
---

> The physical significance of the divergence of a vector field is the rate at which "density" exits a given region of space.
(from Wolfram Mathworld)

Well, umm... Is that all there to it?
Technically, yes; for gaining intuition, *a big NO!*

## Vector?
I aim to keep this article as brief as possible and I am not the one to teach about vectors. You deserve better sources.

## Vector field?
![Vector field](/img/imgs-2019-Week-27/vector space 1.svg.png){:style="float:right" width="300" height="300"}
Every point in the space has a vector attached to it. These are examples of vector fields in 1D, 2D and 3D. (It can be extended to infinitely many dimensions, we however cannot visualize more than 3D with this much clarity.)

### 1D Vector field
Any location on 1D space (ie. number line) is a point $\color{orange}{P f(x)}$ and the vector associated with the point $\color{orange}P$ is $\color{red}{\vec {V} =\left(  \color{grey}{ f(   \color{orange}{P_{x}}   )}   \right)}$ where $\color{grey}{f}$ is an arbitrarily chosen funcion as $\color{grey}{f(x)=(x-5)(x+10)}$.
<iframe src="https://editor.p5js.org/alpersunter1@gmail.com/embed/tshnG3w0J" width="610" height="210">If you see this text, iframe didn't properly loaded the target url. You can check the link https://editor.p5js.org/alpersunter1@gmail.com/embed/tshnG3w0J yourself. :)</iframe>

### 2D Vector field
1D was not so visually appealing but here, in two-dimensions, you will feel reason for the word "field" in your chest. Here, any location on 2D space (ie. $R \times R$ plane) is point $\color{orange}{P(x, y)}$ and the vector associated with the point $\color{orange}P$ is $ \color{red}{\vec V = \begin{pmatrix}  \color{gray}{f(\color{orange}{P_x})} \\ \color{gray}{g(\color{orange}{P_y})} \end{pmatrix}}$ 
