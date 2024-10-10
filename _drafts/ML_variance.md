---
layout: post
author: Rashid Alawadhi
title:  "Effect of Variance on Weight Initialisation"
date:   2024-08-31 22:20:00 +0400
categories: ML
---
Weight initialisation is an important aspect of ML. One might have the right architecture for a given problem but the model wold still not learn. To schematically see how the initial values of weights affect the process of training, assume our neural network is
$$f_{NN} \propto www\cdots wx. $$
If we initialise our weights to be zero or close to zero then after each subsequent layer during a forward pass, the signal becomes smaller and smaller leading to no predictions. This also affects back-propagation and leads to the problems of vanishing and exploding gradients. If the weights are too small then they won't get updated sufficiently since,
$$w = w - \eta \frac{\partial \ell}{\partial w}$$
leads to small partial derivatives.

A possible solution is then to initialise the weights by randomly generating their values from a gaussian distribution with zero mean, i.e. $E(w) = E(x) = 0$. However, this will also potentially suffer from the problem of increasing variance of the output of each node in propotion to the number of the inputs. Meaning,
$$Var(w) \propto n .$$

A solution to this problem is to normalise the variance of each nods output to unity. Notice,
$$Var(O )= Var(w_i x_i)\\
= E(w)^2_i x_i + w_i E(x)^2_i + Var(w)_i Var(x)_i \\
= Var(w)_i Var(x)_i$$
Assuming that the variables are i.i.d, i.e. they all have the same variance, we have
$$Var(w)_i Var(x_i) = n Var(w)Var(x).$$

Therefore, if we renormalise the weights by $w \rightarrow w/\sqrt{n}$ and using the fact that $Var(ax+b) = a^2 Var(x)$ we have,
$$O = Var(\tilde{w})_i Var(x_i) = n (\frac{Var(w)}{n})Var(x).$$

Then we can sample the values of $w$ from gaussian $[\frac{-1}{\sqrt{n}}, \frac{1}{\sqrt{n}}]$ distribution.