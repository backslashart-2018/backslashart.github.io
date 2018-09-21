---
layout: post
title:  "High Fidelity Simulations"
date:   2018-09-21 11:54:00
categories: simulations
---

In the past weeks, we have experimented with game engines to generate particle simulations. As novices in game development, we spent a considerable amount of time getting ourselves familiar with the platforms. Online tutorials were the primary resource for self-learning. Besides getting the hang of the engines, our main focus was to produce a high fidelity simulation that mimics the fluidity of water or mercury based on our t-SNE convergence. 

<br/>
<p align="center"> 
 t-SNE Convergence
</p>
<p align="center"> 
  <img src="/assets/images/embeddings.gif">
</p>
<br/>

Because we are using Tensorflow to calculate the t-SNE embeddings, it was vital for us to connect the platform with the game engine. We achieved the connection with a plugin and tested it out with a simple mnist model prediction as seen below. The connection will then allow us to use the embeddings directly to manipulate the locations of various objects in the 3D scene, representing the t-SNE convergence.

<br/>
<p align="center"> 
 Running Tensorflow on Unreal Engine 4
</p>
<p align="center"> 
  <img src="/assets/images/tensorflow.gif">
</p>
<br/>

<br/>
<p align="center"> 
 Basic Ocean Simulation on Unreal Engine 4
</p>
<p align="center"> 
  <img src="/assets/images/ocean.gif">
</p>
<br/>
Moreover, the aesthetics and physics of the particles were the other major components. Our goal is to create a photorealistic simulation that both follows and defies the real life behaviors of the rendered material. For example, we want the water particles to attract each other in some phases, but repel each other in others. We discovered a platform called NVIDIA FleX that allows a more detailed control of generating particle simulations. In the coming weeks, we plan to delve into this platform to add more complexities in our simulation on the game engine. 

For the drone performance, we are inspired by [Urs Fischer's recent installation](https://gagosian.com/exhibitions/2018/urs-fischer-play/). As seen in the video, we want to program drones to autonomously fly around indoors. Also, the artist concealed the mechanism that controls the movements of the chairs. Similarly, we plan to retrofit drones in such a way that would conceal the appearance of the drones as much as possible. 
