---
layout: post
title:  "Sculpture Prototype"
date:   2019-02-15 09:31:00
categories: Sculpture
---

We focused on making the sculpture prototype in the past couple of weeks. As our aesthetic priority is to produce natural and dynamic movements, the Navier Stokes equations were exactly suitable to simulate fluid motions which are random. The following video shows our prototype:

[![Processing](https://img.youtube.com/vi/NHOxLn1EwEw/0.jpg)](https://youtu.be/NHOxLn1EwEw)

In the video, what we see here is a 20x20 grid vector field that represents forces that propagates according to the equations. The green boxes are the positions in which there are forces going through. Random generators control the magnitudes and directions of the added forces in the field. They will be replaced by the GANs in the coming weeks. We used Processing for live interactive feedback and connected Processing directly with Arduino which controls the magnets in the sculpture hardware. Also, we created a mapping function that translates the grid outputs into the compatible input format for the magnets. The hardware prototype built by Brooklyn Research Group is a 2x2 magnet grid, and they are currently working on a larger scale grid for better visual qualities. Here's the video of the first prototype:

[![Magnets](https://img.youtube.com/vi/gSAofmaXimk/0.jpg)](https://youtu.be/gSAofmaXimk)

We are approaching the finish line as most of what is left to do is back-end related and connecting separate components! 
