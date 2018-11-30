---
layout: post
title:  "Marching Forward"
date:   2018-11-30 09:31:00
categories: Pipeline Integration
---

In the past weeks, we worked on calibrating the data pipeline to produce the compatible outputs for Unreal Engine and Max for video and audio outputs. Since the visual aspect of the animation improved substantially, we focused on integrating different components for the final form. Here’s the overview of the pipeline. 

<br/>
<p align="center"> 
 Pipeline Overview
</p>
<p align="center"> 
  <img src="/assets/images/pipeline.png">
</p>
<br/>

Although we had each component prototyped, we had to optimize them and make them work together. The first component is the t-SNE model. It receives the raw dataset and produces the 3D coordinates with t-SNE. As we mentioned in previous posts, t-SNE reduces the dimensionality of the dataset to visualize it better. The challenge here was to optimize for the speed. Calculating the gradients for t-SNE has a considerable computational complexity. We used Tensorflow to address this issue. 

The second component of the pipeline calculates the centroids of the t-SNE coordinates as the final animation won’t represent thousands of data points. By using K-Means, we can capture the trend of the t-SNE movement because it clusters the data points based on their distances and produces their average positions, namely centroids. The centroids represent the final data points that will be represented in the animation in the form of mercury. The obstacle we faced in this domain was that the centroids jump around and do not produce gradual shifts. In the animation, they would look choppy and irregular. In order to address this, we have to calculate intermediate positions between the iterations.

<br/>
<p align="center"> 
 Centroids Tracking
</p>
<p align="center"> 
  <img src="/assets/images/centroids.gif">
</p>
<br/>

The last module creates and relays a stream of coordinates for the animation and audio engines to render their outputs. For instance, Unreal Engine, which is used for rendering the animation, grabs the centroids’ positions and overlays visuals on the coordinates. 

[![Metaball Visual So Far](https://img.youtube.com/vi/BM3qe0Q5glw/0.jpg)](https://www.youtube.com/watch?v=BM3qe0Q5glw)
