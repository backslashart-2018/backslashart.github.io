---
layout: post
title:  "Animation Backend and Sculpture Display"
date:   2018-12-15 09:31:00
categories: animation, sculpture
---
For the past two weeks, we focused on building the architecture for driving the animation and sound as well as preparing a separate data pipeline driven by GANS to feed into the ferrofluid device. A picture is worth a thousand words - the diagram below summarizes our vision so far.

![Technical Diagram](/assets/images/architecture.jpeg)

In pipeline #1, we wrote a little program to start a local server and we can control the rest of the pipeline using the client application. Below is a screenshot of what the client looks like. Though not much thought was put into making it the prettiest client, it can start and stop the TSNE and clustering processes, write/reset the database and visually see examples of the data generated from the algorithms. 

![Screenshot of data pipeline client](/assets/images/TSNE_client.jpeg)

For pipeline #2, we worked on the display's aesthetics. We built on top of what we had already made with GANs. The models generate static outputs, but we want something dynamic and captivating. Here is an example of what we envision (prototype by Brooklyn Research):

[![Black Mirror](https://img.youtube.com/vi/1Mhz5bCugFM/0.jpg)](https://www.youtube.com/watch?v=1Mhz5bCugFM)

And the example above shows a cohesive and meaningful shape, so our challenge was to figure out a way to make dynamic movements based on static outputs we have from GANs such as this:

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

