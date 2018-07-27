---
layout: post
title: "Morphing Points and Max-triggered Sounds"
date:   2018-07-12 15:26:00
categories: Max
---

| ------------- | ------------- |
| <img src="/assets/images/tsne_500.gif" width="30%"> | <img src="/assets/images/svd_anim.gif" width="30%"> | <img src="/assets/images/pca_anim.gif" width="30%"> | 

This past week, we had a deepened conversation about visualizing "new humans" with the Tajima team. With our meshed dataset handcrafted from various data sources, we finished the initial iterations of PCA, t-SNE, and truncated SVD visualizations.  Regarding the visual direction, we found there are two paradigms going forward. One is to move from one dimensionality-reduction technique to the next (or different steps in t-SNE). The other model is to keep changing the permutations of features included so the points keep moving. There are philosophical arguments to be made on both sides. The first direction shows how machines see things we as humans cannot see about these “Frankenstein" individuals as they exist in high-dimensional space. By employing various dimensionality reduction techniques, the nature of the data in their space emerges in different manners in a way that we can comprehend. As each technique yields a different pattern, we can suppose that not only different aspects of the individuals can show but also the integrity of the data as a whole is kept. On the other hand, the second direction places the emphasis on the multi-faceted nature of human beings -- there are never enough features to fully capture a person. By including different features, we show that there are always new perspectives to see someone. We came to the conclusion that we will be able to make a better decision when we see both so we will be creating examples of technique shift and feature shift visualizations in the coming weeks. 
<br/>

<p align="center"> 
 t-SNE Convergence
</p>
<p align="center"> 
  <img src="/assets/images/tsne.gif">
</p>

<br/>

The next focus is to create endless, moving points such that the visualizations would never loop and we would still be able to see new things. We are experimenting with generative adversarial networks (GANs) to create infinite visualizations. Introduced in 2014 by Ian Goodfellow et al., GANs found numerous powerful applications in image and video generation. Recently, GANs have been used in an [artisic context](https://www.cnet.com/news/ai-gets-naughty-by-generating-nude-portraits/) to generate new artwork based on certain styles, and we also want to test its potential in our project by using it to create a visualization that keeps on changing without looping. On a high level, the architecture is intuitive as it contains a generator that generates new images and a discriminator that decides whether each image was generated or not, and the two models try to outperform one another. As a result, the network produces high quality images that look similar to its training images. The artists were all intrigued by this idea of two digital brains competing and interacting with each other. 

<br/>

![Max playing genetic sequence](/assets/images/max-playing-genetic-seq.png)

<br/>

In the world of sound, we created a Max program (pictured above) in an attempt to make sounds out of genetic sequences, by mapping [SNP](https://en.wikipedia.org/wiki/DbSNP) to pitch, genome position to duration and the two [allels](https://en.wikipedia.org/wiki/Allele) to a few [General MIDI](https://en.wikipedia.org/wiki/General_MIDI) sounds. The result is this bizarre, somewhat random yet steady flow of sounds consisting of bird tweets, flute, piano, and drums. Though we don‘t imagine this specific program to be part of the final art piece, it gave us a lot of ideas for how we might create aural elements that fit with the visually morphing points. One idea is to use chord progressions to simulate as new clusters form. Another idea is to create a signature sound for each individual. There are a lot of questions to be asked relating to the material used and the position of speakers, but we are moving closer and closer to the goal and, most importantly, having fun.
