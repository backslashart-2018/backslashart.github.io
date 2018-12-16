---
layout: post
title:  "Animation Backend and Sculpture Display"
date:   2018-12-15 09:31:00
categories: animation, sculpture
---



For the sculpture, we worked on the display's aesthetics. We built on top of what we had already made with GANs. The models generate static outputs, but we want something dynamic and captivating. Here is an example of what we envision:

[![Black Mirror](https://img.youtube.com/vi/1Mhz5bCugFM/0.jpg)](https://www.youtube.com/watch?v=1Mhz5bCugFM)

And the example above shows a cohesive, meaningful shape. Our challenge was to figure out a way to make dynamic movements based on static outputs we have from GANs such as this:

<br/>
<p align="center"> 
 Initial Output
</p>
<p align="center"> 
  <img src="/assets/images/initialview.png">
</p>
<br/>

In order to create dynamic shapes, we wanted to group the individual points and use the outerbounds as the final outputs. Mika liked the idea of simply lassoing the points and experiment with the results. Here are our steps to execute the idea. First, we applied a gaussian blur on the images iteratively to create some structure in the image. Based on the structure, we can do more interesting experiments. 

<br/>
<p align="center"> 
 Gaussian Blur on GANs Output
</p>
<p align="center"> 
  <img src="/assets/images/blurring.gif">
</p>
<br/>

Given the blurred images, we then created a heightmap by using the brightness in each pixel as the third axis value. Here's how looks. 

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

Then we slice the heightmap on different levels to draw contour plots. The image above shows the contours on different levels in different colors. Here's how it looks when we go over each one in iteration. 

<br/>
<p align="center"> 
  Contour Plots based on Levels
</p>
<p align="center"> 
  <img src="/assets/images/morphing.gif">
</p>
<br/>

We are collaborating with Brooklyn Research Group on how to format the data input for the hardware.

