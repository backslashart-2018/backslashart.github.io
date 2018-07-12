---
layout: post
title: "Plots and Drones for Visualizing Hybrid Profiles"
date:   2018-07-12 15:59:00
categories: Visualizations Drones
---

As we discussed in our previous post, we created “hybrid profiles” using the public profile data from various sources. The OkCupid and 23andMe datasets are the primary sources. Although we found another interesting dataset called MegaFace that contains over 4 million facial images, we decided to focus on the dating and genetic datasets for artistic reasons, leaving the audience to imagine the faces of these new individuals. The hybrid dataset contains characteristics of individuals ranging from physical traits like weight and height to unique talents like having perfect pitch or certain strong sensory abilities. We created these “superpowers” from an absolute pitch survey on [Personal Genome Project](https://https://my.pgp-hms.org). We then treat these data points as new entities in the virtual space.

![t-SNE Visualization of OkCupid Dataset](https://lh6.googleusercontent.com/FVmGc6iy3srfbQ06f9_bZR9V5crpGY_vBkc-Gdj4KUEoxpRG9qJgWvWrJjlheEaKpDTcEcl9aqu62PgTnkXtTOjSOQ6F_kltX4m6PeweTRxAsQzSRHKaOHOmJrGcXE0LqkgSAlcb)

Given the dataset, we created visualizations using different dimensionality reduction techniques such as PCA and t-SNE. By reducing the dimension to 2D and 3D, the patterns in the data emerge for our understanding, and we can create visual effects by layering clusters on top of them. We used k-means for clustering the data points. We plan to layer the visualization by switching between the dimensionality reduction techniques and showing each stage of the clustering.

We’re also very excited to explore the idea of using drones as the means to reconstruct the visualizations in the physical space. Intel’s work at [PyeongChang 2018 Olympic Games](https://https://youtu.be/fCd6P7Ya160) is an excellent example of using drones as an artistic medium. However, there are limitations for this type of visual experience, including safety, battery life, noise, and space. Through the training at MakerLAB on campus, we hope to learn more about hardware to achieve this art form.

In addition to data and material considerations, we plan to add sound as another dimension in our art piece. As we get more familiar with the datasets, the form through which the data manifests itself in sound will become clear. The genetic sequence can essentially serve as a set of numbers that can be mapped to pitch, volume, timbre and other sound qualities, but this process will likely result in a white-noise-like sound due to its random nature. In comparison, would sampled sounds be more philosophically and artistically interesting? And what triggers those sounds? In the coming weeks, we plan to explore ideas for the art form to create both visual and aural representations.  
