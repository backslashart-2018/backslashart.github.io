---
layout: post
title:  "Animation Backend and Sculpture Display"
date:   2018-12-15 09:31:00
categories: animation, sculpture
---



<br/>
<p align="center"> 
 Initial Output
</p>
<p align="center"> 
  <img src="/assets/images/initialview.png">
</p>
<br/>

For the sculpture, we worked on the display's aesthetics. We built on top of what we already made with GANs previously. The outputs from the model are static as seen above. And the points are scattered, so the challenge was to figure out a way to make dynamic movements based on them. Per Mika's vision, we wanted to lasso individual points and create outerbounds for display. Here were the steps to execute the idea. First, we applied a gaussian blur on the images iteratively.

<br/>
<p align="center"> 
 Gaussian Blur on GANs Output
</p>
<p align="center"> 
  <img src="/assets/images/blurring.gif">
</p>
<br/>

Given the blurred image, we created a heightmap based using the brightness as the third axis value. Here's how looks. 

<br/>
<p align="center"> 
 3D Heightmap
</p>
<p align="center"> 
  <img src="/assets/images/3dmap.png">
</p>
<br/>

<br/>
<p align="center"> 
 Heightmap Topview
</p>
<p align="center"> 
  <img src="/assets/images/topview.png">
</p>
<br/>

Then we slice the heightmap on different levels to draw contour plots. The image above shows the plots in different colors. No we can use these to create interesting shapes connecting individual points from the GANs. 


<br/>
<p align="center"> 
  Contour Plots based on Levels
</p>
<p align="center"> 
  <img src="/assets/images/morphing.gif">
</p>
<br/>

We are collaborating with Brooklyn Research Group on how to format the data input for the hardware.

