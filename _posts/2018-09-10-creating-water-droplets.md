---
layout: post
title:  "Creating Water Droplets"
date:   2018-09-10 12:21:00
categories: Water Droplets Unity
---

Continuing working with metaphors, we attempted to use gaming engines to create a realistic rendering of physical particles. The idea is to use water droplets to animate the movements of human data in algorithms like t-SNE, PCA, and GANs. In the meeting with Mika, we also talked about the organizational aspects of the art piece since we were thinking about three major moving parts - drones, waterdrop animations, and sounds. 

Water is surprisingly difficult to recreate graphically. They are translucent, but not all so because you can still see them. They distort the background based on lighting directions. And when they move, if you watch it in slow motion, you can clearly see that the droplets first are pressed against each other, until the shield breaks and they merge into one. Below are a few examples of what we were able to achieve in Unity both statically and dynamically:

![Waterdrop 1](/assets/images/waterdrop1.png)
![Waterdrop 2](/assets/images/waterdrop2.png)
![Water flowing into a wall](/assets/images/water-flowing-into-wall.gif)

The goal moving forward is to create more interesting movements of water droplets. These realistic droplets should follow certain physical rules; they would merging into a bigger droplet like real water droplets would do when they meet. At the same time, they are unreal because they may follow zero gravity and be pushed and separated by invisible external forces. For instance, can a few droplets line up into a curved line, slowly merge and then separate like a splash? Can they move in arbitrary directions given XYZ coordinates and if so, can we orchestrate them through code within the gaming engine? There is a lot more to experiment within the coming weeks.

Besides discussing the visuals, we decided in the meeting with Mika, Eric, and Howie that ideally the animations and sounds would be in sync, mimicking the movements of the data visualizations, while drones following another set of directions. Mika is in talks with Intel to figure out the possibility of incorporating a few drones. Logistically, all the processes should run on one machine. 







