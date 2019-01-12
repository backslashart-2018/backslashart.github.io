---
layout: post
title:  "Chaos Theory and Navier Stokes"
date:   2019-01-10 09:31:00
categories: Sculpture
---

In the past weeks, we focused on the sculpture software. Our previous prototype was visually appealing, yet lacked one of the crucial ideas that we are trying to capture: entropy. We want to create something that looks organic and natural from discrete systems. This effort prompted us to look back at one of our original ideas and further explore Chaos Theory. Its core idea is that from a small change in initial conditions, the outcomes turn out to be vastly different. And the fluid is a great example of chaotic systems. By pouring a colored solution in water, the manner in which the liquids interact is quite random since it's chaotic.

<br/>
<p align="center"> 
 The Navier-Stokes Equations for Fluid Motions
</p>
<p align="center"> 
  <img src="/assets/images/formula.png">
</p>
<br/>

The Navier-Stokes equations are used to simulate motions of fluid substances. Our first approach to introducing entropy in our system was to implement these equations. Thanksfully, much research has been done in this area because of the advances in game technology since they are very useful that generate fluids in games. Our first iteration looks as such (please watch it in 2x speed):

[![Navier Stokes 1](https://img.youtube.com/vi/05RShJG_6Eg/0.jpg)](https://youtu.be/05RShJG_6Eg)

[![Navier Stokes 2](https://img.youtube.com/vi/US8DI976hfE/0.jpg)](https://youtu.be/US8DI976hfE)


It's a very crude prototype, yet the example captures randomness better and bears resemblance to the way the liquid or air interacts. Nonetheless, we need to optimize on the system's speed and capture acceleration better. More intriguing updates coming soon!
