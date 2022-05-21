---
title: "Microseismicity in South Island, New Zealand"
date: "2021-04-13"
tags:
- project
- seismicity
- New Zealand
---

Seismicity rate changes when the stress state in the crust changes. Both seismicity and geodetic data are readily available to us. But how does one translate to another?

In this project, we investigate if the subduction-zone events disturb the seismicity in three  region prior to the Canterbury earthquake sequence starting in 2010, in the South Island of New Zealand. The 2009 M7.8 [Dusky Sound earthquake](https://www.geonet.org.nz/earthquake/story/3124785) is a subduction-zone event that deform large part of the South Island. Its coseismic slip and afterslip left profound footprint in the strain field on the South Island. 

The strain field we resolve is not smooth at all. Does the uneven deformation affect the seismicity as well? Through theory, we know a change of stress will also change the earthquake productivity. To amplify the statistical significance of rate-change estimate from a sparsely instrumented region, we use the [template matching](notes/template%20matching.md) technique to discover small earthquakes that didn't reach the network detection threshold. Because there are few stations to constrain the detection quality, we add another layer of safety using a simple supervised learning method, [the support vector machine](https://scikit-learn.org/stable/modules/svm.html), to tease out false detections.

![](https://yifanyin.github.io/assets/img/cumu_dila4.jpg)

We found that in the seismicity rate change positively correlate with the coseismic strain produced by the Dusky Sound earthquake. The NS extension slow down the earthquake productivity, likely also unclamp the EW Darfield rupture. The effect of strain field changing during the subduction zone events has large impact in low-strain area like the Canterbury Plain. And monitoring microseismicity would be a great complement of available geophysical measurements.


## Publication
**Yifan Yin**, Stefan Wiemer, Edi Kissling, Federica Lanza, Antonio P. Rinaldi, Matthew Gerstenberger, Bill Fry; Seismicity Rate Change as a Tool to Investigate Delayed and Remote Triggering of the 2010–2011 Canterbury Earthquake Sequence, New Zealand. *Bulletin of the Seismological Society of America* 2021;; 111 (4): 2248–2269.[🔗](https://doi.org/10.1785/0120210006)