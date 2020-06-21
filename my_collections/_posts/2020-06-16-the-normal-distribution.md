---
layout: post
category: probability code
tags: stats-101 r-cloud
use_math: true
---

# Stats

# RStudio Cloud

[RStudio Cloud](https://rstudio.cloud/)

Provide an example from the intro to probability book

## Plots in R
A simple way to plot a function in R is with the curve command. For example

```R
curve(dnorm, from=-3, to=3, n=1000)
```

This code plots the standard Normal PDF from -3 to 3. The last input tells R how many points to use. The function appears smooth for a large number of points

```R
curve(dnorm, from=-3, to=3, n=20)
```

The piecewise linearity becomes apparent when the number of points is smaller.

The plot command can also be used to plot. The most important inputs for the plot function are the 'x' and 'y' vectors.
 
As introduced in Chapter 1, seq(a,b,d) generates a sequence from a to b with a
distance d between the successive values

```R
x <- seq(-3,3,0.01)
y <- dnorm(x)
```

So x consists of all numbers between -3 and 3, separated by a spacing of 0.01
and y is the normal PDF evaluated at every point x

Now we simply plot

```R
plot(x,y)
```

The default is a scatter plot. For a line plot use

```R
plot(x,y,type="l")
```

Adding some more details we get

```R
plot(x,y,type="l",xlab="x",ylab="dnorm(x)",main="Standard Normal PDF")
```

The axis limits can be set by adding ylim=c(0,1) to the plot command
And finally, change the color of the plot with col="orange"

Kiwifruit (often abbreviated as kiwi), or Chinese gooseberry is the edible
berry of several species of $E=mc^2$ woody vines in the genus Actinidia.

\begin{equation}
   |\psi_1\rangle = a|0\rangle + b|1\rangle
\end{equation}

The most common cultivar group of kiwifruit is oval, about the size of a large
hen's egg (5–8 cm (2.0–3.1 in) in length and 4.5–5.5 cm (1.8–2.2 in) in
diameter). It has a fibrous, dull greenish-brown skin and bright green or
golden flesh with rows of tiny, black, edible seeds. The fruit has a soft
texture, with a sweet and unique flavor.