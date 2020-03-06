---
layout: post
title: What are Wavenumber and Wave Vector
subtitle: Now I know what a wave number is.
tags: [wave, wavenumber, wave vector, physics]
---


>Waves living in 1D space have a *wavenumber*.
>
>Waves living in 2D or 3D space have a *wave vector*.

Because anything 2D or 3D is basically an extension to the same concept in 1D, I'll head with **wavenumber** first.

## Just another property of waves
Wavenumber is like "wavelength" or "frequency". It is a property that allows us to define waves in a simple manner.


## Pretty similar to frequency

You know, frequency of a wave is defined as $\omega  = \frac{2\pi}{T}$. Whereas the wavenumber of a wave is $k=\frac{2\pi}{\lambda}$.

## What was a wave, BTW?

In fact, anything that oscillates can be considered as a wave. See this definition from Wolfram Scienceworld:

>Waves are defined as disturbances which are periodic in time and space. In order to be a wave, a quantity must satisfy the wave equation. In general, waves
>
>    1. Exhibit no net transport of material, 
>    2. Transport energy, 
>    3. Have characteristic waveforms, 
>    4. Propagate at uniform waveform-independent speed, 
>    5. Have speeds dependent on medium. 

## *A wave is a physical construct.* 
These are waves:

![water waves](/img/imgs-2019-Week-42/wave1.jpg)
![water waves](/img/imgs-2019-Week-42/wave3.jpg)
![sound waves](/img/imgs-2019-Week-42/wave2.jpeg)

Ripples on the surface of a pond are waves, changes in the air pressure are waves. They are all waves but we need a way to represent them mathematically, so that we don't have to think of every *wavy* motion as a unique problem but rather something that we know how to deal with. Mathemagic is comiinngg!!
#
It is the amplitude that is easily measurable, but when we look at a wave, its parameters (wavelength, frequency, wavenumber) don't simply show up. *This is because, those are **model parameters**!* Not natural: human invention.

<div style="width:100%;height:0;padding-bottom:56%;position:relative;"><iframe src="https://giphy.com/embed/3oz8xur099boo4N9aU" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div>

## Look at the gif above, which shows constant change along time and space?
    
    A- Temperature of the water
    B- Smell of the water
    C- Height of the water
    D- Number of fish living inside

>*Well, this question wasn't super-smart since we don't really know temperature or fish density. Just assume that none of them show a noticable change in the time and space we are looking at.*

It is C, of course! We notice that the height of water changes constantly and both by time and position. 

Let's investigate this phenomenon in two independent cases:

### Case 1: **Freeze time, travel along the beach**

You are Dr. Stephen Strange, and you love enjoying the sunset so much that you freeze the time and just walk in beach.

![Still time](/img/imgs-2019-Week-42/timestill.png)

![](/img/imgs-2019-Week-42/posgraf.png)
***Change in the water level due to change in position has something to do with the wavenumber***

### Case 2: **Stop moving, let the waves hit you**

![](/img/imgs-2019-Week-42/position%20still.gif)

![](/img/imgs-2019-Week-42/timegraf.png)

***Change in the water level due to change in time has something to do with the frequency***

#

Mathematicians have functions called **sine** and **cosine**, which when their graph is plotted, look a lot like what we call as a *wave* in physical world. We use them to model real waves in time and space!

## One-Dimensional Wave Equation Modeled As Sine

$$y(x,t)=A\sin(kx +\omega t +\phi)$$

$\sin$ function is only responsible for creating a wave form between $-1$ and $1$. In order it to be able to represent our wave, we need to tell it 

>I want you to make one full waveform, if I move 1 unit length towards beach (and time has no effect).

To achieve that, we need to include some expression to our function so that for each unit increase in $x$, that expression completes one cycle from $0$ radians to $2\pi$ radians -completing one full period for sine.

If that relation is not "easing in or out" (i.e. it is a linear relation) then this might be a good formula:

$$2\pi \frac{x}{1 \text{ unit length}}$$

That added into sine would look like this:

$$\sin (\frac{2 \pi}{1 \text{ unit length}} x)$$

If you remember, by the way, there is a special name for the "length which cover one waveform": **wavelength**

So, this means our sine function should look like this:

$$\sin (\frac{2 \pi}{\lambda} x)$$


### Let's move on!

>I want you to make one full waveform, if 1 unit time passes (and I don't change my position).

To achieve that, we need to include some expression to our function so that for each unit increase in $t$, that expression completes one cycle from $0$ radians to $2\pi$ radians -completing one full period for sine.

Again, if that relation is not "easing in or out" (i.e. it is a linear relation) then this might be a good formula:

$$2\pi \frac{t}{1 \text{ unit time}}$$

That added into sine would look like this:

$$\sin (\frac{2 \pi}{1 \text{ unit time}} t)$$

Similar to previous case, there is a special name for the "time which is required for one full waveform": **period**

So, this means our sine function should look like this:

$$\sin (\frac{2 \pi}{T} t)$$

### Put those two together:

$$\sin(\color{red}{\frac{2 \pi}{\lambda} x } + \color{blue}{\frac{2 \pi}{T} t})$$

-which, behind the scene, means-

$$\sin(\color{red}{\text{I'm responsible for change due to position}} + \color{blue}{\text{I'm responsible for change due to time}})$$


### **Impressive!**

Finally, we should consider this:

>Um, what if at $t=0$ and $x=0$ the amplitude of the wave isn't $0$?

Currently, $\sin(\frac{2 \pi}{\lambda} x + \frac{2 \pi}{T} t)$ has an amplitude of $0$ at $t=0$ and $x=0$. In order to get an amplitude other than $0$ at $t=x=0$, we can *shift* the sine function. That should be easy! We need an expression, that is independent of both time and position but can *shift* the sine.

A simple *phase angle* whose value can range from $0$ to $2\pi$ would be sufficient.

$$\sin(\phi)$$

### To put everything together:

$$\sin(\frac{2 \pi}{\lambda} x + \frac{2 \pi}{T} t + \phi)$$

### Plus, scaling the amplitude:
This will scale the model wave amplitude from $[-1,1]$ to $[-A,A]$ where $A \in \mathbb R ^+$:

$$A \sin(\frac{2 \pi}{\lambda} x + \frac{2 \pi}{T} t + \phi)$$

## We get our own wave defining equation; You are awesome!

Let's compare this with what the physicist call as *wave equation*:

$$y(x,t)=A\sin(kx +\omega t +\phi)$$

**vs**

$$A \sin(\frac{2 \pi}{\lambda} x + \frac{2 \pi}{T} t + \phi)$$

therefore what is called as **wavenumber** is mathematically $k=\frac{2 \pi}{\lambda}$.
It all worked out pretty good in one-dimension. How about 2D or 3D?

# Wavenumber for 2D and 3D waves

> Here we talk a little about plane waves. If you wish, you can skip into wavenumber related part: [Beam me down, Scotty!](#wave-equation-for-plane-waves-whose-waveform-is-modeled-by-a-sine-wave).

A wave can have different wavefronts if it is living in 2D or 3D. In our case, we will limit our interest on only waves with a *simple wavefront*: **plane waves**.  The mathematical modeling of so called plane waves are similar to that of 1D waves (which we've discussed above). Here are some examples of *non-planar* wavefronts:

https://evantoh23.wordpress.com/2011/08/03/wavefront/
![evantoh23 circular wavefront](/img/imgs-2019-Week-42/circular_1.jpg)
https://www.quora.com/What-is-a-spherical-wave-front
![quora spherical wavefront](/img/imgs-2019-Week-42/spherical.png)

We can get non-planar wavefronts by passing a planar wavefront through an imperfect medium.

https://www.wikiwand.com/en/Adaptive_optics
![wikipedia adaptive optics](/img/imgs-2019-Week-42/distorted.png)


## Plane waves, *please?*

2D plane waves have "line" wavefronts:

<a title="Oleg Alexandrov [Public domain], via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Plane_wave.gif"><img width="128" alt="Plane wave" src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Plane_wave.gif"></a>

In the gif above, each color represents a certain amplitude of the wave. For example, if you know the amplitude of the wave at a point which is painted in some shade of blue, every single point in the range of this gif with that same shade of blue will have the exact same amplitude. Of course, the same applies to every shade of each color. Luckily there is another gif showing exactly what we have just stated, only in a more elegant way.

<a title="Herbertweidner [CC0], via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Plane_wave_animation.gif"><img id="wavegif" width="256" alt="Plane wave animation" src="https://upload.wikimedia.org/wikipedia/commons/d/d9/Plane_wave_animation.gif"></a>

At this point I should remind that this is still a 2D wave. The mathematical relationship defining this plot is $z=\sin (\vec k \cdot \vec r + \omega t+\phi)$ where $\vec k$, $\vec r \in \mathbb R^2$. We are using third dimension to represent amplitude but position vector $\vec r$ is two-dimensional.

### 3D plane waves have "plane" wavefronts:

https://www.wikiwand.com/en/Plane_wave

![3D plane wave](/img/imgs-2019-Week-42/caldim.png)

There is also a gif for that, YAY!

<a title="Dave3457 [Public domain], via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Plane_Wave_3D_Animation_300x216_255Colors.gif"><img width="256" alt="Plane Wave 3D Animation 300x216 255Colors" src="https://upload.wikimedia.org/wikipedia/commons/4/44/Plane_Wave_3D_Animation_300x216_255Colors.gif"></a>

This time, every red point you see is the same as red points in the above figure; and every red rectange is analogous to red lines. Above, red points (or blue, or whatever colored points) were forming "lines"; here, red points form "planes".

Sadly, there is no easy way to visualize 4D graphs, means [this gif](#wavegif) has no analog in this case. Previously space was X and Y; amplitude was Z and everyone was happy. Now, space is X, Y and Z; and amplitude (let's pick W for that) has no axis to be represented on. Though, not a big deal. The mathematical expression for such a wave is the same as the other $w=\sin (\vec k \cdot \vec r + \omega t+\phi)$ where this time $\vec k$, $\vec r \in \mathbb R^3$

Moving on!

## Wave equation for plane waves whose waveform is modeled by a sine wave

$$w(\vec r,t)=A\sin(\vec k \cdot \vec r +\omega t +\phi)$$

where $\vec r$ is the vector representing position relative to some origin and $\vec k$ is the *wave vector* whose magnitude is wavenumber and direction is in the *direction of propagation*.

To restate:

>$k$ is *wavenumber* and is a scalar quantity

>$\vec k$ is *wave vector* and is a vector quantity

>$\lVert \vec k \rVert=k$ (wave vector has a magnitude equal to wave number)

>Plane waves propagate in space in the same direction as their *wave vector*

### But you said in 2D and 3D there is wave vector, not wavenumber?

I lied, kinda. 

If we want to define wavenumber for a wave propagating in higher dimensions, we still can do that. We defined $k=\frac{2\pi}{\lambda}$. Wavelength is still "the length between two peaks or troughs"! Only difference is, this time, the shortest line between two peaks is not parallel to x-axis but rather along some other direction (in fact, it is exact same direction where the $\vec k$ (wave vector) is pointing).

Similarly, if we want to define wave vector for a wave in 1D, we simply pick $\vec k$ as a vector pointing along the x-axis (which is only valid axis in 1D) whose length equal to $\frac{2\pi}{\lambda}$.

### Forget maths for a second: **abstraction time!**

How it looks for 2D vectors:

<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/KRuvLOqNaik?modestbranding=1"
  frameborder="0"></iframe>

How it looks for 3D vectors:

<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/BbUpsbInkDA?modestbranding=1"
  frameborder="0"></iframe>


## **Endgame:** Making sense of the dot product

We learned how the math work in 1D very well. We also observe the visual relationship between a wave and its wave vector. Now, it is time to learn the math for 2D and 3D as well. *I am excited!*

To start right away, let's put our general wave formula:

$$w(\vec r,t)=A\sin(\vec k \cdot \vec r +\omega t +\phi)$$

Since the topic of this article is wave vector and it is independent of time or phase; I would ignore $\omega t + \phi$ term. Additionaly, the $A$ factor has no effect on the spatial distribution of our wave. In other words, if some point in space was a peak point with some $A$ coefficient, then it will also stay as a peak with other $A$s ($A \ne 0$) and without $A$ (ie. $A=1$). Therefore the formula simplifies to:

$$w(\vec r)=\sin(\vec k \cdot \vec r)$$

Way better!


### Quiz Time! Dot (inner) product of vectors can be interpreted as ...
    
    A- Temperature of the water
    B- Smell of the water
    C- Height of the water
    D- Projection of one vector onto another

That was tough, huh? Well, it is not *just* projection of course. Result of the dot product $\vec a \cdot \vec b$ is **"magnitude of $\vec a$" multiplied with "the magnitude of the projection of $\vec b$ onto $\vec a$"**.

If you need a refresher on the topic, this old man with his toys is where you should go:

<iframe width="560" height="315" src="https://www.youtube.com/embed/f5liqUk0ZTw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Create our own 2D wave

$$z(\vec r)=\sin(\vec k \cdot \vec r)$$

- $z$ is the amplitude. It is a result of the expression on the right. So it is dependent variable. 
- $\sin$ is the famous sine function allowing us to model real waves.
- $\vec k$ is the *wave vector* and **we know its value**. It is a model parameter.
- $\vec r$ is position and it is our independent variable. We will experiment with different values of it and observe what happens to $z$ (aka dependent var.)

### Deciding a value for $\vec k$

We can make up a $\vec k$ out of thin air because we are not referring to a real wave. We are just experimenting. We decided our wave to live in 2D, therefore $\vec k \in \mathbb R ^2$. 

$$\vec k = \begin{pmatrix} k_x \\ k_y \end{pmatrix} = \begin{pmatrix} \frac{2 \pi}{\lambda _x} \\ \frac{2 \pi}{\lambda _y} \end{pmatrix} $$

> For those who are interested; $\lambda ^2 \ne {\lambda _x}^2 + {\lambda _y}^2$. It is not like *x and y components of a vector*. Correct relationship is $\lambda ^2 ({\lambda_x}^2 + {\lambda_y}^2)= {\lambda_x}^2 {\lambda_y}^2$ . Can you figure out why? *Tip: $\lambda_x$ and $\lambda_y$ are edges of the right triangle. $\lambda$ is the height of that triangle from hypotenuse. Watch the video "Case 0-2..." below for more.*

Let's pick the wavelength along x axis to be 3 and wavelength along y axis to be 4.

$$ \lambda _x := 3 \implies k_x = \frac{2 \pi} {3}$$

and

$$ \lambda _y := 4 \implies k_y = \frac{2 \pi} {4} $$

therefore 

$$\vec k = 2 \pi \begin{pmatrix} 1/3 \\  1/4 \end{pmatrix} $$

### **Case #0:** At origin

When $\vec r = \begin{pmatrix} 0 \\ 0 \end{pmatrix}$, $\vec k \cdot \vec r$ becomes $0$.

$$z(\begin{pmatrix} 0 \\ 0 \end{pmatrix})=\sin(0)=0$$

### **Case #1:** Keep $\vec r$ parallel (ie. aligned) with $\vec k$

We are only interested at the positions which are on the same line with our wave vector. 

$$ \vec r = \alpha \frac{\vec k}{\lVert \vec k \rVert} = \alpha \hat k$$

$\alpha$ is a scalar. It scales the unit vector $\hat k$ (spelled key-hat) (which is parallel to $\vec k$) up and  down to create all vectors who share the same line with $\vec k$. Any vector $\alpha \hat k$ has a magnitude of $\alpha$. If this is the case then our wave equation becomes:

$$z(\vec r)=\sin(\vec k \cdot \vec r) = \sin (\vec k \cdot \alpha \hat k)$$

$$= \sin (\alpha (\vec k \cdot \hat k))=\sin(\alpha ( \lVert \vec k \rVert ))$$

> $\lVert \vec k \rVert=k$ (wave vector has a magnitude equal to wave number)

$$=\sin(\alpha  k)$$

> $k = 2 \pi / \lambda$

$$=\sin(2\pi \frac{\alpha}{\lambda})$$

> where $\lambda = (3 \times 4)/5=2.4$

$$=\sin(2\pi \frac{\alpha}{2.4})$$

Pause and think for a second what this means.

...

It means that if we walk along $\vec k$; at every 2.4 units **one complete waveform** is drawn.

### **Case #2:** Keep $\vec r$ perpendicular to $\vec k$

When $\vec r$ and $\vec k$ are perpendicular to each other; $\vec k \cdot \vec r$ becomes $0$.

$$z(\vec r)=\sin(0)=0$$

It means that if we walk along a direction which is perpendicular to $\vec k$, independent of how many units we've moved; *the wave amplitude won't change*.


### **Case 0-2 explained visually:**
This video covers cases #0 to #2 and contains insight for case 3.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hpA3X-Bk0sE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



### **Case #3:** Arbitrary $\vec r$ 

This is my favorite! We first downgrade our 2D or 3D problem into 1D, and then solve it with the same equation for 1D waves.

$$ z(\vec r) = \sin(\vec k \cdot \vec r)$$

$$ z(\vec r) = \sin( \color{purple}{(\lVert \vec k \rVert)} \color{green}{(\text{Magnitude of the projection of } \vec r \text{ onto } \vec k)})$$

$$ z(\vec r) = \sin(\color{purple}{k}\color{green}{(\text{Magnitude of the projection of } \vec r \text{ onto } \vec k)})$$
$$ z(\vec r) = \sin(\color{purple}{ \frac{2\pi}{\lambda}}\color{green}{(\text{Magnitude of the projection of } \vec r \text{ onto } \vec k)})$$

>Meanwhile 1D waves: 
>
>$$y= \sin (\color{purple}{\frac{2 \pi}{\lambda}} \color{green}{x})$$

Did you notice the similarity?

Reason for the use of "dot" operation is only to be able to make use of 1D wave equation. It allows us to ignore the component(s) of $\vec r$ who won't contribute to amplitude change. Then, because we got rid of component(s) who is (are) perpendicular to $\vec k$, there is just a line left: the line which $\vec k$ lives in; and line means, now we are in 1D!


### **Case 3 explained visually:**
<iframe width="560" height="315" src="https://www.youtube.com/embed/TJsGyJMQmSU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



# Oof. Finally.

It want to believe that after my 15 days of effort, you know what a wavevector or wavenumber is. Thank you for your participation.

if you need any help or you think you have a suggestion feel free to mail me: alpersunter1@gmail.com

The End

(not exactly. because I still need to record a video that covers the whole post.)
