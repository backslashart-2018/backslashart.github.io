---
layout: post
title:  "Marching Forward"
date:   2018-11-12 09:31:00
categories: t-SNE movement-tracking point-reduction ferrofluid
---

Last Monday, we had a very productive meeting with the team at Tajima Studio. We finalized on the approach to creating real-time animations and Brooklyn Research helped us make promising prototypes with different materials for the physical liquid device.

As we experimented with creating animations, we decided that the best way to create visually interesting animations while keeping it real-time and data-driven is to model the movements in t-SNE visualizations and then use the output of the movement tracking algorithm as parameters to render pre-modeled animations. Another aspect of the “translation” from pure t-SNE to the final animation is to reduce the number of points from tens of thousands of points representing synthetic humans to around a dozen of points representing potentially morphing clusters -- clusters that could be potentially made up of different individuals as the t-SNE model evolves. To summarize, the data pipeline consists of:

1. Run t-SNE on the synthetic human dataset
2. Capture the 3D coordinates of the t-SNE visualization
3. For every frame, reduce the number of points by grouping them
4. Track vector movements of the reduced clusters
5. Render the animation using tracked clusters

Below are some ideas of basic movements to render in the animation.

<p align="center">
 Centering
</p>
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/UOD3NkV3K4U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

<p align="center">
 Aligning
</p>
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/LK_6SXdqETY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

<p align="center">
 Separate and Retract
</p>
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/Tzx00wk1a1U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

On a side note, we are also putting ourselves in the dataset! We are working on compiling a survey and collecting our own answers to the questions asked in the original dating and biometric surveys, as part of an artsy gesture. So we will be “seeing” ourselves morphing in the animation. 

The art piece also consists of a liquid device component and an aural component triggered by MAX. The liquid device will move physical liquids according to images produced by GANS, while the sound will correspond to the clustering output by t-SNE. We have also made progress with those two respective components. Brooklyn Research Group has been prototyping with different liquid materials and motors to drive liquid movements. So far we have seen very promising results using ferrofluid and electromagnets. Below is a short documentary:

<p align="center">
 Ferrofluid Prototype
</p>
<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/fO-n6QAyQRc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

In the coming weeks, we hope to develop the point-reduction and movement tracking algorithms and define some basic cluster movements to be rendered. We are also consulting with a sound expert to figure out the sound texture to use as a backdrop of the artwork and ways to manifest the animation movements in an aural context.